---
published: true
layout: post
title: API Design Maturity At Capital One
date: 2017-10-16T15:00:00.000Z
tags:
  - API Evangelist
  - Design
  - Governance
image: >-
  https://s3.amazonaws.com/kinlane-productions/capital-one/capital-one-api-maturing-pyramid.png
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/capital-one/capital-one-api-maturing-pyramid.png" align="right" width="40%" style="padding: 15px;" /></p>API design is something that many have tried to quantify and measure, but very few ever establish any meaningful way of doing so properly in my experience. [I've been learning about the approach to API governance from the Capital One DevExchange team](https://matthewreinbold.com/2017/10/03/API-Governance-Blueprint/), and found their approach to defining API design maturity pretty interesting. I'm mostly interested in their approach because it speaks to actual business objectives, and aren't about the common technical aspects we see API design being quantified across the community each day.

Capital One breaks things down into five distinctive layers that offer value to any organization doing APIs. Starting at the bottom of their maturity period, here are the levels of maturity they are measuring things by:

- **Functional** - Doing the basics, providing some low-level functionality, and nothing more.
- **Reliable** - An API that is reliable, and scalable, beyond just basic functionality.
- **Intuitive** - Where an investment in developer experience is made, further standardizing and streamlining what an API does.
- **Empowering** - Where an API really begins to deliver value to an organization by being function, reliable, and intuitive, which all contributes significantly to operations.
- **Transformative** - APIs that are game changer. Few APIs ever rise to this level, but all should aspire to this level of maturity.

It provides a whole other lens for looking at API design through. Moving beyond just, is it RESTful? Hypermedia, GraphQL, gRPC, or other emerging approach. It also understands that not all APIs will be equal, and that we should be standardizing the value the design of our APIs deliver to our business operations. Forcing us to ask some pretty simple questions about the API design patterns we are using, and the actual value they bring to the table. Moving beyond API design being about technical details, and considering the business, and other political aspects of doing APIs.

The Capital One API design maturity definition also demonstrates another important aspect of all of this. That it takes work, time, and experience to properly design an API that will rise an empowering or transformative level. It can be easy to deliver functional APIs, but making them become reliable, and intuitively get the job done will take investment. I'm adding this definition to [my API design research](http://design.apievangelist.com), as well as my upcoming API governance research. I'm looking to evolve my definition of what API design looks like beyond just REST, and I'm wanting to move API governance beyond some IT led concept, and something that is in sync with business objectives, like I'm seeing from the Capital One team. It is easy to think of API design as mature once it enters production, but I'm thinking there is a lot more we should be considering before we consider our approach to API design mature.
