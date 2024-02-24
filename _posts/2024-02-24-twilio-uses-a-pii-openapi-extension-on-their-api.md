---
published: true
layout: post
title: 'Twilio Uses A PII OpenAPI Extension on Their API'
image: https://kinlane-productions2.s3.amazonaws.com/algorotoscope-master/gone-with-the-wind-cell-tower-close-2.jpeg
author:
    name: kinlane
tags:
- PII
- Personal Identifiable Information
- Privacy
- GDPR
---
I have been immersed in the [profiling of the Twilio API](https://github.com/apis-json/artisanal/blob/main/apis/twilio/apis.yml), and as with most of my work, there are stories in the cracks of this profiling. Twilio maintains their own OpenAPI for their APIs, which I prefer to having to create myself. I’d like it if API producers would maintain their own OpenAPI and APIs.json, but I will take whatever I can get. I learn a lot from API producers when they maintain their own OpenAPI, but also when they extend OpenAPI like Twilio does.

Through the 30+ OpenAPI from Twilio you’ll find an x-twilio OpenAPI extension namespace, and within this extended layer of the Twilio APIs they inject in a Personal Identifiable Information, or PII property:
```
x-twilio:
  pii:
    handling: standard
    deleteSla: 0
```
I will have to do more research, and ping them with some questions about how it gets used, but I found something worth noting here in the API Evangelist notebook.  The property gets applied to different properties within the requests and responses of Twilio APIs, helping Twilio understand where PII exists across their infrastructure. [I did an interview with former Twilio executive Peter Shafton](https://www.youtube.com/watch?v=Ai8iF7myYmk) who implemented the system-—he talks a little about how they rolled it out in response to GDPR, and other privacy regulatory concerns.

I am going to add it to my list of OpenAPI extensions, but also consider how PII scanning could be done for any API using an APIs.json overlay. I am using a new property for overlays we are adding into the [next 0.17 version of APIs.json](https://apisjson.org/2024/02/24/a-proposal-for-apis-json-version-017/) to overlay metadata, ratings, SDKs, and now potentially PII related services on top of APIs defined using APIs.json. I think helping enterprises scan their APIs, and flag PII using APIs.json overlays is a good way to help think about this at scale, and something multiple API service providers could step up and do to satisfy the growing need for compliance.