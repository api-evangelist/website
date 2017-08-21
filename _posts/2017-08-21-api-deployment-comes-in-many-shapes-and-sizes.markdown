---
published: true
layout: post
title: API Deployment Comes In Many Shapes And Sizes
date: 2017-08-21T09:00:00.000Z
tags:
  - API Evangelist
  - Deployment
image: 'https://s3.amazonaws.com/kinlane-productions/bw-icons/bw-deploy.png'
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/bw-icons/bw-deploy.png" align="right" width="40%" style="padding: 15px;" /></p>Deploying an API is an interesting concept that I've noticed folks struggle with a little bit when I bring it up. My research into API deployment was born back in 2011 and 2012 when my readers would ask me  which API management provider would help them deploy an API. How you actually deploy an API varies pretty widely from company to company. Some rely on gateways to deploy and API from an existing backend system. Some hand-craft their own API using open source API frameworks like [Tyk](https://s3.amazonaws.com/kinlane-productions/partners/tyk-logo.png) and deploy alongside your existing web real estate. Others rely on software as a services solutions like [Restlet](http://apis.how/5ytnitnakm) and [Dreamfactory](http://apis.how/bgdteovduo) to connect to a data or content source and deploy an API in the clouds.

Many folks I talk with simply see this as developing their APIs. I prefer to break out development into define, design, deploy, and then ultimately manage. In my experience, a properly defined and designed API can be deployed into a variety of environments. The resulting OpenAPI or other definition can be used to generate server side code necessary to deploy an API, or maybe used in a gateway solution like AWS API Gateway. For me, API deployment isn't just about the deployment of code behind a single API, it includes the question about where we are deploying the code, acknowledging that there are many places available when it comes to deploying our API resources.

API deployment can be permanent, ephemeral, or maybe just a sandbox. API deployment can be in a Docker container, which by default deploys APIs for controlling the underlying compute for the API you deploying. Most importantly, API deployment should be a planned, well-honed event. APIs should be able to be redeployed, load-balanced, and taken down without friction. It can be easy to find one way of deploying APIs, maybe using similar practices surrounding web deployments, or dependent on one gateway or cloud service. Ideally, API deployment comes in many shapes and sizes, and is something that can occur anywhere in the clouds, on-premise, or on-device. Pushing our boundaries when it comes to which platforms we use, which programming languages we speak, and what API deployment means.
