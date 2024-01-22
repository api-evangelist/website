---
published: true
layout: post
title: 'Operational API Rules Using APIs.json'
image: https://kinlane-productions2.s3.amazonaws.com/algorotoscope-master/every-sunday-morning-plumbing-water-agriculture.jpeg
author:
    name: kinlane
tags:
- Governance
- Spectral
- OpenAPI
- APIs.json
---
I have been immersed in the creation of [APIs.json for many of the top APIs out there](https://github.com/apis-json/artisanal), including [Twilio](https://github.com/apis-json/artisanal/blob/main/apis/twilio.json) and [Stripe](https://github.com/apis-json/artisanal/blob/main/apis/stripe.json). These APIs are held up as an example for how we should be doing APIs. I wanted to understand this more, so I spent a couple of weeks exploring the APIs.json, and OpenAPIs for 49 Stripe, and 32 Twilio APIs. There is no better way to get to know an API provider than crafting an APIs.json for their operations, and there is no better way to get to know their individual APIs than doing the work to refine, polish, and augment their OpenAPI. Luckily Stripe and Twilio maintain their own OpenAPIs, but as I’ve seen across other providers, they go about it in different ways, leaving some work before you can rate each API provider using a common set of rules.

First, I created APIs.json indexes for both Stripe and Twilio. These index the general details for the entity behind each suite of APIs, but also the common properties like signup, blogs, and terms of service in place to support all APIs. Then I get to work creating APIs.json entries for each individual API. I didn’t get them all, but profiling [49 Stripe](https://github.com/api-search/explore/tree/main/_apis/stripe/properties) and [32 Twilio APIs](https://github.com/api-search/explore/tree/main/_apis/twilio/properties) takes time. But it is worth it. First Stripe opts to provide one massive OpenAPI for their APIs, but thankfully Twilio has already broken their APIs into very micro OpenAPIs. I like this. I ended up writing a custom tool which does it for APIs so that I can “explode” Stripe’s API into micro OpenAPI. Once you have a name, description, tags, docs, and OpenAPI for each individual API, you really begin to see the potential of APIs.json and OpenAPI together.

After profiling Stripe and Twilio I found these common properties across them like documentation, OpenAPI, authentication, sign up, login, about, sdk, plans, status page, change log, blog, privacy policy, and terms of service. There are more unique ones for each API provider, but I wanted to start with the basics. Once I had each of them profiled I got to work creating Spectral rules for the core APIs.json info, but then also all of the common properties in use across each API provider. This way I can lint Stripe and Twilio’s APIs, but also all of the other APIs.json I have defined for APIs.io. When I encounter new properties I will just add a new Spectral rule for it, so I can quickly build a vocabulary for the common API building blocks in use across API providers. It doesn’t take much to add new rules, and expand their vocabulary to understand all of the different property types. The work comes in creating new APIs.json for API providers. Something I wish API providers would do, but  until that happens I am doing the work.

I consider these rules operational level rules. They are different from the Spectral rules I use to lint and rate the surface area of Apis using their OpenAPI. My intent is to zoom out from each API and look at the operations round them. identifying the common building blocks and then developing rules to automate the profiling of other API providers. These rules will help me scale the profiling of API providers after I produce an APIs.json for them, and provide me the rules, ratings, and points I am using in the APIs.io API ratings engine. Due to the format of APis.json it is pretty straightforward to create Spectral rules for other properties, with them looking something like this:

```
  apis-json-v15-apis-properties-documentation:
    description: API Properties Documentation
    message: There is a documentation property.
    severity: info
    given: 
    
      - '$.apis.*.properties.*'
      - '$.common.*'
      
    then:

      - field: type
        function: pattern
        functionOptions:
          notMatch: "\\b(documentation|Documentation)\\b"   

      - field: url
        function: pattern
        functionOptions:
          match: "^((http|https)://)[-a-zA-Z0-9@:%._\\+~#?&//=]{2,256}\\.[a-z]{2,6}\\b([-a-zA-Z0-9@:%._\\+~#?&//=]*)$"    

```

I am excited about expanding governance beyond just the design of APIs using Spectral and OpenAPI, by applying Spectral to AsyncAPI and GraphQL, but I am even more excited by expanding governance beyond the APIs, as this is where most of the issues actually lie. The issues we are uncovering in the design of our APIs are often symptoms of operational level problems. I want to begin developing a vocabulary for talking about these problems. I have spent years showcasing the common building blocks of our API operations using APIs.json. These rules are allowing me to scale how I profile APIs and establish references for what the common building blocks for API operations across leading API providers and the industries they operate in. Next, I would like to find a way to do the same but for common internal building blocks—-the trick is, how do you map this much more obfuscated API landscape.