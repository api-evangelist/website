---
published: true
layout: post
title: You See Duplicate Work While I See Common Patterns
date: 2017-07-31T11:00:00.000Z
tags:
  - API Evangelist
  - Definitions
image: >-
  https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories/carryload_diego_rivera1.jpg
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories/carryload_diego_rivera1.jpg" align="right" width="40%" style="padding: 15px;" /></p>Someone asked me on Twitter recently how I deal the duplicate work required to manage a large volume of OpenAPIs. All the same things you have to do when crafting the headers, parameters, responses, and schema across every OpenAPI you are crafting. My response was that I don't see these things as repetitive or duplicate work, I see these things as common patterns across the resources I am making available. They main reason I think they seem repetitive is the tooling we are currently using needs to play catch up, and help us better apply common patterns across all our APIs--dealing with the duplicate, repetitive work for us.

I'm confident that open source API design tooling like [Apicurio](http://www.apicur.io/) are going to help us better manage the common patterns we should be applying across our OpenAPIs. I'm also hopeful that [OpenAPI 3.0](https://github.com/OAI/OpenAPI-Specification/blob/master/versions/3.0.0.md) contributes to reuse of parameters, schema, errors, and other common building blocks across the request and response surface of our API. I'm counting on OpenAPI + Apicurio as well as other API definition and design tooling to step up and do the hard work wen it comes to helping us manage the common patterns across our APIs, and make the reuse of common patterns across our APIs a good thing, and never a burden.

This reuse shouldn't just being within any company, and we should be reusing and sharing patterns from across the space, including common web concepts and standards. The fact that you use ISO 8601 for all your dates, while employing a handful of date field names over and over across your systems isn't repetition or duplicate work, that is consistency, and sensible reuse of common API patterns. It is the job of API design service and tooling providers to help us get over this hump, and craft notebooks, catalogs, collections, dictionaries, and stores of the common patterns we will need to be applying (over and over again) across our API definitions--OpenAPI.

I enjoy these regular reminders regarding how differently folks see the API space. I also enjoy the focus on the role that API specification formats and tooling will play in helping carry the load enough so folks don't see detailed API definitions as a burden. I regularly come across OpenAPIs that you can tell are incomplete because someone was just doing the minimum amount of work they needed to deliver documentation for an API. It should be a no-brainer for API designers and developers to make sure there is always a robust, complete, and detailed OpenAPI for any existing API--while ensuring common patterns are applied at every turn.
