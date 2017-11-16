---
published: true
layout: post
title: >-
  The Information You Get When Allowing Developers To Sign Up For An API Using
  Github
date: 2017-11-16T13:00:00.000Z
tags:
  - API Evangelist
  - Authentication
  - Github
image: >-
  https://s3.amazonaws.com/kinlane-productions/github/github-authentication-screenshot.png
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/github/github-authentication-screenshot.png" align="right" width="45%" style="padding: 15px;" /></p>I'm a big Github user. I depend on Github for managing all my projects, and Github Pages for the presentation layer around all my research. When anything requires authentication, whether for accessing an API, or gaining access to any of my micro apps, I depend on Github authentication. [I have a basic script that I deploy regularly after setting up a Github OAuth application](https://gist.github.com/kinlane/00db3d871b615c8b1c43dbc60ae41f86), which I use to enable authentication for my API portals and applications, handling the OAuth dance, and returning me the information I need for my system.

After a user authenticates I am left with access to the following fields: id, avatar_url, gravatar_id, url, html_url, followers_url, following_url, gists_url, starred_url, subscriptions_url, organizations_url, repos_url, events_url, received_events_url, type, site_admin, name, company, blog, location, email, hireable, bio, public_repos, public_gists, followers, following, created_at, updated_at, private_gists, total_private_repos, owned_private_repos, disk_usage, collaborators, two_factor_authentication, and plan. Not all these fields are filled out, and honestly I don't care about most of them for my purposes, but it does provide an interesting look at what you get from Github, over a basic email and password approach to authentication.

I'm just looking for any baseline information to validate someone is a human being when signing up. Usually a valid email is this baseline. However, I prefer some sort of active profile for a human being, and have chosen Github as the baseline. When anyone signs up I also quickly calculate some other considerations regarding how long they've had a Github account, how active it is, and some numbers regarding this history and activity. I don't expect everyone to have a full blown public Github profile like I do, but if you are looking to use on of my APIs, or API-driven micro tools I'm looking for something more than just a valid email--I want some sign of life. I will be evolving this algorithm, and enforcing it in different ways at different times.

I always hesitate using Github as the default login for my API portals and applications, but honestly I think it is a pretty low bar to expect folks to have a Github account. I feel like we should be raising the bar a little when it comes to who is accessing our resources online. The APIs and tooling I'm making available are mine, and I just want to make sure you are human, and are verifiable on some level, and I find that the links available as part of your Github profile provide me with more reliable and verifiable aspects of being human in the tech space. Making the fields returned as part of Github authentication pretty valuable for verifying humans in my self-service, and increasingly automated world.
