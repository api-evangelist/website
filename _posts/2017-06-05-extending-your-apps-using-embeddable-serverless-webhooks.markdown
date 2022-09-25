---
title: Extending Your Apps Using Embeddable Serverless Webhooks
date: 2017-06-05 16:00:00 Z
tags:
- Webhooks
- Serverless
- API Evangelist
- Embeddable
image: https://s3.amazonaws.com/kinlane-productions/auth0/auth0-extensions-screenshot-editor.png
---

<p><a href="https://auth0.com/blog/introducing-auth0-extend-the-new-way-to-extend-your-saas/"><img src="https://s3.amazonaws.com/kinlane-productions/auth0/auth0-extensions-screenshot-editor.png" align="right" width="35%" style="padding: 15px;" /></a></p>[Auth0 has released a pretty interesting way to extend your web applications using what is an embeddable, serverless, webhooks environment](https://auth0.com/blog/introducing-auth0-extend-the-new-way-to-extend-your-saas/)--for lack of a better description.  It's a pretty interesting way to extend applications in a scrappy, hackable, scriptable, webhooky kind of way. The extensions are definitely not for non-developers, but provide a kind of scriptable view source that any brave user could use to get some interesting things done within an existing web application interface.

Here are some of the selling features of Auth0 extensions:

* They are deployed outside of your product and managed externally.
* They run securely and in isolation from your SaaS application. The SaaS will not go down due to a faulty Webhook.
* They are generally easy for a developer to create, whether it's your own engineers, customers, or partners.
* They can be authored in a number of programming languages.
* They can use whatever third-party dependencies they need.

I think it is an interesting approach to extending existing applications using Webhooks. I'm guessing some users might be intimidated by it, but I could see it be something that developers and tech savvy users could hack together some pretty interesting implementations. Then when you start saving these interesting scripts, making them available to power users via a catalog--I could see some useful things emerge. I remember several jobs I've had that had some sort of universal SQL text area within a system, allowing power users to craft and reuse useful SQL scripts--this seems like a similar approach, but for the API age. 

I'm curious to see where this kind of solution goes. It is a quick way to extend SaaS functionality, allowing users to get more from an application without expensive developer cycles, and offloading the compute to external services. I think it is a creative convergence of what I see as embeddable, serverless, and webhooks--all part of an effective API strategy. I'm hoping it injects some creativity and extensibility into existing apps, allowing them to better serve the long tail of users needs in an API serverless webhook way.