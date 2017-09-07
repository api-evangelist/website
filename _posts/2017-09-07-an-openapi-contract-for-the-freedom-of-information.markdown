---
published: true
layout: post
title: An OpenAPI Contract For The Freedom Of Information
date: 2017-09-07T09:00:00.000Z
tags:
  - API Evangelist
  - Federal Government
  - Definitions
  - FOIA
  - Transprency
  - Observability
image: >-
  https://s3.amazonaws.com/kinlane-productions/foia/freedom-of-information-stamp.jpg
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/foia/freedom-of-information-stamp.jpg" align="right" width="40%" style="padding: 15px;" /></p>Today's stories are all based around my preparation for providing some feedback on the next edition of the FOIA.gov API. I have a call with the project team, and want to provide ongoing feedback, so I am loading the project up in my brain, and doing some writing on the topic. The first thing that I do when getting to know any API project, now matter where it is at in it's lifecycle, is craft an [OpenAPI](https://github.com/OAI/OpenAPI-Specification), which will act as a central contract for discussions. Plus, there is no better way, short of integration, to get to know an API than crafting a complete (enough) OpenAPI definition.

After looking through [the FOIA recommendations for the project](https://github.com/18F/foia-recommendations/blob/master/recommendations.md), I took the draft FOIA API specification and crafted this OpenAPI definition:

<script src="https://gist.github.com/kinlane/ca85e904c05e1ec28c6d277f62be2f80.js"></script>

The specification is just for a single path, that allows you to POST a FOIA request. I made sure I thought through the supporting schema that gets posted, flushing out using the definitions (JSON schema) portion of the OpenAPI. This helps me see all the moving parts, and connect the dots between the API request and response, complete with definition for three HTTP status codes (200,404,500)--just the basics. Now I can see the technical details of a FOIA request in my head, preparing me for my discussion with the project owners.

After loading the technical details in my head, I always like to step back and think about the business, political, and ultimately human aspects of this. This is a Freedom of Information Act (FOIA) API, being used by U.S. citizens to request that information within the federal government be freed. That is pretty significant, and represents why I do API Evangelist. I enjoy helping ensure APIs like this exist, are usable, and become a reality. It is interesting to think of the importance of this OpenAPI contract, and the potential it will have to make information in government more accessible. Providing a potential blueprint that can be used by all federal agencies, establishing a common interface for how the public can engage with government when it comes to holding it more accountable.
