---
layout: blog
title: Notes From Select Talks at DEFCON 21
tags:
- defcon
- nsa
- civil liberty
- snowden
---


## Notes from Select Talks at DEFCON 21
Earlier this year I had the privilege to attend DEFCON 21. I wanted to experience the security community's reaction to the breaking news about Edward Snowden and the NSA. Not surprisingly, many of the talks focused on issues related to privacy and civil liberty, and these are the onesI tried to attend most. Here are my notes.

1. Welcome / Badges
2. The Growing Irrelevance of US Government Cybersecurity Intelligence Information
3. Backdoors, Government Hacking, and the Next Crypto Wars
4. Meet the VCs
5. ACLU Presents
6. UFOs and Government: A Historical Inquiry
7. Hacking Institutions
8. Home Invasion 2.0
9. RFID Hacking: Live Free or RFID Hard
10. Stalking a City for Fun and Frivolity
11. An Open Letter — the Whitehat’s Dilemma: Professional Ethics in the Age of Swartz, Prism, and Stuxnet
12. HiveMind
13. Defending Networks with Incomplete Information: A Machine Learning Approach




### Welcome / Badges
#### 

Traditional DC trifecta:
rotary dial: early way to connect to net
skull&bones: privacy / security
floppy: ??

new one:
keyhole: locks, keys crypto symbol of observation.

badge types:
uber/black: elite competitions & awards. free dc entry for life
human: regular badge
inhuman: speaker, press, vendor

alternate having microcontrollers and not every year. dc 22 will have powerful yet-to-be-released chip (evolution of dc20's chip). if it's not ready, however, they'll use the [msp 430]. dc22's badge will incorporate watchmaking, an inspiration from his grandfather.

this year, press badge is a deuce, all others are face cards.


### The Growing Irrelevance of US Government Cybersecurity Intelligence Information
#### Mark Weatherford

irrecoverable hard drive failure last night led to no slides... d'oh!

last year, he was a fed. Won't be talking about snowden but will talk about defensive analysis. cybersecurity intelligence useless to private sector but not much more to public sector.

why?
1. washington think it knows more about private sector than you do about your business.
2. govt isn't coming on a big white horse to save you. policies, procedures aren't designed to work with private sector
3. private orgs can already monitor and analyze much of the same data as govt
4. govt is beaurocracy
5. the people who really need to know classified info are the ones who don't have clearance. ex: us gets much of its power from canada, but can't reveal latest threats on power grid to canadian citizens.
6. of all incidents revealed to private sector, only 4% were things private sector didn't already know!

mentioned [worm]: book about confickr.

why isnt govt doing anything? what is govts role then?

well value of clasified info depends on whats in it. not all classified info has same value. problem is over-classification, and no good method exists to sanitize and provide to private.

also, what about foreign CEOs? how can they receive classified info?

not enough manpower to provide stuff necessary for mass declassification. snowden only makes it worse.

past year, banks have gone through ddos. best part about it: CSOs of banks got together to talk, lots of info sharing, collaboration. we need more sharing.

info exchange programs:
[taxi program]
[mandiant open ioc framework]
[itf program] (used by csirt)
[isacs]... no funding unfortunately

"you're not invited clubs" spring up in incidents like confickr outbreak, but only people with skillset and connections get brought into those situations.

what govt can do:
1. open r&d: more $$ to fund startups
2. lots of great govt tech sitting on classified shelves. figure out how to get it out.
3. increase training, amount of qualified people
4. fund the isacs!


### Backdoors, Government Hacking, and the Next Crypto Wars
#### Christopher Soghoian

He was first technologist at ACLU to focus solely on privacy & surveillance.

First crypto wars:
there was when you couldn't export strong crypto from the US. in mid 90s, govt sought to demonize crypto. socially acceptable, fbi-backed crypto was [clipper chip]. '96 clinton signed [crypto bill], pgp and others could then export crypto.
but no one uses pgp cause it's too hard. terrorists, pedophiles, don't use pgp.
https more widely used cause it was transparent. but only for e-commerce, banks. most sites still get info over http.
fbi starts to get worried cause more and more companies are building crypto into their products.
fbi general counsel [valerie caproni] says crypto is a problem for certain companies.

january 2010, something remarkable happens: [google turns ssl on by default in gmail]. first of the large email providers to do so. afterward, several silicon valley companies followed suit.

Mentioned [Perfect-forward secrecy] "next-gen ssl". but doesn't mean encrypted at rest -- how can google show ads if it can't read your email?

companies do get requests from lea for data. years past, metadata would be available to govt. [first wiretaps 1895]. phone companies typically offered dragnet while silicon valley companies only allowed targetted. apple did something great with imessages: bypassed phone companies (on handset).

diff between silicon valley and phone companies is culture: valley has security. so how does govt solve this problem? backdoors!

[CALEA]: law requiring backdoors

valerie caproni testified: fbi wants power to go to a company secretly and force a backdoor into their products. justice dpt involved

snowden revealed this, politicians won't touch it now. govt agencies don't have tools / backdoors b/t each other. in other countries, govt can't access data if no office there.

[FINFISHER]: IT intrusion software, developed by [Gamma]
CEO of Gamma is [Martin Munch], creator of [Backtrack Linux]
can operate webcams w/out user knowing, has been used by oppressive regimes.

[HACKINGTEAM] [da vinci]: markets itself to LEA who are trying to deal with things like skype. has been to trade shows, conventions to sell these things. (to small LEAs).

but feds wouldn't use this. instead, would have resources to write 0days.

aclu filed foi act request to see if any govt agencies were really going dark. response: [remote operations unit]. provides lawful hacking to law enforcement.

[bimen associates] provides hackers to fbi. [jerry menchhoff], president. also member of [(San Diego?) metasploit user group].

recent case in texas where fbi sought warrant to monitor individual. fbi [tweeted] "pirated software may contain malware"

what will fbi do when silicon valley starts providing e2e encryption? backdoor like skype?
no, [silent circle], [spider oak].

calea omits wiretapping if user encryption is used, so govt will probably target this section of the law.


### Meet the VCs
#### Deepak, John, Ping, Andressen Horowitz, Accel Partners

guy from [Lookout Security] is panel moderator

Q: What are you looking for?
A: market applicability. security doesn't sell itself... bigger opportunities sell better when security is tacked on. they’re looking for stuff that takes 3 years at least and is a killer product. motivated not to invest in “me too” tech, even if they’re looking 3 years out. great entrepreneurs are ones who see around the corner. security is particularly hard because there’s so many knowledgeable people. mobile, cloud, big data mean super ambitious security applications.

traits of good entrepreneurs / CEOs:
1. great evangelist
2. look around market changes
3. best of breed
4. great group

security is huge with the advent of the internet of things. net present value utility curve can diverge pretty rapidly.

[deferred stock investment]:
don’t take money if you’re going to have a small biz. Ex: [Nessus] was bootstrapped for 5-6 years, then raised VC $$. take VC money if you’re building a huge company to change the world.
if you’re looking for vc funding, you’ve got to find firms that help you be successful. [executive briefing center at A-H].
every step you take should be able to increase your odds of success.
banks look for low-risk investment — if they’ll lend then VCs won’t.

Q: what do you look for when making a really big bet?
A: best entrepreneurs are ones that convince the vc the impossible is possible
*you can be in a meeting w/ an entrepreneur and it they make you feel like a child teaching you the way the works, you’ll back them. VCs are groups of humans making best decisions off of little info.

Q: at what stage do you contact VCs?
A: whenever, start building relationships right away

Q: why not invest in anti-child porno?
A: gave the dude a 10-min pitch opportunity on the spot

other options to raise money include [kickstarter], [ angelist ]


### ACLU Presents
#### Alex Abdo, Catherine Crump, Christopher Soghoian, Nicole Ozer, Cate Crockford

Applause to Ed Snowden…
revealed what we’ve worried about for a while. privacy should be protected by constitutional law, not [moore’s law].

alex abdo:
[2008 fisa ammendments act]: gives government unfettered access to international communication. aclu battled this b/c you can’t often control how packets were routed. government blocked efforts to sue.
[PRISM] is one version of implementation of fisa act. only for international but americans’ are always swept up. government can keep americans info for [5 years]. they will keep you communication if they *think* you’re a foreigner. PRISM program allows NSA to do [geographic surveillance].

catherine crump:
NSA cellular metadata domestic surveillance
storing metadata going back 5 years
fisa court has approved general approach to collecting data. [section 215 patriot act] authorizes certain surveillance. verizon provides phone service to ACLU… whoops! conflict there.

chris soghoian:
what do you do when you lack resources necessary to monitor dragnet-style? subsidized telco monitoring equipment. you [deputize internet & telco companies], sometimes paying (hundreds of millions of $$).
there wouldn’t be a prism program if companies / telco weren’t participating.
but some companies are avoiding participation. this will help but really need to increase cost of surveillance.

nicole ozer:
snowden has given us first real info of how often government is taking advantage of outdated privacy laws. largely unsupervised shopping spree by internet companies, government. agencies weren’t required to provide info on collection (companies too). companies then released transparency reports to assuage the people of how many thousands of requests come in. how many come with a subpoena vs how much are warrants?

cate crockford:
guilty until proven innocent
personal privacy and government transparency have been flipped recently. [automatic license plate readers] aren’t as ubiquitous as [cctv cameras] but soon will be. [vigilant solutions] has over [1 billion license plate reads]. available not only to government, but also to [private companies!] (WTF). twitter notifies users of [subpoenas issued for them]. [join aclu], 700,000 members, to increase their voice in D.C.


### UFOs and Government: A Historical Inquiry
#### 

They’re here. but what does it mean? WWII marked modern era of UFO reports and denials. [Only book] recommended by [CHOICE] for academic study. [Chinatown]: movie that describes this talk. chinatown moments are moments where you realize everything you thought is no longer the same. people in power just wait it out. easy political game. this talk is not about standard UFOs pictures that have been faked / hoaxed.

this is what we mean by UFO:
massachusetts: [1952 coast guard pic of UFOs in formation]

first reported as foo fighters over gemany and we didn’t know what they were. no one knew though but everyone suspected they were other countries military vehicles.

1947: military knew about these and anomamlous, and a fact. serious issue and take seriously.
project [SIGN]’s conclusion was that it was extraterrestrial but this was shot down. project [ GRUDGE ]was then formed to come up wihth a better answer. but no one knew what it was and people wanted to know if these UFOs were threats.
US airforce was commussioned to protect airspace over washington so they took these as threats. and loaded anti-aircraft guns and scrambled fighters.

[Project Blue Book]: [Allen Hynek]!
flying saucers are not a threat to national security. reports of flying saucers are. hynek started a skeptic but after hundreds of interviews started realizing something after interviewing hundreds of global incidents. higher intensity illumination by UFOs corresponded to higher power movement. 3 or 4 civilizations are likely visiting based on correlated events.

1. illusions
2. distractions


### Hacking Institutions
#### Mudge

Darpa-mil announcement for new supercomputer
Mudge
Tell some stories!
Not long after joing [DARPA], got funding for targetting “advanced” [APT], called [CINDER].

How the DoD unintentionally created [ WikiLeaks ]:
     2009  - talk going on about wikileaks in berlin: [ strobe ], [ prof ] were [ assange ]’s handles. mudge talks to assange over dinner. and asked, if assange received incriminating evidence would he publish? never answered. assange was working on research at university when the funding gets pulled by the US government. at that point he decided he was going to devote his life to exposing secrets that disadvantage others.

[Anonymous] at the DoD:
     at some points Anon’s scope grew to include the government. strategy was that DoD was going to treat cyberspace as a domain to test in. this galvanized folks to respond, problem was, they didn’t specify who.
so a couple of websites got defaced, which is a warning message. but the government didn’t understand and just thought it was hostile. so keep in the DoD has only very specific intents & agendas so ensure you send messages both sides can understand.

Can’t government contractors make more money remaining compromised? game theory is a bitch.
1. [RSA is compromised]
2. [stealth drone contractor gets compromised]
3. [drone goes missing over middle east]

what happens when someone steals some of your tech? you have to make more. and, most likely, government contractor will be requested to build better tech.

Mudge went to DARPA to try and fix from the inside.
result: CFT: [Cyber Fast Track]
CFT helped to transition thoughts of hackers from criminals to researchers. suggestions for the government:
1. go engage & interact with the local community
2. stop with the offensive recruitment. instead, contribute to the community. it’s a meritocracy.

“challenging government is why we’re such a great nation” somebody’s gonna change CFA: support them

[Barnaby Jack]
crazy exploits: [wireless router exploit]. [ PCI boot exploit ]


### Home Invasion 2.0
#### Daniel Crowley & David Bryan ([Trustwave]), Jennifer Savage ([TabbedOut Security])

Dystopian science fiction serves as a warning of the future device and product makers. locks, thermostats, fridges, toilets, lights, toys. [song-du]: high-tech city

[Karotz Smart Rabbit]:
camera, microphone, RFID reader, RFID toys. USB port
SSID, auth sent unencrypted.
unencrypted remote API calls
unencrypted setup package download
code signing but python module hijacking
raw video stream
python module hijacking similar to DLL hijacking ([LD_PRELOAD exploit via PYTHON_PATH])
bunny botnet! one-time tokens can be re-used for spying raw video.

[Belkin WeMo Switch]:
belkin has good security culture!
provides free devices to security researchers
vulnerable libupnp
unauthed upnp actions
EULA used to secure devices, runs linux
nmap: broadcast upnp_info

[ Sonos Bridge ]:
support console information disclosure
netstat, process list, list of users, ifconfig, whoami

[ LIXIL Satis Smart Toilet ]
android app that controls via bluetooth, bidet, music, flush
default bluetooth PIN: 0000

[ INSTEON Hub ]
home control device for home automation. has no encryption whatsoever, no authentication by default
hard-coded base64

[ MiCasa Verde VeraLite ]
no authentication as a guest user, can update firmward
CSRF
no shadow, vulnerable libupnp


### RFID Hacking: Live Free or RFID Hard
#### 

RFID Pentest:
1. Steal badge info
2. Clone info
3. Use info

Problem: Require people to be within 2-3cm
[Proxmark]: RFID Hacking tool (most popular)
Required to be within 1” (little too close for comfort)

[Tastic long-range RFID reader]
1ft x 1ft
Long-distance commercial badge reader
writes to cards.txt microSD card internal circuit. easily removable cover

programmable [t557 rfid card] used to clone

how it works:
card receives power, sends out bits into the air always 44 bits. starts with six 0s and a 1.

[proxmark 3]: $400
[proxbrute]: custom firmware you can use to do bruteforcing. [ RFIDiot ]
[ RFIDeas tools ]
usb sticks for reading badges
commercial readers 2 HID readers
tastic solution: arduino capabilities
[cloner 2.0 by paget]: long-distance reader


### Stalking a City for Fun and Frivolity
#### Bendan O'Connor

every single thing leaks way too much data. we’ve forgotten as a community how to protect privacy & security of our users. it’s no longer possible to blend into the crowd. it’s possible to own someone’s life. bluecoat boxes found in enemy countries or countries with oppressive regimes. cops with cameras are less likely to use excessive force.

[creepyDOL]:
true identity theft for a city. stalking as a service. we can’t rely on government to prosecute hackers.

darpa cft is not cft work. reticle and visualization system. how much can we extract from only wireless? wi-fi devices send everything out they know around them.
large-scale sensing w/out centralized communications. so threat can’t be tracked / disabled.

goal 1: intelligibility
until every script kiddie can operate these things, it won’t get better.
background, large-scale surveillance


[f-bomb v1], shmoocon 2012
[pogoplug]
fits inside carbon monoxide detector
uses 2-WiFi
[PortalSmash] auto-agrees to wi-fi hotspots
[Reticle]:
Designed to work a lot like a botnet
[couchDB], [nginx], tor hidden services
boots only with USB key, volatile memory, [Tor]

centralized query for centralized questions, only 8 GBs of drive storage.
observation filters
google reader alternatives are typically very insecure.
creepyDOL

[shark]: in-memory derivative of hadoop hive

second darpa cft contract. used unity game engine. servers do the heavy lifting
can be used for counter infiltration

why is privacy important? someone will do something wrong at some point & you can catch them. can be sealed up pretty easily.

[RTLSDR]: software-defined radio.
[reaver] - wi-fi encryption break

mitigation: we have to sacrifice things we love to fix this.
problems: IEEE protocol spec says you can beacon wi-fi networks. turn on VPN *before* any packets are sent. IOS should have this feature.
[thehark.net]


### An Open Letter — the Whitehat’s Dilemma: Professional Ethics in the Age of Swartz, Prism, and Stuxnet
#### 


infosec sellout, corporate whitehat sellout
why? fun. get paid to do fun things.
pick a side: white or black
white: make system better
black: make yourself better

white hat:
big corporate
independent researcher
consultant
academic

there used to be fewer moral dilemmas: found a bug, ok report it. when’s the future coming? future already happened.
corp vs corp & state vs corp infowarfare already
semi-autonomous killer robots
crime prevention via massive data collection

[stuxnet], flame, and vuln disclosure

cyberware is real
almost any important corporation is facing highly motivated, well-funded companies
us software companies are directly attacked to create electronic munitions

[flame] was designed to attack microsoft
exploits are sent to adversaries as weapons, vendors notified by unaffiliated researchers

how do you interact with cyberwar?
who is getting your bugs?
[ sergey alikinov ], [ samarth agrawal ], [ Ben Pn ], [ sahil uppal ]

[ CFAA ]:
[david nasal]
[lori drew]
[weev]
[ aaron swartz ]

his product is used to prosecute people who’ve done bad things
what is the tech expert’s responsibility beyond telling the truth? just a passive observer?

NSA scandals, long-time paranoids are validated
[overton window]: most important thing about an idea is whether it’s publicly acceptable discourse. otherwise, revolt
NSA conspiracy changes overton window.
[fiber optic cables cut allowed for tap to be installed]!
exciting time to be in industry, but must make extremely careful decisions.

what is the united states? dirt we walk on? government? proud of the idea, federalist papers. but when the best people act against the people given the chance. responsibility to your family prevents risky disclosures.

idea of tribes, work teams: tribe, society, nation, species

any universal moral obligations? health has this. what about security? we are technological priests.

vast majority of people do not understand complexity of technology. internet should be a tool of liberation.

peter singer: 2 excuses for preventing evil are 1. “someone else’s job”, 2. “don’t know them”

things that drive careers:
- reduce suffering
- global economy
- family wealth
- build something that lasts
- never be forgotten

chapter 3: make decisions, activity preparation [test Q & A session]
choose, avatar, (ultima IV)

find an exploit in a public product:
A. announce
B. black hat
C. responsible disclosure
D. sell consulting
E. weaponize to govt
F. weaponize to other govt
G. self

CSIRT found incident report, then extreme penalties:
A. assist persecution
B. do nothing
C. gently push company
D. refuse to assist
E. volunteer to testify
F. publicly take a stand

NSA contacts you:
A. immediately
B. avoid
C. email questions
D. run screaming
E. guy fawkes

cloud company remote exploit:
A. drop it
B. escalate
C.

IDS is used to oppress, what do you do?
[MadeOpen]: personal cloud
IIW


### HiveMind
#### Sean Malone

uses real web apps to store, no vulnerability that can be fixed. not going anywhere

web browser is a botnet node!
sandboxing? not relevant since not using anything out of the ordinary. great way to build a botnet
use websockets, but fallback to ajax
data storage is html5 web storage
back end:
[rails], [redis], [mySQL]
network scanning (can JS do this??)
DDoS attacks
data processing (web workers)

##################################
          File

Name     Mimetype     Data

Encrypted Data
Base64
Block1 Block2 Block3… etc
##################################

storing a block:
server keeps track of which nodes have which blocks.
once a set of live nodes go offline, server distributes file to new nodes. password is entered on to the server to decrypt assembled file.

if server is seized:
1. nodes go offline
2. replication fails
3. blocks are lost
4. files are unrecoverable

unanswered legal questions:
is this legal? mostly legal, or does this constitute unauthorized use of a computer?
what about bandwidth? processing power?
is a user responsible for illegal content placed on their system?

(demo)


### Defending Networks with Incomplete Information: A Machine Learning Approach
#### Alexandre Pinto

lot of math involved
used to work in brazil, leading SOCs either inside the company. how can machine learning help defend a network?

security monitoring: we are doing it wrong.
logs everywhere, but no one’s happy… breaches occur but can’t track 90% of them.
bigest hurdle is identifying key events from the mountain. correlation rules are typical method of finding this. behavioral rules are only a little better.
training does not include how to use data + dashboards to find these things.

big data:
how many know/will learn statistics, data analytics, data science? we need an army.
|machine learning| how do you build features to tell the algorithm how to learn?
applications of machine learning: big in sales and trading
find cat pictures on the internet: google
security applications: bayesian filtering, fraud detection network anomaly detection, spam filters

spam filtering has been solved — perhaps we can do the same for security?

supervised learning:
- classification
- regression

unsupervised learning:
- clustering (k-means)
- decomposition (PCA, SVD)

models will generally get better with more data, but will always make mistakes
BUT
people would like to fuck with it? in security world, people will try to mess with you. designing a model to detect malicious behavior. firewall block data from SANS dshield (per day).  SANS will provide if nicely asked.
model intuition: proximity
assumptions to aggregate the data
[SpamHaus] came up and said the whole ISP is malicious
[google malware report]: some places are more likely to have malware.
[moura 2013]
[hilbert curve]
[temporal decay] (important)

as time passes, back off and forget people were attacking you. training data usually spans multiple days. training the model: you need negative and positive observations.
[support vector machines] (SVM). 70-92% true positive, 95-99% true negative rate… if the model says something is bad, it is multiple times more likely to actually be bad.
tier 1 & 2 SOC analysts can really benefit from this.

[http://www.mlsecproject.org]
@MLSecProject
