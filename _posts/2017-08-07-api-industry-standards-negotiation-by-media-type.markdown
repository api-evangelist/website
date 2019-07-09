---
published: true
layout: post
title: API Industry Standards Negotiation By Media Type
date: 2017-08-07T11:00:00.000Z
tags:
  - API Evangelist
  - Standards
  - Definitions
  - Design
image: 'https://s3.amazonaws.com/kinlane-productions/bw-icons/bw-services.png'
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/bw-icons/bw-services.png" align="right" width="30%" style="padding: 15px;" /></p>I am trying to help push forward the conversation around [the API definition for the Human Services Data Specification (HSDS)](https://openreferral.github.io/api-specification/definition/) in a constructive way amidst a number of competing interests. I was handed a schema for sharing data about about organizations, locations, and services in a CSV format. I took this schema and exposed it with a set of API paths, keeping the flat file structure in tact, making no assumptions around how someone would need to access the data. I simply added the ability to get HSDS over the web as JSON--I would like to extend to be HTML, CSV, JSON, and XML, reaching as wide as possible audience with the basic implementation.

As we move forward discussions around HSDS and HSDA I'm looking to use media types to help separate the different types of access people are looking for using media types. I don't want to leave folks who only have basic CSV export or import capabilities behind, but still wanted to provide guidance for exchanging HSDA over the web. To help organize higher levels of demand on the HSDS schema I'm going to break out into some specialized media types as well as the default set:

- **Human Services Data Specification (HSDS)** - text/csv - Keeping data package basic, spreadsheet friendly, yet portable and exchangeable.
- **Human Services Data API (HSDA)** - application/json and text/xml, text/csv, and text/html - Governing access at the most basic level, keeping true to schema, but allowing for content negotiation over the web.
- **Human Services Data API (HSDA) Hypermedia** - (application/hal+json and application/hal+xml)  - Allowing for more comprehensive responses to HSDA requests, addressing searching, filtering, pagination, and relationship linking between any HSDS returend.
- **Human Services Data API (HSDA) Bulk** - (application/vnd.hsda.bulk) - Focusing on heavy system to system bulk transfers, and eventually syncing, backups, archives, and migrations. Dealing with the industrial levels of HSDA operations.
- **Human Services Data API (HSDA) Federated** - (application/vnd.hsda.federated) - Allowing for a federated HSDA implementation that allows for the moderation of all POST, PUT, and DELETE by a distributed set of partners. Might also accompany the bulk system where partners can enable sync or bulk extraction for use in their own implementations.

I am working to define an industry level API standard. I am not operating an individual API implementation (well I do have several demos), so media types allows me to enable each vendor, or implementation to negotiate the type of content they desire. If they are interested developing single page applications or conversational interfaces they can offer up the hypermedia implementation. If they are system administrators and looking to load up large datasets, or extract large datasets, they can work within the HSDA Bulk realm. In the end I can see any one of these APIs being deployed in isolation, as well as all four of them living side by side, driving a single HSDS/A compliant platform.

This is all preliminary thought. All I have currently is HSDS, and HSDA returning JSON. I'm just brainstorming about what possible paths there are forward, and what I think the solution involves content negotiation, at the vendor, implementation, and consumption levels. Content type negotiation seems to provide a great way to break up and separate concerns, keeping simple things simple, and some of the more robust integrations segregated, while still working in concert. I'm always impressed by the meaningful impact something like content type has had on the web API design conversation, and always surprised when I learn new approaches to leveraging the content type header as part of API operations.
