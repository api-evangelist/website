---
published: true
layout: post
title: Could I Please Get An API Discovery Tool That Evaluates An OpenAPI Diff
date: 2017-11-14T11:00:00.000Z
tags:
  - API Evangelist
  - Definitions
  - Communications
  - Road Map
  - Change Log
  - Github
image: 'https://s3.amazonaws.com/kinlane-productions/openapi/openapi-logo.png'
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/openapi/openapi-logo.png" align="right" width="30%" style="padding: 25px;" /></p>I am increasingly tracking on OpenAPI definitions published to Github by leading API providers I track on. Platforms like [Stripe](http://apievangelist.com/2017/11/12/stripes-openapi-is-available-on-github-in-version-30/), [Box](http://apievangelist.com/2017/05/22/box-goes-all-in-on-openapi/), [New York Times](http://apievangelist.com/2017/03/01/new-york-times-manages-their-openapi-using-github/) are actively managing their OpenAPI definitions using Github, making them well suited for integration into their platform operations, API consumer scenarios, and even within analyst systems like what I have going on as the API Evangelist.

Once I have an authoritative source of an OpenAPI, meaning a public URI for an OpenAPI that is actively being maintained by the API provider, I have a pretty valuable feed into the roadmap, as well as change log for an API. I feel like we are getting to the point where there are enough authoritative OpenAPIs that we can start using as a machine readable notification and narrative tool for helping us stay in tune with one or many APIs across the landscape. Helping us stay in tune with APIs in real-time, and giving APIs an effective tool for communicating out changes to the platform--we just need more OpenAPIs, and some new tooling to emerge.

I'm envisioning an OpenAPI client that regularly polls OpenAPIs and caches them. Anytime there is a change it does a diff, and isolated anything new. Think of an RSS reader, but for OpenAPIs, and going well beyond new entries, and actually creates a narrative based upon the additions and changes. Tell me about the new paths added, and any new headers, parameters, or maybe how the schema has grown. Provide me insights on what has changed, and possibly what has been removed, or will be removed in future editions. As an API analyst, I'd like to be able to have an OpenAPI-enabled approach to receiving push notifications when an API changes, with a short, concise summary about what has change in my inbox, via Twitter, or Github notification.

OpenAPI already provides API discovery features through the documentation it generates, and I'm increasingly using Github to find new APIs after they publish their OpenAPIs to Github, but this type of API discovery and notification at the granular level would be something new. If there was such tooling out there, it would provide yet another incentive for API provides to publish and maintain an active, up to date OpenAPI definition. This is a concept I'd like to also see expanded to the API operational level using [APIs.json](http://apisjson.org/), where we can receive notifications about changes to documentation, pricing, SDKs, and other critical aspects of API integration, beyond just the surface area of the API. All of this stuff will take many years to unfold, as it has taken over five years for us to reach a critical mass of OpenAPI definitions to emerge, I suspect it will take another five to ten years for robust tooling to emerge at this level, which also depends on many API definitions to be available.
