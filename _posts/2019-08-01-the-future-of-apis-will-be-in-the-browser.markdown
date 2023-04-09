---
published: true
layout: post
title: 'The Future Of APIs Will Be In The Browser'
date: 2019-08-01T09:00:00.000Z
tags:
  - API Evangelist
  - Discovery
  - Browsers
image: https://s3.amazonaws.com/kinlane-productions2/algorotoscope-master/nazi-invasion-dark-hallway.jpg
---

I have been playing with the new <a href="https://developer.mozilla.org/en-US/docs/Web/API/Reporting_API">browser reporting API</a> lately, and while it isn’t widely supported, it does work in Chrome, and soon Firefox. I won’t go into too much technical detail, but the API provides an interesting look at reporting on APIs usage in the browser. Offering a unique view into the shadows of what is happening behind the curtain in our browser when we are using common web applications each day. I have been proxying my web traffic for a long time to produce a snapshot at the domains who are operating beneath the covers, but it is interesting for browsers to begin baking in a look at the domains who are violating, generating errors, and other shenanigans.

As I’m contemplating the API discovery universe I can’t help but think of the how “API innovation” is occurring within the browser.  When I say “API innovation”, I don’t mean the kind that got us all excited from 2005 through 2010, or the golden days from 2010 through 2015-—I am talking the exploitative kind. Serving advertisers, trackers, and other exploitative practices. Most people would scoff at me calling these things APIs, but they are using the web to deliver machine readable information, so they are APIs. I’ve been tracking on the APIs I use behind the scene in my browser using Charles Proxy for a while now, but I’m feeling I should formalize my analysis.

I’m thinking I’ll take a sampling of domain, maybe 250+, and automate the browsing of each page, while also running through Charles Proxy. Then aggregate all of the domains that are loaded, and categorize them by media type--just to give me a sampling of the APIs in operation behind the scenes of some common sites. I’m sure most are advertising or social related, but I’m guessing there are a lot of other surprises in there. While some of the APIs will be publicly showcased in some way, there are no doubt a number of APIs being used that do not have a public presence, documentation, or other visible element. While I am interested in learning how the public APIs I track on are used, I’m more interested in painting a picture of the shadow APIs that are running behind the JavaScript libraries, and other embeddable in use across the web.

Developer portals and API documentation are not the only way to find APIs. Reverse engineering mobile and web applications will continue to be a significant player when it comes to understanding the next generation of APIs. When I look across the web, all I see are APIs. I know I’m biased, but I think there is something to this. I don’t think all companies are interested in doing APIs the same way many of us API evangelist, pundits, analysts and believers are. They like APIs, but aren’t that interested in showcasing their practices, and sharing patterns with the rest of the community. I’m guessing they are more interested in penetrating our worlds via our browsers, and capturing some of the valuable behavioral exhaust we all produce on a daily basis.
