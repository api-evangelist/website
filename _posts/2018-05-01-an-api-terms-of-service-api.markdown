---
published: true
layout: post
title: An API Terms of Service API
date: 2018-05-01T11:00:00.000Z
tags:
  - API Evangelist
  - Terms of Service
image: 'https://s3.amazonaws.com/kinlane-productions/box/box-terms-of-service-api.png'
---
<p><img src="{{ page.image }}" width="45%" align="right" style="padding: 15px;" /></p>I've been [tracking on the terms of service for APIs](http://terms-of-service.apievangelist.com/) for eight years, but I haven't ever come across a terms of service API. I found one the other day while looking through [the Box API](https://developer.box.com/), and thought it was worth showcasing as part of my research. [The Box terms of service API](https://developer.box.com/v2.0/reference#terms-of-service-object), "allows Box Admins to configure ToS and end users to accept / re-accept ToS for custom applications." The Box terms of service API represents the association between Terms of Services and users, providing several different configurations:

- There is exactly one Terms of Service User Status for a given Terms of Service and a given user.
- There are multiple Terms of Service User Statuses for a given Terms of Service (e.g. one per each user).
- There could be multiple Terms of Service User Statuses for a given user. The user could accept/reject multiple external ToS for enterprises they have been collaborated into in addition to accepting/rejecting their own enterprise’s managed ToS.

The Box terms of service API allows for managing multiple terms of service, and multiple users  engagement with those terms of service. Providing eight separate API endpoints for managing each individual terms of service, and the users agreement to them. I'd like to see a more modular approach to managing the components of each terms of service, as it applies to APIs. Allowing for more reusable terms of service modules that can be reused across many different APIs. I'm thinking beyond just documents and their applications, I am thinking about widely applied across APIs and any application that can be built on them.

I'm going to add Box's terms of service API definition to my research, and use as a base for other potential use cases. It is one of those areas I feel like need some investment in, to help make this layer of API operations more observable. Every building block of the API platform should have an API in my opinion, especially the terms of service layer. It is an API pattern I'd like see exist in the API space, and is an API definition I'll add to to help make more applicable, and forkable so that API providers can implement their own terms of service API.
