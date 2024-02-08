---
published: true
layout: post
title: 'Adding OpenAI Plugin Manifest to the APIs.json Properties'
image: https://kinlane-productions2.s3.amazonaws.com/algorotoscope-master/bf-skinner-old-pay-phone.jpg
author:
    name: kinlane
tags:
- Methods
- PUT
- Design
- REST
---
I love the meta dimensions of my API work. I am [profiling the OpenAPI](https://github.com/apis-json/artisanal/blob/main/apis/openai/apis.yml) for inclusion into the APIs.io search engine. To do this I create an APIs.json and add all of the properties of the OpenAI API operations to it. This includes things like getting started, docs, their OpenAPI, terms of service, and other common building blocks. After landing on the [OpenAI plugin page](https://platform.openai.com/docs/plugins/getting-started) I decided that I would also add the OpenAI plugin manifest as an APIs.json property type, so that it can be included for any API—the OpenAI manifest looks like this.
```
{
    "schema_version": "v1",
    "name_for_human": "TODO List",
    "name_for_model": "todo",
    "description_for_human": "Manage your TODO list. You can add, remove and view your TODOs.",
    "description_for_model": "Help the user with managing a TODO list. You can add, remove and view your TODOs.",
    "auth": {
        "type": "none"
    },
    "api": {
        "type": "openapi",
        "url": "https://example.com/openapi.yaml"
    },
    "logo_url": "https://example.com/logo.png",
    "contact_email": "support@example.com",
    "legal_info_url": "http://www.example.com/legal"
}
```
There is some overlap between what OpenAI is indexing in their plugin manifest and what you can index with an APIs.json. Properties like OpenAPI, terms of service, and other aspects of an API can be added to your plugin manifest, providing what you need to consume an API in OpenAI. To help jump start this engagement I am going to propose the addition of a new API property type with the next release of [APIs.json](https://apisjson.org).
```
    {
    "type": "OpenAI Plugin Manifest",
    "url": "https://example.com/ai-plugin.json"
    }
```    
This APIs.json property will enable any API producer to provide a template OpenAI manifest that any consumer can use to connect your API into their OpenAI implementation using an OpenAI plugin that points to an OpenAPI for the API. Phewww!! That was a mouthful. I am interested in possibly adding this property to the APIs.json I am producing for top APIs, making it easier to put each API to work when training a model. 

There are several dimensions I am looking to shape the API to AI layer, as well as the AI to API layer of this conversation. I am adding the [rich metadata like titles, summaries, descriptions, and tags to each APIs.json](https://github.com/apis-json/artisanal/blob/main/apis/stripe/overlays/apis-io-search.yml) and the OpenAPI I am defining as part of my [APIs.json / APIs.io work](https://github.com/apis-json/artisanal). I think an OpenAI overlay to this work would add some value to the AI conversation, but I’d like to better translate my API tags into JSON-LD, ALPS, or some other semantic overlay to my index as well. We’ll see what I have time for, but I am at least identifying all of the ways I can contribute to the AI conversation in a meaningful way, without losing my soul in the shuffle.