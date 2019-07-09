---
published: true
layout: post
title: We Are Not Supporting OpenAPI (fka Swagger) As We Already Published Our Docs
date: 2018-01-10T09:00:00.000Z
tags:
  - API Evangelist
  - Definitions
  - Documentation
  - Clients
image: >-
  https://s3.amazonaws.com/kinlane-productions/hashicorp/hashicorp-consul-github-swagger-docs.png
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/hashicorp/hashicorp-consul-github-swagger-docs.png" align="right" width="45%" style="padding: 15px;" /></p>I was looking for an OpenAPI for [the Consul API](https://www.consul.io/api/index.html) to use in a project I'm working on. I have a few tricks for finding OpenAPI out in the wild, which always starts with looking over at [APIs.guru](https://apis.guru/), then secondarily Githubbing it (are we to verb status yet?). From a search on Github [I came across an issue on the Github repo for Hashicorp's Consul](https://github.com/hashicorp/consul/issues/555), which asked for "improved API documentation", a Hashicorp employee ultimately responded with "we just finished a revamp of the API docs and we don't have plans to support Swagger at this time.". Highlighting the continued misconception of what is "OpenAPI", what it is used for, and how important it can be to not just providing an API, but also consuming it.

First things first. Swagger is now [OpenAPI](https://github.com/OAI/OpenAPI-Specification) (has been for a while), an API specification format that is in [the Open API Initiative (OAI)](https://www.openapis.org/), which is part of the Linux Foundation. Swagger is proprietary tooling for building with the OpenAPI specification. It's an unfortunate and confusing situation that arose out of the move to the Open API Initiative, but it is one we need to move beyond, so you will find me correcting folks more often on this subject.

Next, let's look at the consumer question, asking for "improved API documentation". OpenAPI (fka Swagger) is much more than documentation. I understand this position as much of the value it delivers to the API consumer is often the things we associate with documentation delivering. It teaches us about the surface area of an API, detailing the authentication, request, and response structure. However, OpenAPI does this in a machine readable way that allows us to take the definition with us, load it up in other tooling like Postman, as well as use to autogenerate code, tests, monitors, and many other time saving elements when we are working to integrate with an API. Lesson for the API consumers here is that OpenAPI (fka Swagger) is much, much, more than just documentation.

Then, let's look at it from the provider side. Looks like you just revamped your API documentation, without much review of the state of things when it comes to API documentation. Without being too snarky, after learning more about the design of your API, I'm guessing you didn't look at the state of things when it comes to API design either. My objective is to not shame you for poor API design and documentation practices, just to point out you are not picking your head up and looking around much when you developed a public facing API, that many "other" people will be consuming. It is precisely the time you should be picking up your head and looking around. Lesson for the API provider her is that OpenAPI (fka Swagger) is much, much, more than just documentation.

OpenAPI (fka Swagger) is much, much, more than just documentation! Instead of me being able to fork an OpenAPI definition and share with my team members, allowing me to drive interactive documentation within our project portal, empower each team member to import the definition and getting up and running in Postman, I'm spending a couple of hours creating an OpenAPI definition for YOUR API. Once done I will have the benefits for my team that I'm seeking, but I shouldn't have to do this. As an API provider, Consul should provide us consumers with a machine readable definition of the entire surface area of the API. Not just static documentation (that are incomplete). Please API providers, take the time to look up and study the space a little more when you are designing your APIs, and learn from others are doing when it come to delivering API resources. If you do, you'll be much happier for it, and I'm guessing your API consumers will be as well!
