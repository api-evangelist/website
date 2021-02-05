---
published: true
layout: post
title: Docker Engine API Has OpenAPI Download At Top Of Their API Docs
date: 2018-01-18T09:00:00.000Z
tags:
  - API Evangelist
  - Definitions
  - Containers
  - Documentation
image: 'https://s3.amazonaws.com/kinlane-productions/docker/docker-engine-openapi-download.png'
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/docker/docker-engine-openapi-download.png" align="right" width="45%" style="padding: 15px;" /></p>I am a big fan API providers taking ownership of their OpenAPI definition, which enables API consumers to download a complete OpenAPI then import into any client tooling like Postman, using it to generate client SDKs, and getting up to speed regarding the surface area of an API. This is why I like to showcase API providers I come across who do this well, and occasionally shame API providers who don't do it, and demonstrate to their consumers that they don't really understand what OpenAPI definitions are all about.

This week I am showcasing an API provider who does it well. I was on the hunt for an OpenAPI of the Docker Engine API, for use in a project I am consulting on, and was please to find that [they have a button to download the OpenAPI for each version of the Docker Engine API right at the top of the page](https://docs.docker.com/engine/api/v1.35/#). Making it dead simple for me, as an API consumer, to get up and running with the Docker API in my tooling. OpenAPI is about much more than just the API documentation, and something that should be a first class companion to ALL API documentation for EVERY API provider out there--whether or not you are a devout OpenAPI (fka Swgger) believer.

The Docker API team just saved me a significant amount of time in tracking down another OpenAPI, which most likely would be incomplete. Let alone the amount of work that would be required to hand-craft one for my project. I was able to take the existing OpenAPI and publish to the team Github Wiki for a project I'm advising on. The team will be able to use the OpenAPI to import into their Postman Client and begin to learn about the Docker API, which will be used to orchestrate the containers they are using to operate their own microservices. A subset of this team will also be crafting some APIs that proxy the Docker API, and allow for localized management of each microservice's underlying engine.

[I had to create the Consul OpenAPI for the team last week](https://apievangelist.com/2018/01/08/i-created-an-openapi-for-the-hashicorp-consul-api/), which took me a couple hours. I was pleased to see Docker taking ownership of their OpenAPI. This is a drum I will keep beating here on the blog, until EVERY API provider takes ownership of their OpenAPI definition, providing their consumers with a machine readable definition of their API. OpenAPI is much more than just API documentation, and is essential to making sense of what an API does, and then take that knowledge and quickly translate it into actual integration, in as short of time as possible. Don't make integrating with your API difficult, reduce as much friction as possible, and publish an OpenAPI alongside your API documentation like Docker does.
