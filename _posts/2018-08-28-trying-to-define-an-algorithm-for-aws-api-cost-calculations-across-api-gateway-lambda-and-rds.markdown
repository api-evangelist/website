---
published: true
layout: post
title: >-
  Trying To Define An Algorithm For My AWS API Cost Calculations Across API
  Gateway, Lambda, And RDS
date: 2018-08-28T09:00:00.000Z
tags:
  - API Evangelist
  - Monetization
  - Plans
  - Cloud
image: >-
  https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories/4882162452_fa3126b38d_b_aqua.jpg
---
<p><img src="{{ page.image }}" width="45%" align="right" style="padding: 15px;" /></p>I am trying to develop a base base API pricing formula for determining what my hard costs are for each API I'm publishing using Amazon RDS, EC2, and AWS API Gateway. I also have some APIs I am deploying using Amazon RDS, Lambda, and AWS API Gateway, but for now I want to get a default base for determining what operating my APIs will cost me, so I can mark up and reliably generate profit on top of the APIs I'm making available to my partners. AWS has all the data for me to figure out my hard costs, I just need a formula that helps me accurately determine what my AWS bill will be per API.

Math isn't one of my strengths, so I'm going to have to break this down, and simmer on things for a while, before I will be able to come up with some sort of working formula. Here are my hard costs for what my AWS resources will cost me, for three APIs I have running currently in this stack:

- **AWS RDS** - I am running a db.r3.large instance which costs me $0.29 per hour or 211.70 per month, with the bandwidth free to my Amazon EC2 instances in the same availability zone. I do not have any public access, so I don't have any incoming or outgoing traffic, except from the EC2 instance.
- **AWS EC2** - I am running a t2.large instance which costs me $0.0928 per hour or $67.74 per month with bandwidth out costing me $0.155 per GB. I'm curious if they have an Amazon EC2 to AWS API Gateway data consideration? I couldn't find anything currently.
- **AWS API Gateway** - Overall using AWS API Gateway costs me $3.50 per million API calls received, with the first 1GB costing me $0.00/GB, and costing me $0.09/GB for the next 9.999 TB.

Across these three APIs, I am seeing an average of 5KB per responses, which is an important variable to use in these calculations. The [AWS API Calculator](https://calculator.s3.amazonaws.com/index.html) helps me figure out your monthly bill across services, but it doesn't help me break down what my hard costs are per API call. I need to establish a flat rate of what it costs for a single API call to exist. Each API will be in its own plan, so I can charge different rates for different APIs, but I need a baseline that I start with for each API call to make sure I'm covering my hard AWS costs. Sure, the more API calls I make, the more profitable I'll be, but at some point I'll also have to scale the infrastructure to keep a certain quality of service--there are a number of things to consider here.

I envision my API pricing having the following components:

- **Base** - A base cost to cover my AWS bill, considering AWS RDS, EC2, and API Gateway hard costs.
- **Resource** - A price for covering investment in resource. Work finding, cleaning up, refining, and evolving.
- **Markup** - The percentage of markup for each API call, allowing me to generate a profit from the resources I'm providing.
- **Partner** - Provide a volume discount, charging light users more, and giving a break to my partners who are consumer larger volumes.

I'm studying other pricing models from the telco, and software hosting spaces. I'll also be doing some landscape analysis to see what people are charging for comparable API resources. I possess a wealth of data on what API providers and service providers are charging for their services. The trick will be finding comparable services to what I'm offering, and for the unique resources I possess, I'm going to have to be able to set my own price, and then test out my assumptions, and formula over time--until I find the sweet spot for covering my hard costs, and generating profit at some point from a specific service I'm offering.

If you have an advice for me. Help on the math side of things, or examples from other industries, I'd love to hear more. I'll be open sourcing and sharing everything I figure out, and tell the story of how it is being applied to each API I am publishing. I want the history to be present for each of my APIs, adding to my wider [API monetization](http://monetization.apievangelist.com/) and [API planning](http://plans.apievangelist.com/) research. In the end, I don't think there is a perfect answer to what the pricing for an API should be. The best path forward involves covering your hard costs, and then experimenting over time to see what the market will bear. This is why AWS has gotten so good at doing this for cloud, because they have been doing this work for over a decade now. I am sure they have a lot of data, as well as experience understanding how to price API resources so they are both competitive, disruptive, and profitable.
