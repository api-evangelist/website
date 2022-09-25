---
published: true
layout: post
title: People Who Provide Enum For Their OpenAPI Definitions Are Good People
date: 2018-02-20T09:00:00.000Z
tags:
  - API Evangelist
  - Enums
  - Definitions
  - Parameters
  - Design
image: >-
  http://kinlane-productions.s3.amazonaws.com/algorotoscope/builder/filtered/64_116_800_500_0_max_0_-5_-1.jpg
---
<p><img src="http://kinlane-productions.s3.amazonaws.com/algorotoscope/builder/filtered/64_116_800_500_0_max_0_-5_-1.jpg" align="right" width="45%" style="padding: 15px;" /></p>I'm processing a significant amount of OpenAPI definitions currently, as well as crafting a number of them from scraped API documentation. After you work with a lot of OpenAPI definitions, aiming to achieve a specific objective, you really get to know which aspects of the OpenAPI are the most meaningful, and helpful when they are complete. [I talked about the importance of summary, description, and tags last week](http://apievangelist.com/2018/02/15/the-importance-of-the-api-path-summary-description-and-tags-in-an-openapi-definition/), and this week I'd like to highlight how helpful it is when the stewards of OpenAPI definitions include enum values for their parameters, and I think they are just good people. ;-)

Enums are simply just a list of potential values for each of the parameters you outline as part of your API definition. So if you have state as a parameter for use in the request of your API, you have a list of the 50 US states as the enum. If you the parameter is color, you have just the color black, because we all know it is the only color(all the colors). ;-) If you provide a parameter that will accept a standard set of inputs, you should consider providing an enum list to help your consumers understand the potential for that parameter. Outlining the dimensions of the parameter in a simple JSON or YAML array of every single possible value.

I can't articulate how many times I have to go looking for a list of values. Sometimes it is present within the description for the OpenAPI, but often times I have to go back to the portal for the API, and follow a link to a page that lists out the values. That is, if an API provider decides to provide this information at all. The thoughtful ones do, the even more thoughtful ones put it in their OpenAPI definitions as enum values. Anytime I come across a list of enums that I can quickly build an array, select, and other common aspects of doing business with APIs, I'm a happy camper.

Which is why you find me writing up enums. Boring. Boring. Boring. However, it is something that makes me happy, potentially multiple times in a single day, and imagine that multiplied by the number of developers you have, or maybe "had", depending on how frustrating it is to find the values that can be used in your API's parameters. In my opinion, enums add rich dimensions to what your API does, and can be as important as the overall design of your API. Depending on how you've designed your API, you may have invested heavily in design, or may be leaning on your API parameters to do the heavy lifting of helping you--making them even more important when it comes to documenting them as part of your API operations.
