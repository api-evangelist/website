---
published: true
layout: post
title: 'Replacing the PetStore OpenAPI With the Train Travel OpenAPI'
tags:
  - OpenAPI
  - Templates
  - Blueprints
  - API Commons
image: https://kinlane-productions2.s3.amazonaws.com/algorotoscope-master/bf-skinner-high-speed-train-station-france.jpg
---
While writing the story on [Bump.sh's adoption of APIs.json](https://apievangelist.com/2024/06/16/bumpsh-support-apisjson-with-their-api-documentation-hubs/) I stumbled across their story on [replacing the ubiquitous PetStore OpenAPI that comes default with the Swagger and OpenAPI tooling](https://bump.sh/blog/modern-openapi-petstore-replacement) of the previous decade. I am a big fan of replacing this default OpenAPI that comes with services and tooling, but I am also impressed with Bump.sh's approach to actually deliver a well designed OpenAPI that people can learn from.

Bump.sh approach to designing the Train Travel OpenAPI reflects what you will want to do with your own API. Their approach leverages modern OpenAPI and JSON Schema, as well as employs modern standards like Problems JSON for errors. Of course, [Bump.sh manages the OpenAPI in a Github repo](https://github.com/bump-sh-examples/train-travel-api), and they even have a working copy of it—as you should. [It is a clean, simple, modern, and useful API](https://bump.sh/bump-examples/doc/train-travel-api), which is worthy of becoming the new default OpenAPI across API services and tooling.

I like the design of the API because it isn’t just a straight CRUD. The bookings have CRD, but the other operations are practical and real world. It provides a simple set of resources that could easily be expanded upon and reworked as a base for other API resources. I am going to use the patterns they provide as a base for some of the common APIs I will be publishing as part of our ongoing [API Commons](http://apicommons.org/) work. I like that. It feels like a fresh start, which is something we need in multiple areas of the API universe. Reusing and building upon existing healthy patterns will be what API Commons, in alignment with APIs.json and APIs.io is all about. 

Contributions like the Train Travel OpenAPI is another positive sign from an API service provider, signaling an investment into the API community. I am going to be looking for other ways I can incentivize API service providers to emulate what Bump.sh does. Both supporting APIs.json, and other community specs, but also contributing reusable JSON Schema, OpenAPI, AsyncAPI, and other building blocks. I am confident that if we are going to take things to the next level in the API space we are going to have to stop competing and reinventing the wheel on the most common aspects of API operations, and focus on the real value we each bring to the table.