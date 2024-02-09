---
published: true
layout: post
title: 'Titles, Summaries, Descriptions, and Tags For APIs.json and OpenAPI'
image: https://kinlane-productions2.s3.amazonaws.com/algorotoscope-master/every-sunday-morning-docks-oakland-3.jpeg
author:
    name: kinlane
tags:
- OpenAPI
- Titles
- Summaries
- APIs.json
- Descriptions
- Tags
- Metadata
---
I can’t stress enough the importance of providing well thought out and useful titles, summaries, descriptions, and tags for your APIs, taking full advantage of APIs.json and OpenAPI capabilities. I am sorry, but after profiling a [couple hundred APIs (recently)](https://github.com/apis-json/artisanal/tree/main), and many thousands more over the years, I just don’t understand why API producers phone it in when it comes to providing this vital metadata. If you want to be successful with your API, and be successful with AI, you are going to need to have this meta data present, otherwise your business will always be operating slower and with more friction than is needed. 

I know. AI is going to solve this for us. It will generate the metadata. It will write descriptions and tag our APIs. Maybe. But, after getting to know [32 Twilio](https://github.com/apis-json/artisanal/blob/main/apis/twilio/apis.yml), [49 Stripe](https://github.com/apis-json/artisanal/blob/main/apis/stripe/apis.yml), and [10 OpenAI APIs](https://github.com/apis-json/artisanal/blob/main/apis/openai/apis.yml) intimately, I just don’t think AI will follow all of the nuance and abstractions present across the surface area of these APIs. A lack of desire to do this hard work is why we don’t have a suitable set of API discovery solutions available today. Properly defining, describing, documenting, and tagging your APIs takes investment. Doing this coherently across large numbers of APIs delivered across many teams, takes investment and coordination.

I just wrote a script that spiders Stripe, Twilio, OpenAI, and the 70+ API providers and generated an APIs.json collection for each tag that was applied. I am building a rich hand-crafted index of APIs for APIs.io. I am accomplishing this by publishing APIs.json and supporting OpenAPI to a GitHub repository I am calling “Artisanal”. Once I hand-craft an APIs.json for each API, I work to discover or generate an OpenAPI, or suite of OpenAPI for each one. Then I do the hard work to fine tune the title, summaries, descriptions, and tags for the overall API provider, but also each individual API, and down to the API operation level, using APIs.json and OpenAPI properties. This meta data gives me what I need to provide a rich API search over at APIs.io, and is work that I shouldn’t have to be doing in the first place.

I just don’t understand why companies insist on producing API products and not want to properly inventory and provide labels for them. Most people just do not see APIs as a product. Most people just do not see APIs. Despite APIs playing such a central role in our daily lives, they just aren’t seen, tangible, or discoverable. Sadly the API narrative coming out of many API providers sounds like a mix of incoherent words, acronyms, and CRUD grunts and groans. The APIs that are able to tell a coherent story are the ones that get adopted. They make sense. I have tools that distill down APIs.json and OpenAPI down into simple outlines and other types of visualizations like tag clouds, subway maps, and workflows. This helps me see the story present within each API. This helps me see each chapter in the story. Which also helps me understand how you can tell stories across API providers, grouping by tag, industry, workflows, and other bounded contexts.