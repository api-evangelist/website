---
published: true
layout: post
title: A README For Your Microservice Github Repository
date: 2018-04-30T09:00:00.000Z
tags:
  - API Evangelist
  - Microservices
  - Documentation
  - Communication
  - Road Map
  - Github
image: 'https://s3.amazonaws.com/kinlane-productions/bw-icons/bw-readme.png'
---
<p><img src="{{ page.image }}" width="45%" align="right" style="padding: 15px;" /></p>I have several projects right now that are needed a baseline for what is expected of microservices developers when it comes to the README for their Github repository. Each microservice should be a self-contained entity, with everything needed to operate the service within a single Github repository. Making the README the front door for the service, and something that anyone engaging with a service will depend on to help them understand what the service does, and where to get at anything needed to operate the service.

Here is a general outline of the elements that should be present in a README for each microservice, providing as much of an overview as possible for each service:

- **Title** - A concise title for the service that fits the pattern identified and in use across all services.
- **Description** - Less than 500 words that describe what a service delivers, providing an informative, descriptive, and comprehensive overview of the value a service brings to the table.
- **Documentation** - Links to any documentation for the service including any machine readable definitions like an OpenAPI definition or Postman Collection, as well as any human readable documentation generated from definitions, or hand crafted and published as part of the repository.
- **Requirements** - An outline of what other services, tooling, and libraries needed to make a service operate, providing a complete list of EVERYTHING required to work properly.
- **Setup** - A step by step outline from start to finish of what is needed to setup and operate a service, providing as much detail as you possibly for any new user to be able to get up and running with a service.
- **Testing** - Providing details and instructions for mocking, monitoring, and testing a service, including any services or tools used, as well as links or reports that are part of active testing for a service.
- **Configuration** - An outline of all configuration and environmental variables that can be adjusted or customized as part of service operations, including as much detail on default values, or options that would produce different known results for a service.
- **Road Map** - An outline broken into three groups, 1) planned additions, 2) current issues, 3) change log. Providing a simple, descriptive outline of the road map for a service with links to any Github issues that support what the plan is for a service.
- **Discussion** - A list of relevant discussions regarding a service with title, details, and any links to relevant Github issues, blog posts, or other updates that tell a story behind the work that has gone into a service.
- **Owner** - The name, title, email, phone, or other relevant contact information for the owner, or owners of a service providing anyone with the information they need to reach out to person who is responsible for a service.

That represent ten things that each service should contain in the README, providing what is needed for ANYONE to understand what a service does. At any point in time someone should be able to land on the README for a service and be able to understand what is happening without having to reach out to the owner. This is essential for delivering individual services, but also delivery of service at scale across tens, or hundreds of services. If you want to know what a service does, or what the team behind the service is thinking you just have to READ the README to get EVERYTHING you need.

It is important to think outside your bubble when crafting and maintaining a README for each microservice. If it is not up to date, or lacking relevant details, it means the service will potentially be out of sync with other services, and introduce problems into the ecosystem. The README is a simple, yet crucial aspect of delivering services, and it should be something any service stakeholder can read and understand without asking questions. Every service owner should be stepping up to the plate and owning this aspect of their service development, and professionally owning this representation of what their service delivers. In a microservices world each service doesn't hide in the shadows, it puts it best foot forward and proudly articulates the value it delivers or it should be deprecated and go away.
