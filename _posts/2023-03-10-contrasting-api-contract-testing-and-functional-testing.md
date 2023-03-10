---
published: true
layout: post
title: 'Contrasting API Contract Testing and Functional Testing'
image: https://kinlane-productions2.s3.amazonaws.com/algorotoscope-master/citizenship-fire-hydrant-water.jpg
author:
    name: kinlane
tags:
    - Testing
    - Contract Testing
    - Functional Testing
    - OpenAPI
    - JSON Schema
    - Assertions
---
I am neck deep in very philosophical debates around API specifications and testing right now, which I am working with my team get more precise in how we discuss API testing and avoid drowning in the semantics and perspectives that spin many of these conversations out. As always, I need to work through independently aspects of this conversation using storytelling, so that I can wrap my brain around the nuances and details of it all.

My co-worker Jordan Walsh published a great walk through of what contract testing is, and specifically what producer vs consumer contract testing is, but for this conversation I am just workshopping a single concept I thought he articulated very well, when comparing how OpenAPI and specifically JSON Schema differs from common assertion-based testing using code. Here is a screen shot of the slide from Jordan’s contract testing.

![OpenAPI Schema and Postman Tests](https://kinlane-productions2.s3.amazonaws.com/provider-managed-contract-tests.png)

One the left you have a JSON Schema from an OpenAPI contract, and on the right, you have test assertions being executed against an API. While this shows two separate ways to approach the problem of testing, there is a whole lot of unspoken nuances here that gets at why API contract testing is desirable over just API functional testing alone. I am not saying that functional testing is going anywhere, what I am saying is that you can do much of what you are accomplishing with functional testing using a contract, but the scope and perspective is where you get more bang for your buck.

## Coders Like to Code
While discussing this topic with folks I encounter many people who feel strongly that code-based functional testing is where the value is. These folks often do not understand JSON Schema and they do see the narrow scope in which there are interpreting API functionality and writing tests. There will always be a place for code-based functional testing using assertions, but writing code to cover all functionality, and update code to deal with change will always be fraught with challenges.

## Scope of Functionality
One of the biggest differences you see occurring here is at what scope the functionality of an API is defined. With functional you often have a lone developer or QA writing assertions based upon their understanding of the functionality, where with the contract approach you likely have multiple stakeholders including an architect, product manager, as well as designers, developers, and QA. Ideally a mix of business and technical folks hammering out what the functionality and baking the definition, constraints, and shape of functionality using JSON Schema rather than a series of tests.

## Scope of Change
The challenge in maintaining a code-based approach to functional testing is that every time the API changes you must go update all of the tests to reflect the changes made. In a contract-first world the change gets made in the contract, then the code and gateway are changed, and your tests are either simple JSON Schema validation tests and/or generated tests that are dynamically created to reflect your contract scope. Change is the portion of this conversation where things really begin to go off the rails and a contract-driven approach begins to shine, but it is hard to help people see it when they are down in the weeds of enterprise change.

## Regulatory Compliance
Where the scope conversation gets even more powerful is when you begin to employ contracts that are governed by standards bodies for specific industries. Using JSON Schema and OpenAPI to get entire industries on the same page when it comes to what API functionality means across thousands or millions of producers and consumers. You just aren’t going to be able to scale functional testing at an industry scale, sorry. Before any code gets written you are going to have to define, negotiate, iterate, and then agree upon a contract. You can rely on just production being the source of truth anymore at this scale, sorry.

## This Takes Work
This is not an easy conversation. It is very difficult to get lost in the semantics, perspective, and incentives for why we test our APIs. It is one that not everyone will be able to have because of the scope of where they work in the API delivery supply chain. Which for me, demonstrates why we should be providing these folks with contracts, standardizing the testing they do and leave them only delivering on the last mile of assertions that need to be made. Contract testing will only get you so far, but it will get you a lot further down the road than functional testing. The nuance here is really in the detail of what API functionality is at an API, business, or industry level. Most people I encounter who push back on the notion of contract testing are only operating at the API level, or in a very narrow view of business. 

This conversation gets even more complicated once I start diving into the differences between testing the API interface and the contract itself with Spectral rules. Which feed into each other. Meaning if you have multiple status codes in your OpenAPI and are linting for that, your contract testing will be more robust when it comes to knowing the surface area of your contract. I have several smaller stories to publish on this topic to help me see things straight at this intersection. There is so much ambiguity and obfuscation at this intersection of our API operations, and there are several competing scopes and incentives. I am just trying to work my way through things so that I can make sense of what is happening and get more opinionated without getting lost in semantics. Stay tuned for lots of interesting discussions on this subject here as I work through things, but also at Postman as we formalize different views of what is happening.
