---
published: true
layout: post
title: 'Mapping API Experiences to API Rules Using API Policies'
tags:
  - Experiences
  - Rules
  - Policies
image: https://kinlane-productions2.s3.amazonaws.com/algorotoscope-master/birth-of-a-nation-docks-far-way.jpeg
---
I am developing the experience filter for [my Just-in-Time API Guidance kiosk](https://apievangelist.com/2024/10/21/my-just-in-time-api-guidance-kiosk/), allowing teams who are producing or consuming APIs to filter API governance (guidance) rules by experience. To define my experiences I had reverse engineered what I considered to be the baseline of Spectral rules for an HTTP API. There are more rules needed, but this was my baseline. The role of the API policy in this situation is to help me align the technical with business outcomes, but I wanted to start where the current narrative operates—-which is focused on linting the technical details of a technical spec (OpenAPI).

The experiences (top level bullet) and policies (second level bullet) listed below represent the work I need to do when it comes to powering my Just-in-Time API Guidance kiosk filtering mechanism, but it is also the hard work I am doing to map the business side of API governance using strategies and experience that are mapped to the technical rules using policies. This work is hard. Really hard as a technologist and I invite any product managers to sit down for a conversation to help me think through. 

 - Access
    - Login
    - Authentication
    - Privacy Policy
    - Governance
    - Standards
 - Alignment
    - Metadata
    - Use Cases
    - Versioning
    - Support
    - Governance
    - Standards
 - Change
    - Use Cases
    - Change Log
    - Road Map
    - Versioning
    - Support
    - Terms of Service
    - Licensing
    - Governance
    - Standards
 - Communication
    - Metadata
    - Use Cases
    - Versioning
    - Support
    - Governance
    - Standards
 - Consistency
    - Use Cases
    - Authentication
    - Versioning
    - Support
    - Licensing
    - Governance
    - Standards
 - Products
    - Metadata
    - Plans
    - Rate Limits
    - Feedback
 - Discovery
    - Metadata
    - API Metadata
    - Use Cases
    - Support
    - Governance
    - Standards
 - Legal
    - Terms of Service
    - Privacy Policy
    - Licensing
    - Governance
    - Standards
 - Onboarding
    - Metadata
    - API Metadata
    - Use Cases
    - Login
    - Authentication
    - Licensing
    - Governance
    - Standards
 - Quality
    - Testing
    - Versioning
    - Support
    - Privacy Policy
    - Governance
    - Standards
 - Reliability
    - Testing
    - Versioning
    - Support
    - Privacy Policy
    - Governance
    - Standards
 - Money
    - Plans
    - Usage
    - Invoicing
 - Security
    - Authentication
    - Governance
    - Standards
 - Simplicity
    - Use Cases
    - Support
    - Governance
    - Standards

I am negotiating with myself regarding what should be present in my Just-in-Time API Guidance kiosk filtering mechanism. Like other areas of my work, that list is long. Too long. I need to keep distilling. I think I’ll just allow filtering by experience (top level bullet) for now, but the policy (second level) is actually how I map it to the rules you will see applied to any APIs.json or OpenAPI the rules are being applied. So, I need to keep this layer visible for myself (and a few others), so that it can continue to be dialed in. I will think about how to make it visible in the background, but not front and center for filtering-—helping keep things simple.

Quality and reliability looks redundant to me. I’ll likely combine. I need to just get in place and then apply to several hundred APIs to see how well it all stands up when it comes to enabling me to do the work. OpenAPI and all it's policies is missing here. I will develop some experience-based reporting to help me validate this outline, but it is good enough for now. I am curious to see how each top-level experience area filters the Spectral rules in the kiosk. I think I will learn a lot just by applying and then come back around for another set of changes. I also have a lot of work to do on the strategy to policy link, which is meant to speak to leadership—providing another abstraction layer on top of the technical details governed by rules. More to come...