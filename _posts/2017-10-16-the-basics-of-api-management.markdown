---
published: true
layout: post
title: The Basics Of API Management
date: 2017-10-16T09:00:00.000Z
tags:
  - API Evangelist
  - Management
image: >-
  https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories-new/42_16_600_400_0_max_1_1_1-5.jpg
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories-new/42_16_600_400_0_max_1_1_1-5.jpg" align="right" width="40%" style="padding: 15px;" /></p>I am developing a basic API management strategy for one of my client's API. With each area of their API strategy I am taking what I've learned monitoring the API sector, but pausing for a moment to think about again, and then applying to their operations. Over the years I have separated out many aspects of API management, distilling it down to a core set of elements that reflect the evolution of API management as its evolved into a digital commodity. It helps me to think through these aspects of API operations in general, but also applying to a specific API I am working on, helping me further refine my API strategy advice.

API management is the oldest area of my research. It has spawned every other area of the lifecycle I track on, but also is the most mature aspect of the API economy. This project I am working on gives me an opportunity to think about what is API management, and what should be spun off into separate areas of concern. I am looking to distill API management down to:

- **Portal** - A single URL to find out everything about an API, and get up and running working the resources that are available.
- **On-Boarding** - Think just about how you get a new developer to from landing on the home page of the portal to making their first API call, and then an application in production.
- **Accounts** - Allowing API consumers to sign up for an account, either for individual, or business access to API resources.
- **Applications** - Enable each account holder to register one or many applications which will be putting API resources to use.
- **Authentication** - Providing one, or multiple ways for API consumers to authenticate and get access to API resources.
- **Services** - Defining which services are available across one or many API paths providing HTTP access to a variety of business services.
- **Logging** - Every call to the API is logged via the API management layer, as well as the DNS, web server, file system, and database levels.
- **Analysis** - Understanding how APIs are being consumed, and how applications are putting API resources to use, identifying patterns across all API consumption.
- **Usage** - Quantifying usage across all accounts, and their applications, then reporting, billing, and reconciling usage with all API consumers.
- **APIs** - API access to accounts, authentication, services, logging, analysis, and usage of API resources.

There are other common elements bundled with API management, but this reflects the core of what API management is about--the business of APIs. Keeping track of who has access to what, and how much they are using. There are a number of other aspects of API management that many will consider under the API management umbrella, but I've elevated to being their own stops along the API lifecycle. Some areas are:

- **Documentation** - Static or interactive documentation for all available API paths, parameters, headers, and other details of the request and response surface area of the API.
- **Support** - Self-service, or direct support channels that API consumers put to use to get help along the way.
- **SDKs** - The SDKs, samples, libraries, and other supporting code elements for web, mobile, or other types of applications.
- **Road Map** - Communicating what the future holds when it comes to the API.
- **Issues**  - Notification of any open issues with the available of the API.
- **Change Log** - A history of what has happened when it comes to changes to the API.

These areas compliment API management, but should be approached beyond the day to day management aspects of API operations. I'd also consider authentication, logging, and analysis to be bigger than just about API management, as all three areas should cover more than just the API, but they are still very coupled to the core aspects of API management. In my definition, API management is very much about managing the consumption of resources, and not always the other aspects of API operations. This isn't just my definition, it is what I'm seeing with the commodization of API management like we see over at Amazon Web Services.

AWS API Gateway is really about accounts, applications, authentication, and services. The logging, analysis are delivered by AWS CloudWatch. For this particular project I'm using Github and Jekyll as the portal, and custom delivering on-boarding, usage, and supporting APIs separately. Further narrowing down my definition of just what is API management. I'd say that AWS represents this evolution in API management well, with the decoupling of concerns between AWS API Gateway and AWS CloudWatch. If you apply [AWS Cognito](https://aws.amazon.com/cognito/) to authentication, you can separate out another. I do not see any viable solution to handling usage, billing, and what used to be the business and monetization side of API management.

This API project I am working on is already using AWS for the backend of their operations, so I'm investing cycles into better understanding the moving parts of API management in context of the AWS platform. It makes sense to think some more about the decoupling of API management in context of AWS, since they are a major player in the commodization, and maturing of the concept. Once I'm done with AWS, I'm going to take another look at Google, then Azure, who are the other major players who are defining the future of API management.
