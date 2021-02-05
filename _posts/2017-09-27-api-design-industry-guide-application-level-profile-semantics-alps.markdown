---
published: true
layout: post
title: 'API Design Industry Guide: Application-Level Profile Semantics (ALPS)'
date: 2017-09-27T16:00:00.000Z
tags:
  - API Evangelist
  - Design
  - Definitions
image: >-
  https://s3.amazonaws.com/kinlane-productions/guides/definition/design/api-design-industry-guide-api-stylebook.png
---
<p><a href="http://design.apievangelist.com/#Guide"><img src="https://s3.amazonaws.com/kinlane-productions/guides/definition/design/api-design-industry-guide-alps.png" align="right" width="40%" style="padding: 15px;" /></a></p>
_This post is from the latest copy of my [API Evangelist API Design Industry Guide](http://design.apievangelist.com/#Guide), which provides a high level look at the API design layer of the industry. Providing a quick look at the services, tools, and some of the common building blocks of API design. The guide is heavily rooted in REST and hypermedia, but is working to track on the expansion of the space beyond just these formats. My industry guides change regularly, and I try to publish the articles from them here on the blog to increase their reach and exposure._

Current API design focusses on using schema to help quantify the payload of the request and response structure of our APIs. JSON Schema, MSON, and other data specifications have emerged to help us quantify the bits we are passing back and forth with APIs. Alongside this evolution, another data format has emerged to help us define simple descriptions of our application-level semantics, similar to how we are using HTML microformats to share data on the web, Application-Level Profile Semantics (ALPS).

ALPS goes well beyond schema, which provides a representation of a plan or theory in the form of an outline or model. ALPS provides a way to define the meaning behind the data, content, and other resources you are making available via an API. ALPS seeks to establish a shared understanding by illuminating the meaning behind hypermedia interfaces (data and state transitions) such as HTML, Collection+JSON, HAL or Siren. It encourages reusability of common profile documents across the media types we are depending on.

Using ALPS you can easily define the common data elements we all use in our API like contacts, todo lists. It can even describe the structure of our APIS for verbose and more useful error responses. What really matters is that you can also define the transitions surrounding these data elements. You can get at the meaning and use behind them, like rolling dice, or playing with a deck of cards. It’s much more than just metadata describing the data elements at work.

If we want our APIs designs to reflect the meaning and interactions around the valuable resources we are serving up, we need to work hard to make sure we are all using common data formats and schema. Schema.org provides us with a good start, but we also need to invest in more in ALPS registries, directories, and dictionaries. These provide machine readable definitions of the common data elements exchanged between systems and applications, as well as the meaning, relationships, interactions, and transitions that make these data elements valuable in our digital worlds.

ALPS has been submitted as an Internet Engineering Task Force (IETF) draft, and provides one possible standard to consider when looking to define the semantics behind API operations.  Visit: http://apis.how/alps-io/ for more information.
