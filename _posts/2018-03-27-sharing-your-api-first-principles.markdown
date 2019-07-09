---
published: true
layout: post
title: Sharing Your API First Principles
date: 2018-03-27T09:00:00.000Z
tags:
  - API Evangelist
  - Design
  - Guides
  - Communications
image: 'https://s3.amazonaws.com/kinlane-productions/zalando/zalando-screenshot.png'
---
<p><img src="{{ page.image }}" width="45%" align="right" style="padding: 15px;" /></p>I've been publishing regular posts from the API design guides of API providers I've been studying. API providers who publish their API design guides tends to be further along in their API journey. These API providers tend to have more experience and insight, and are often worth studying further, and learning from. [I've bee getting a wealth of valuable information from the German fashion and technology company Zalando, who has shared some pretty valuable API first principles](https://zalando.github.io/restful-api-guidelines/).

In a nutshell Zalando's API First principles focuses on two areas:

- define APIs outside the code first using a standard specification language
- get early review feedback from peers and client developers

By defining APIs outside the code, Zalando wants to facilitate early review feedback and also a development discipline that focus service interface design on:

- profound understanding of the domain and required functionality
- generalized business entities / resources, i.e. avoidance of use case specific APIs
- clear separation of WHAT vs. HOW concerns, i.e. abstraction from implementation aspects — APIs should be stable even if we replace complete service implementation including its underlying technology stack

Moreover, API definitions with standardized specification format also facilitate:

- single source of truth for the API specification; it is a crucial part of a contract between service provider and client users
- infrastructure tooling for API discovery, API GUIs, API documents, automated quality checks

Their guidance continues by stating:

_An element of API rirst are also a review process to get early review feedback from peers and client developers. Peer review is important for us to get high quality APIs, to enable architectural and design alignment and to supported development of client applications decoupled from service provider engineering life cycle._

_It is important to learn, that API First is not in conflict with the agile development principles that we love. Service applications should evolve incrementally — and so its APIs._

_Of course, our API specification will and should evolve iteratively in different cycles; however, each starting with draft status and early team and peer review feedback. API may change and profit from implementation concerns and automated testing feedback. API evolution during development life cycle may include breaking changes for not yet productive features and as long as we have aligned the changes with the clients. Hence, API First does not mean that you must have 100% domain and requirement understanding and can never produce code before you have defined the complete API and get it confirmed by peer review._

_On the other hand, API First obviously is in conflict with the bad practice of publishing API definition and asking for peer review after the service integration or even the service productive operation has started. It is crucial to request and get early feedback — as early as possible, but not before the API changes are comprehensive with focus to the next evolution step and have a certain quality (including API Guideline compliance), already confirmed via team internal reviews._

Zalando get's at one of the reasons I'm a big advocate for a design, mock, and document API lifecycle, forcing developers to realize their API vision, get feedback, and iterate upon their designs, before they ever consider moving into a production environment. I feel like there are many views of what API first means, and many do not focus on the process, and obsess too much on just API design. I think Zalando's API design guide reflects this, where the guide is more about API guidance, than it is just about the design of an API. It provides a wealth of wisdom and knowledge, but is still labeled as being about API design. 

Similar to pushing companies, organizations, institutions, and government agencies to do in APIs in the first place, I'm encouraging more of them to begin publishing their API design guides as part of their journey. It seems like it is an important part of being able to articulate not just the API design guidelines, but also a place to articulate the overall reasons behind doing APIs in the first place, and the principle, ethics, and process surrounding how we are doing APIs across the disparate teams that make things go around in our worlds.
