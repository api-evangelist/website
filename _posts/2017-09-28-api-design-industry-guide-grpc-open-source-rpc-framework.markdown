---
published: true
layout: post
title: 'API Design Industry Guide: gRPC, Open Source RPC Framework'
date: 2017-09-28T16:00:00.000Z
tags:
  - API Evangelist
  - Design
  - Protocols
image: >-
  https://s3.amazonaws.com/kinlane-productions/guides/definition/design/api-design-industry-guide-grpc-open-source-rpc-framework.png
---
<p><a href="http://design.apievangelist.com/#Guide"><img src="https://s3.amazonaws.com/kinlane-productions/guides/definition/design/api-design-industry-guide-grpc-open-source-rpc-framework.png" align="right" width="40%" style="padding: 15px;" /></a></p>
_This post is from the latest copy of my API Evangelist API Design Industry Guide, which provides a high level look at the API design layer of the industry. Providing a quick look at the services, tools, and some of the common building blocks of API design. The guide is heavily rooted in REST and hypermedia, but is working to track on the expansion of the space beyond just these formats. My industry guides change regularly, and I try to publish the articles from them here on the blog to increase their reach and exposure._

gRPC is a high-performance open source remote procedure call (RPC) framework that is often used to deploy APIs across data centers that also supporting load balancing, tracing, health checks and authentication. While gRPC excels in more controlled, tightly coupled environments, it is also applicable for delivering resources to web, mobile, and other Internet connected devices.

When crafting gRPC APIs, you begin by defining the service using Protocol Buffers, a language and toolset for binary serialization that has support across 10 leading programming languages. Protocol Buffers can be used to generate client and server stubs in these programming languages with tight API/client  coupling  — delivering a higher level of performance than your average REST API and SDK can.

gRPC API design patterns takes advantage of HTTP/2 advances and uses authenticated bi-directional streaming to deliver APIs that can be scaled to millions of RPC calls per second. Its an effective  approach for larger, more demanding API platforms that have begun to see the performance limitations of a more RESTful API design approach. gRPC is not ideal for every API implementation, but is definitely an approach providers should consider when high volumes anticipated, especially within the data center or other tightly controlled environment.

Google has been using gRPC internally for over a decade now, but has recently committed to delivering all their public APIs using gRPC in addition to RESTful APIs, demonstrating that the API design patterns can coexist. This approach makes it a welcome addition to any microservice style architecture. It has  the added benefit of API management features like authentication, tracing, load balancing, and health checking that are required to deliver high  performance.

gRPC is definitely more of an industrial grade API design pattern, shifting APIs into the next gear when it comes to performance. It also leverages the next generation of the HTTP protocol, HTTP/2. While not an API design pattern that every API provider will be working with, they should be aware it exists so that they understand what it is and the role it plays in the space.
