---
published: true
layout: post
title: Importing OpenAPI Definition To Create An API With AWS API Gateway
date: 2017-10-19T09:00:00.000Z
tags:
  - API Evangelist
  - Definitions
  - Deployment
  - Gateway
  - Proxy
image: >-
  https://s3.amazonaws.com/kinlane-productions/amazon/api-gateway/aws-api-gateway-create-new-api.png
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/amazon/api-gateway/aws-api-gateway-create-new-api.png" align="right" width="45%" style="padding: 15px;" /></p>I've been learning more about AWS API Gateway, and wanted to share some of what I'm learning with my readers. The AWS API Gateway is a robust way to deploy and manage an API on the AWS platform. The concept of an API gateway has been around for years, but the AWS approach reflects the commoditization of API deployment and management, making it a worthwhile cloud API service to understand in more depth. With the acquisition or all the original API management providers in recent years, as well as Apigee's IPO, API management is now a default element of major cloud providers. Since AWS is the leading cloud provider, AWS API Gateway will play a significant role into the deployment and management of a growing number of APIs we see.

Using AWS API Gateway you can deploy a new API, or you can use it to manage an existing API--demonstrating the power of a gateway. What really makes AWS API Gateway reflect where things are going in the space, is the ability to import and define your API using OpenAPI. When you first begin with the new API wizard, you can upload or copy / paste your OpenAPI, defining the surface area of the API, no matter how you are wiring up the backend. OpenAPI is primarily associated with publishing API documentation because of the success of Swagger UI, and secondarily associated with generating SDKs and code samples. However, increasingly the OpenAPI specification is also being used to deploy and define aspects of API management, which is in alignment with the AWS API Gateway approach.

I have server side code that will take an OpenAPI and generate the server side code needed to work with the database, and handle requests and responses using the Slim API framework. I'll keep doing this for many of my APIs, but for some of them I'm going to be adopting an AWS API Gateway approach to help standardize API deployment and management across the APIs I deliver. I have multiple clients right now who I am deploying, and helping them manage their API operations using AWS, so adopting AWS API Gateway makes sense. One client is already operating using AWS which dictated that I keep things on AWS, but the other client is brand new, looking for a host, which also makes AWS a good option for setting up, and then passing over control of their account and operations to their on-site manager.

Both of my current projects are using OpenAPI as the central definition for all stops along the API lifecycle. One API was new, and the other is about proxying an existing API. Importing the central OpenAPI definition for each project to AWS API Gateway worked well to get both projects going. Next, I am exploring the staging features of AWS gateway, and the ability to overwrite or merge the next iteration of the OpenAPI with an existing API, allowing me to evolve each API forward in coming months, as the central definition gets added to. Historically, I haven't been a fan of API gateways, but I have to admit that the AWS API Gateway is somewhat changing my tune. Keep the service doing one thing, and doing it well, with OpenAPI as the definition, really fits with [my definition of where API management is headed as the API sector matures](http://apievangelist.com/2017/10/16/the-basics-of-api-management/).
