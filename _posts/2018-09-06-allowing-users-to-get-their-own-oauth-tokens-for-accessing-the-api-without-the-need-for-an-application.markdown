---
published: true
layout: post
title: >-
  Allowing Users To Get Their Own OAuth Tokens For Accessing An API Without The
  Need For An API Application
date: 2018-09-06T09:00:00.000Z
tags:
  - API Evangelist
  - Authentication
  - Github
  - OAuth
image: >-
  https://s3.amazonaws.com/kinlane-productions/github/github-personal-access-token.png
---
<p><img src="{{ page.image }}" width="45%" align="right" style="padding: 15px;" /></p>I run a lot of different applications that depend on GitHub, and use GitHub authentication as the identity and access management layer for these apps. One of the things I like the most about GitHub and how I feel it handles it's OAuth more thoroughly than most other platforms, is how they let you get you own OAuth token under your settings > developer settings >personal access tokens. You don't need to setup an application, and do the whole OAuth dance, you just get a token that you can use to pass along with each API call.

I operate my own OAuth server which allows me to authenticate using OAuth with many leading APIs, so generating an OAuth token, and setting up a new provider isn't too hard. However, it is always much easier to go under my account settings, create a new personal access token for a specific purpose, and get to work playing with an API. I wish that ALL API providers did this. At first glance, it looks like [GitLab](https://docs.gitlab.com/ee/user/profile/personal_access_tokens.html), [Harvest](https://help.getharvest.com/api-v2/authentication-api/authentication/authentication/), [TypeForm](https://developer.typeform.com/get-started/personal-access-token/), and [ContentFul](https://www.contentful.com/r/knowledgebase/personal-access-tokens/) all provide personal access tokens as a first option for on-boarding with their APIs. Demonstrating this is more of a pattern, than just a GitHub feature.

One of these days I'm going to have to do another story documenting the entire GitHub OAuth system, because they have a lot of interesting bells and whistles that make using their platform much more secure, and just a more frictionless experience than other API providers I use on a regular basis. GitHub has ground down a lot of the sharp corners on the whole authentication experience when it comes to OAuth. It would make a nice blueprint to share, and work to convince other API providers it is a pattern worth following. Reducing the cognitive load around OAuth management for any API integration, and standardizing how API providers support their API consumers, and end-users.

I have 3 separate Twitter Apps setup for specific purposes, but I wanted to have a separate personal application just for managing my person @kinlane account. I submitted a Twitter application for review, but haven't heard back after almost a month. As a individual user of any platform, I should be able to instantly issue a personal access token that let's me, or someone I sanction, to access my data and content on the platform. Personal access tokens should be a default feature for any consumer focused platform, putting API access more within the control of each end-user, and the platform power users.
