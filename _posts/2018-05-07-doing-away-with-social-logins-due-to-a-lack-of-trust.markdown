---
published: true
layout: post
title: Doing Away With Social Logins Due To A Lack Of Trust
date: 2018-05-07T11:00:00.000Z
tags:
  - API Evangelist
  - Authentication
  - Politics of APIs
  - On-boarding
image: 'https://s3.amazonaws.com/kinlane-productions/social-login.png'
---
<p><img src="{{ page.image }}" width="45%" align="right" style="padding: 15px;" /></p>I received an email from my CRON job API ([EasyCRON](https://www.easycron.com/)) provider this morning about discontinuing the usage of social logins to their service with Gmail, Facebook, etc. Something that I think is a sign of things to come in response to the recent (and continued) bad behavior by many of the leading technology platforms. EasyCRON gave the following response for removing social logins from their service:

> In order to: 1) prevent any confusion that could be caused by using third party platform's authentication API, 2) decouple from those data greedy platforms, 3) and keep our system simple, we decide to stop using third party platform's authentication API on EasyCron.

As much as I prefer one click login using my Github or Google (rarely use Facebook), I can't argue with their logic. I'm a big fan of minimizing data sharing, surveillance, and of course keeping things simple. I wish we could trust tech companies to be good citizens with our data, but they seem to prefer repeatedly demonstrating they are more concerned with profits than they are about us.

I'm still on board with using Github login for my infrastructure related services, but will definitely stop using Google, Twitter, Facebook, and any other purely advertising related service for authentication purposes. As much of a pain in the ass as it might be to create yet another login, it is more of a pain in the ass to be surveilled, and exploited on a daily basis by technology platforms. I wish people would have more respect, and be better behaved, but things are what they are, and we should respond accordingly.

Thanks for fucking this one up for us all Facebook, Google, Twitter, and other platforms who just can't see the big picture over their short term profit. I am going to stop advising API platforms utilize social logins as part of their API management and on-boarding process, due to  it putting developers and consumers at risk for exploitation.
