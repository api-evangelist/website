---
published: true
layout: post
title: 'An API Commons Base for Problem Details for HTTP APIs'
tags:
  - Problems
  - Errors
  - HTTP Status Codes
  - Communication
image: https://kinlane-productions2.s3.amazonaws.com/algorotoscope-master/yellow-journalism-building-art-construction.jpeg
---
[I created a new API Commons base for Problem Details for HTTP APIs](https://apicommons.org/base/problem-details-for-http-apis/). The work is evolved from the [Train Travel API template](https://bump.sh/bump-examples/doc/train-travel-api) created by [Bump.sh](https://bump.sh/), but I wanted to isolate just the [Problem Details for HTTP APIs](https://datatracker.ietf.org/doc/rfc9457/) all by itself so others can easily copy and paste. The OpenAPI is set up to make it easy to copy and paste the schema, response objects, and the HTTP status code references—helping teams not reinvent the wheel when it comes to errors, and standardize how they communicate problems.

<script src="https://gist.github.com/kinlane/1d72cbfd4abce1a13e5c489c950486b2.js"></script>

I will keep polishing the base, and publish a set of Spectral rules to support the governance of API errors next, so that teams applying the standard can also easily lint for the presence or absence of Problem Details for HTTP APIs. Really there is no reason why we should return anything else but Problem Details for HTTP APIs now there is an official standard, and having rules, tests, and more backend implementation examples will help people stop being special snowflakes in this department.

Error handling is one of the areas we must standardize across APIs, and [the Problem Details for HTTP APIs base from API Commons](https://apicommons.org/base/problem-details-for-http-apis/) should provide most of what you need to ensure all of your APIs are communicating problems in a consistent way.