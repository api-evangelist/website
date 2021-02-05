---
published: true
layout: post
title: A Reminder To Always Have A Plan B For Our API Related Github Infrastructure
date: 2017-09-27T15:00:00.000Z
tags:
  - API Evangelist
  - Github
  - Backups
  - Migration
image: >-
  https://s3.amazonaws.com/kinlane-productions/github/github-api-evangelist-flagged.jpeg
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/github/github-api-evangelist-flagged.jpeg" align="right" width="40%" style="padding: 15px;" /></p>I had a scare this last weekend regarding my Github infrastructure. My Github organization for API Evangelist was flagged as SPAM and taken down. The Github organization contains almost 100 repositories that I use across my platform. These repositories drive the public side of my research, but also contain YAML files that are used in automation across my entire platform, and network of websites. At about 12:00 PM on Saturday, everything came to a screeching halt, with all the data I depend on to make things go around becoming unavailable.

I have backups of all the data, and the website templates that produce the public side of API Evangelist. I also have a plan B in place for setting up a Jekyll instance that runs on Amazon EC2, but I hadn't ever actually ran any drills on plan B. After submitting a ticket to Github, I got to work firing up the AWS EC2 instance, and unloading and unpacking the almost 100 website backups for my API Evangelist research. After getting things setup, and as I was preparing to switch over the DNS, I got an email from Github saying:

> Sorry for the hassle! It appears your organization had been caught up in a spam filter and was flagged incorrectly. I've cleared that flag now, so your account should be back to normal. You shouldn't see that message again, but let me know if I can help with anything else!

Crisis averted. Luckily this was just my own company Github organization. I operate numerous other API developer portals, code repositories, documentation sites, and other API related projects and tooling that lives entirely on Github. If my personal account was frozen, or any of these organizations taken offline, I would have been in a lot more hot water, and accountable to my clients. Overall I was down for a little over six hours. It showed me the fragile nature of depending on Github, not just for my data driven project public presence, but also it being the center of so many workflows that depend on the YAML, JSON, and code that I publish there.

The experience has forced me to look at my backup process some more, and given me the opportunity to actually run a live drill on failing over to a secondary provider. Even with this failover I still wouldn't have the Github API available as part of these data project workflows, an API that I depend on, which I really cannot replace. I can replace Git, and Jekyll, but not the Github API portion of the orchestration I depend on so heavily. I have to do some more meditating on this dependency in my world. Don't get me wrong. I love me some Githubz, but this worries me. Any API dependency worries me if I can't easily replicate and replace. But, I guess this is what the API game is often about right? Establishing dependencies that are difficult or impossible to walk away from. ;-(
