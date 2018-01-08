---
published: true
layout: post
title: 'API Life Cycle Basics: Gateway'
date: 2018-01-08T15:00:00.000Z
tags:
  - API Evangelist
  - Gateway
  - Deployment
image: 'https://s3.amazonaws.com/kinlane-productions/bw-icons/bw-gateway.png'
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/bw-icons/bw-gateway.png" align="right" width="35%" style="padding: 15px;" /></p>API gateways have long played a role in providing access to backend resources via web services and APIs. This is how web services have historically been deployed, but it is also how modern web APIs are being managed. Providing a gateway that you can stand up in front of existing web APIs, and proxy them through a single gateway that authenticates, logs, and manages the traffic that comes in and out. There are many management characteristics of API gateways, but I want to provide a stop along the API lifecycle that allows us to think about the API deployment, as well as the API management aspects of delivering APIs.

I wanted to separate out the API gateway discussion from deploy and manage, focusing specifically on the opportunities to deploy one or many gateways, while also looking at it separately as a pattern in service of microservices. While code generation for API deployment is common, gateways are making a resurgence across the sector when it comes to working with a variety of backend systems, on-premise and in the cloud. There are many API gateway solutions available on the market, but I wanted to focus in on a handful that help span deployment and management, as well as allowing for new types of routing, and transformation patterns to emerge. Here are a couple of the gateway solutions I'm studying more these days:

- [**AWS API Gateway**](https://aws.amazon.com/api-gateway/) - The Amazon API Gateway allows for the ingestion of OpenAPIs (Swagger) and the deployment of APIs that connect to a variety of backend services define as part of the AWS infrastructure.
- [**Kong**](https://konghq.com/) - Quickly build API-centric applications. Leverage the latest microservice and container design patterns. And tie it all together with the Kong microservice API gateway.
- [**Zuul**](https://github.com/Netflix/zuul) - I’m putting Zuul here, because it has some routing characteristics with makes it a deployment, as well as management solution. One you begin routing, you start to do some of the heavy lifting of design and deployment of resources.
- [**API Gateway Pattern**](http://microservices.io/patterns/apigateway.html) - A pattern for delivering microservices that use an API gateway, and support a variety of applications.
- [**Building Microservices Using an API Gateway**](https://www.nginx.com/blog/building-microservices-using-an-api-gateway/) - Designing, building, and deploying microservices introduced the Microservices Architecture pattern.

You'll notice there is a mix of several concepts here. API gateway as a pattern, in service of delivering microservices, as well as deploying and managing your APIs. I'm doing this on purpose, to try and show how the API gateway landscape is shifting, and evolving with the microservices evolution, as well as in service of devices, and the Internet of Things (IoT). I think Netflix's approach to using Zuul reflect the shifting middleware roots of the gateway, while working hard to establish the right set of patterns to meet the demanding needs of a growing variety of clients who are consuming our APIs. You see this landscape with new providers like Kong, as well as other leading web server platforms like NGINX outlining how we navigate this new world.

The API Gateway was always a single, monolithic point of entry in my mind. However, as I use AWS API Gateway in a variety of geographic regions and client accounts, and do more deploying of Kong wherever I need it, I'm beginning to change my tune. I'm working with more enterprise groups who have multiple API gateway solutions in play--the result of many disparate teams, as well as acquisitions, and incongruous evolution along the way. Sometimes this is seen as a bad thing, but when it is embraced as part of a larger API life cycle strategy, and driven my an API definition approach to doing APIs, you begin to see a method to the madness. Something that you can even begin to govern, and orchestrate at scale across many different groups, and thousands of APIs.
