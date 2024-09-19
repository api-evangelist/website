---
published: true
layout: post
title: 'Using API Policies To Align Product and Engineering as Part of API Governance'
tags:
  - Spectral
  - Rules
  - Governance
  - Linting
  - Policies
image: https://kinlane-productions2.s3.amazonaws.com/algorotoscope-master/bf-skinner-skyscraper-construction-crane-2.jpeg
---
One of the greatest challenges with API governance is aligning the product and engineering interests across every stage of the API lifecycle. API governance is heavily invested in from a engineering side of things (OpenAPI, JSON Schema, Spectral), but rarely are aligning the business side of things (Use Cases, Provenance, Education), and I am very interested in closing this gap in my API governance work moving forward. I have numerous tools in my toolbox, but one of the ways I am aligning the current engineering investment of API governance is using API policies.

An API policy is a simple human and machine readable artifact to organize the business reasoning behind any area of governance, and used to organize one or many rules that define the shape of an API governance policy. API policies are used to align engineering with product through grounding and organizing rules, but also providing an ongoing vehicle that encourages API governance teams, but also product and engineering teams producing APIs to participate in shaping API policy.

```
version: 2024-09-19
name: API Versioning
slug: api-versioning
schema: OpenAPI
image: /images/meta-data.png
description: Defining how change is managed as part of the technical contract for an API as defined using the OpenAPI specification. Change is managed using Semantic Versioning which is applied as part of the header, and not as part of the path, ensuring that API consumers can be explicit about which version of an API they are using. The version of an API is used to communicate change via the surface area of the API, but also via road map, change log, and other communication.
discussion: https://example.com/discussion
guidance: https://example.com/guidance
policies:
  - apis-json-change-log
  - apis-json-road-map
  - apis-json-versioning
rules:
  - openapi-version-semantic-info
  - openapi-version-in-path-error
  - openapi-version-in-path-info
  - openapi-version-custom-header-error
tags:
  - Contracts
  - Discovery
solutions:
  - Change
  - Communication
```

This is an example API policy for API versioning which aligns engineering with product in a handful of ways. It provides a grouping for Spectral rules, leveraging both positive and negative rules that define the patterns and anti-patterns that shape the policy. The policy should provide a simple business explanation of why versioning matters, and offers additional links that document the provenance of the discussion that led to this policy, and further guidance that helps educate the team regarding how they should apply versioning. The policy also defines the solutions this policy provides, and has other tagging to help organize, as well as other related policies that work in concert with this policy to define the larger change management strategy.

API policies allow you to group many different Spectral rules into a single business rationale for why something like versioning is being governed, expanding what is possible using a single Spectral rule, targeting many different patterns and anti-patterns that all go into defining, applying, and enforcing API governance.

## Use Semantic Versioning in OpenAPI
```
openapi-version-semantic-info:
  description: Semantic Versioning
  message: APIs MUST Use Semantic Versioning
  severity: info
  given: $.info.version
  then:
    function: pattern
    functionOptions:
      notMatch: >-
        ^(0|[1-9][0-9]*)\.(0|[1-9][0-9]*)\.(0|[1-9][0-9]*)(-(0|[1-9A-Za-z-][0-9A-Za-z-]*)(\.[0-9A-Za-z-]+)*)?(\+[0-9A-Za-z-]+(\.[0-9A-Za-z-]+)*)?$     
```
## Not Using Versioning in the Path
```
openapi-version-in-path-error:
  description: Version Path
  message: APIs MUST Use Version in Path.
  severity: error
  given: $.paths[*]~
  then:
    function: pattern
    functionOptions:
      notMatch: /((?:/)(v|version)?[0-9]{1,3}(?:/)?)/i   
```
## Using Versioning in the Path
```
openapi-version-in-path-info:
  description: Version Path
  message: APIs Uses Version in Path.
  severity: info
  given: $.paths[*]~
  then:
    function: pattern
    functionOptions:
      match: /((?:/)(v|version)?[0-9]{1,3}(?:/)?)/i                   
```
## Not Using Versioning in a Custom Header
```
openapi-version-custom-header-error:
  description: Custom Header Error
  message: APIs MUST Not Use Custom Version header
  severity: error
  given: $.components.headers
  then:
    field: X-API-Version
    function: truthy        
```

Over time we can add other rules to this to get more precise about headers that shouldn’t exist, and possibly compare versioning across multiple OpenAPI artifacts. You’ll notice I have a positive and negative rule for versioning in the path because I want to ensure teams are versioning, and be able to report on compliance—-something I may extend to Semantic Versioning and other rules. API policies give new shape and dimensions to API rules, going well beyond just linting for what developers should not do, and helping showcase and educate around what they should be doing.

Every policy provides what team members need to get up to speed on the work that went into the policy and rules for each area of API governance. The discussion link should provide all of the provenance regarding the internal and external research, discussions, meetings, and everything that went into the policy decision—plus the ability to join in and help shape and further evolve policy. API policies augment API rules with all of the business context and background of each area of API governance, which is something that can continue be aligned with product and engineering leadership over time—providing a vehicle that moves API governance forward with teams who are producing APIs involved in the process, and given a voice to change the policies and rules they don’t think are adequate or relevant.

You will also notice there is a solutions property for a policy, which can be used to roll out policies and rules applied to APIs across domains, lines of business, and teams, and report to leadership regarding how well we are doing in areas like change, communication, as well as security, performance, and other areas of friction that API governance is being brought in to provide solutions. I have around 175 policies that I use to shape almost 400 individual Spectral rules that define and automate API governance with an intent on keeping the product in alignment with engineering. There are a number of individual policies that specifically address product and engineering alignment—-things like Use Cases, but API policies in general are an important vehicle for defining where product and engineering are out of alignment--over time closing the gap that exists by applying and enforcing policies against specific APIs at different stages of the API lifecycle.