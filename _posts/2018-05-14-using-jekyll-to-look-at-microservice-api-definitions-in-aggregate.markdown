---
published: true
layout: post
title: Using Jekyll To Look At Microservice API Definitions In Aggregate
date: 2018-05-14T11:00:00.000Z
tags:
  - API Evangelist
  - Microservices
  - Design
  - Governance
  - Github
  - Jekyll
image: >-
  https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories/kin-mountain_dali_three.jpg
---
<p><img src="{{ page.image }}" width="45%" align="right" style="padding: 15px;" /></p>I've been evaluating microservices at scale, using their OpenAPI definitions to provide API design guidance to each team using Github. I just finished a round of work where I took 20 microservices, evaluated each OpenAPI definition individually, and made design suggestions via an updated OpenAPI definition that I submitted as a Github issue. I was going to submit as a pull request, but I really want the API design guidance to be a suggestions, as well as a learning experience, so I didn't want them to feel like they had to merge all my suggestions.

After going through all 20 OpenAPI definitions, I took all of them and dumped them into a single local repository where I was running Jekyll via localhost. Then using Liquid I created a handful of web pages for looking at the APIs across all microservices in a single page--publishing two separate reports:

- **API Paths** - An alphabetical list of the APIs for all 20 services, listing the paths, verbs, parameters, and headers in a single bulleted list for evaluation.
- **API Schema** - An alphabetical list of the APIs for all 20 services, listing the schema definitions, properties, descriptions, and types in a single bulleted list for evaluation.

While each service lives in its own Github repository, and operates independently of each other, I wanted to see them all together, to be able to evaluate their purpose and design patterns from the 100K level. I wanted to see if there was any redundancy in purpose, and if any services overlapped in functionality, as well as trying to see the potential when all API resources were laid out on a single page. It can be hard to see the forest for the trees when working with microservices, and publishing everything as a single document helps flatten things out, and is the equivalent of climbing to the top of the local mountain to get a better view of things.

Jekyll makes this process pretty easy to do by dumping all OpenAPI definitions into a single collection, which I can then navigate easily using Liquid on a single HTML page. Providing a comprehensive report of the functionality across all microservices. I am calling this my microservices monolith report, as it kind of reassembles all the individual microservices into a single view, letting me see the collective functionality available across the project. I'm currently evaluating these service from an API governance perspective, but at a later date I will be taking a look from the API integration perspective, and trying to understand if the services will work in concert to help deliver on a specific application objective.
