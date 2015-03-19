---
layout: blog
title: Exploring Patterns in 350,000 Bitcoin Block Hashes
tags:
- bitcoin
- sha256
---

## Exploring Patterns in 350,000 Bitcoin Block Hashes

Bitcoin's blockchain provides a treasure trove of applied cryptography data. In
a playful effort to learn more about the structure of the blockchain, I've set
out to perform some analysis on a 1-1 correlation of block header bits to its
corresponding block hash to see if there any interesting (but not necessarily
flawed) patterns in the double SHA256 operation over time.

Ideally, SHA256 should roughly provide a "random oracle" for Bitcoin. That is,
the input should not be correlated with the output with any statistical
significance. However, with Bitcoin, this turned out *not* to be the case for
reasons explained below.


There appears to be a simple pattern, more vivid early in Bitcoin's life but
diminishing as the mining difficulty increases. What's the cause of this? The



