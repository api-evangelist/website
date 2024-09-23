---
published: true
layout: post
title: 'Managing An Engineering API Platform Definition'
tags:
  - APIs.json
  - Platform
  - APIs.io
  - Postman
image: https://kinlane-productions2.s3.amazonaws.com/algorotoscope-master/uncle-sam-subway-platform.jpeg
---
I use APIs.json to define the [engineering API platform for APIs.io](https://github.com/api-search/engineering-platform?tab=readme-ov-file). The machine-readable definition of the engineering platform for APIs.io provides a definition of all of the services and tooling I use to run the API search engine. A platform APIs.json differs from an index or contract in that at the APIs included are usually 3rd party, and I am using them to manually manage the deliver and sustainment of API infrastructure, and automate what I can using their APIs-—I have eleven APIs that I use to manage and automate my APIs, each defined as a separate API.

<script src="https://gist.github.com/kinlane/9b9b0547d0e23eea57e6f80512888ed5.js"></script>

You will notice that each API has a link to the documentation, OpenAPI, and Postman Collection for the API. For some of them you’ll notice I have what I consider to be Postman capability collections-—modular API capabilities that help me run and automate bits of my API infrastructure. I am busy creating new ones. Basically there is an OpenAPI and Postman Collection for each service I depend on, then I am breaking out the operations that I use regularly. Then I’ll get to work defining some workflow ones that make multiple API calls in a specific order.

You will find my engineering API platform defined across the [GitHub repository](https://github.com/api-search/engineering-platform) and [Postman workspace](https://api-evangelist.postman.co/workspace/APIs.io-Engineering-Platform~fe320942-e505-4ee8-8b7c-d72eae00d93f/overview) I use to manage the definition, but also automate around it. Most of the automation around API operations is manually right now, but once a capability or workflow gets hardened enough, I’ll fire up a Postman monitor, EasyCRON job, or bake into a GitHub Action. Right now I am just defining all of the digital resources and capabilities of my API platform as modular executable bits, and then I will work to automate what I can, but always keeping an eye on still manually running tasks via my Postman workspace—helping me keep an eye on what is happening, while still enabling to do more with less time and money spent.

The first two ways I am automating using my APIs.json engineering platform definition is to [auto generate the README of the repository I use to manage the definition](https://github.com/api-search/engineering-platform), but I am also [generating a section of all the READMEs for individual APIs I am managing as part of APIs.io](https://github.com/api-search/search-api?tab=readme-ov-file#apisio-engineering-platform). After that I will be generating the overview for the Postman workspace, and the platform page that will be part of the [APIs.io developer portal](https://developer.apis.io/). Then I am looking to automate some API governance policies using my API platform definition as a guide, seeing what other aspects of my API governance that I can put on autopilot—-being mindful to automate only things that are well-defined and make sense to automate.

Now that I have a machine readable platform definition I will also produce a business platform definition of the APIs I use to manage the business side of APIs.io. Then I will work on a visualization that lets you see and interact with your platform, going well beyond what I did with the README generation. If you are needing help in defining your API engineering or business platform, let me know how I can help. It is a great way to define the services you are using, but then break things up into more usable and automatable units of API value. Honestly, it is the only way I can run two businesses (APIs.io and API Evangelist) with minimal help from others.