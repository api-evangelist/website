---
published: true
layout: post
title: A Summary Of AWS API Gateway As An API Deployment and Management Solution
date: 2018-02-14T11:00:00.000Z
tags:
  - API Evangelist
  - Deployment
  - Management
  - Cloud
  - Gateway
image: 'https://s3.amazonaws.com/kinlane-productions/aws/aws-api-gateway-icon.png'
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/aws/aws-api-gateway-icon.png" align="right" width="45%" style="padding: 15px;" /></p>I was providing an overview of Kong, AWS API Gateway, and other solutions for a team I'm advising a couple weeks back. I was just looking to distill down some of the key features, and provide an overview to a large, distributed team. This work lends itself well to publishing here on the blog, so [I published an overview of Kong yesterday](http://apievangelist.com/2018/02/13/summary-of-kong-as-an-api-management-solution/), and today I wanted to publish the summary of the AWS API Gateway. The API gateway solution from AWS has some overlap with what Kong delivers, but I consider it to be more of an API deployment, as well as an API management gateway.

The [AWS API Gateway brings API](https://aws.amazon.com/api-gateway/) deployment front and center, allowing you to define and deploy APIs that are wired up to your backend (AWS) infrastructure:

- **API Endpoint** - a host name of the API. the API endpoint can be edge-optimized or regional, depending on where the majority of your API traffic originates from. You choose a specific endpoint type when creating an API.
- **Backend Endpoint** - A backend endpoint is also referred to as an integration endpoint and can be a Lambda function, an HTTP webpage, or an AWS service action, or a mock interface.
- **Swagger / OpenAPI** - Using Swagger to import and export API configuration and definitions.

Then the gateway brings a wealth of API management features, providing a look at how it has been baked into the cloud now:

 - **Accounts** - Creation and management of Accounts.
 - **Keys** - Creation and management of API Keys
 - **Certificates** - Adding and management of certifications
 - **Documentation** - Publishing of ApI documentation
 - **Domains** - Mapping of domains
 - **Response** - Custom Gateway responses.
 - **Models** - Management of schema models.
 - **Validation** - Validation of API requests
 - **SDK Generation** - Generating of client SDKs
 - **Staging** - Establishing of stages
 - **Tags** - Tagging of resources
 - **Templates** - Mapping template used to transform a payload.
 - **Plans** - Establishing of different plans for API usage.
 - **VPC** - Usage of VP under the caller's account in a region.
 - **Regions** - Deployment of gateways in different AWS regions.
 - **Serverless** - Usage of Lambda for serves integration.
 - **Logging** - Logging using Cloudwatch.
 - **IAM** - You can use AWS administration and security tools, such as AWS Identity and Access Management (IAM) and Amazon Cognito, to authorize access to your APIs.

Then of course, everything with AWS has two separate programmatic interfaces for you to work with everything:

 - **API** - Programmatic access through hypermedia API.
 - **Command Line** - The AWS CLI is an open source tool built on top of the AWS SDK for Python that provides commands for interacting with AWS services.

 AWS API Gateway doesn't have some of the bells and whistles associated with other leading API management solutions, however it makes up for this with its API deployment capabilities--answering the age old question, which of the API management solutions will help me deploy my APIs. If you are operating your infrastructure within AWS, then AWS API Gateway makes a lot of sense. The connectivity it brings to the table is hard to ignore. What really sold it for me, is the IAM part of the equation. Before using AWS, I never had fine grained policies for what backend systems my APIs can or cannot access.

I avoided AWS API Gateway for a while. I was waiting for it to mature, and looking for enough benefit to get me beyond my vendor lock-in fears with API infrastructure. The IAM and Serverless aspects of delivering APIs are the features that pushed me to the point where I'm now using it for about 50% of my API infrastructure. It isn't as portable, and versatile as solutions like Kong or Tyk are, but it does provide a solid set of API deployment and management features for me to put to work on projects that are already running in the AWS cloud.
