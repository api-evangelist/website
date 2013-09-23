---
layout: post
title: "Interactive API Documentation With Swagger"
url: 'http://apievangelist.com/2013/03/21/interactive-api-documentation-with-swagger/'
image: 'http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/blog/reverb-for-developers-swagger.png'
---

[<img class="c1" src="https://s3.amazonaws.com/kinlane-productions/api-evangelist/swagger/reverb-for-developers-swagger.png" alt="" width="225" align="right" />][1]

It is becoming more common for API providers to deliver documentation using what's known as [interactive API documentation][2], instead of the usual static API documentation. Understanding how to use an API can be tough sometimes, and rather than just reading about it how it works, interactive API documentation allows you make real calls against an API, while learning about the interface.

While there are several approaches to delivering interactive API documentation, my personal favorite is using [Swagger][1]. Swagger comes built in with [3Scale][3], which is the API management platform I use for the [API Evangelist API][4], but Swagger is available for anyone to use as an [open source project][5].

Interactive API documentation using Swagger starts with a Swagger definition, which is a JSON representation of an API endpoint. In this case, the endpoint is for accessing my blog posts:

This JSON describes everything about my very basic endpoint, which allows users to query almost 3 years of API Evangelist blog posts. Using this definition, Swagger generates the following API documentation automatically:

<img class="c2" src="https://s3.amazonaws.com/kinlane-productions/api-evangelist/swagger/swagger-interactive-documentation-1.png" alt="" width="500" />

As someone learning about the API Evangelist Analysis API, this describes the endpoint, which fields are required to make an API call, but it doesn’t just describe this with text, it provides an interactive interface in which I can enter my API keys, provide a query value and actually make a request against the API:

<img class="c2" src="https://s3.amazonaws.com/kinlane-productions/api-evangelist/swagger/swagger-interactive-documentation-2.png" alt="" width="500" />

So I don’t just learn about the API endpoint. I learn about what keys are needed and fields are present that allow me to request different information of the API endpoint. It allows me to actually see the request to the API, the resulting body of my API request.

This type of hands on learning is essential to onboarding new users with your API. I can read your API documentation and not see the value, but when I am walked through how to build a request, and actually see the value returned in real-time, it changes the game. As a developer I’m more likely to understand and integrate with an API when I am given interactive API documentation over static pages.

The benefits of describing your API using Swagger don’t stop with just providing [interactive API documentation][6]. Swagger can also help deliver [code samples][7] in multiple programming languages for developers to put to use, [generate server side code][8] for new APIs and [provide potential benefits for API discovery][9].

It is well known that [API documentation is the number one pain point for developers][10]. Make sure your API documentation is hands-on, and interactive, so developers will understand the value your API delivers immediately, and go from learning, to integration, in as short of period as possible.

**Disclosure**: 3Scale is an API Evangelist partner

   [1]: https://developers.helloreverb.com/swagger/ (Swagger)
   [2]: /buildingblocks/interactive_documentation.php (interactive API documentation)
   [3]: http://3scale.net (3Scale)
   [4]: https://apievangelist.3scale.net/
   [5]: https://github.com/wordnik/swagger-core/wiki
   [6]: https://github.com/wordnik/swagger-ui
   [7]: https://github.com/wordnik/swagger-codegen
   [8]: https://github.com/wordnik/swagger-core
   [9]: /2011/11/09/can-swagger-deliver-a-restful-api-discovery-service/
   [10]: http://blog.programmableweb.com/2010/08/12/web-api-documentation-best-practices/
