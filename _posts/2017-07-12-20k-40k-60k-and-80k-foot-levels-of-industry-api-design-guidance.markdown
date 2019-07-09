---
published: true
layout: post
title: '20K, 40K, 60K, and 80K Foot Levels Of Industry API Design Guidance'
date: 2017-07-12T14:00:00.000Z
tags:
  - API Evangelist
  - Design
  - Industry
  - Standards
  - HDSA
image: 'https://s3.amazonaws.com/kinlane-productions/definition-of-high-altitude.jpg'
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/definition-of-high-altitude.jpg" align="right" width="40%" style="padding: 15px;" /></p>[I am moving my Human Services Data API (HSDA) work](http://org.open.referral.adopta.agency/) forward and one of the top items on the list to consider as part of the move from version 1.1 to 1.2 is all around the scope of the API design portion of the standard. We are at a phase where the API design still very much reflects the Human Services Data Specification (HSDS)--basically a very CRUD (Create, Read, Update and Delete) API. With version 1.2 I need to begin considering the needs of API consumers a little more, looking to vendors and real world practitioners to help understand what the next version(s) of the API definition will/should contain.

The most prominent discussion in the move from version 1.1 to 1.2 centers around scope of API design at four distinct levels of this work, where we are looking to move forward a variety of API design concerns for a large group of API consumers:

* [Data Scope / Filtering](https://github.com/openreferral/api-specification/issues/22) - Discussions around how to filter data, allowing API consumers to search across the contents of any HSDA implementation, getting exactly the data they need, no more, no less.
* [Schema Scope / Filtering](https://github.com/openreferral/api-specification/issues/21) - Considering the design of simple, standard, or full schema responses that can specified using a prefer header, parameter, or path levels.
* [Path Scope / Filtering](https://github.com/openreferral/api-specification/issues/38) - How are API paths going to be group and organized, allowing a large surface area to be shared via documentation (APIs.json) in a way that new API consumers can start simple, advanced users can get what they need, and serving as many needs in between as we can.
* [Project Scope / Filtering](https://github.com/openreferral/api-specification/issues/40) - Adding the fourth dimension to this scope / filtering discussion, I'm proposing we discuss how projects are defined and isolated, which can allow them to move forward at different rates, and be reflected in documentation, code, and other resources--allowing for filtering by consumers, as  well as prioritization by vendors involved in the API design discussion.

In short I have a large number of desires put on the table by vendors and practitioners. There is a mix of desire to load up as much functionality and API design guidance as we can at the single path level--meaning /organizations, /locations, and /services will allow you to get as much, or as little, as you desire. In this same conversation I have to defend the interests of newcomers, allowing them to easily learn about, and get what they need from these three distinct API paths, without loading them up with too much functionality. While also defend the long tail of needs for mobile, voice, and other leading edge application developers.

I'm looking at this discussion in these four dimensions, but I am trying to apply a horizontal or vertical approach in all four dimensions. Meaning, do I access or filter the amount of data I receive vertically with parameters or headers at the single API path level, or do I access and filter the amount of data I want horizontally across many separate API paths. The same logic applies to the API schema level with accessing vertically at the same path, by adding many subpaths, or do we approach horizontally with new paths. This continues at the API path, and project levels--how do discuss, develop, evolve, and allow API consumers to filter and only get at the API paths and projects they need--limiting the scope for new users, but meeting the demand of vendors, implementors, analysts, and other power consumers.

Aight, ok. Phew. I just needed to get that out. Not 100% sure it makes sense, but it is a framework I'm running with for a group conversation I'm having tomorrow--so we'll see how it goes. One significant difference in this API design process from others is that it is not about any single API implementation. It is focused on moving forward a single API definition, or in the case of this discussion, many little API definition discussions, with lots of overlap, and under a single umbrella--to support thousands of API implementations. I'll be publishing another piece shortly which zooms out to the 100K level of my HSDA work, where I'd consider this to be a little 20K (data), 40K (schema), 60K (path), and 80K (project) levels. I just needed to get a handle on this piece--if you actually read this far in the post, you are pretty geeky, and probably need a hobby (HSDA is mine).
