---
published: true
layout: post
title: Using APIs To Manage My APIs
date: 2017-11-09T13:00:00.000Z
tags:
  - API Evangelist
  - Deployment
  - Gateway
  - Management
  - Inception
image: >-
  https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories/cargo-ship-on-sea_blue_circuit.jpg
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories/cargo-ship-on-sea_blue_circuit.jpg" align="right" width="45%" style="padding: 15px;" /></p>I'm going further down the AWS rabbit hole lately with my APIs. Historically my APIs ran on an AWS EC2 instance with leveraged Linux for the OS, Apache for the web server, and Slim for the RESTful framework of my APIs--all with an RDS MySQL backend. I've now evolved the EC2 instance to be spread across numerous AWS Lambda scripts, tied together into various stacks of APIs using AWS API Gateway. At first, I was hesitant to go further down the AWS rabbit hole, but [the security benefits of AWS-driven solutions](http://apievangelist.com/2017/11/06/api-security-beginning-to-outweigh-my-vendor-lock-in-concerns/), as well as the API-driven aspects of operating my APIs, is slowly shifting my view of how I need to be managing my APIs.

AWS RDS, Lambda, and API Gateway all have APIs. I've been spending the week developing Lambda scripts that help me manage my APIs, using the AWS APIs behind these three services, leveraging them to setup, configure, deploy, manage, and test my APIs. I enjoy how APis push me to think about my digital resources, and when my digital resources are APIs, the benefts begin to feel like API inception. I'm increasingly having APIs that do one thing and do it well, when it comes to API operations, allowing me to distill down the building blocks of my API operations, into a very workable world of API functionality.

I am now deploying, backing up, migrating, and working with the database behind my APIs using APIs. I primarily use AWS RDS MySQL instances behind my APIs, but when I'm using AWS DynamoDB, I leverage AWS APIs even more, as DynamoDB lets you do adds, updates, queries, and deletes using the API, elevating beyond SQL to manage the contents of each data store. Whether it is RDS or DynamoDB, I'm using APIs manage the operational side of each database behind the API, and I'm beginning to explore how to make my database more ephemeral, and scalable using AWS APIs, giving me more control over my database budgets.

Moving up the API stack, I'm deploying, optimizing, testing, and working with all my AWS Lambda scripts using the API. I'm working to organize, index, and manage all my Lambda scripts using AWS S3, bringing some order to the serverless madness I'm unleashing. This approach to using APIs to manage the code layer for my API operations is entirely new. I've never had API access to the code I deployed in the Slim framework, on my Linux servers. While there is significant overhead in architecting and setting up this new approach, the benefits down the road for deploying, updating, and managing the code that drives my APIs will be significant.

Lastly, I'm crafting a whole suite of API Gateway scripts, allowing me to setup plans, issue and revoke keys, quantify API consumption, and a whole host of other API gateway driven functionality across all my APIs. I'm even to the point where I'm launching new APIs in the gateway using OpenAPI definitions, and now I am figuring out how I can wire each API resource and method to their appropriate Lambda function behind. I'm still figuring this part out. This is where I find myself in my API driven journey to automate my API lifecycle using APIs. I've long had APIs for my API management, but only recently was I able to deploy new APIs that help me manage my APIs, beyond the base stack given to me by my API management provider.

Using APIs to manage APIs quickly becomes API inception in my brain. I quickly find myself looping infinitely through what is possible, but discovering new ways to orchestrate my world, and save myself work. I thoroughly enjoy the concept of using my cloud provider APIs to manage my APIs, but I'm also finding it rewarding to design, deploy, and operate new APIs that contribute to the management of my APis. This is where I think the whole API game is going to shift. When I'm not just deploying all my data, content, and algorithms using APIs, but also using APIs to manage these APIs, a new found freedom emerges to program the digital world around me.
