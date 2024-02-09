---
published: true
layout: post
title: 'Breaking OpenAI OpenAPI Into 10 Separate OpenAPIs'
image: https://kinlane-productions2.s3.amazonaws.com/algorotoscope-master/america-immigration_dumping-ground-containers-white.jpg
author:
    name: kinlane
tags:
- OpenAPI
- OpenAI
- Artificial Intelligence
- APIs.json
- Micro
- Mono
---
As I [profile APIs for APIs.io using APIs.json](https://github.com/apis-json/artisanal/blob/main/apis/openai/apis.yml), I break up OpenAPIs for providers along base path lines. I prefer distributed sprawl for my [Artisanal APIs.json profiling work](https://github.com/apis-json/artisanal/tree/main). I prefer my API representations using OpenAPI to be the smallest unit possible. Like OpenAI’s own advice for crafting OpenAPI for your ChatGPT plug—it just makes sense to keep things bit-size, fast-loading, and easy to understand. OpenAI maintains their own OpenAPI, but it is just a single artifact, which I opted to break up into 10 separate OpenAPIs, indexed by a single APIs.json.

The OpenAPI provided by OpenAI for their API had ten separate base resources available for consumers to use:

- [**Assistants**](https://github.com/apis-json/artisanal/blob/main/apis/openai/properties/assistants-openapi-original.yml)
- [**Audio**](https://github.com/apis-json/artisanal/blob/main/apis/openai/properties/audio-openapi-original.yml)
- [**Chat**](https://github.com/apis-json/artisanal/blob/main/apis/openai/properties/chat-openapi-original.yml)
- [**Completions**](https://github.com/apis-json/artisanal/blob/main/apis/openai/properties/completions-openapi-original.yml)
- [**Embeddings**](https://github.com/apis-json/artisanal/blob/main/apis/openai/properties/embeddings-openapi-original.yml)
- [**Files**](https://github.com/apis-json/artisanal/blob/main/apis/openai/properties/files-openapi-original.yml)
- [**Fine Tuning**](https://github.com/apis-json/artisanal/blob/main/apis/openai/properties/fine-tuning-openapi-original.yml)
- [**Images**](https://github.com/apis-json/artisanal/blob/main/apis/openai/properties/images-openapi-original.yml)
- [**Models**](https://github.com/apis-json/artisanal/blob/main/apis/openai/properties/models-openapi-original.yml)
- [**Threads**](https://github.com/apis-json/artisanal/blob/main/apis/openai/properties/threads-openapi-original.yml)

I broke up the OpenAPI along these lines. I am still getting to know the suite of APIs from OpenAI, but I find this list of resources to be pretty intuitive, helping reduce the cognitive load associated with onboarding with OpenAI. You are still going to need to work across each of these areas, but the need will vary depending on the type of application, integration, or workflow. I like to have the OpenAPI broken down into modular services like this so I can index with a single APIs.json, but surface in many different searches via APIs.io, and workflow, tag, or industry API collections.

Next I will produce an overlay for the OpenAI APIs.json, as well as ten separate OpenAPIs, tightening up and adding to the titles, summary, descriptions, and tags. After that I will rate each individual OpenAPI as well as the overall APIs.json using my API Evangelist ratings engine I build for APIs.io. This process will help make the OpenAI more discoverable via APIs.io, but also help me better understand the surface area of all ten of the OpenAI resources, but also how they approach their overall operation and developer experience. This whole process takes me about an hour to do with an API the size of OpenAPI, but it is something I am working to keep refining and automating along the way.