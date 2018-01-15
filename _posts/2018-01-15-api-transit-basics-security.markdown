---
published: true
layout: post
title: 'API Transit Basics: Security'
date: 2018-01-15T11:00:00.000Z
tags:
  - API Evangelist
  - Security
image: 'https://s3.amazonaws.com/kinlane-productions/bw-icons/bw-padlock.png'
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/bw-icons/bw-padlock.png" align="right" width="25%" style="padding: 15px;" /></p>

_This is a series of stories I'm doing as part of [my API Transit work](http://basics.apievangelist.com/), trying to map out a simple journey that some of my clients can take to rethink some of the basics of their API strategy. I'm using a subway map visual, and experience to help map out the journey, which I'm calling [API transit](http://basics.apievangelist.com/)--leveraging the verb form of transit, to describe what every API should go through._

Hopefully you already have your own security practices in place, with the ability to scan for vulnerabilities, and understand where security problems might exist. If you do, I'm guessing you probably already have procedures and protocols around reporting, and handling security problems across teams. Ideally, your API security practices are more about prevention than they are about responding to a crisis, but your overall strategy should have plans in place for addressing both ends of the spectrum.

Unfortunately in the wider API space, much of the conversation around API security has been slowed by many people feeling like their API management solutions were doing everything that is needed. Luckily, in 2017 we began to see this thaw a bit and some API security focused solutions began to appear on the market, as well as some existing players began tuning into to address the specific concerns of API security, beyond the desktop, web, and other common areas of concern.

- [**Scanning APIs with OWASP Zap**](https://zaproxy.blogspot.com/2017/06/scanning-apis-with-zap.html) - OWASP is the top place for understanding security vulnerabilities of web applications, and they are expanding their focus to include APIs.
- [**42 Crunch**](https://www.42crunch.com/) - A new, OpenAPI driven API security solution for helping deliver policies across API operations.
- [**OWASP REST Security Cheat Sheet**](https://www.owasp.org/index.php/REST_Security_Cheat_Sheet) - A checklist of considerations when it comes to API security out of OWASP.

After crafting this stop along the API lifecycle I wanted to make sure and include API discovery in the conversation. API definitions like OpenAPI, and a solid API discovery strategy helps provide the details of the surface area of API operations, allowing for easier scanning and securing of existing infrastructure. Another area that significantly introduces security benefits is making logging a first class citizen, allowing the DNS, gateway, code, server, and database layers to analyzed for vulnerabilities.

I prefer keeping this security stop short and sweet, as I know from experience that not all my readers have a strategy in place, and I want to give them a handful of options to consider as they look to get started. Many groups have been focusing on web and mobile security, but are just getting started thinking about API security. As APIs move out of the shadows behind mobile applications, and the number of threats increase, companies, institutions, and government agencies are getting more nervous, increasing the need for more API security storytelling here on my site.
