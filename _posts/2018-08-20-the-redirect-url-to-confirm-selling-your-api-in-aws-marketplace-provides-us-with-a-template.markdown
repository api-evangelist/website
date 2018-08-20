---
published: true
layout: post
title: >-
  The Redirect URL To Confirm Selling Your API In AWS Marketplace Provides Us With A Positive
  Template
date: 2018-08-20T09:00:00.000Z
tags:
  - API Evangelist
  - Marketplace
  - Management
  - DNS
image: >-
  https://s3.amazonaws.com/kinlane-productions/amazon/aws-marketplace-aws-saas-seller-integration-guide.png
---
<p><img src="{{ page.image }}" width="45%" align="right" style="padding: 15px;" /></p>I am setting up different APIs using the AWS API Gateway and then publishing them to the AWS Marketplace, as part of [my work with Streamdata.io](http://streamdata.io). I'm getting a feel for what the process is all about, and how small I can distill an API product to be, as part of the AWS Marketplace process. My goal is to be able to quickly define APIs using OpenAPI, then publish them to AWS API Gateway, and leverage the gateway to help me manage the entire business of the service from signup to discovery.

As I was adding one of my first couple of APIs to the AWS Marketplace, and I found the instructions regarding the redirect URL for each API to be a good template. Each individual API service I'm offering will have its own subscription confirmation URL with the AWS API marketplace, with the relevant variables present I will need to scale the technical and business of delivering my APIs:

- **AWS Marketplace Confirmation Redirect URL:** https://YOUR_DEVELOPER_PORTAL_API_ID.execute-api.[REGION].amazonaws.com/prod/marketplace-confirm/[USAGE_PLAN_ID]

This URL is what my retail customers will be given after they click to subscribe to one of my APIs. Each API has its specific portal (present in URL), as well as being associated with a specific API usage plan within AWS API Gateway. Also notice that they have a variable for region, allowing me to deliver services by region, and scale up the technical side of delivering the various APIs I'm deploying--another important consideration when delivering reliable and performant services.

Pointing out the URL for a signup process might seem like a small thing. However, because of AWS's first mover advantage in the cloud, and their experience as an API pioneer, I feel like they are in a unique position to be defining the business layer of delivering APIs at scale in the cloud. The business opportunities available at the API management and marketplace layers within the AWS ecosystem are untapped, and represent the next generation of API management that is baked into the cloud. It's an interesting place to be delivering and integrating with APIs, at this stage of the API economy.
