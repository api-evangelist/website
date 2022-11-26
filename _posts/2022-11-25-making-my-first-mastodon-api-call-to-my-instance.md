---
published: true
layout: post
title: 'Making the First Mastodon API Call to My Instance'
image: https://s3.amazonaws.com/kinlane-productions2/algorotoscope-master/uncle-sam-waterpump-old-time.jpg
author:
 name: kinlane
tags:
- Social
- Twitter
- Mastodon
- Timeline
- Federated
---
[I just got a Mastodon instance setup for my Kin Lane domain](https://kinlane.com/2022/11/25/i-have-my-mastodon-instance-for-kin-lane-setup/). I am being thoughtful about this shift in my social presence, but as with every other aspect of my digital life, I am most interested in Mastodon because of the platform API. For me, Twitter is first and foremost an API platform, and secondarily a social platform. For me, the value of Twitter is to be able to automate and orchestrate the research, curation, and communication I do via the platform. It is the same for Mastodon. So, now that I have an instance, I want to start playing with the API. 

You can find the documentation for the [Mastodon API](https://docs.joinmastodon.org/api/guidelines/) via their docs site, and to help guide my work I have setup a public Mastodon API workspace. To get started, I wanted to play around with the lowest hanging fruit, and in my opinion that would be the [Mastadon Timeline API](https://docs.joinmastodon.org/methods/timelines/). I created what I’d consider to be [a “capabilities” collection for pulling the timeline for my instance(https://www.postman.com/api-evangelist/workspace/mastodon/request/35240-6b0d54d1-3476-4423-aa33-aa10faa675f7). The Timeline API doesn’t require authentication as it is a public feed, so I am able to quickly setup a request and see the response in JSON. Once I get a 200 OK, I add a little test script to visual each of the users plus messages in a simple HTML layout.

![Mastodon Timeline API Capability Collection](https://kinlane-productions2.s3.amazonaws.com/mastodon-timeline-api-hello-world.png)

Now I can create different versions of this collection to help me harvest the pulling of data and automating the curation, syndication, and engagement with people I follow in similar ways to what I do on Twitter. I can tweak and evolve the test script to look for hashtags and other keywords, make decisions based upon the user, and customize how I want to automate how I consume messages via my Mastodon instance. Honestly this is something I should revisit for my email inboxes, standardizing how I use APIs to maximize how I work across these federated channels—both private and public messaging. 

This is kind of my Mastodon API hello world moment. Honestly, I am very excited about the potential here. This feels similar to the early days of Twitter, but this is MY API. This is MY DATA. I can do whatever I want with my data and my relationships. T/his is huge! This is something that will have me thinking very deeply about how I use Mastodon across my different domains, but also how this gravity shifts the balance across my other social networks like Twitter, but also Facebook and LinkedIn. The Mastodon API is pretty verbose, giving me full control over my instances. So this is just the start of some interesting automation and orchestration, which I will be sharing via public workspaces—-helping share how I do what I do openly here on API Evangelist.