---
published: true
layout: post
title: 'APIs and Browser Bookmarklets'
date: 2019-07-24T09:00:00.000Z
tags:
  - API Evangelist
  - Embeddables
  - Browsers
  - Bookmarklets
image: https://s3.amazonaws.com/kinlane-productions/algorotoscope-master/gears-4882162452-fa3126b38d-b-blue-circuit.jpg
---
<img src="{{ page.image }}" width="45%" align="right" style="padding: 15px;" />
I have quite a few API driven bookmarklets I use to profile APIs. I recently quit using Google Chrome, so I needed to migrate all of them to Firefox. I saw this work as an opportunity to better define and organize them, as they had accumulated over the years without any sort of strategy. When I need some new functionality in my browser I would create a new API, and craft a bookmarklet that would accomplish whatever I needed. I wish I had more browser add-on development skills, something I regular try to invest in, but I find that bookmarklets are the next best thing when it comes to browser and API interactions.

There are a number of tasks I am looking to accomplish when I’m browsing the web pages of an API provider. The first thing I want to do is record their domain, then retrieve as much intelligence about the company behind the domain in a single click of the bookmarklet. This was the first bookmarklet and API I developed. Since then, I’ve made numerous others to record the pricing page, parse the terms of service, OpenAPI, and other valuable API artifacts from across the landscape. Bookmarklets are a great way to provide just a little more context combined with a URL pointer, for harvesting, processing, and possibly some human review. Allowing me to augment, enrich, and automate how I consume information as I’m roaming around the web, researching specific topics, and do what I do.

At this point I am actually glad I didn’t invest a lot of energy into developing Chrome browser extension, because it wouldn’t have easily translated to a Firefox world. Since I have been investing in APIs plus bookmarklets, I can easily import, or copy and paste my bookmarklets over. I”m spending the time to go through them, inventory them, and better organize them for optimal usage, so the migration is a little more work than just import and export. Another aspect of this work that I am thankful for is that I abstracted away is the usage of other 3rd party APIs. My very first bookmarklet which profiles the domain of the website I’m looking at has used several different business intelligence solutions, all of which I have been priced out of using, so I’ve resorted to other ways to obtain the profile information I need--the API continues to work despite the APIs I use under the hood.

Browsers are an area of my API research that is significantly deficient. I am working to invest a little more time here, focusing on the migration and evolution of my API driven bookmarklets, but also playing around with the <a href="https://developer.mozilla.org/en-US/docs/Web/API/Reporting_API">Browser Reporting API</a>, which is some pretty interesting HEADER voodoo. I can’t help but feel like the browsers will continue to play an increasingly important role when it comes to APIs. Not just because of browser APIs like the Reporting API, but also because of the hidden APIs web and mobile applications use, as well as the above the tables APIs we leverage within the browser—-like my bookmarklets. I find the browser a more interesting place to study how APIs are being put to work than with startups these days. I feel like it is where the “innovation” is occurring these days, and sadly, it isn’t the good kind of “innovation” everyone so passionately believes in—-it is the more exploitative ad-driven “innovation” that is pretty invasive in our lives.
