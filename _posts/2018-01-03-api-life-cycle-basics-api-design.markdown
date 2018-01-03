---
published: true
layout: post
title: 'API Transit Basics: API Design'
date: 2018-01-03T15:00:00.000Z
tags:
  - API Evangelist
  - Design
  - Life Cycle
image: 'https://s3.amazonaws.com/kinlane-productions/bw-icons/bw-design.png'
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/bw-icons/bw-design.png" align="right" width="25%" style="padding: 15px;" /></p>

_This is a series of stories I'm doing as part of [my API Transit work](http://basics.apievangelist.com/), trying to map out a simple journey that some of my clients can take to rethink some of the basics of their API strategy. I'm using a subway map visual, and experience to help map out the journey, which I'm calling [API transit](http://basics.apievangelist.com/)--leveraging the verb form of transit, to describe what every API should go through._

API design is not just about REST. Sure, a great deal of the focus within this stop along the API journey will be focused on REST, but this is because it is the dominant methodology at this moment in time. API design is about establishing a framework for how you will consistently craft your APIs across teams, whether they are REST, GraphQL, Microservices, or even gRPC. Your API design strategy might be dominated by RESTful practices, especially early on in your journey, but API design should not be considered to be only REST methodologies.

In the last five years API design has matured into its own discipline, focusing on a define and design first approach to developing APIs, shifting away from a code then document approach we've seen dominate for the last decade, and is still common place at many organizations. There are a handful of tooling, and websites that have emerged to help API providers, architects, developers, and designers get a handle on this stop along the API journey--here are just a few.

- [**Swagger Editor**](http://editor.swagger.io) - Leverage the Swagger editor for manually working with OpenAPI definitions.
- [**Apicurio**](http://www.apicur.io/) - A robust, and beautiful open source tool for designing APIs.
- **API Design Guide** - Continue to establish, evolve, and disseminate the organizational API design guide, providing guidance for all teams--make sure there is a feedback loop involved with its development.
- [**API Stylebook**](http://apistylebook.com/) - Learning and extracting from other companies API design guides.
- [**Designing and Implementing Hypermedia APIs**](https://www.infoq.com/articles/hypermedia-api-tutorial-part-one) - A thoughtful post on how to design hypermedia APIs.
- [**GraphQL Design**](http://graphql.org/learn/best-practices/) - The best practices for designing a GraphQL API.
- [**GRPC API Design**](https://grpc.io/docs/guides/) - A guide to designing gRPC APIs that leverage HTTP/2 and Protocol Buffers.

API design is as much of a discipline as it is a methodology rooted in a specific standard, protocol, or history. It is about having the discipline to document current practices for designing APIs that are in production, then standardize, communicate, and evolve those practices in a formal way. While also studying and learning from other leading API providers and practitioners regarding how they are designing their APIs. Which is why I include the API Stylebook in this stop along the API journey--everyone should be learning from each other, which also includes sharing your API design guide when it is ready.

We need to move beyond API design meaning REST in the API community. This is something that has caused significant damage to the health of many API operations, and is a dogmatic approach that has replicated itself in hypermedia, and GraphQL--it needs to stop. API design is about defining a common framework for designing your APIs, no matter which approach you adopt internally. Ideally, your API design philosophy is multi-approach, allowing you to apply the right pattern where is needed, and not viewing API design as a one size fits all set of rules. When it comes to API design within your organization, start small, keep things loose, learn from others, and begin documenting your approach in a guide, that can eventually grow into a wider set of API governance practices that will allow your operations to grow in the way you envision.
