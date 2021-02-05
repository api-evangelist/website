---
published: true
layout: post
title: YAML API Management Artifacts From AWS API Gateway
date: 2018-11-23T09:00:00.000Z
tags:
  - API Evangelist
  - Gateway
  - Definitions
  - Discovery
  - Lifecycle
image: >-
  https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories-new/old-door-lock-2_marcel_duchamp.jpg
---
<p><img src="{{ page.image }}" width="45%" align="right" style="padding: 15px;" /></p>I've always been a big supporter of creating machine readable artifacts that help define the API lifecycle. While individual artifacts can originate and govern specific stops along the API lifecycle, they can also bring value when applied across other stops along the API lifecycle, and most importantly when it comes time to govern everything. The definition and evolution of individual API lifecycle artifacts is the central premise of [my API discovery format APIs.json](http://apisjson.org)--which depends on there being machine readable elements within the index of each collection of APIs being documented, helping us map out the entire API lifecycle.

[OpenAPI](https://www.openapis.org/) provides us with machine readable details about the surface area of our API which can be used throughout the API lifecycle, but it lacks other details about the surface area of our API operations. So when I do come across interesting approaches to extending the OpenAPI specification which are also injecting a machine readable artifact into the OpenAPI that support other stops along the API lifecycle, I like to showcase what they are doing. I've become very fond of one within the OpenAPI export of any AWS API Gateway deployed API I'm working with, which provides some valuable details that can be used as part of both the deployment and management stops along the API lifecycle:
<pre><code>
x-amazon-apigateway-integration:
	uri: "http://example.com/path/to/the/code/behind/"
	responses:
		default:
			statusCode: "200"
	requestParameters:
		integration.request.querystring.id: "method.request.path.id"
	passthroughBehavior: "when_no_match"
	httpMethod: "GET"
	type: "http"
</code></pre>
This artifact is associated with each individual operation within my OpenAPI. It tells the AWS gateway how to deploy and manage my API. When I first import this OpenAPI into the gateway, it will deploy each individual path and operation, then it helps me manage it using the rest of the available gateway features. From this OpenAPI definition I can design, then autogenerate and deploy the code behind each individual operation, then deploy each individual path and operation to the AWS API Gateway and map them to the code behind. I can do this for custom APIs I've deployed, as well as Lambda brokered APIs--I prefer the direct way, because it is still easier, stabler, more flexible and cost effective for me to write the code behind each of my API operations, than to go full serverless.

However, this artifact demonstrates for me the importance of artifacts associated with each stop along the API lifecycle. This little bit of OpenAPI extended YAML gives me a significant amount of control when it comes to the automation of deploying and managing my APIs. There are even more properties available for other layers of the AWS Gateway not included in this example, but is something that I will keep mapping out. Having these types of machine readable artifacts present within our OpenAPI specifications for describing the surface area of our APIs, as well as present within our APIs.json indexes for describing the surface area of our API operations will be critical to further automating, scaling, and defining the API lifecycle as it exists across the enterprise.
