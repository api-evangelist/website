---
published: true
layout: post
title: API Definitions Are Important
date: 2019-06-12T09:00:00.000Z
tags:
  - API Evangelist
  - Definitions
image: >-
  https://s3.amazonaws.com/kinlane-productions2/algorotoscope-master/christianity-christianity-under-construction-copper-circuit.jpg
---
<img src="{{ page.image }}" width="35%" align="right" style="padding: 15px;" />
I found myself scrolling down the home page of API Evangelist and thinking about what topic(s) I thought were still the most relevant in my mind after not writing about APIs for the last six months. Hands down it is API definitions. These machine and human readable artifacts are the single most important thing for me when it comes to APIs I'm building, and putting to work for me.

Having mature, machine readable API definitions for all API that you depend on, is essential. It also takes a lot of hard work to make happen. It is why I went API define first a long time ago, defining my APIs before I ever get to work designing, mocking, developing, and deploying my APIs. Right now, I'm heavily dependent on my:

- **JSON Schema** - Essential for defining all objects being used across API contracts.
- **OpenAPI** - Having OpenAPI contracts for al my web APIs is the default--they drive everything.
- **AsyncAPI** - Critical for defining all of my non HTTP 1.1 API contracts being provided or consumed.
- **Postman Collections** - Providing me with the essential API + environment definitions for run-time use.
- **APIs.json** - Helping me define all the other moving parts of API operations, indexing all my definitions.

While there is plenty of other stops along the API lifecycle that are still relevant to me, my API definitions are hands down the most valuable intellectual property I possess. These four API specifications are essential to making my world work, but there are other more formalized specifications I'd love to be able to put to work:

- **Orchestrations** - I'd liked to see a more standardized, machine readable way for working with many API calls in a meaningful way. I know you can do this with Postman, and I've done with OpenAPI, and like Stoplight.io's approach, but I want an open source solution.
- **Licensing** - I am not still actively using API Commons, but I'd like to invest in a 2.0 version of the API licensing specification, moving it beyond just the API licensing, and consider SDK, and other layers.
- **Governance** - I'd like to see a formal way of expressing API governance guidance that can be viewed by a human, or executed as part of the pipeline, ensuring that all API contracts conform to a set of standards.

These area hit on the main areas that concern for me when it comes to defining the contracts I need to further automate the integration and deployment of API resources in my life. While there are definitely other stops along the API lifecycle on my mind, I spend the majority of my time creating, refining, communicating, and moving forward API definitions that define and drive every other stop along the API lifecycle.

API definitions represent API sanity for me. If they aren't in order, there is disorder. An immature API definition requires investment, socialization amongst stakeholders, and iterating upon before it will ever be considered for publishing. I'll be exploring the other things that matter for me along the API lifecycle, and then I'm guessing that the rest of this stuff I've been researching over the last eight years will either disappear, or just be demoted on the site. We'll see how this refresh rolls out, but I'm guestimating about 25% of my research will continue to move forward after this reboot.
