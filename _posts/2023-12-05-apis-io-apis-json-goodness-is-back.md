---
published: true
layout: post
title: 'APIs.io APIs.json Goodness is Back'
image: https://developer.apis.io/images/apis-io.jpg
author:
    name: kinlane
tags:
- API
- Search
---
Steve Willmott came to me asking what we should do with the [APIs.io](https://apis.io) search engine. I don’t have much interest in developing tooling these days, but I am interested in hardening and moving forward our API discovery format [APIs.json](https://apis.json). Regardless, to really push forward APIs.json I need to push forward the concept of API discovery, and this is what APIs.io is all about. So, to help me move APIs.json forward I did a round of investment in APIs.io with Steve to see what was possible, but what was needed.

## The APIs.json Specification
APIs.json is a specification format for defining your API operations, allowing you to maintain a machine-readable index of your public or private API landscape. The specification was created in 2014, and is something we have moved forward incrementally over the years, but have recently found more energy for lately as the API landscape continues to expand.

-  **Specification** ([Website](https://apisjson.org/)) - The current JSON or YAML format you can put into any well-known location.
-  **Builder** ([Website](http://builder.apisyaml.org/)) - A form for building APIs.json files quickly using a simple single page application.
-  **Artisanal** ([Repo](https://github.com/apis-json/artisanal)) - A growing number of hand-crafted artisanal APIs.json for top API providers today.

This work on the APIs.json specification is important. Code tends to be ephemeral in my experience, and the specifications are what matter over any specific open-source or code implementation that may come or go over the years, however tooling are also essential for the adoption of the specification, so we can’t just stop there.

## APIs Powering APIs.io
APIs.io is primarily just an API, or more accurately, a suite of APIs. Because any honest API specification, service, and tooling should be API-first, APIs.io is API-first. APIs.io is powered by ten separate APIs that all work in concert to help solve the API discovery across the realm of public APIs. These APIs all live in their own repositories, with their own documentation, and other resources, making for a buffet of API discovery solutions.

-  **Engine** ([Documentation](https://engine-docs.apis.io/))) ([Repo](https://github.com/api-search/engine-api)) - The API that actually pulls and processes the APIs.json files and the APIs they contain.
-  **Rules** ([Documentation](https://rules-docs.apis.io/))) ([Repo](https://github.com/api-search/rules-api)) - A collection of YAML Spectral rules that identify healthy APIs.json and OpenAPI patterns.
-  **Ratings** ([Documentation](https://ratings-docs.apis.io/))) ([Repo](https://github.com/api-search/ratings-api)) - Apply rules and other criteria to APIs.json and and OpenAPI to rate on overall quality.
-  **Linter** ([Documentation](https://linter-docs.apis.io/))) ([Repo](https://github.com/api-search/linter-api)) - The API that takes the rules, applies them to APIs.json and OpenAPI, returning results.
-  **Maintainers** ([Documentation](https://maintainers-docs.apis.io/))) ([Repo](https://github.com/api-search/maintainers-api)) - An API for managing the maintainers that are publishing the different APIs.json.
-  **Properties** ([Documentation](https://properties-docs.apis.io/))) ([Repo](https://github.com/api-search/properties-api)) - Another API for managing all of the API and common properties in each APIs.json.
-  **Tags** ([Documentation](https://tags-docs.apis.io/))) ([Repo](https://github.com/api-search/tags-api)) - The API for managing, enhancing, and making sense of the tags being applied to APis.json.
-  **Publishing** ([Documentation](https://publishing-docs.apis.io/))) ([Repo](https://github.com/api-search/publishing-api)) - An API for publishing API indexes to static single page applications hosted on GitHub.
-  **Search** ([Documentation](https://search-docs.apis.io/)) ([Repo](https://github.com/api-search/search-api)) - The API that actually provides a search on top of all of the APIs in which the engine indexes.
-  **Authentication** ([Documentation](https://auth-docs.apis.io/)) ([Repo](https://github.com/api-search/authentication-api)) - An API for authentication and generating a token so you can use the APIs.io API.

These are the APIs that power the APIs.io search engine, pulling, rating, refining, and publishing the APIs using the APIs.json format. While still in beta, the APIs are openly licensed, and provide a modular approach to not just building, but also adopting and putting the APIs.io search to work for any API search engine. The goal is to eventually provide a suite of implementations using the APIs.json format that anyone can choose from to solve API discovery in their way.

## Supporting Sites
When it comes to finding APIs, we needed an API search engine that humans can use on top of the suite of APIs made available. To support the discovery of APIs, as well as the evolution of the API search, we’ve published a website, developer portal, and a simple administrative website to help manage things. These are the more visible aspects of the APIs.io search engine, but they are just one possible approach to how we can solve API discovery.

-  **Website** ([Site](https://apis.io/)) ([Repo](https://github.com/api-search/web-site)) - A simple static website that is hosted using Jekyll on GitHub pages, providing a way to discovery APIs.
-  **Developer Portal** ([Site](https://developer.apis.io/)) ([Repo](https://github.com/api-search/developer-portal)) - The developer portal that provides access to the suite of APIs that are powering APIs.io.
-  **Administration** ([Site](https://admin.apis.io/)) ([Repo](https://github.com/api-search/admin)) - A simple administrative site for making common API calls, as well as refining APIs in the search.

These websites make the APIs indexed using the APIs.io search discoverable. They also are designed to demonstrate how to operate your API with our own public developer portal for the APIs.io API, with supporting APIs.json. The website and developer portal are designed to work together to not just make APIs discoverable, but also help make APIs more discoverable through better defined API operations and supporting APIs.json indexes.

## The Discussion
APIs.io is a work in progress, and open community affair. The entire website is managed via GitHub out in the open, showing our work as we go along, while also encouraging feedback and contribution from the community. Our goal is to keep iterating on the APIs.json specification, as well as the APIs.io websites and APIs out in the open based upon feedback from the community who is using them.

-  **Discussions** ([Forum](https://github.com/orgs/api-search/projects/1/views/1)) - Where you can find discussions about creating APIs.json for specific APIs, as well as discuss the APIs.io project.
-  **Project** ([Kanban](https://github.com/orgs/api-search/projects/1/views/1)) - The kanban board where we are adding, moving forward, and completing a variety of tasks across the APIs.io project.

We aren’t adding too many new features until we hear from more of the community about what API discovery means to them, and what they are looking for when searching for private and public APIs. We are keeping the APIs and websites very modular so that they can be rewritten to easily meet the needs of consumers, encouraging new features to be delivered in a modular API-first way, and helping provide all of the Lego building blocks we need to help with API discovery.

## What is Next?
The work has only begun. We want to keep adding APIs, by both creating more APIs.json, but also encouraging API producers to maintain them on their own. We are talking to more API service providers to support APIs.json like SwaggerHub does in their API. We’d like to keep improving the search and the rating system behind the engine-—what is there is just the first version, and something that will only get better. We just need the community’s help to define what matters most when it comes to search and a ratings system.

Alongside making APIs.io the best search engine possible, we are also exploring what an API search engine looks like within the enterprise. This is where an API discovery solution can have the greatest impact. However, providing a simple, yet high quality index of public APIs is where we are focused today, and would love to hear from you about what you need when it comes to API discovery. Googling for APIs is the most common approach to discovering APIs, but we are convinced that this will prove inadequate as we move from depending on a handful of APIs to needing hundreds or thousands of Apis to power our businesses. We feel that APIs.io provides the seeds of a more open, distributed, and community-driven approach to solving this problem, which is one that commercial API service providers have been unable to solve for over a decade.