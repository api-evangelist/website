---
published: true
layout: post
title: 'Testing the Size of My API Payload During Design, Development, Build, and Post Production'
image: https://kinlane-productions2.s3.amazonaws.com/test-for-payload-1.png
author:
 name: kinlane
tags:
- Gateways
- Testing
- Payload
- Size
- Scope
---
I am working on some new approaches to telling consistent visual stories around the API Lifecycle, and I have a list of small little common API testing scenarios I will be working through as stories here on API Evangelist but then also via the Postman blog and learning center. [The first one I did was on testing for API keys](https://apievangelist.com/2022/12/06/how-can-i-test-that-my-api-requires-and-api-key/), and this one is about testing for the payload size of an API response. This is something I wanted to explore from a consumer vantage point, but also as part of the design process, and operations. 

If I want to enforce a size limitation on API responses I could start with creating a Spectral rule that would check for size constraints on my OpenAPI contract, which could be checked for during design and development, but also enforced at the CI/CD pipeline as well. This approach would help educate API designers and developers about keeping the payloads efficient, and allow for mandating when desired.

![Testing the Payload Size](https://kinlane-productions2.s3.amazonaws.com/test-for-payload-2.png)

While this is unlikely to actually restrict API responses from being too large, it does provide a learning opportunity earlier on in the lifecycle for developers. The next dimension of testing the size of the payload can occur after the API is in production, layering on size constraints as part of contract tests, and developing performance and load testing that explores the scope of responses for each API operation. I can then run these tests manually, using runners, or scheduling via monitors.

![Testing the Payload Size](https://kinlane-productions2.s3.amazonaws.com/test-for-payload-3.png)

Now we are testing the instance of the API, rather than just the surface area or design of the API. What if I want to go further? What if I want to actually test the configuration of my gateway for configuration that will introduce size constraints for my API. I am actually looking to be able to get all available size configurations via the API for my API gateway. I may want to do this after the API is in production, but also explore what the opportunities for shift left are.

![Testing the Payload Size](https://kinlane-productions2.s3.amazonaws.com/test-for-payload-4.png)

Knowing what size configurations exist for my gateway is a good start. Being able to automate testing on these configurations across gateways and APIs published to them is even better. If a configuration is available we can even possibly update it, if things are within ideal and known conditions. Next, I am looking to just make sense of what is happening across these three dimensions of testing the size of each API response as part of my existing APM and reporting.

![Testing the Payload Size](https://kinlane-productions2.s3.amazonaws.com/test-for-payload-5.png)

Even if I am not automating the testing of the gateway, I am guessing I can still inform the design and development of an API with what we learn as part of this exercise. It will take some work to assemble a suite of tests to demonstrate this, and gets exponentially more challenging when you consider multiple gateways. As with all of my governance challenges, I am looking for multiple dimensions in which I can test across the surface area of an API, the behavior of a specific instance of an API, as well as the gateway and other operational elements around an API.

I am looking to explore even more areas like I did with testing for API keys and testing for the size of each API response payload. I am looking to explore a variety of API testing scenarios, while pushing the scope of what we consider testing to be. I am interested in pushing forward the standard testing approaches I have available, while also evolving how I use our lifecycle diagram tool to provide accompanying visuals for each testing blueprint. 

