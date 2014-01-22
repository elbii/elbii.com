---
layout: blog
title: Fully Automate Your Rails / NodeJS Tests in 30 Minutes
tags:
- nodejs
- jenkins
- mocha
- automated testing
- continuous integration
---

# Fully Automate Your Rails / NodeJS Tests in 30 Minutes

<i class='icon-time icon-large'></i> 30 minutes

Hello there! Happy {{ site.time | date: "%A" }}. My goal with this guide
is to extinguish any excuse you may have for not automating your tests with a
continuous integration server. All too often, a slight configuration or version
mismatch in engineer's environments causes tests to pass/fail for one engineer
and not another. In the worst case I've seen, one engineer spent hours
troubleshooting a failing test that turned out to be a problem with her Redis
version. Let's make that impossible! Tests should be run in a sanitary, stable
environment, safe from the chaotic 
and ready to go, 
[NodeJS](http://nodejs.org "NodeJS")
[continuous integration](https://en.wikipedia.org/wiki/Continuous_integration "Continuous Integration")
[automated testing](https://en.wikipedia.org/wiki/Automated_testing "Automated Testing")
server using:

1. [Jenkins](http://jenkins-ci.org "Jenkins") for continuous integration
2. Code coverage reports using [Istanbul](https://github.com/gotwarlost/istanbul "Istanbul")
3. Full-stack Javascript tests with [Mocha](http://visionmedia.github.io/mocha/ "Mocha")
4. [Git](http://git-scm.com "Git") server for source code management
5. [Nginx](http://nginx.org "Nginx") as a reverse-proxy in front of Jenkins


In this guide I'll be assuming you're using a Debian-flavored Linux distro for
your continuous integration and git server. I used
[Ubuntu 12.04 Server](http://www.ubuntu.com/download/server "Ubuntu 12.04 Server")
but any recent Debian-based distribution will be similar. We're
going to roll our own git server instead of going with [Github](http://github.com "Github")
because it gives you full control to build whatever hooks you want into your
repo.


### Step 1. Install required packages
---

{% highlight bash %}
% sudo add-apt-repository ppa:chris-lea/node.js
% sudo add-apt-repository ppa:nginx/stable
% wget -q -O - http://pkg.jenkins-ci.org/debian/jenkins-ci.org.key | sudo apt-key add -
% sudo sh -c 'echo deb http://pkg.jenkins-ci.org/debian binary/ > /etc/apt/sources.list.d/jenkins.list'
% sudo apt-get update
% sudo apt-get install build-essential sendmail jenkins ttf-dejavu nginx nodejs git-core
% sudo usermod -a -G shadow jenkins
{% endhighlight %}

The last step is required to allow Jenkins to read the /etc/shadow file. By
default, Jenkins ships with **authentication disabled**, so this will allow
system users to login to Jenkins when we enable security later on.




### Configure Jenkins
---

Security
Email host
Plugins

### Create a Jenkins Job
---

If you're new to Jenkins, it's basically a system that provides a well-defined
blueprint for automating things. It comes with hundreds of plugins available
that enable automating pretty much any kind of software-related task. In Jenkins
terminology, a "job" is used to refer to a set of repeatable steps that
perform a useful function. Every job is structured as follows:

1. trigger a shell command to run
2. capture the exit code
3. if success (the job succeeds), perform action X.
4. if failure (the job breaks), perform action Y.

In this manner, it's relatively easy to automate running your test suite in
a [post-receive hook](https://www.kernel.org/pub/software/scm/git/docs/githooks.html)
and perform some useful action when tests fail. In this guide, that action will 
be to to send an email when the build breaks and another when the build is
fixed.

We'll start by creating a new job. Enter a job name and select "Build a
free-style software project", then click OK.

<img src='/img/jenkins_new_job.png' class='img-responsive' alt='jenkins new job'>

For now, forget about the SCM section and scroll all the way down to the Build
section. Click the Add build step dropdown, then select "Execute shell".

<img src='/img/jenkins_add_build_step.png' class='img-responsive' alt='jenkins add build step'>

Our build sequence will consist of first cleaning up any potentially stale
directories, installing updated requirements / libraries, running the test
suite and generating the failure report, and finally generating the code
coverage report. You can combine these steps however you like, but I like to
use the Makefile convention with the following build steps:

1. make clean
2. make install
3. make test-xunit
4. make cov

<img src='/img/jenkins_build_steps.png' class='img-responsive' alt='jenkins build steps'>

Finally, we'll add post-build action that will notify us when the build fails.
At the bottom of the page click the "Add post-build action" dropdown and then
select "E-mail notification". This section is pretty straightforward... enter
your scrum master's email address, your team's alias, or a comma-separated list
of whoever you want to receive broken build notifications.

<img src='/img/jenkins_email_notification.png' class='img-responsive' alt='jenkins email notification'>

Click Save, then on the following screen, select "Build now".

<img src='/img/jenkins_build_now.png' class='img-responsive' alt='jenkins build now'>

If sendmail is working properly on your machine you should receive an
email complaining that you broke the build! :-)

<img src='/img/jenkins_build_failure.png' class='img-responsive' alt='jenkins build failure'>


### Create a Makefile to run your tests
---

This assumes your NodeJS project is structured like a typical npm module. That
is, all of your application code lives in lib/ and all tests in test/. Mocha
starts running your test suite at test/test.js by default.

    install: npm-install bower-install

    test-all:
      NODE_ENV=test ./node_modules/mocha/bin/mocha --check-leaks

    test-xunit:
      NODE_ENV=test ./node_modules/mocha/bin/mocha --check-leaks -R xunit > \
        $$WORKSPACE/$$BUILD_NUMBER_results.xml

    npm-install:
      npm install

    bower-install:
      bower install

    cov:
      NODE_ENV=test ./node_modules/istanbul/lib/cli.js cover \
        ./node_modules/mocha/bin/_mocha -- --check-leaks -R spec

    clean:
      rm -rf coverage
      rm -rf node_modules
      rm -rf components
