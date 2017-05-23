---
title: Avoid Moving Too Fast For My API Audience
date: 2017-05-23 14:00:00 Z
tags:
- Design
- HSDS
- HSDA
- '211'
- Road Map
image: https://s3.amazonaws.com/kinlane-productions/algorotoscope/stories/freeway_atari_missle.jpg
---

<p><img style="padding: 15px;" src="https://s3.amazonaws.com/kinlane-productions/algorotoscope/stories/freeway_atari_missle.jpg" align="right" width="40%" /></p>I am stepping back to today and thinking about a pretty long list of API design considerations for [the Human Services Data API (HSDA)](http://developer.open.referral.adopta.agency/documentation/), providing guidance for municipal 211 who are implementing an API. I'm making simple API design decisions from how I define query parameters all the way to hypermedia decisions for the version 2.0 of the HSDA API.

There are a ton of things I want to do with this API design. I really want folks involved with municipal 211 operations to be adopting it, helping ensure their operations are interoperable, and I can help incentivize developers to build some interesting applications. As I think through the laundry list of things I want, I keep coming back to my audience of practitioners, you know the people on the ground with 211 operations that I want to adopt an API way of doing things. 

My target audience isn't steeped in API. They are regular folks trying to get things done on a daily basis. This move from v1.0 to v.1 is incremental. It is not about anything big. Primarily this move was to make sure the API reflected 100% of the surface area of the Human Services Data Specification (HSDS), keeping in sync with the schema's move from v1.0 to v1.1, and not much more. I need to onboard folks with the concept of HSDS, and what access looks like using the API--I do not have much more bandwidth to do much else.

I want to avoid moving too fast for my API audience. I can see version 2,3, even 4 in my head as the API architect and designer, but am I think of me, or my potential consumers? I'm going to seize this opportunity to educate my target audience about APIs using the road map for the API specification. I have a huge amount of education of 211 operators, as well as the existing vendors who sell them software when it comes to APIs. This stepping back has pulled the reigns in on my API design strategy, encouraging me to keep things as simple as possible for this iteration, and helping me think more thoughtfully about what I will be releasing as part of each incremental, as well as major releases the future will hold.