---
published: true
layout: post
title: 'How Can I Test That My API Requires and API Key'
image: https://kinlane-productions2.s3.amazonaws.com/test-for-api-keys-1.png
author:
 name: kinlane
tags:
- Gateways
- Security
- Keys
---
I am working on some new approaches to telling more consistent visual stories across the API lifecycle. I have a list of common API testing scenarios I will be working ny through as stories here on API Evangelist, but then also via the Postman blog and via the learning center. The first one on my list is a pretty simple one, but as you will see poosesses a couple of dimensions, which in my opinion push the traditional definition of what API testing is. 

For this story, I am looking to establish a Spectral rule that I can apply at design, develop, as well as build time. I want to automate checking that every API operational that goes out the door is secured with an API key—something I am enforcing using my CI/CD.

![Test for API Keys](https://kinlane-productions2.s3.amazonaws.com/test-for-api-keys-2.png)

I am using platform rules linting and collection testing to look at the OpenAPI contract at design, but also development, and enforced rules at build time. This is a great start, but I am also looking to test for the API key when making a series of test calls to the API, but also lint the gateway for proper configuration using the gateway API. This approach gives me three dimensions I can test and automate looking at how tall my APIs are properly secured using keys.

![Test for API Keys](https://kinlane-productions2.s3.amazonaws.com/test-for-api-keys-3.png)

This approach pushes my API testing beyond just the instance of an API. I can test all operations to see if they require keys or not. But I can also “test” the surface area of the API for the same design patterns I am looking for. I can add another dimension as well. I can “test” the gateway to see if the API has been configured to require a key. This gives me a repeatable blueprint I can apply here to my API key scenario, but also beyond, approach API testing in 3D.



