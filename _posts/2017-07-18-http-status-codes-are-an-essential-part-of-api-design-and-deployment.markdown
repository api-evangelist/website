---
published: true
layout: post
title: HTTP Status Codes Are An Essential Part Of API Design And Deployment
date: 2017-07-18T09:00:00.000Z
tags:
  - API Evangelist
  - Monitoring
  - Design
  - HTTP Status Codes
image: >-
  https://s3.amazonaws.com/kinlane-productions/api-evangelist/runscope/runscope-200-ok.jpeg
---
<a href="https://www.runscope.com/"><img src="https://s3.amazonaws.com/kinlane-productions/api-evangelist/runscope/runscope-200-ok.jpeg" alt="" align="right" width="40%" /></a>
It takes a lot of work provide a reliable API that people can depend on. Something your consumers can trust, and will provide them with consistent, stable, meaningful, and expected behavior. There are a lot of affordances built into the web, allowing us humans to get around, and make sense of the ocean of information on the web today. These affordances aren't always present with APIs, and we need to communicate with our consumers through the design of our API at every turn.

One area I see IT and developer groups often overlook when it comes to API design and deployment are [HTTP Status Codes](https://en.wikipedia.org/wiki/List_of_HTTP_status_codes). That standardized list of meaningful responses that come back with every web and API request:

- **1xx Informational** - An informational response indicates that the request was received and understood. It is issued on a provisional basis while request processing continues.
- **2xx Success** - This class of status codes indicates the action requested by the client was received, understood, accepted, and processed successfully.
- **3xx Redirection** - This class of status code indicates the client must take additional action to complete the request. Many of these status codes are used in URL redirection.
- **4xx Client errors** - This class of status code is intended for situations in which the client seems to have errored.
- **5xx Server error** - The server failed to fulfill an apparently valid request.

Without HTTP Status codes, application won't every really know if their API request was successful or not, and even if an application can tell there was a failure, it will never understand why. HTTP Status Codes are fundamental to the web working with browsers, and apis working with applications. HTTP Status Codes should never be left on the API development workbench, and API providers should always go beyond just 200 and 500 for every API implementation. Without them, NO API platform will ever scale, and support any number of external integrations and applications.

The most important example I have of the importance of HTTP Status Codes I have in my API developers toolbox is when [I was working to assist federal government agencies in becoming compliant with the White House's order for all federal agencies to publish a machine readable index of their public data inventory of their agency website](http://apievangelist.com/2012/06/02/tracking-federal-agencies-progress-on-api-deployment/). As agencies got to work publishing JSON and XML (an API) of their data inventory, I got to work building an application that would monitor their progress, indexing the available inventory, and providing a dashboard the the GSA and OMB could use to follow their progress (or lack of).

I would monitor the dashboard in real time, but weekly I would also go through many of the top level cabinet agencies, and some of the more prominent sub agencies, and see if there was a page available in my browser. There were numerous agencies who I found had published their machine readable public data inventory, but had returned a variety of HTTP status codes other than 200-resulting in my monitoring application to consider the agency not compliant. [I wrote several stories about HTTP Status Codes](http://kinlane.com/2013/11/06/knowing-your-http-status-codes-in-federal-government/), in which the GSA, and White House groups circulated with agencies, but ultimately I'd say this stumbling block was one of the main reasons that cause this federated public data API project to stumble early on, and never gain proper momentum--a HUGE loss to an open and more observable federal government. ;-(

HTTP Status Codes aren't just a nice to have thing when it comes to APIs, they are essential. Without HTTP  Status Codes each application will deliver unreliable results, and aggregate or federated solutions that are looking to consume many APIs will become much more difficult and costly to develop. Make sure you prioritize HTTP Status Codes as part of your API design and deployment process. At the very least make sure all five layers of HTTP Status Codes are present in your release. You can always get more precise and meaningful with specific series HTTP status codes later on, but ALL APIs should be employing all five layers of HTTP Status Codes by default, to prevent friction and instability in every application that builds on top of your APIs.
