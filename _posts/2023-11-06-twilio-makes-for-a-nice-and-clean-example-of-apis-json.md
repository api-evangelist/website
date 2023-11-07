---
published: true
layout: post
title: 'Twilio Makes for a Nice and Clean Example of APIs.json'
image: https://s3.amazonaws.com/kinlane-productions2/algorotoscope-master/norman-rockwell-ruby-bridges-bright-light-bulb.jpg
author:
    name: kinlane
tags:
- Discovery
- SMS
- Email
- Twilio
- APIs.json
---
You really can’t find a better example of APIs.json, then the one for Twilio. Twilio doesn’t have their own official APIs.json (yet), but I created one that I think really shows the strength of the API discovery format. I still have more work to do, but this Twilio APIs.json shows how the format can be used to index an API operation, while revealing individual human and machine readable properties of multiple APIs, as well as a common set of properties across all APIs--this version of my APIs.json for Twilio covers six of their APIs:

- Video
- Messaging
- Email
- Accounts
- Programmable Voice
- Identity and Verification

What I like is that each individual API has a property for human-readable documentation, as well as a property for the machine-readable OpenAPI, and the essential building blocks of an public API are defined as common properties shared by all APIs. 

- Sign-Up
- About
- Support
- SDKs
- Status
- Change Log
- Blog
- Privacy
- Terms of Service

Twilio still has other building blocks I want to index as part of this APIs.json, but I wanted to start somewhere. Ideally Twilio would manage their own index, but create one provides me with a good opportunity for pushing the APIs.json spec forward while also learning about how Twilio does what they do--here is the YAML edition of the APIs.json format I have right now.

```
name: Twilio
description: "We are a software company that strengthens businesses by unifying their
  data to build insightful paths to customers, so they are smarter with every interaction
  and able to outmaneuver their competition."
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
url: https://www.twilio.com/en-us

created: 2023/9/25
modified: 2023/9/26
specificationVersion: '0.16'

tags:

  - SMS
  - Voice
  - Messaging
  - Identity
  - Verification

apis:

- name: Twilio Messaging API
  description: Send and receive messages via SMS, MMS, WhatsApp, Facebook Messenger,
    and more through our Messaging and Conversations APIs.
  image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
  humanURL: https://www.twilio.com/en-us/ahoy
  baseURL: https:/api.twilio.com
  tags:
    - Messaging
  properties:
    - type: X-documentation
      url: https://www.twilio.com/en-us/messaging
    - type: X-pricing
      url: https://www.twilio.com/en-us/sms/pricing/us 
    - type: X-openapi
      url: https://raw.githubusercontent.com/twilio/twilio-oai/main/spec/yaml/twilio_messaging_v1.yaml

- name: Twilio Email API
  description: Reach customers with the Twilio SendGrid Email API for reliable email
    delivery at scale.
  image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
  humanURL: https://www.twilio.com/en-us/sendgrid/email-api
  baseURL: https:/api.twilio.com
  tags:
   - Email
  properties:
    - type: X-documentation
      url: https://www.twilio.com/en-us/sendgrid/email-api
    - type: X-openapi
      url: ''

- name: Twilio Identity and Verification API
  description: Set up SMS or voice verifications to quickly authenticate users, fight
    fraud, and protect user accounts.
  image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
  humanURL: https://www.twilio.com/en-us/trusted-activation/verify
  baseURL: https:/api.twilio.com
  tags:
    - Verification
    - Identity
  properties:
    - type: X-documentation
      url: https://www.twilio.com/en-us/trusted-activation/verify
    - type: X-pricing
      url: https://www.twilio.com/en-us/verify/pricing 
    - type: X-openapi
      url: http://example.com/openapi.json

- name: Twilio Programmable Voice API
  description: Build custom voice call experiences for your applications to reach
    customers around the world.
  image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
  humanURL: https://www.twilio.com/en-us/voice
  baseURL: https:/api.twilio.com
  tags:
    - Voice
  properties:
    - type: X-documentation
      url: https://www.twilio.com/en-us/voice
    - type: X-openapi
      url: https://raw.githubusercontent.com/twilio/twilio-oai/main/spec/yaml/twilio_voice_v1.yaml

- name: Twilio Video API
  description: Twilio Video is a programmable real-time communications platform that allows you to add video chat functionality to your web, iOS, and Android applications. The platform provides APIs, SDKs, and helper tools to capture, distribute, record, and render high quality audio and video applications.
  image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
  humanURL: https://www.twilio.com/docs/video
  baseURL: https:/api.twilio.com
  tags:
    - Video
  properties:
    - type: X-documentation
      url: https://www.twilio.com/docs/video
    - type: X-openapi
      url: https://raw.githubusercontent.com/twilio/twilio-oai/main/spec/yaml/twilio_video_v1.yaml

- name: Twilio Accounts API
  description: When you first sign up with Twilio, you have just one account, your main account. But you can also create more accounts... subaccounts are useful for things like segmenting phone numbers and usage data for your customers and controlling access to data.
  image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
  humanURL: https://www.twilio.com/docs/iam/api/account
  baseURL: https:/api.twilio.com
  tags:
    - Video
  properties:
    - type: X-documentation
      url: https://www.twilio.com/docs/iam/api/account
    - type: X-openapi
      url: https://raw.githubusercontent.com/twilio/twilio-oai/main/spec/yaml/twilio_accounts_v1.yaml

# Central Properties
common:

  - type: X-signup
    url: https://www.twilio.com/try-twilio
  - type: X-about
    url: https://www.twilio.com/en-us/company
  - type: X-support
    url: https://support.twilio.com/   
  - type: X-sdks
    url: https://www.twilio.com/docs/libraries    
  - type: X-status
    url: https://status.twilio.com/   
  - type: X-change-log
    url: https://www.twilio.com/en-us/changelog     
  - type: X-blog
    url: https://www.twilio.com/blog      
  - type: X-privacy
    url: https://www.twilio.com/en-us/legal/privacy  
  - type: X-terms-of-service
    url: https://www.twilio.com/en-us/legal/tos           

maintainers:
- FN: API Evangelist
  email: info@apievangelist.com
```

I have created an APIs.json for Stripe, which I will write a separate story about, but I really like the Twilio example. I feel like their approach not only shows the strength of APIs.json, it provides a template other API producers can follow. I mean, we all have talked about and emulated Twilio over the years, but this provides a simple machine-readable blueprint that anyone can follow. For me, it really is where the bar is for any public API program, demonstrating how to organize your APIs as well as the supporting building blocks for your consumers.