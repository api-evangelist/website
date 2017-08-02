---
published: true
layout: post
title: When Cities Use A Common API Definition To Report Non-Emergency Issues
date: 2017-08-02T11:00:00.000Z
tags:
  - API Evangelist
  - City Government
  - State Government
  - County Government
  - Federal Government
  - Open311
  - Open Source
image: 'https://s3.amazonaws.com/kinlane-productions/open311/open311-api-list.png'
---
I am taking a deeper look at Open311, as part of some wider municipal level API research and development I am doing. I am going to be helping evolve an OpenAPI for the project, as well as JSON schema for the API and underlying data model. As I'm working my way through the Open311 portal reacquainting myself with the open format for reporting of non-emergency issues within cities, I came across the list of cities who have implemented Open311, and get a glimpse at what the future of APIs at the city level can be.

[When you land on the Open311 GeoReport v2 Servers listing page you get a table of the twenty-one cities who have published an Open311 API](http://wiki.open311.org/GeoReport_v2/Servers/), with the name, country, API discovery document, API key request location, documentation, production and sandbox environment URLs. Twenty-one separate cities, twenty-one separate APIs for reporting non-emergency issues, all using the same API definition. This is the way that all APIs at the city, county, state, and federal levels should work. They should leverage common schema and API definition, providing a federated list of resources that can be integrated into any application.

<p align="center"><a href="http://wiki.open311.org/GeoReport_v2/Servers/"><img src="https://s3.amazonaws.com/kinlane-productions/open311/open311-api-list.png" width="80%" style="padding: 15px;" align="center" /></a></p>

Imagine when all cities have a common 311 API for reporting of non-emergency issues, as well as a 211 API for finding human services within a city. Imagine when the entire stack of city services all use common API definition(s), and schema across all API requests and responses. In this environment any city will be able take existing SDKs, or open source application, tools, or plugin, and put to work for a new city, with little or no changes. This is the way city, county, state, and federal agency software and application development should work. There should be a buffet of open source solutions for each layer of government operations.

When it comes to this level of API operations within cities, Open311 is the furthest along down the road in the journey. This is why I want to help them further develop the OpenAPI, and supporting JSON schemas, take a look at their overall portal, and operations, to see where else I can lend a hand, and contribute to their momentum. I am looking to bring Open311 alignment with the work I am doing on the Open Referral Human Services Data API, which is essentially Open211. It's gonna take me a few weeks to get up to speed on everything going on with Open311, and find the bandwidth to work on the OpenAPI, and JSON schema, alongside [my Human Services API work](http://org.open.referral.adopta.agency/), but I am invested in seeing both these open government API standards move forward, and enjoy wider adoption by cities around the world, so I will find the time somewhere.
