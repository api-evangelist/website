---
published: true
layout: post
title: >-
  Seeing Reflections From The Past Rippling In The API Pool When I Translated
  WSDL To OpenAPI
date: 2018-01-08T16:00:00.000Z
tags:
  - API Evangelist
  - Definitions
  - SOAP
  - WSDL
  - Transformation
image: 'https://s3.amazonaws.com/kinlane-productions/matrix-neo.jpg'
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/matrix-neo.jpg" align="right" width="45%" style="padding: 15px;" /></p>I was looking for [the API definition and schema for the Service Interface for Real Time Information (SIRI) standard](http://user47094.vs.easily.co.uk/siri/schema/schemas.htm), but all they have were WSDL and XSDs. I am working with [the Metropolitan Transit Authorities (MTA) SIRI feed](http://bustime.mta.info/wiki/Developers/SIRIIntro), which returns JSON, and I wanted to have a JSON schema reflecting the responses I was working with. [So I took the WSDLs and converted them to OpenAPI using the API Transformer](https://apimatic.io/transformer), which kind of felt like that scene in the matrix where the world around him is beginning to turn to liquid as he pokes at it, right before he exits the matrix.

I regularly get the emails and tweets from folks telling me "we've done all this before", when I talk about OpenAPI. I'm fully aware that we have, and have even written a few stories about it. However, translating my first WSDL into an OpenAPI was a new experience for me, and made me think deeply about where we are at in 2018 a little bit more. I was reminded once again of how much we've left behind, and how much of this we are slowly recreating as part of the OpenAPI specification, and the other definitions and tooling we are developing. I don't think all of this is bad, but I do think we've never been able to have an honest conversation about all of this.

Over the last decade I feel like there has been two camps, those still committed to web services, and those that had invested in this new paradigm. Web service folks have mostly dug in their heals, and proclaimed, "we've already done all this". While us web API folks moved forward with this new realm, somewhat in denial about where we've been. Most discussions have been pretty black or white, meaning it was all new, or all old, and we couldn't really ever talk about things at a granular level, and exploring the grey layers in between. There was a lot of good in the web services model, and I don't think we have ever processed what that good was--we just moved on.

When I work with WSDL and XSD it is clear that this stuff wasn't meant for humans. Something I think web APIs, and using YAML for describing interfaces and schema has significantly improved upon. I think an API design first approach has also helped out significantly, making the interfaces, and schema much softer, and easier to sit down and understand WTF is going on. However I think a lot of the scaffolding and structure that existed in the web services world is being recreated, and we are doing a lot of the same work all over again. I feel like the same polarizing conversation we see around hypermedia, GraphQL, microservices, and other areas of evolution in the space reflect the same damaging effects of technological dogma that keeps us from being sensible about this stuff.

Anyhoo, I don't think there is any solutions here. I'm just going to develop a robust toolbox for helping me map web services to a fresher web API implementation. I'm not a fan of translating SOAP to REST, but I do like having tools that help me make sense of what was, and create a scaffolding for what can be. Then I just dive in and clean up, polish, and move forward as I see fit. I just had to share my moment of anxiety as I translated that WSDL into OpenAPI. For a moment I felt like Neo in the Matrix, and wasn't entirely sure whether this was real, or a simulation. I'm betting this is all real, we are just humans, and enjoy being our own worst enemies most of the time, and doign work over and over and over--rarely ever learning from the past. ;-(
