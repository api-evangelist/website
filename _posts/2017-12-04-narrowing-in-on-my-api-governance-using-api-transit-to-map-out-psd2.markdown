---
published: true
layout: post
title: Narrowing In On My API Governance Strategy Using API Transit To Map Out PSD2
date: 2017-12-04T13:00:00.000Z
tags:
  - API Evangelist
  - API Transit
  - PSD2
  - Banking
  - Governance
image: >-
  https://s3.amazonaws.com/kinlane-productions/talks/november-2015/subway-map-15.png
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/talks/november-2015/subway-map-15.png" align="right" width="45%" style="padding: 15px;"></p>[I'm still kicking around my API Transit strategy in my head](https://apievangelist.com/2017/08/17/testing-out-the-concept-of-api-transit-instead-of-api-lifecycle/), trying to find a path forward with applying to API governance. [I started moving it forward a couple years ago as a way to map out the API lifecycle](https://apievangelist.com/2015/11/29/the-api-lifecycle-my-talk-from-defrag-and-apistrat/), but in my experience, managing APIs are rarely a linear lifecycle. I have been captivated by the potential of the subway map to help us map out, understand, and navigate complex infrastructure since I learned about [Harry Beck's approach to the London Tube map which has become the standard for quantifying transit around the globe](https://en.wikipedia.org/wiki/Tube_map). 

I am borrowing from Beck's work, but augmenting for a digital world to try and map out the API practices I study in my research of the space in a way that allow them to be explored, but also implemented, measured, and reported upon by all stakeholders involved with API operations. While I'm still pushing forward this concept in the safe space of my own API projects, I'm beginning to dabble with applying at the industry level, by applying to PSD2 banking, and seeing if I can't provide an interactive map that helps folks see, understand, and navigate what is going on when it comes to banking APIs.

An API Transit map for PSD2 would build upon the framework I have derived from my API research, applied specifically for quantifying the PSD2 world. Each of the areas of my research broken down into separate subway lines, that can be plotted along the map with relative stops along they way:

- **Definition** - Which definitions are used? Where are the OpenAPI, schema, and other relevant patterns.
- **Design** - What design patterns are in play across the API definitions, and what is the meaning behind the design of all APIs.
- **Deployment** - What does deployment look like on-premise, in the cloud, and from region to region.
- **Portals** - What is the minimum viable standard for an API portal presence with any building blocks.
- **Management** - Quantify the standard approaches to managing APIs from on-boarding to analysis and reporting.
- **Plans** - How are access tiers and plans defined, providing 3rd party access to APIs, including that of aggregators and application developers.
- **Monitoring** - What does monitoring of web APIs look like, and how is data aggregated and shared.
- **Testing** - What does testing of web APIs look like, and how is data aggregated and shared.
- **Performance** - What does performance evaluation of web APIs look like, and how is data aggregated and shared.
- **Security** - What are the security practices in place for the entire API stack?
- **Breaches** - When there is a breach, what is the protocol, and practices surrounding what should happen--where is the historical data as well.
- **Terms of Service** - What does terms of service across many APIs look like?
- **Privacy Policy** - How is privacy protected across API operations?
- **Support** - What are all the expected support channels, and where are they located?
- Road Map - What is expected, and where do we find the road map and change log for the platform?

These are just a handful of the lines I will be laying out as part of my subway map. I have others I want to add, but this provides a nice version of what I"d like to see as an API Transit map of the PSD2 universe. Each line would have numerous stops that would provide resources and potentially tooling to help educate, quantify, and walk people through each of these areas in detail, but in the context of PSD2, and the banking industry. This where I'm beginning to push the subway map context further to help make work in a virtualized world, and augmenting with some concepts I hope will add new dimensions to how we understand, and navigate our digital worlds, but using the subway map as a skeuomorph.

To help make the PSD2 landscape I'm mapping out more valuable I am playing with adding a "tour" layer, which allows me to craft tours that cover specific lines, hitting only the stops that matter, bridges multiple lines, and creates a meaningful tour for a specific audience. Here are a handful of the tours I'm planning for PSD2:

- **Introduction** - A simple introduction to the concepts at play when it comes to the PSD2 landscape.
- **Provider Training** - A detailed training walk-through for anyone looking to provide a PSD2 compliant platform.
- **Provider Certification** - A detailed walkthrough that gathers information and detail to map out, quantity, and assess a specific PSD2 API / platform.
- **Executive** - A robust walk-through of the concepts at play for an executive from the 100K view, as well as those of their own companies PSD2 certified API, and possibly those of competitors.
- **Regulator** - A comprehensive walk through the entire landscape, including what is required, as well as the certification of individual PSD2 API platforms, with real-time control dashboard.

These are just a few of the areas I'm looking to provide tours through this quantified PSD2 API Transit landscape. I am using Github to deploy, and evolve my maps, which leverages Jekyll as a Hypermedia client to deliver the API Transit experience. While each line of the API Transit map has it's own hypermedia flow for storing and experiencing each stop along the line, the tours also have its own hypermedia flows which can augment existing lines and stops, as well as inject their own text, images, audio, video, links and tooling along the way.

The result will be a single URL which anyone can land on for the PSD2 API Transit platform. You can choose from any of the pre-crafted tours, or just begin exploring each line, getting off at only the stops that interest you. Some stops will be destinations, while others will provide transfers to other lines. I'm going to be investing some cycles into my PSD2 API Transit platform over the holidays. If you have any questions, comments, input, or would like to invest in my work, please let me know. I'm always looking for feedback, as well as interested parties to help fund my work and ensure I can carve out the time to make them happen.
