---
published: true
layout: post
title: 'Making Sure Definitions In OpenAPI Are Robust For Use In Schema Validation'
date: 2017-09-11T11:00:00.000Z
tags:
  - API Evangelist
  - Definitions
  - Schema
  - Validation
  - Testing
image: 'https://s3.amazonaws.com/kinlane-productions/open-referral/hsda-schema.png'
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/open-referral/hsda-schema.png" align="right" width="40%" style="padding: 15p;" /></p>I'm working on v1.2 of [my Human Sevices Data API (HSDA)](http://org.open.referral.adopta.agency/), and with this wave of work I'm making sue there is a functional API for validating all JSON that gets posted as the body in requests, as well as when it gets returned as part of API responses. To drive my validator I'm using JSON schema, which I already have defined as part of [the OpenAPI definition for the project](https://github.com/human-services/portal/tree/master/_data/api-commons). I want to reuse, and build on top of this work, but I found the definitions for my OpenAPI to be pretty deficient in much of the details I am needing to validate the request and response bodies of my HSDA APIs.

The process has showed me the importance of making sure the definitions portion of my OpenAPIs are as robust as I can. Possessing required, default, regex patterns, and other details I'm going to need to make sure my schema validator is as robust as possible. I'm entering the phase of this project where vendors, and implementors are looking for guidance on whether or not their schema are HSDS/A compliant, and they are supporting the fields necessary to get a stamp of approval. The schema validator is essential to this, but the new validation API I've created is only as good as the JSON schema that I'm using as part of its engine.

I come across a number of OpenAPIs in the wild which do not possess schema definitions, and references for each API. These API providers are only describing enough of the surface area of their API to be able to generate API documentation using Swagger UI. This is something I've also been guilty of in the past, where I would only define the surface area of the API, just to get what I needed for my API discovery needs. Over the last year, I've spent more time making sure the definitions portion of the OpenAPI is also present, but it isn't until now that I've been making sure the fine details of the schema are present. I need this to be in place for validation, which will be used across monitoring, testing, and other stops along the API life cycle I will be delivering as part of this work.

Honestly, my JSON schema chops were not up to snuff for this work, something I've struggled with making the time for this summer. However, I feel like I'm finally getting there. I'm beyond the basics of JSON schema validation, and have my simple API validator API in place. I just need to make sure I'm always investing the time required to develop robust JSON schema for all my APIs, so that the validator provides rich responses with each API schema validation. I'm thinking I will be build a tool for helping identify what is lacking with the definitions in my OpenAPIs, pointing out the common things I'm lacking, and running this before I ever consider actually validating the schema that are used in the API request body, or the API response body for the projects I'm working on. Always making sure the schema, and API definitions are harmonized, and speaking the same language is essential to all of this human services API effort to work properly.