---
published: true
layout: post
title: Plugin Infrastructure For Every Stop Along The API Lifecycle
date: 2017-08-03T16:00:00.000Z
tags:
  - API Evangelist
  - Plugins
  - iPaaS
  - Integration
  - Lifecycle
image: 'https://s3.amazonaws.com/kinlane-productions/tyk/tyk-plugins.png'
---
<p><a href="https://tyk.io/features/extend-tyk/"><img src="https://s3.amazonaws.com/kinlane-productions/tyk/tyk-plugins.png" align="right" width="40%" style="padding: 15px;" /></a></p>I'm continuing [my integration platform as a service (iPaaS) research](http://ipaas.apievangelist.com), understanding [how API providers are quickly integration with other platform](http://apievangelist.com/2017/08/02/making-sure-your-api-service-connects-to-other-stops-along-lifecycle/), I am also looking into how API service providers are opening up their services to the entire API lifecycle. I'm seeing API service provides offer up a default set of integrations with other platforms, ad in some cases using Zapier by default--opening up 750+ other API driven platforms pretty quickly. Another dimension of this that I'm tracking on is when API service providers offer up plugin infrastructure, allowing other platforms to develop plug and play integrations that any platform user can take advantage of.

You can see this in action over at my partner Tyk, who has [a nice set of plugins for their API management solution](https://tyk.io/features/extend-tyk/). They start with three language focused middleware plugins allowing you to write scripts in Java, Lua, and JavaScript. Then they offer two gRPC plugins, which might be another post all by itself. While very similar to the iPaaS, or custom integration solution I've seen from other API providers, I'm going to be categorizing plugin approaches to integration like this separately, because it invites developers to come develop integrations as plugin--something that is very API in my book.

[I've added a separate research area to tune into what types of integrations platforms are introducing via plugin infrastructure](http://plugin.apievangelist.com/). I'm trying to understand how plugins are evolving from being more about platform, browser, and other common forms and becoming more API lifecycle middleware (for lack of better term), like Tyk. I want to be aware of each of their approaches, and how different stops along the API lifecycle are embedding scripting engines, injecting integrated features into operations, and making it part of any continuous integration and deployment workflow(s). Like the other areas of my API lifecycle research, I will stop in from time to time, and understand if plugin API infrastructure is evolving and becoming more of a thing.
