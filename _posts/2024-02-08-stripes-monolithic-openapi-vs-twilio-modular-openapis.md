---
published: true
layout: post
title: 'Stripes Monolithic OpenAPI vs. Twilio Modular OpenAPIs'
image: https://kinlane-productions2.s3.amazonaws.com/algorotoscope-master/gone-with-the-wind-containers-stack.jpeg
author:
    name: kinlane
tags:
- OpenAPI
- Twilio
- Stripe
- APIs.json
- Micro
- Mono
---
I profiled [Stripe](https://github.com/apis-json/artisanal/blob/main/apis/stripe/apis.yml) and [Twilio](https://github.com/apis-json/artisanal/blob/main/apis/twilio/apis.yml) using APIs.json recently. My API profiling process requires that I get to know an API, and while Stripe and Twilio do not maintain their own APIs.json index, they both do maintain OpenAPI for their APIs-—they just do it differently from each other. Stripe chooses to use one large OpenAPI for every path and operation they provide. Twilio chose somewhere along the way to break theirs down into modular OpenAPIs. I worked with both of these companies while working at Twilio, so I have insight into the pipelines behind the generation of these OpenAPI. While I am glad both companies maintain their own OpenAPI, in my experience it just makes more sense in the long run to break your OpenAPI into modular parts, which  go a long ways to reducing the cognitive as well as the processing load involved with putting each API to work.

The [Twilio OpenAPI](https://github.com/twilio/twilio-oai) was pretty straight forward, they have everything already broken down into modular OpenAPIs. I took it a little further, breaking down a couple of the bigger ones that needed it—ending up with [32 separate OpenAPIs](https://github.com/apis-json/artisanal/tree/main/apis/twilio/properties). One thing that is difficult about breaking OpenAPIs down after they are published by producers, is it doesn’t always nicely line up with schema used across requests and responses, as well as linking to other properties of API operations like docs and other things. However, once broken up, the suite of Twilio APIs really provides a rich toolbox or resources, and capabilities that are the fundamental building blocks of modern applications.

The [Stripe OpenAPI](https://github.com/stripe/openapi) was a single massive OpenAPI. I have had a conversation with the Stripe team about the size of their OpenAPI, and there is little interest in breaking it up into modular OpenAPIs. So I did. I ended up with [49 separate OpenAPIs](https://github.com/apis-json/artisanal/tree/main/apis/stripe/properties). The mono OpenAPI was just bloated. It froze up most applications I imported it into. I get it, it is generated, and you don’t want to do the work to break up, keep organized, and iterate upon. Make your OpenAPIs useful for consumers. I get folks prefer monolithic complexity over distributed complexity, but you are just pushing the work and burden on to your consumers, and taking away from the value provided by having an OpenAPI in the first place.

I get that folks don’t want to do the work to organize their APIs. But, this is important work. This is the last mile of developer experience that will help you make your API narrative tell the story you set out to tell. Breaking up the Stripe and Twilio OpenAPIs helped me get to know the buffet of resources and capabilities they offer. It forced me to spend time thinking about each individual path and operation, but also how they potentially work in concert, or can be modularized to reduce the cognitive load for consumers. I like working with APIs at this level. I get that the suite of Twilio and Stripe APIs are delivered across many disparate teams, and each team has their own purpose and incentives, but still...it all perpetually leaves me wondering who is paying attention to the overall narrative and experience for these APIs?

When I look at the 49 Stripe, and 32 Twilio APIs I see the warehouse of their digital resources and capabilities. When these APIs are all thrown together into a single API, or lack summaries, descriptions, and tags, I see a company that doesn’t care about the organization and accessibility of its warehouses and supply chain It took me time and effort to get the two APIs.json for Stripe and Twilio organized, but now that I do I am easily able to add overlays for APIs.io, ratings from API Evangelist, and potentially JSON-LD for use in AI, or SDKs from a company like APIMATIC. It makes it much easier for me to distribute the digital resources and capabilities that Stripe and Twilio are offering into other stories, systems, and solutions. If nothing else, I learn a lot along the way.