---
published: true
layout: post
title: 'OpenAI Injects Code Samples Into Their OpenAPI Using An Extension'
image: https://kinlane-productions2.s3.amazonaws.com/algorotoscope-master/america-under-socialism-highway-line.jpeg
author:
    name: kinlane
tags:
- Visibility
- Tangible
- Print
- Art
---
As I was profiling the [OpenAI API](https://github.com/apis-json/artisanal/blob/main/apis/openai/apis.yml) I noticed they had vendor extensions. This is a common thing I come across while profiling APIs, so I always make sure I spend some time evaluating the approach so that I can better understand why API producers feel the need to extend the spec. Twilio and Stripe both utilize extensions that help track maturity, PII, and other details of API operations that aren’t commonly expressed as OpenAPI. I harvested the OAS extensions from the OpenAI OpenAPI (I love using those two words together), and set them aside for documents here in my API Evangelist notebook.

OpenAI adds an x-oaiMeta property to every API operation in their OpenAI, which they add code and JSON examples of the request and responses for each API, embedding what API consumers will need when putting each API operation to work. 
```
x-oaiMeta:
  name: List models
  group: models
  returns: 'A list of [model](/docs/api-reference/models/object) objects.'
  examples:
  request:
    curl: |
      curl https://api.openai.com/v1/models \
        -H "Authorization: Bearer $OPENAI_API_KEY"
    python: |
      from openai import OpenAI
      client = OpenAI()
      client.models.list()
    node.js: |-
      import OpenAI from "openai";
      const openai = new OpenAI();
      async function main() {
        const list = await openai.models.list();
        for await (const model of list) {
          console.log(model);
        }
      }
      main();
  response: |
    {
      "object": "list",
      "data": [
        {
          "id": "model-id-0",
          "object": "model",
          "created": 1686935002,
          "owned_by": "organization-owner"
        },
        {
          "id": "model-id-1",
          "object": "model",
          "created": 1686935002,
          "owned_by": "organization-owner",
        },
        {
          "id": "model-id-2",
          "object": "model",
          "created": 1686935002,
          "owned_by": "openai"
        },
      ],
      "object": "list"
    }
```
I am always interested in the reasoning behind the ways APIs extend OpenAPI. I’d say that for this use case the JSON response example should be part of the OpenAPI proper, leveraging the [example object](https://spec.openapis.org/oas/v3.1.0#example-object). But the curl and python code they include don’t have a natural home within the OpenAPI definition. I know many will cringe at the thought of publishing code samples within your JSON or YAML OpenAPI. I don’t cringe, but I feel like these things should be indexed via an [APIs.json](https://apisjson.org), and not in the OpenAPI. 

I prefer keeping OpenAPI describing the surface area of each API, possessing the technical details of requests and responses. I add an OpenAPI as a property for each API I profile in an APIs.json, and add anything else like spectral rules rating, SDKs, and other elements as properties or overlay. This approach keeps everything modular, with clear bounded context for each artifact indexed for an API. This allows me to [index OpenAPI, AsyncAPI, JSON Schema, as well as the SDKs, Postman Collections, and other elements separate, but all indexed together](https://apievangelist.com/2019/10/31/a-diverse-api-json-index-example-for-slack/). 

Regardless of my opinions and bias towards APIs.json, I genuinely find their approach to extending OpenAPI interesting. Many people hit a wall with OpenAPI and declare the spec not suitable for their needs. I encourage extending the spec, and if you feel your usage is something others might benefit from, you can submit as a proposal to the OpenAPI spec. If not, just extend away and keep it doing what you need within your custom applications, pipelines, and the other areas of your operations.