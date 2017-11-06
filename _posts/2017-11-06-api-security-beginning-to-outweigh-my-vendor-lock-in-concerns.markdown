---
published: true
layout: post
title: API Security Beginning To Outweigh My Vendor Lock-In Concerns
date: 2017-11-06T11:00:00.000Z
tags:
  - API Evangelist
  - Security
  - Cloud
  - IAM
image: >-
  https://s3.amazonaws.com/kinlane-productions/amazon/iam/aws-iam-api-gateway.jpg
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/amazon/iam/aws-iam-api-gateway.jpg" align="right" width="45%" style="padding: 15px;" /></p>I've been on the AWS train since day one. I've been integrating Amazon S3 and EC2 into my business(es) since they first launched a decade ago. While the platform has faithfully provided my storage and compute for over a decade I've always been wary of vendor lock-in. After a decade long ride on Microsoft (1998-2008), I felt pretty burned. Then recently after a similar decade long ride on Google (2005-2015), I felt burned, but in a different way. After a decade on AWS I'm nervous, but I don't feel as burned, however I'd say there is one aspect of doing business online that is making me put aside some of my concerns regarding vendor lock-in on AWS, and even on Google, and Azure--SECURITY. I'm just not convinced I can do this alone, and I need the help of the platforms I operate on to help make sure my operations are secure.

I spent the weekend setting up a set of APIs using AWS RDS as the backend database, AWS Lambda as the code layer, and AWS API Gateway as the API front-end. As part of this work I established an identity and access management (IAM) role with policies tailored for brokering the exchanges between RDS, Lambda, and the API Gateway. I'm leaning on AWS for two key API security pieces here: 1) API key management with AWS API Gateway, and 2) backend security using AWS IAM. The key management stuff is pretty straightforward and something I can easily replicate, but the AWS IAM stuff is a little more involved, and I'm grateful for how easy AWS IAM makes it for me to setup roles, cherry pick from common policies, and lock down the infrastructure I a using to drive the backend of my APIs and other applications.

As I moved another API project into the home stretch this weekend, I migrated an RDS, and EC2 instance into a separate account for a client. I had been defining, designing, and developing an API for them over the last coupe of months, and as we approached completion, I wanted everything in their own account where they could be accountable for the AWS bill, and take control over operations, as well as security of their own API operations. Being able to configure IAM for each project, and pass it off to clients using a separate AWS account is super beneficial to me, as well as my clients. I'm not confident my clients can tackle API security any better than I can in the long run, and being able to configure roles, policies, and stand-up a working set of APIs that are secure, is a critical aspect of doing business online using APIs for both me and my clients.

While I still have vendor lock-in concerns with AWS, especially when it comes to adopting a serverless approach with Lambda, the ability to define API and backend security in this way is softening these concerns. In the volatile online environment we find ourselves in I am just not confident that I have the time, skills, and resources to do API security properly. I'm also not confident my clients can either. I'm thankful for AWS IAM, and the other security solutions they bring to the table. I'm feeling like we are going to need our cloud platform providers to have our backs like this in the future, as well as the services of a suite of other API security providers to help us do all of this properly. I wish it was a utopian online world where we could hand roll our infrastructure and remain safe online, but in 2017 I'm not interested in doing any of this alone. There are just too many threats out there.
