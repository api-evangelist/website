---
published: true
layout: post
title: 'API Life Cycle Basics: Testing'
date: 2018-01-12T13:00:00.000Z
tags:
  - API Evangelist
  - Testing
image: 'https://s3.amazonaws.com/kinlane-productions/bw-icons/bw-testing.png'
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/bw-icons/bw-testing.png" align="right" width="35%" style="padding: 15px" /></p>Every API should be tested to ensure it delivers what is expected of it. All code being deployed should meet required unit and code tests, but increasingly API testing is adding another layer of assurance to existing build processes, even going so far as halting CI/CD workflows if tests fail. API testing is another area where API definitions are delivering, allowing tests to be built from existing artifacts, and allowing detailed assertions to be associated with tests to add to and evolve the existing definitions.

API testing has grown over the last couple of years to include a variety of open source solutions, as well as cloud service providers. Most of the quality solutions allow you to import your OpenAPI, and automate the testing via APIs. Here are a few of the solutions I recommend considering as you think about how API testing can be introduced into your API operations.

- [Runscope](https://www.runscope.com/) - An API testing service that uses OpenAPI for importing and exporting of API tests and assertions.
- [Hippie-Swagger](https://github.com/CacheControl/hippie-swagger) - An open source solution for testing your OpenAPI defined APIs.
- [Spring Cloud Contract](https://cloud.spring.io/spring-cloud-contract/) - Spring Cloud Contract is an umbrella project holding solutions that help users in successfully implementing the Consumer Driven Contracts approach.
- [Postman Testing](https://www.getpostman.com/docs/postman/scripts/test_scripts) - With Postman you can write and run tests for each request using the JavaScript language.
- [Frisby.js](https://www.frisbyjs.com/) - Frisby is a REST API testing framework built on Node.js and Jasmine that makes testing API endpoints easy, fast, and fun.

There are numerous ways to augment API testing on top of your existing testing strategy. More of these providers are integrating with Jenkins and other CI/CD solutions, allowing API testing to deeply integrate with existing pipelines. My recommendation is that the artifacts from these tests and assertions also live alongside OpenAPI and other artifacts and are used as part of the overall definition strategy, widening the meaning of “contract” to apply across all stops along the lifecycle--not just testing.

While API testing may seem like common sense, I'd say that more than 50% of the organizations I'm talking with do not actively test all their APIs. Of the ones that do, I'd say less than half get very granular in their testing or follow test driven development philosophies. This is where service providers like Runscope deliver, helping bring the tools and expertise to the table, allowing you to get up and running in a cloud environment, building on a platform, rather than started from scratch when it comes to your API testing.
