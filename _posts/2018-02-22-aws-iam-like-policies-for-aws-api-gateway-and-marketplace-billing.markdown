---
published: true
layout: post
title: AWS IAM-Like Policies For AWS API Gateway And Marketplace Billing
date: 2018-02-22T09:00:00.000Z
tags:
  - API Evangelist
  - Monetization
  - Plans
image: >-
  https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories-new/server-cloud1_internet_numbers.jpg
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories-new/server-cloud1_internet_numbers.jpg" align="right" width="45%" style="padding: 15px;" /></p>The primary reason I've been adopting more AWS solutions as part of my API stack, and using tools I have historically felt lock me into the AWS ecosystem, is the available of AWS identity and access management (IAM). I just cannot deliver secure at this level as a small business owner, and their robust solution lets me dial in exactly what I need when it comes to defining who has access to what across my API infrastructure. I can define different policies, and apply them at the API management layer using both AWS Lambda and AWS API Gateway. Keeping everything separated, yet with a single API stack as the point of entry, for all consumers and applications.

I want all of this security goodness, but for the business of my APIs. Similar to the engine that drives the relationship between me as an AWS Marketplace user and AWS, I want a framework for applying business policies at the plan level within AWS API Gateway. I want to determine who has access to which resources, as well as what they can use, but I want to be able to meter this usage, and charge different rates. Compute, storage, and bandwidth for my partners is different than for retail API consumers, with a mix of resource and API call based metrics.

[The AWS monetization policies would reflect the AWS Marketplace framework](https://plans.apievangelist.com/2017/10/23/api-monetization-framework-introduced-by-aws-marketplace/), giving me a mix of metering and contract based billing, reflecting single or multi-dimensional usage across the eight areas of consumption they support currently. I want to be able to establish common monetization policies across all my microservices, and allow product managers to implement them consistently at scale using AWS API Gateway. Like security, these API product managers shouldn't be experts in the economics of the services being offered, they should just be able to apply from a common pool of business policies, and provide feedback on how to evolve, when appropriate.

This concept is very much in the realm of traditional API management service composition, but would possess a machine readable policy format just like IAM policies. API monetization policies could be reported upon, providing breakdown of consumption of resources at the backend system, or front-end API path level, helping translate the monetization side of our API strategy, into actual API plans that can be executed at run-time. Providing a standardized, scalable, quantifiable way to measure the value exchange that occurs at the API level. Done in a way that could be applied internally, or external with partners, and 3rd party developers. Making the business of my APIs more consistent, modular, and reusable--just like the rest of my API infrastructure.

I think AWS has a significant advantage in this area. They have the advanced resource management infrastructure, as well as the business side of all of this from managing their own APIs, but also from slowly rolling it out as part of the AWS Marketplace. AWS API Gateway has the plan, and marketplace key, providing the beginning of the implementation. All we need is the standardized policies based upon their existing pricing framework, and the ability to measure and report upon at the AWS API Gateway plan level. The working parts are there, it just needs to be brought together. It might also be something someone could piece together from logging, and other existing outputs on the AWS platform, and create an external reporting and billing solution. IDK. Just brainstorming, what I'd like to see, and getting it here on the blog before the thought passes.
