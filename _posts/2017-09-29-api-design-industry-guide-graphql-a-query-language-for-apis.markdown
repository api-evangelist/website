---
published: true
layout: post
title: 'API Design Industry Guide: GraphQL, A Query Language For APIs'
date: 2017-09-29T09:00:00.000Z
tags:
  - API Evangelist
  - Design
  - Protocols
image: >-
  https://s3.amazonaws.com/kinlane-productions/guides/definition/design/api-design-industry-guide-graphql.png
---
<p><a href="http://design.apievangelist.com/#Guide"><img src="https://s3.amazonaws.com/kinlane-productions/guides/definition/design/api-design-industry-guide-graphql.png" align="right" width="40%" style="padding: 15px;" /></a></p>
_This post is from the latest copy of my API Evangelist API Design Industry Guide, which provides a high level look at the API design layer of the industry. Providing a quick look at the services, tools, and some of the common building blocks of API design. The guide is heavily rooted in REST and hypermedia, but is working to track on the expansion of the space beyond just these formats. My industry guides change regularly, and I try to publish the articles from them here on the blog to increase their reach and exposure._

GraphQL is a query language designed by Facebook to build client applications using a flexible syntax and provide a system for describing the data requirements and interactions required by each application. GraphQL began as a Facebook project that soon began powering all their mobile applications. By 2015, became a formal specification. GraphQL provides a query language for your APIs that allows users to describe how they would like their API requests be fulfilled. The approach shifts the API design process to be more about request flexibility requiring API providers to design all API paths ahead of time. It opts for an augmented query language over investing in static schema that requires specific API paths.

REST APIs focus on paths to your resources, but GraphQL is all about fields and data types, with everything accessed through a single API path. GraphQL does a better job of providing a more comprehensive approach access to data stored in a database by offloading design to the query layer for interpretation at query render time. The ability to define what data is returned opens up some interesting approaches to delivering resources, especially when it comes to potentially constrained network environments.

When it comes to providing access to data used in responsive web and mobile applications, GraphQL can be successful in allowing application developers to get exactly what they need for an interface and nothing more. This can increase performance and give UI / UX designers more of a voice in what an API does. GraphQL has played a significant role in the evolution of React, Facebook’s open source framework for deploying user interfaces. React is well-known has achieved some significant traction in application development circles. This design approach to delivering data using APIs a natural fit for rapidly delivering web and mobile apps.

GraphQL has seen some significant adoption beyond Facebook, notably at Github and Pinterest. GraphQL strengths become clear when it is used to deliver complex data stores quickly and efficiently by developers that require a greater level of control what data they need. While GraphQL is not traditional API design, it is an important design constraint to consider when planning the future of your API design practices and toolbox.
