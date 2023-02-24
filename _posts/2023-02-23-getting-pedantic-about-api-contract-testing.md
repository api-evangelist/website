---
published: true
layout: post
title: 'Getting Pedantic About API Contract Testing'
image: https://kinlane-productions2.s3.amazonaws.com/algorotoscope-master/bf-skinner-crypto-wheels-old-compute-bletchley.jpg
author:
name: kinlane
tags:
- Testing
- Contracts
---
I am immersed in very detailed and pedantic discussions lately about API contract testing lately. Like many phrases in the world of APIs, the phrase contract testing gets thrown around a lot, without much understanding of what it means. I use it so often, and hear it so often, in so many different scenarios I lose track of what it means. Thankfully Kevin Swiber (<a href="https://twitter.com/kevinswiber">@kevinswiber</a>) is on my team and regularly gets all pedantic about it on calls, with their head coming really close to exploding, reminding me of where I stand on this subject. Kevin is right, and here is wher emy head is at on the subject.

I encounter a lot of conversation around auto-generation of contract testing, which is really something that is more difficult than it may seem, if not impossible without some human intervention. To understand, let's start with the basics--simple API testing.

<p><img src="https://kinlane-productions2.s3.amazonaws.com/contract-testing/contract-testing-1.jpg" width="100%"></p>

This is pretty fundamental API testing using a Postman collection--something I see many times each day, and something millions of developers accomplish daily. This is not contract testing. It is just simple testing. There is no contract. You can get pretty crafty with your test scripts, but it doesn't equal contract testing. Now, let's move into the auto-generation possibilities when it comes to producing collections for tests using a proxy or Interceptor.

<p><img src="https://kinlane-productions2.s3.amazonaws.com/contract-testing/contract-testing-2.jpg" width="100%"></p>

This scenario can be used to generate collections from existing API traffic, but you will still have to add test scripts to your collections to actually test each API. Something that is still not contract testing. We could also generate the collections from our gateway.

<p><img src="https://kinlane-productions2.s3.amazonaws.com/contract-testing/contract-testing-3.jpg" width="100%"></p>

However we generate our collection from the gateway, we will still have to hand-craft our test scripts, but one could envision easily generating test scripts as well. Something that still is not contract testing. We could also generate the collections from our code or the SDK we use.

<p><img src="https://kinlane-productions2.s3.amazonaws.com/contract-testing/contract-testing-4.jpg" width="100%"></p>

Like from the gateway or the proxy, we will still have to produce the test scripts. Like with the gateway, we could envision where the scripts get generated as well. This still isn't contract testing. Now, let's begin to seismically shift the conversation more towards what is contract testing by hand-crafting our OpenAPI, and then generating our test collection from this artifact.

<p><img src="https://kinlane-productions2.s3.amazonaws.com/contract-testing/contract-testing-5.jpg" width="100%"></p>

This is one area I am guilty of misusing the phrase contract testing. I often call OpenAPI the contract and thus annointing the collection test generated from it a contract test. This is not contract testing either. However, I could also generate my gateway configuration and my code behind my gateway using my OpenAPI artifact.

<p><img src="https://kinlane-productions2.s3.amazonaws.com/contract-testing/contract-testing-6.jpg" width="100%"></p> 

This really helps with striking an alignment between my OAS, collection tests, and what is in production. This still is not contract testing. Now to flip things around again, we could also generate our OpenAPI from the gateway and the code.

<p><img src="https://kinlane-productions2.s3.amazonaws.com/contract-testing/contract-testing-7.jpg" width="100%"></p>

This is a good way to get us an OpenAPI artifact which we could then use to generate our test collection. This still isn't contract testing. Like the collection, we could also generate our OpenAPI using a proxy.

<p><img src="https://kinlane-productions2.s3.amazonaws.com/contract-testing/contract-testing-8.jpg" width="100%"></p>

This gets us an OpenAPI artifact which we can then use to generate our test collections and even the scripts. This still isn't contract testing. One key ingredient that actually moves us into the realm of API contract testing is the usage of the JSON Schema in the OpenAPI in our collection test scripts.

<p><img src="https://kinlane-productions2.s3.amazonaws.com/contract-testing/contract-testing-9.jpg" width="100%"></p>

Honestly, if I am being completely pedantic here, it really isn't contract testing until the JSON Schema is complete with not just object properties, but also validation, min, max, and other JSON Schema properties that are used to validate the structure and shape of the object. 

Taking it even further, it really isn't a contract until it is actually negotiated between producer and consumer and they have agreed upon the structure, shape, and access of our digital resources and capabilities. 

We haven't even begun to talk about change. I was going to add in, and then I decided to leave this until the next piece and just focus on the contract testing and not breaking the contract with changes.

Putting an API into production does not create a contract. Testing an API in production isn't contract testing. The only way to establish a contract is to establish an agreed upon contract as OpenAPI, include JSON Schema for the structure and shape of requests and responses, and use that artifact agreed upon between producer and consumer as part of manual, scheduled, or automated testing. 