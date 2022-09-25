---
published: true
layout: post
title: I Like The Scope Of The AWS SDK for JavaScript
date: 2017-11-02T15:00:00.000Z
tags:
  - API Evangelist
  - SDK
  - Node.js
  - Cloud
  - Database
  - Gateway
  - Storage
image: >-
  https://s3.amazonaws.com/kinlane-productions/amazon/SDK/aws-sdk-for-javascript.png
---
<p><a href="http://docs.aws.amazon.com/AWSJavaScriptSDK/latest/"><img src="https://s3.amazonaws.com/kinlane-productions/amazon/SDK/aws-sdk-for-javascript.png" align="right" width="45%" style="padding: 15px;" /></a></p>I've tried picking up Node.js as a server side approach to delivering APIs a couple of times in the past few years. Both times express, and a handful of other issues ran me off from using it as my default backend programming language for APIs. I use a lot of JavaScript in the client, but it just didn't feel like it was what I needed to drive my backend solutions. Over the last week I've been architecting a handful of APIs using Lambda and Node.js scripts, and I have to admit I'm pretty sold on Node.js as a backend solution now. This conversion is partly due to Lambda and a serverless way of doing things, but is also due to [the AWS SDK for JavaScript](http://docs.aws.amazon.com/AWSJavaScriptSDK/latest/), which is a pretty robust example of an API SDK.

[The AWS SDK for JavaScript](http://docs.aws.amazon.com/AWSJavaScriptSDK/latest/) covers 106 separate AWS services, and I haven't actually calculated how many methods are available--a lot. I've been using it recently to manage AWS RDS, DynamoDB, and API Gateway, and the SDK is a delight to use, is well documented, and enjoys excellent coverage of AWS services. There were two elements at play here that made this work for me, 1) simplicity of the AWS SDK in Node, and 2) the simplicity of implementing in the serverless environment that is Lambda. I found Node.js scaffolding to be overly complex for APIs in previous experiences, something that melted away with a serverless implementation. I am well versed in JavaScript, and with the AWS SDK being so simple enough, I was able to get up and running with a variety of functions on Lambda pretty quickly. Something that becomes really powerful when exposed as an API resource using AWS API Gateway.

This is going to date me, and I know that only a handful of people will understand, but the AWS SDK for JavaScript, combined with Lambda and API Gateway reminds me of VBScript on Windows server, circa 2000. Back in the day, I had my own server farm, on my own dedicated T1, on an entire C block of IP addresses, running Windows 2000. I was able to orchestrated some pretty cool cross-server voodoo using VBScript when it came to managing the server, database, web server, DNS (Active Directory), and other moving parts of my world. I have way more resources at my disposal with AWS, and a much more robust vocabulary with the AWS SDK for Javascript than I did back in the day, but the feeling I have is very similar. I am able to orchestrate pretty effectively across my operations, using a variety of AWS, 3rd party, as well as my own home grown APIs. I have the control over my infrastructure that I am looking to have, allowing me to get what I need done.

I like the scope of the AWS SDK for JavaScript. It gives me access to what I need, while also introducing me to other AWS APIs at the same time. I set out to use the SDK for DynamoDB, then RDS, and API Gateway, and now I'm exploring how I can use it for managing EC2 ad S3, evolving the current PHP SDK I've had in place for the last five years. I was't looking to evolve some of my legacy API infrastructure using this new approach which I've evolving for a client, but the ease of use, scalability, and benefits brought to the table are proving to be worth the extra work. I'm rolling out a suite of Lambda functions for managing RDS, EC2, S3, and API gateway, as well as expanding to work with Github, Stripe, and other external APIs I depend on. This ease of use, plus the security benefits introduced by AWS IAM is pushing me further into the AWS universe, without the vendor lock-in regret I was expecting to have.
