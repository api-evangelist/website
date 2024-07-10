---
published: true
layout: post
title: 'An APIs.json API Contract'
tags:
  - APIs.json
  - Contracts
  - Producers
  - Consumers
image: https://kinlane-productions2.s3.amazonaws.com/algorotoscope-master/john-wayne-the-searchers-western-union-telegraph-and-cable.jpeg
---
I have been [exploring the addition of a new property type to APIs.json called “Contract”](https://apisjson.org/2024/07/07/considering-some-new-apis-json-types/). I wrote about recently [how we need to expand our definition of the API contract beyond a technical contract like OpenAPI or AsyncAPI](https://apievangelist.com/2024/07/06/expanding-the-definition-of-our-api-contracts/). I am looking to establish a baseline any company could use as a boilerplate contract between API consumer and producer. Here is the draft I have crafted to express the minimum API contract.

<script src="https://gist.github.com/kinlane/9fe33d1639d6988d9180cadad8c15b98.js"></script>

I’d consider this to be a B2B API consumer and producer API contract. It reflects what I like to have from all of the API providers I depend on to run API Evangelist. Next I will make a slightly more advanced version of this B2B API contract, and consider what an API contract might look like at the industry level, for PSD2, FHIR, or other standard. I will work on better documenting how to share an API contract with your API producers, and brainstorm other ways to encourage API consumers to leverage API contracts. 