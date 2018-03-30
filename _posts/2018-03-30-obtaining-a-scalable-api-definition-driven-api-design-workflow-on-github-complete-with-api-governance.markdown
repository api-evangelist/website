---
published: true
layout: post
title: >-
  Obtaining A Scalable API Definition Driven API Design Workflow On Github
  Complete With API Governance
date: 2018-03-30T11:00:00.000Z
tags:
  - API Evangelist
  - Definitions
  - Design
  - Orchestration
image: >-
  https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories/G0520270_blue_circuit.jpg
---
<p><img src="{{ page.image }}" width="45%" align="right" style="padding: 15px;" /></p>There is a lot of talk of an API design first way of doing things when it comes to delivering microservices. I'm seeing a lot of organizations make significant strides towards truly decoupling how they deliver the APIs they depend on, and continue to streamline their API lifecycle, as well as governance. However, if you are down in the weeds, doing this work at scale, you know how truly hard it is to actualy get everything working in concert across many different teams. While I feel like I have many of the answers, actually achieving this reality, and assembling the right tools and services for the job is much harder then it is in theory.

There was [a question posted on API Craft recently that I think gets at the challenges we all face](https://groups.google.com/forum/#!topic/api-craft/H3tpTPJnoZQ):

> _We plan to use Open API 3 specification for designing API's that are required to build our enterprise web application. These API's are being developed to integrate the backend with frontend. They are initially planned to be internal/private. To roll out an API First strategy across multiple teams (~ 30) in our organization we want to recommend and centrally deploy a standard set of tools that could be used by teams to design and document API's._<br /><br />
> _I am new to the swagger tool set. I understand that there is a swagger-editor tool that can help in API design while swagger-ui could help in API documentation. Trying them I realized a few problems_<br /><br />
> _1. How would teams save their API's centrally on a server? Swagger editor does not provide a way to centrally store them._<br />
> _2. How can we get a directory look up that displays all the designed API's?_<br />
> _3. How can we integrate the API design and API documentation tool?_<br />
> _4. How can the API specifications be linked with the implementation (java) to keep them up-to-date?_<br />
> _5. How do we show API dependencies when one api uses the other one?_<br /><br />
> _We basically need to think about the end-to-end work-flow that helps teams in their SDLC to design API's. For the start I am trying to see what can we achieve with free tools. Can someone share their thoughts based on their experience?_
This reflects what I'm hearing from the numerous projects I'm consulting with. Some of the OpenAPI (Swagger) related questions can be addressed using Github, but the code integration, dependency, and other aspects of this question are much harder to answer, let alone solve with a single tool. Each team has their existing workflows, pipelines, and software delivery processes in place, so helping articulate how you should do this at scale, gets pretty difficult very quickly.

**Github, Gitlab, or BitBucket At Core**
The first place you want to start is with Github, Gitlab, or Bitbucket at the core. If you aren't managing your services, and supporting API definitions as individual repositories within a version control system, achieving this at scale will be difficult. These software development platforms are where your APIs should begin, live and evolve, as well as experience their end of life. Making not just the code accessible throughout the lifecycle, but also the API definitions and other artifacts that are essential throughout the API lifecycle.

**Full API Lifecycle Service Providers**
There are a handful of API service providers out there who will help you get pretty far down this road. Evolving towards being what I consider to be a full lifecycle API service provider. Not just helping you with design, or any other individual stop along the API lifecycle, and emerging to help you with as much of what you'll need to get the job done. Here are just a handful of the leading ones out there that I track on:

- [**Postman**](https://www.getpostman.com/) - Focusing on the client, but bringing in a full stack of lifecycle development tools to support.
- [**Stoplight**](https://stoplight.io/) - Beginning with API design, but then expanding quickly to help you manage and govern the lifecycle.
- [**APIMATIC**](https://apimatic.io/) - Emphasis on quality SDK generation, but approach life cycle deployment as a pipeline.
- [**Swagger**](https://swagger.io/) - Born out of the API definition, but quickly introducing other lifecycle solutions as part of the package.

I can't believe I'm talking about Swagger, but I'll vent about that in another post. Anyways, these are what I'd consider to be the leading API lifecycle development solutions out there. They aren't going to get you all the way towards everything listed above, but they will get you pretty far down the road. Another thing to note is that they ALL support OpenAPI definitions, which means you can actually use several of the providers, as long as your central truth is an OpenAPI available on a Github repository.

No single one of these services will address the questions posted above, but collectively they could. It shows how fragmented services in the space are, and how many different interpretations of the API lifecycle there are. However, it also shows the importance of an API definition-driven approach to the lifecycle, and how using OpenAPI and Postman Collections can help bridge our usage of multiple API service providers to get the job done. Next, I'll work on a post outlining some of the open source tooling I'd suggest to help solve some of these problems, and then work to connect the dots more on how you could actually do this in practice on the ground within your organization.
