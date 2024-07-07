---
published: true
layout: post
title: 'An APIs.json for the Train Travel API'
tags:
  - Templates
  - APIs.json
  - Blueprints
  - API Commons
image: https://kinlane-productions2.s3.amazonaws.com/algorotoscope-master/america-immigration_dumping-ground-high-speed-train-station.jpg
---
I am working on producing an APIs.json for the [Train Travel API produced by Bump.sh](https://bump.sh/bump-examples/doc/train-travel-api). I am adding the [API to the API Commons as a base API](http://localhost:4000/base/train-travel/), and publishing an APIs.json is where it all starts. I will be producing a template type APIs.json for the API, and will leave for Bump.sh to create an index of their own API. I am simply looking to build on their great work and establish a set of APIs.json + OpenAPI templates I can use to flesh out other base APIs in the commons like accounts, images and videos.

I like the seed APIs.json Bump.sh approach provides. It is pretty minimal for an API, but it really works! It provides the essentials, stays simple and clean, but provides the machine-readable API contract you need to put an API to work.

<script src="https://gist.github.com/kinlane/2be2b7f6c2638cbdaab322813f0b19b5.js"></script>

I will add this to the commons as a blueprint. I see the Train Station API as a base API, and Bump.sh approach to the operations around it as a blueprint. Once I do this, I will then produce a set of Spectral rules that covers the surface area of the API base, and then begin copying the APIs.json and OpenAPI to power other bases like the account, images, and videos. It is a solid foundation. I can begin adding other properties I think should be present and augment the great work Bump.sh has already done.