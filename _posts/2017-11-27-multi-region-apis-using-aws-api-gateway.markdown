---
published: true
layout: post
title: Multi-Region APIs Using AWS API Gateway
date: 2017-11-27T13:00:00.000Z
tags:
  - API Evangelist
  - Gateway
  - Cloud
  - Regions
  - Deployment
image: >-
  https://s3.amazonaws.com/kinlane-productions/amazon/amazon-api-gateway-regions.png
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/amazon/amazon-api-gateway-regions.png" align="right" width="45%" style="padding: 15px;" /></p>I've been deploying two project using AWS API Gateway, Lambda, and Amazon RDS lately. I've become so sold on this approach to deploying APIs as part of this work, that I am evolving my own internal API process to use the same approach. The technical aspect of serverless plus the gateway definitely convinced me of the potential, but it was also the usage of AWS IAM which sealed the deal for me. I'm all too aware of how much my API security lacks as a one person shop, something that I also see reflected in my client operations, and I'd rather be offloading security to AWS than ending up taking the hit on it down the road.

While deploying my project using AWS API Gateway, and Lambda, I was faced with the question regarding which zone I should be deploying the APIs in. It is the first time I've been faced with the opportunity to deploy my APIs into multiple zones. Sure, I could have deployed my servers into any AWS zone before, but for some reason now that I'm doing with AWS API Gateway, and Lambda, the opportunity seemed more of a possibility. I've pitched it to my client to consider an east as well as a west coast API deployment, so that we can give developers the choice in the documentation to choose which availability zone they'd like to use in their application. Before I make the proposal I'm going to deploy some prototypes, and do some benchmark testing, and see what the benefits are.

Even if I end up publishing APIs into separate regions, I still have the backend database to content with. Where do I put the database, and how to I replicate between zones. Amazon RDS gives me the tools to tackle this, but historically I would only do this just for backup, not for actual redundancy, as well as performance gains. Amazon zones have been a staple of the cloud since early days, but I still have many clients who only operate in the east coast region. I'm thinking I will begin to push for a multi-region approach, and see if I can't convince some of them to start thinking bigger. Getting to know where their customers are, and delivering infrastructure closer where the resources are needed.

I'm rolling out some new APIs as part of my own infrastructure. Most of my APIs are retail, as well as wholesale APIs. Meaning you can use the APIs I've published, or I'll deploy them specifically for you, in your own AWS account. I think I'm going to make east / west an option for my retail APIs, and ALL the AWS regions an option for the wholesale APIs. I'm seeing geographical region as another consideration when I'm thinking about how I should be breaking down my APIs, into smaller more bite-size chunks. I see geographical region as a variable in the host for my APIs, just like I'd add any other variable in the path. Opening up a whole new set of possibilities when it comes to not just API deployment, but also API reliability and performance.

As I continue to drink the AWS Kool-Aid I'm questioning my increased dependence on the platform. However, it gets harder to deny when they bring security to the table, and increased performance, availability, and reliability to my API stack, and the APIs I'm delivering for my clients. There is no way I could afford to do APIs at scale, across multiple regions without AWS. I think back to the day when I would secure my own T1s, colo-facility, and servers. Even with the threat of vendor lock-in, I do not want to ever go back to that world. I enjoy the benefits of AWS. I'm just going to try and keep things as well defined as simple, microservice APIs, so that I can migrate to Google, Azure, or if necessary my own infrastructure. As much as I'd like to reduce my dependencies on major cloud providers, in the current online environment I just can't. Being able to operate in any region around the globe is a pretty significant benefit to doing business online.
