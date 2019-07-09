---
published: true
layout: post
title: >-
  Google Releases a Protocol Buffer Implementation of the Fast Healthcare
  Interoperability Resources (FHIR) Standard
date: 2018-03-13T12:00:00.000Z
tags:
  - API Evangelist
  - Data
  - Healthcare
  - Definitions
  - Standards
image: 'https://s3.amazonaws.com/kinlane-productions/fhir/FHIR_logo-1080x675.png'
---
<p><img src="{{ page.image }}" width="45%" align="right" style="padding: 15px;" /></p>Google is renewing its interest in the healthcare space by [releasing a protocol buffer implementation of the fast healthcare interoperability resources (FHIR) standard](https://research.googleblog.com/2018/03/making-healthcare-data-work-better-with.html). Protocol buffers are "Google's language-neutral, platform-neutral, extensible mechanism for serializing structured data – think XML, but smaller, faster, and simpler". Its the core of the next generation of APIs at Google, often using HTTP/2 as a transport, while also living side by side with RESTful APIs, which use OpenAPI as the definition, in parallel to what protocol buffers deliver.

It's a smart move by Google. Providing a gateway for healthcare data to find its way to their data platform products like Google Cloud BigQuery, and their machine learning solutions built on Tensorflow. They want to empower healthcare providers with powerful solutions that help onboard their data, and be able to connect the dots, and make sense of it at scale. However, I wouldn't stop with protocol buffers. I would also make sure they also invest in API infrastructure on the RESTful side of the equation, developing OpenAPI specs alongside the protocol buffers, and providing translation between, and tooling for both realms.

While I am a big supporter of gRPC, and protocol buffers, I'm skeptical of the complexity it brings, in exchange for higher performance. Part of making sense of health care data will require not just technical folks being able to make sense of what is going on, but also business folks, and protocol buffers, and gRPC solutions will be out of reach of these users. Web APIs, combined with YAML OpenAPI has begun to make the API contracts involved in all of this much more accessible to business users, putting everything within their reach. In our technological push forward, let's not forget the simplicity of web APIs, and exclude business healthcare users as IT has done historically.

I'm happy to see more FHIR-compliant APIs emerging on the landscape. PSD2 for banking, and FHIR for healthcare are the two best examples we have of industry specific API standards. So it is important that the definitions proliferate, and the services and tooling emerge and evolve. I'm hoping we see even more movement on this front in 2018, but I have to say I'm skeptical of Google's role, as they've come and gone within this arena before, and are exceptional at making sure all roads lead to their solutions, without many roads leading back to enrich the data owners, and stewards. If we can keep API definitions, simple, accessible, and usable by everyone, not just developers and IT folks, we can help empower healthcare data practitioners, and not limit, or restrict them, when it is most important.
