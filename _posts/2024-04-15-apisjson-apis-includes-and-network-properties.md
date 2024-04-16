---
published: true
layout: post
title: 'APIs.json APIs, Includes, and Network Properties'
image: https://kinlane-productions2.s3.amazonaws.com/algorotoscope-master/gone-with-the-wind-radio-antanae.jpeg
author:
    name: kinlane
tags:
- APIs.json
- Search
- Discovery
- Federated
---
Since the beginning of the specification, [APIs.json](https://apisjson.org/) has had an “apis” property as well as an “includes” properties, providing a way to immediately index your APIs, or “include” a reference to other APIs.json indexes. The APIs.json specification is designed to be flexible in how you can define and organize your collections, but as I spend more time profiling and indexing APIs, I am finding a need to further expand on how APIs.json indexes work together in concert to provide a more federated approach to API discovery.

## APIs.json APIs Property
The top level apis property for APIs.json is where you index your immediate APIs and publish in the index of your developer portal, where you might have 1-25 APIs indexed as part of your public operation—-maybe a few more ([I stuffed 360+ in AWS](https://github.com/api-search/cloud/blob/main/_apis/amazon-web-services/apis.md)). I am thinking that depending on the size of your APIs, that 25 is going to be my recommended limit. Of course you can index way more, but why? It really depends on who your audience is and what information you are looking to provide.

```
specificationVersion: '0.17'
aid: stripe
name: Stripe
description: >-
  Millions of companies of all sizes use Stripe online and in person to accept
  payments, send payouts, automate financial processes, and ultimately grow
  revenue.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
url: https://artisinal.apisjson.org/apis/stripe/apis.yml
created: 2023/10/06
modified: '2024-03-09'
tags: []
apis:
  - aid: stripe:stripe-balance-api
    name: Stripe Balance API
    description: >-
      This is an object representing your Stripe balance. You can retrieve it to
      see the balance currently on your Stripe account. You can also retrieve
      the balance history, which contains a list of transactions that
      contributed to the balance (charges, payouts, and so forth).
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://stripe.com/docs/api/balance
    baseURL: https://api.stripe.com
    tags: []
    properties:
      - type: Documentation
        url: https://stripe.com/docs/api/balance
      - type: OpenAPI
        url: properties/balance-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/balance-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/balance-openapi-api-evangelist-ratings.yml
common:
  - type: Sign Up
    url: https://dashboard.stripe.com/register
  - type: Authentication
    url: https://stripe.com/docs/api/authentication
  - type: Blog
    url: https://stripe.com/blog
  - type: Status
    url: https://status.stripe.com/
  - type: Change Log
    url: https://stripe.com/docs/upgrades#api-versions
  - type: Terms of Service
    url: https://stripe.com/privacy
  - type: Support
    url: https://support.stripe.com/
overlays:
  - type: APIs.io Search
    url: overlays/apis-io-search.yml
  - type: API Evangelist Ratings
    url: overlays/apis-io-search.yml
maintainers:
  - FN: APIs.json
    email: info@apis.io
```

After breaking up APIs like AWS, Stripe, and others into many individual APIs indexed using the APIs.json apis property. It is the quickest way to organize them, but once I get them all tagged, I begin to think about other bounded contexts that I could also start breaking them down on. AWS has some pretty clear groupings, but Stripe and others take more domain expertise to think about to break down. I am opting to aggregate many APIs using the apis object before I begin to shard them even further—I will do more of that down the road.

## APIs.json Includes Property
The APIs.json includes properties is how you can begin to shard and/or stitch together many different types of APIs. For example, payments API—you can publish an APIs.json with the name of Payments, and don't have any APIs in the apis properties, and you just link to Stripe, PayPal, and other payment APIs. You could use it for lines of business or any other meaningful bounded context for an industry. 

```
specificationVersion: '0.17'
aid: payments
name: APIs.io - Payments
description: The APIs that make payments possible, as well as a number of other related
  capabilities.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
url: https://payments.apis.io/apis.json
created: 2024/04/13
modified: 2024/04/13
tags:
- Payments
includes:
- name: Adyen
  url: https://raw.githubusercontent.com/api-search/payments/main/_apis/adyen/apis.md
- name: Paypal
  url: https://raw.githubusercontent.com/api-search/payments/main/_apis/paypal/apis.md
- name: Stripe
  url: https://raw.githubusercontent.com/api-search/payments/main/_apis/stripe/apis.md
maintainers:
- FN: APIs.io
  email: info@apis.io
```

I tend to profile API providers using a single APIs.json, leveraging the apis properties, but then based upon tags, begin to shard and organize them into other more meaningful collections. I am doing this with properties like SDKs or plans and pricing pages, as well as pushing the boundaries based upon different ways I am rating APIs. The APIs.json includes property is how I am putting the federated in our approach to APis.io.

## APIs.json Network Property
We haven’t officially added this property to the APIs.json specification, but I’ll craft up a proposal to add with version .18 of the specification. I needed this network property to further “network” the different search nodes I was deploying as part of sharding my APIs.json profiling work. I needed a way to articulate the network of APIs I am managing, helping me power my search engine across the growing number of Apis I was profiling.

```
---
specificationVersion: '0.18'
aid: explore
name: APIs.io
description: The first API search engine.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
url: https://explore.apis.io/apis.json
created: 2024/04/13
modified: 2024/04/13
tags:
- APIs
- Search
network:
- name: Artificial Intelligence
  url: https://ai.apis.io/apis.json
- name: Banking
  url: https://banking.apis.io/apis.json
- name: Cloud
  url: https://cloud.apis.io/apis.json
- name: Code
  url: https://code.apis.io/apis.json
- name: Commerce
  url: https://commerce.apis.io/apis.json
- name: Documents
  url: https://documents.apis.io/apis.json
- name: Financial
  url: https://financial.apis.io/apis.json
- name: Infrastructure
  url: https://infrastructure.apis.io/apis.json
- name: Messaging
  url: https://messaging.apis.io/apis.json
- name: Payments
  url: https://payments.apis.io/apis.json
- name: Travel
  url: https://travel.apis.io/apis.json
- name: Videos
  url: https://videos.apis.io/apis.json
maintainers:
- FN: APIs.io
  email: info@apis.io
```

I am going to stress test this properly over the next couple of weeks. I am thinking that I am going to need to add a tags property to both the includes and network property so I can further organize the networks into groups. IDK. I might just get more strict with how I roll out and group my API search nodes. It really depends on the tags accumulated for the APIs profiling, and how they cluster together as I continue the work.

## Federating and Localizing
This round of [APIs.io exploration](https://explore.apis.io/) is all about federating and localizing the search engine, demonstrating the potential of the APIs.json format. I am working hard to find the sweet spot when it comes to working with many different APIs. One of the keys to success I am finding is reducing the cognitive load with anything I am doing across the hundreds, and now thousands of APIs I am profiling for APis.io. My approach to localizing and federating APIs as part of APIs.io is also how I’d recommend larger enterprises approach their own API discovery internally. Keeping things small and manageable along lines of business, team boundaries, work streams, and other organically forming bounded contexts. 

I have probably another fifteen search nodes to deploy using the APIs I have already profiled in my Artisanal work. I just wanted to see if it was possible to shard and network things, and produce a federated search mechanism. So far, so good. Now I just want to pile a bunch more APIs on top of it. I need to share individual APIs like GitLab, but also additional dimensions of API discovery like shipping, government, and the top categories you’d expect with an API search engine. Next, I am looking to pile on about 2-3K APIs across 25+ search nodes, with a single federated search, but also a more powerful API-driven cloud search after I ingest all of my nodes into a database. Then I’ll document my network and search websites behind APIs.io to help make them more forkable and usable anywhere GItHub pages or even Jekyll will run.