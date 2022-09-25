---
published: true
layout: post
title: Either You Own The Conversation Around Your APIs Or Someone Else Will
date: 2017-07-11T11:00:00.000Z
tags:
  - API Evangelist
  - Rogue
  - Mobile
  - Politics of APIs
image: >-
  https://s3.amazonaws.com/kinlane-productions/rogue/tinder-api-google-search.png
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/rogue/tinder-api-google-search.png" align="right" width="40%" style="padding: 15px;" /></p>I was looking at how many of the top mobile applications in the iTunes story actually had a public API presence, and was finding it very telling what came up in the Google search results for each company when I searched [company name] + API. It tells a lot about how a company sees the world, when they don't have a public API presence, but they have a very public mobile application that uses APIs.

An example of this is with Tinder, where the top listings are all Github rogue API repositories, when you Google "Tinder API". Tinder doesn't own the conversation when it comes to their own APIs. While the Tinder APIs are public, and well documented, Tinder prefers acting like they are private--they aren't. Pinterest uses SSL pinning, but [there is even a good amount of information out there at how to get around that](https://ritcsec.wordpress.com/2016/12/11/bypassing-certificate-pinning-on-tinder/), making the mapping out and documenting of Tinder APIs a pretty doable thing.

Honestly, I don't care about Tinder's APIs. They are just an easy example to point a finger at and use as a poster child. I don't even expect them to have fully public APIs that any developer could use without permission. Sure, lock that shit down, but provide a sandbox, and make sure every application gets approval before they can more access to live data. Make sure that you own the API conversation by having a developers portal, and provide information regarding what it takes to get access, and maybe some day actually become an approved partner.

I'm not saying that every company should have freely available public APIs. I'm saying every company should own the public conversation around their APIs, no matter what their strategy for developing applications around a platform's APIs. Have a presence. Own the conversation. Have a door for application developers to walk, even if there is a waiting room. Not all applications will be competing with your own web, mobile, device, or network applications. Some will be about enabling data portability for you users, or maybe provide useful access aggregate data for use in visualizations--you never know what folks will be bringing to the table, why keep the door closed?

I understand. You may not be all team API like I am, but you are using APIs to drive your mobile experience. I just don't get why you wouldn't want to own the conversation around these APIs. You are leaving so much on the table. If your mobile app is finding success, people will want access to the goodness going on behind it--[a rogue API is what kickstarted the Instagram API in the early days](http://apievangelist.com/2011/02/08/instagram-launches-api/). It is pretty easy to reverse engineer any mobile application, and map out the surface area of the API behind, as well as the authentication in play. Either you own the conversation around your API, or someone will step up and do it for you in todays online world.
