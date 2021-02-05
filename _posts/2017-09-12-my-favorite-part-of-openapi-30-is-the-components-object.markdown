---
published: true
layout: post
title: My Favorite Part Of OpenAPI 3.0 Is The Components Object
date: 2017-09-12T11:00:00.000Z
tags:
  - API Evangelist
  - Definitions
  - Design
image: >-
  https://s3.amazonaws.com/kinlane-productions/openapi/openapi-30-components-object.png
---
<p><a href="https://github.com/OAI/OpenAPI-Specification/blob/master/versions/3.0.0.md#componentsObject"><img src="https://s3.amazonaws.com/kinlane-productions/openapi/openapi-30-components-object.png" align="right" width="40%" style="padding: 15px;" /></a></p>There were a number of changes made to the structure of Open API in the move to version 3.0 that I am a fan of, but if I had to point at a single seismic shift that I think will move the conversation forward it is [the components object](https://github.com/OAI/OpenAPI-Specification/blob/master/versions/3.0.0.md#componentsObject). According to the specification the components object, "holds a set of reusable objects for different aspects of the OAS. All objects defined within the components object will have no effect on the API unless they are explicitly referenced from properties outside the components object." It is the store for for all the common and reusable aspects of defining, and designing your APIs--which will have huge benefits on how we are doing all of this.

Here is the laundry list of what you can put into your OpenAPI 3.0 components object, and reference throughout your API definitions:

- **schemas** - An object to hold reusable data schema used across your definitions.
- **responses** - An object to hold reusable responses, status codes, and their references.
- **parameters** - An object to hold reusable parameters you are using throughout your API requests.
- **examples** - An object to hold reusable the examples of requests and responses used in your design.
- **requestBodies** - An object to hold reusable the bodies that will be sent with your API request.
- **headers** - An object to hold reusable headers that define the HTTP structure of your requests.
- **securitySchemes** - An object to hold reusable security definitions that protect your API resources.
- **links** - An object to hold reusable links that get applied to API requests, moving it towards hypermedia.
- **callbacks** - An object to hold reusable callbacks that can be applied.

[I've written about how many API developers see this stuff as duplicate work across our APIs](http://apievangelist.com/2017/07/31/you-see-duplicate-work-while-i-see-common-patterns/), where I see them as common, resusable patterns that we should be getting organized--the OpenAPI 3.0 components object is the beginning of us getting this house in order. The components object is how API architects and designers can ensure that API developers are being consistent in their work, and not just reusing common elements, but reusing well thought out, fully baked elements that adhere to standards and common definitions used throughout the industry.

The OpenAPI 3.0 components object is where we are going to start injecting API literacy training into the development process. It is where we will teach developers about headers, and common ways of securing our APIs. It is where we will start reusing common dictinaries like Schema.org so we STOP re-inventing the wheel when it comes to defining our schema definitions, fields, and other mundane aspects of crafting an API. The components object isn't just where we are reusing components within a single OpenAPI, it is where we will start reusing across all the OpenAPIs we are crafting, and learning, sharing, collaborating, and reusing across OpenAPIs that are made publicly available.

The OpenAPI 3.0 components object is where we are going to start delivering the hypermedia literacy that was required to get the adopttion that hypermedia advocates envision, but were stonewalled because people just didn't get it. I'm pretty excited about this aspect of OpenAPI 3.0, and I got myself so fired up about it last night I started building some of my API dictionary tooling I've had in my head for a while, but didn't have just the right vehicle in mind for delivering at scale. I haven't had much time for playing with OpenAPI 3.0, or the tooling that has emerged, but I got the bug now. I'm going to prioritize some work in this area, if nothing else for generating some relevant stories here on the blog, and keeping me in tune with folks are doing. Oh, that reminds me, have you seen what my friend Mike Ralphson ([@PermittedSoc](https://twitter.com/PermittedSoc)) is up to? [He is leading the charge when it comes to OpenAPI 3.0 tooling](https://github.com/Mermade/) << I recommend keeping an eye on what he is up to on Github.