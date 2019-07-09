---
published: true
layout: post
title: Everything Is Headless In A Decoupled API World
date: 2017-10-12T11:00:00.000Z
tags:
  - API Evangelist
  - Headless
  - Deployment
image: >-
  https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories/catacombs_copper_circuit_2.jpg
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories/catacombs_copper_circuit_2.jpg" align="right" width="40%" style="padding: 15px;" /></p>It is always funny how long some concepts take to fully capture my attention. Sometimes I understand a concept on the surface, but never really invest the time into thinking deeply about how it actually fits into the big picture of my API research. One of these concepts is "headless". Most commonly applied to the "headless CMS". The wikipedia entry for headless CMS proclaims, "[a Headless CMS is a back-end only content management system (CMS) built from the ground up as a content repository that makes content accessible via a RESTful API for display on any device.](https://en.wikipedia.org/wiki/Headless_CMS)"

A headless CMS is basically API-first, but instead of API being the first focus, the entire CMS, and administrative system for managing the content gets top billing, with API playing a critical supporting role. It's what I am always prescribing as a way for API providers to consider the role between their applications, and their backend API resources. Decoupling your apps, from the backend resources. The administration interface for the content management system is one application, and each of your web, mobile, or other applications act as independent solutions. I see headless as just a business view of doing APIs, which makes sense when selling the concept to normals.

I'm adding a research area for headless that augments [my API deployment research](http://deployment.apievangelist.com/). Some of the open source implementations I've come across like [Directus](https://getdirectus.com/) are pretty slick. It's a pretty quick way to go from API to something that immediately benefits the average user in as short of time as possible. Headless is just another way to frame the the API conversation in the context of delivering an internal content management system, over getting 3rd party developers to build applications on top. It is something that is still possible because their is an API behind, but it is not the primary objective in any headless implementation.

While the main definition of headless is about having an API behind everything, I am also finding examples where Github is the backend, instead of just a RESTful API. [Prose.io](http://prose.io/) which is actually the CMS I use for API Evangelist is considered a headless CMS, but Github acts my backend. Some of the headless CMS solutions I've used that depend on Github use Git as the connection, while others depend on the Github API for reading and writing data and content. This reflects how I use Github across my projects, beyond just Prose.io, except I am depending on web APIs, Github, as well as Google Sheets for the backend of Jekyll driven websites and applications.

I have been tracking on headless CMS stories for almost two years now, but after diving a little deeper this last week, it finally clicked for me. I feel headless is a good way to help the world move past WordPress, and embrace a more decoupled way of delivering websites, mobile, and other types of applications. I'm going to deploy Directus so that I can better understand headless as an approach to deploying APIs, and see about deploying basic demo implementations that I can point to. I'm hoping to use it as a way to introduce folks to APIs where public APIs is not the first objective, allowing them to get their feet wet with a simple API and website implementation. Helping deliver value without all the immediate risk, allowing folks to learn about how APIs can drive one or many applications in a more controlled internal environment.
