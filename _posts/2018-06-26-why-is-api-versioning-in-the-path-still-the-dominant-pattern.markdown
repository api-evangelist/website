---
published: true
layout: post
title: Why Is API Versioning In The Path Still The Dominant Pattern?
date: 2018-06-26T09:00:00.000Z
tags:
  - API Evangelist
  - Versioning
  - Politics of APIs
image: >-
  https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories/los-angeles-downtow-freeway_blue_circuit_5.jpg
---
<p><img src="{{ page.image }}" width="45%" align="right" style="padding: 15px;" /></p>API versioning is almost always one of the top attended discussions at conferences I help organize, and one of the first questions I get in the QA sessions at workshops I conduct. People want to understand the "right way" to version, when it my experience there is rarely ever a "right way" to version your APIs. There are commonly held practices regarding sensible ways to version your APIs, as well as dominant patterns for how you version APIs, but there isn't any 100% solid answer to the question, despite what many folks might say.

In my experience, the most commonly held approach to properly versioning your APIs (if you are going to), is to put the major and minor version in your header and / or combine it with content-type negotiation via your header. However, even with this knowledge being widely held, the most dominant pattern for versioning your APIs is sticking it in the URL of your API. I know many API providers who put the version in the header, despite many on their team fully being aware that it is something that should be put in the header. So, why is this? Why do people still do it the "wrong way", even though then know how to do it the "right way"?

I feel like this phenomenon reflects the wider API space, and how upside down many API belief systems are. People put the version in the URL because it is easier for them, and it is easier for their developers to understand. While headers are a native aspect of developing using the web, they are still very foreign and unknown to most developers. While this shows the lack of web literacy that is rampant amongst developers, it also demonstrates why simple web APIs have dominated the landscape--they are easy for a wide segment of developers to understand. An aspect of why this whole API thing has worked that many technologists overlook, and take for granted as they try to push the next trend or solution on the sector.

While conducting workshops, I always teach the more sensible patterns around versioning, but I can't always sell them as the "right way". Because I don't see a "right way". I see people trying to get a job done, and reach a wide audience. I see people trying to keep things simple for their developers, and taking the path of least resistance. I see a whole lot of web literacy education that needs to occur across the tech sectors and in school. I just don't see any perfect answer to the API versioning debate. I see a whole lot of interesting and useful patterns, and I see people doing the best they can with what they have. Reflecting why APIs work so well, because they are scrappy, often times simple, and allow people to get business done on the web using low cost, easy to understand approaches to making resources available.
