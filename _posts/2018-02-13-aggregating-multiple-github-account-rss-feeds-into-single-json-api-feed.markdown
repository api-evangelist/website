---
published: true
layout: post
title: Aggregating Multiple Github Account RSS Feeds Into Single JSON API Feed
date: 2018-02-13T12:00:00.000Z
tags:
  - API Evangelist
  - Real Time
  - Streaming
  - Github
  - Monitoring
  - Social
image: 'https://s3.amazonaws.com/kinlane-productions/github/octocat-aggregate.png'
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/github/octocat-aggregate.png" align="right" width="45%" style="padding: 15px;" /></p>Github is the number one signal in my API world. The activity that occurs via Github is more important than anything I find across Twitter, Facebook, LinkedIn, and other social channels. Commits to repositories and the other social activity that occurs around coding projects is infinitely more valuable, and telling regarding what a company is up to, than the deliberate social media signals blasted out via other channels is. I'm always working to dial in my monitoring of Github using the Github API, but also via the RSS feeds that are present on the public side of the platform.

I feel RSS is often overlooked as an API data source, but I find that RSS is not only alive and well in 2018, it is something that is actively used on many platforms. The problem with RSS for me, is the XML isn't always conducive to working with in many of my JavaScript enabled applications, and I also tend to want to aggregate, filter, and translate RSS feeds into more meaningful JSON. To help me accomplish this for Github, I crafted a simple PHP RSS aggregator and converter script which I can run in a variety of situations. I published the basic script to Github as a Gist, for easy reference.

<script src="https://gist.github.com/kinlane/30461b54300f29da462db4f63fccd6f5.js"></script>

The simple PHP script just takes an array of Github users, loops through them, pulls their RSS feeds, and then aggregates them into a single array, sorts by date, and then outputs as JSON. It is a pretty crude JSON API, but it provides me with what I need to be able to use these RSS feeds in a variety of other applications. I'm going to be mining the feeds for a variety of signals, including repo and user information, which I can then use within other applications. The best part is this type of data mining doesn't require a Github API key, and is publicly available, allowing me to scale up much further than I could with the Github API alone.

Next, I have a couple of implementations in mind. I'm going to be creating a Github user leaderboard, where I stream the updates using Streamdata.io to a dashboard. Before I do that, I will have to aggregate users and repos, incrementing each commit made, and publishing as a separate JSON feed. I want to be able to see the raw updates, but also just the most changed repositories, and most active users across different segments of the API space. [Streamdata.io allows me to take these JSON feeds and stream them to the dashboard using Server-Sent Events(SSE)](http://apis.how/streamdata), and then applying each update using JSON Patch. Making for a pretty efficient way to put Github to work as part of my monitoring of activity across the API space.
