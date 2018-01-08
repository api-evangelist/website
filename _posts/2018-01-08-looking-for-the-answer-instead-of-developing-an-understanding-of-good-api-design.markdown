---
published: true
layout: post
title: >-
  Looking For THE Answer Instead Of Developing An Understanding Of Good API
  Design
date: 2018-01-08T13:00:00.000Z
tags:
  - API Evangelist
  - Design
image: >-
  https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories/status-berlin_matrix.jpg
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories/status-berlin_matrix.jpg" align="right" width="45%" style="padding: 15px;" /></p>I recently worked with a large team on a microservices and API governance training a couple months back, where I saw a repeating pattern that I've experienced with other large enterprise groups. They seemed to want the right answers to doing APIs and microservices, instead of developing an understanding of good (or bad) API design, and determining the right way for themselves. The biggest challenge with this perception amongst development groups, is that there is no right answer, or one way of doing APIs and microservices--you need to find the right way forward for your team, and for each project.

I get this a lot within large organizations who are just beginning their API journey--just show us the right way of doing it! To which I usually reply with, let's roll up our sleeves and get to work on one of your services, and we will start showing you have to craft a simple, sensible, yet robust API that meets the needs of the project. I can't show you the "right way", until I understand what the particular need are, and zeroing in on what is the "right way", takes work, refinement, and crafting f a robust definition for the service.

API design isn't easy. It takes time to understand what schema is involved, and what role that schema will play in the request and response of an API. It takes work to understand whether the complexity should be spread horizontally across each API paths, or vertically within a single path, using parameters, the body, and other aspects of the surface area of the API. Until I understand the client needs I can't fully articulate whether we should stick with a simple JSON response, or a more sophisticated hypermedia media type, or possibly even go with something like GraphQL.

Ultimately, I need you to go on this journey with me. I can help ask hard questions, and provide relevant answers about best practices I see across the API space, but I do not know the THE answer. Sometimes there might be multiple right answer, or we won't know fully until we mock the interface and get to work playing with it. I know you want quick and direct solutions to how you should be doing this, but ultimately it is up to you to do the hard work of learning about what good API design is, and how we can apply it to this particular project. Each microservice within this project might have specific needs, and we'll have to come up with a variety of solutions that we can apply consistently across the entire project.

I am spending more time helping train teams using OpenAPI as a scaffolding for walking through practical API design, in the context of each service. Going through the paths, verbs, parameters, body, responses, status codes, schema, and fields for each service, one step at a time. It is providing a great way to teach them good API design, in the context of each service they are looking to deliver. Helping them understand that there is no one right answer to all of this. That we just have to invest in their overall API design toolbox. Understand the pros and cons of each decision they make, and develop a healthy understanding of what API design is, both good, and bad--over time.
