---
published: true
layout: post
title: When To Build Or Depend On An API Service Provider
date: 2017-09-06T16:00:00.000Z
tags:
  - API Evangelist
  - Monitoring
  - Testing
image: 'https://s3.amazonaws.com/kinlane-productions/bw-icons/bw-heart-monitor.png'
---
<p><a href="http://monitoring.apievangelist.com/"><img src="https://s3.amazonaws.com/kinlane-productions/bw-icons/bw-heart-monitor.png" align="right" width="35%" style="padding: 15px;" /></a></p>I am at that all too familiar place with a project where I am having to decide whether I want to build what I need, or depend on an API service provider. As an engineer it is always easy to think you can just build what you need, but the more experience you have, you begin to realize this isn't always the smartest move. I'm at that point with API monitoring. I have a growing number of endpoints that I need to make sure are alive and active, but I also see an endless road map of detailed requests when it comes to granularity of what "alive and active" actually means.

At first I was just going to use my default cron job service to hit the base url and API paths defined in my OpenAPI for each project, checking for the expected HTTP status code. Then I thought I better start checking for a valid schema. Then I thought I better start checking for valid data. My API project is an open source solution, and I thought about each of my clients and implementations as me for testing and monitoring for their needs. Then I thought, no way!! I'm just going to use [Runscope](http://apis.how/8nlsropidv), and build in documentation and processes that each of my clients and implementations can also use Runscope to dial in monitoring and testing of their API on their own terms.

Since all of my API projects is OpenAPI driven, and Runscope is an OpenAPI driven API service provider (as ALL should be), I can use this as the seed for setting up testing and monitoring. Not all of my API implementations will be using 100% of the microservices I'm defining, or 100% of the API paths available fo each of the microservices I'm defining. Each microservice has it's core set of paths that deliver the service, but then I'm also bundling in database, server, DNS, logging and other microservice operational level APIs that not all my implementations will care about monitoring (sadly). So it is important for my clients and implementations to be easily select with APIs they care about monitoring, which OpenAPI will help do the heavy lifting. When it comes to exactly what API monitoring and testing means to them, I'll rely on Runscope to do the heavy lifting.

If Runscope didn't have the ability to import an OpenAPI to plant the seeds for API testing and monitoring I might have opted to just build out a basic solution myself. The manual process of setting up my API monitoring and testing for each client would quickly become more work than just building a solution--even if it was nowhere near as good as Runscope. However, we are increasingly living in an OpenAPI driven API lifecycle where service providers of all shapes and sizes allow for the importing and exporting of common API definition formats like OpenAPI. Helping API providers and architects like myself stick to what we do best, and not reinvent the wheel for each stop along the API lifecycle.

**Disclosure:** [Runscope](http://apis.how/8nlsropidv) is an API Evangelist partner.
