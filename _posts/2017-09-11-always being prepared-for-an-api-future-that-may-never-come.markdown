---
published: true
layout: post
title: Always Being Prepared For An API Future That May Not Come
date: 2017-09-11T16:00:00.000Z
tags:
  - API Evangelist
  - GraphQL
  - Hypermedia
  - Design
  - Politics of APIs
image: >-
  https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories/copper-servers.jpg
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories/copper-servers.jpg" align="right" width="40%" style="padding: 15px;" /></p>I'm just coming out of a sprint for [my Human Services Data API (HSDA) work](http://org.open.referral.adopta.agency/). Throughout the process of gathering feedback across emails, Slack Channels, and Github Issues, and trying to decide where I should be steering this ship, I'm regularly reminded that I'm often preparing for a future that may never come. I'm working real hard to make my API design as future proof as possible, but I find that in many cases I risk leaving folks behind with some of my API design decisions. When it comes to the audience for this API, municipalities and nonprofit organizations, this concern was present with every decision I have been making.

As part of this latest evolution, I took hypermedia and GraphQL off the table, as both areas seem to confuse and muddy the conversation, not help. I was hoping that GraphQL might help some of the requests around query-ability of APIs, and the tendency to load up individual paths with numerous parameters, and enums. I tried to facilitate discussions around unique identifiers, moving things beyond just incremental integers, taking a cue from Twitter and other large providers, but many just deemed these conversation overkill, unnecessary, and bothersome. While I have learned a lot over the last seven years as the API Evangelist, I am regularly reminded that not everyone has been along for the ride, and I need to always bring things back to ground level, even if it means making some cringe-worthy API design choices.

I find as a technologist, I suffer from hopeless futurism. Even though I know better, I still tend to prefer looking at what is next, preparing as much as I can for the future, even at the expense of where we've been, and possibly leaving people behind. I can argue until I'm blue in the face regarding the benefits of hypermedia when it comes to supporting clients, and the benefits of GraphQL when it comes to giving API consumers a stronger voice when it comes to querying and getting access to EXACTLY the data they need, but without the proper groundwork, and education, my audience is rarely going to care. APIs are a journey, and I feel like APIs have to take their course, and folks have to be along for the ride. There is just no hurrying this process, no matter how much knowledge about the future I may possess, or how passionate and aggressive I am about why a particular API design decision will matter down the road. 

I am working very hard to tame my tech bro futurism fetish, and better understand what the humans here on the ground in the present will need. I'm also working a lot harder to try and figure out how I can incorporate API lessons into my API design and definition work. How can I teach folks about headers, with specific design decisions I've made? How can I teach folks about how the client will break with a certain API design approach? As a technologist it is very hard to allow myself the space to make sub-standard API design decisions for the sake of helping an audience learn along the way. I want everything to be right, dammit! However, I'd much rather that my APIs actually get used, and the folks I'm targeting with my designs aren't turned off by what I've delivered because they don't see the value, or relevance. I'm working hard to not always be a tech boy scout, and always being prepared for a future that may not come.

**P.S.** I am guessing that all the folks who keep saying I'm so anti-GraphQL will not recognize how much I'm incorporating it into my work, and storytelling, and that this is a POSITIVE story about how GraphQL might have helped. It also still highlighting my argument(s) around investment in API education, and not being aggressive when you are pushing GraphQL, as I've learned first hand and keep trying to share in my (aggressive) GraphQL posts.