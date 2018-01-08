---
published: true
layout: post
title: 'API Life Cycle Basics: Deployment'
date: 2018-01-08T11:00:00.000Z
tags:
  - API Evangelist
  - Deployment
image: 'https://s3.amazonaws.com/kinlane-productions/bw-icons/bw-api-deployment.png'
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/bw-icons/bw-api-deployment.png" align="right" width="30%" style="padding: 15px;" /></p>There are many ways to deploy an API, making this another confusing stop along the API life cycle for some of my readers. My goal in having this be a separate stop from design, or possibly management, is to help API providers think about where and how they deploy APIs. From my perspective, API deployment might be about which framework and language you choose to deploy in, spanning all the way to where you might deploy it, either on-premise, on-device, or in the cloud. The how and why of deploying your API will play a significant role in determining how stable and consistent you are able to deploy API resources, impacting almost every other stop along the API life cycle.

Many API providers still think of API deployment in the context of their internal operations, as opposed to thinking about how they will be put to use. The providers I'm seeing enjoy more flexibility and agility when it comes to API consumption are able to deploy APIs in a variety of languages, supporting a variety of existing platforms, and in any environment where they are needed. There are several concepts that are beginning to define API deployment in this new generation of compute in the cloud, here are just a handful of them.

- **Polyglot Deployment** - The ability to deploy APIs in a variety of programming languages.
- **Multi-Platform** - The ability to deploy APIs in a variety of platforms, and using existing system.
- **Multi-Cloud** - The ability to deploy APIs within Amazon, Azure, Heroku, and Google environments.
- **Frameworks** - Leverage a variety of open source API frameworks for deploying APIs.

I normally would put API gateways here as well, but because of renewed energy around gateway solutions actually deploying APIs instead of just managing and securing them, I'm breaking out gateway into its own stop along the API lifecycle. Gateway spans API deployment and management in my opinion, and while it should be considered alongside these elements, it is increasingly becoming its own stop. Ideally, teams are able to use a combination of gateway, as well as hand-rolled, and auto-generated approaches to deploying APIs, with the diversity I mentioned above.

Most groups I work with have one way to deploy APIs, using a single programming language. This results in many of them thinking about API consumption on the same terms. When you allow for, and support a variety of languages, platforms, and cloud environments, you open up a new world of possibilities when it comes to scaling, migrating, and hiring talent as part of your API operations. API deployment will be a new concept to many of my readers, and something not all will be ready for, but being able to think outside the API box you've been operating within until now is one of the basic aspects of the API life cycle you should be looking at evolving.
