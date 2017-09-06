---
published: true
layout: post
title: Github OAuth Applications As A Blueprint
date: 2017-09-06T13:00:00.000Z
tags:
  - API Evangelist
  - Authentication
  - OAuth
  - Mnaagement
  - Github
image: >-
  https://s3.amazonaws.com/kinlane-productions/github/github-oauth-application.png
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/github/github-oauth-application.png" align="right" width="40%" style="padding: 15px;" /></p>I was creating a very light-weight API management solution for one of my projects the other day, and I wanted to give my API consumers a quick and dirty way to begin making calls against the API. Most of the API paths are publicly available, but there were a handful of POST, PUT, and DELETE paths I didn't want to just have open to the public. I didn't feel like this situation warranted a full blown API management solution like [Tyk](http://apis.how/zflfesymzk) or [3Scale](http://apis.how/ake3nxbapm), but if I could just let people authenticate with their existing Github account, it would suffice.

This project has it's own Github organization, with each of the APIs living as open source API repositories, so I just leveraged Github, and the ability to create Github OAuth applications to do what I needed. You can find OAuth applications under your Github organizational settings, and when you are creating it, all you really need is to give the application a name, description, and a home page and callback URL, then you are given a client id and secret you can use to authenticate individual users with their Github accounts. I didn't even have to do the complete OAuth dance to get access to resources, or refresh tokens (may will soon), I was just able to implement a single page PHP script to accomplish what I needed for this version:

<script src="https://gist.github.com/kinlane/25e58174ed8b51a30274a3b371b4ca02.js"></script>

I am wiring this script up to a Github login icon on my developer portal, and each API consumer will be routed to Github to authenticate, and then the page will handle the callback where I capture the valid Github OAuth token, and the login, name, email, and other basic Github information about the user. Right now the API is open to anyone who authenticates, but eventually I will be evaluating the maturity of the Github account, and limiting access based upon a variety of criteria (number of repos, account creation date, etc.). For now, I'm just looking for a quick and dirty way to allow my API consumers to get access to resources without creating yet another account. Normally I would be using OAuth.io for this, but I'm trying to minimize dependencies on 3rd party services for this project, and Github OAuth applications plus this script worked well.

Once a user is authenticated they can use their Github user name as the appid, and the valid Github OAuth token as the appkey, which are both passed through as headers, leveraging encryption in transport. I'm not overly worried about security of my APIs, this is more about a first line of defense and identifying consumers, however I will be validating the token with particular API calls. I'm also considering publishing API consumption data to Github repository created within each users accounts as part of API activity, publishing it as YAML, with a simple dashboard for view (authenticated with Github of course). I've had this model in my head for some time, and have written about it before, but I'm just now getting around to having a project to implement it in. I'm calling it my poor man's API management, and something that can be done on a budget (FREE), but if my needs grow any further I will be using a more professional grade solution like [3Scale](http://apis.how/ake3nxbapm) or [Tyk](http://apis.how/zflfesymzk).
