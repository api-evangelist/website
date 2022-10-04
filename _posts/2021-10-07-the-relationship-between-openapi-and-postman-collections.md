---
published: true
layout: post
title: 'The Relationship Between OpenAPI and Postman Collections'
image: https://blog.postman.com/wp-content/uploads/2020/07/bann-blog-open-api-postman.jpg
tags:
   - Collections
   - OpenAPI
   - Lifecycle
---
I found myself talking about the relationship between OpenAPI and Postman Collections again today, and whenever I repeat a story like this I try to capture it here on the blog so I can scale my storytelling by sharing links with folks. Understanding the difference, but also the relationship between OpenAPI and Postman Collections is an essential part of the Postman API platform, but with the scope of usage of Postman, a pretty significant cross-section of the API economy. This is a story I will be telling over and over in many different ways to help API producers understand how they can maintain a source of truth for each of their APIs, but then also realize that API potential across many different stops along the API lifecycle.


Since collections started being used by developers the difference and relationship between Swagger/OpenAPI and Postman collections came into question. It can be hard to see the difference because they can both be used to provide a machine-readable reference of an API, complete with documentation. If you are just describing all of the paths, parameters, request bodies, and responses for an entire API, you can really use them interchangeably. However, when you begin applying collections across the API lifecycle, this is where you begin to see the difference, with your OpenAPI acting as the source of truth for what your API can do, and the derivative collections representing these essential stops along the API lifecycle.


- **Documentation** - Collections can be used to deliver complete reference, or very specific documentation for your API, describing the surface area of requests and responses and showing examples of what is possible as a workable, shareable, and executable collection. 
- **Mock Servers** - Collections can be combined with one or more examples to simulate what an API can do in a variety of different scenarios, providing ephemeral or long-living mock servers that can be used during the design process, as part of testing, or as sandbox environments.
- **Tests** - Collections can be used to deliver contract, integration, unit, performance, security, and many other types of tests across many API paths, or a small specific subset of paths, providing an executable unit that can be tested manually, scheduled as monitor, or as part of a pipeline.
- **Workflows** - Collections are excellent for developing workflows on top of many different APIs, daisy-chaining different API paths together, gathering outputs and passing in inputs, making API calls in a specific order, which can also be run manually, scheduled as monitor, or as part of a pipeline.


These are just a handful of the most common areas of the lifecycle in which collections are used. While documentation, mocking, and powering API tests aren't unique to collection, they definitely have taken these elements in different directions, and workflows are something that OpenAPI can’t touch (yet). Postman allows you to define APIs using OpenAPI, but then generate collections for documentation, mock servers, testing, and other use cases. Providing you with what you need to keep them in sync if anything changes with the source of truth for your API, ensuring that each stop along the API lifecycle doesn’t get out of sync with the source. Further differentiating how OpenAPI and Postman collections are different, but also the relationship between them and how they can actually work in concert.
   
Postman collections allow for better organization of API requests by folder, and allow for the creation of examples that can be used to enrich documentation, power mock responses, and apply as part of testing. OpenAPI can store examples but are not as robust and precise as collections. Collections also allow for the defining of pre and post request scripts that can be used as part of the testing, automation, and orchestration. It is this ability to script things, and then execute each collection as a runner, monitor, or pipeline. I like to describe the relationship between OpenAPI and collections by saying the OpenAPI is the source of truth for what is possible with an API, and the Postman collections are how you realize those possibilities across the entire API lifecycle. Once you begin to see the difference between these two specifications and understand the relationship between them, you begin to see past just a single API or single stop along the API lifecycle, and you can see the bigger picture across the entire life of an API, and across many different APIs.
