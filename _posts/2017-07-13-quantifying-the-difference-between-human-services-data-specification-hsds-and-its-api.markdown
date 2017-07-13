---
published: true
layout: post
title: >-
  Quantifying The Difference Between Human Services Data Specification (HSDS)
  And Its API
date: 2017-07-13T12:00:00.000Z
tags:
  - API Evangelist
  - Definitions
  - HSDA
  - HSDS
image: >-
  https://s3.amazonaws.com/kinlane-productions/3D-Printing/regions/api-regions-global-map-from-google.png
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/api-evangelist/openapi-spec/openapi-spec-icon.png" align="right" width="25%" style="padding: 15px;" /></p>To help quantify the move from version 1.0 to 1.1 of the Human Services Data API (HSDA) definition I took the existing Ohana API and created an OpenAPI definition to describe what was present in version 1.0 of the HSDA. Then I took [version 1.1 of the Human Services Data Specification (HSDS)](http://openreferral.readthedocs.io/en/latest/reference/#organization) and made sure as much of HSDS was returned as part of API responses, as well as allowing adding, updating, and deleting across the schema.

During the vendor API review portion of our process I took the documentation for four of the vendors APIs and created OpenAPI for each of them. I then laid all the vendor OpenAPIs alongside [the current draft I had of the HSDA definition](https://openreferral.github.io/api-specification/definition/). I then consider each path, the parameters, body, and responses for inclusion as part of the HSDA definition. This allowed me to consider the existing vendor API implementations that are already serving human service implementations.

OpenAPI plays a central role in defining what is, what might be, while opening up a forum for having a conversation about the specific detail of the HSDS/A definition. I'm using OpenAPI to establish a definition of what both HSDS and HSDA are. It will be the contract that gets hammered out as part of the Open Referral governance process, so you will see me use it regularly to articulate specific aspects of what is going. With this in mind, I'd like to use a distilled OpenAPI, articulated just a single API path for GET /organizations.

<script src="https://gist.github.com/kinlane/b44af277c9ad8948e82215ee31a7e195.js"></script>

I won't go into to much detail on the OpenAPI, [I recommend learning more about the specification on the GitHub repository](https://github.com/OAI/OpenAPI-Specification), and at [the OpenAPI Initiative (OAI)](https://www.openapis.org/). What I'd like to articulate for this story is to help quantity the separation and connection between the Human Services Data Specification (HSDA), and the Human Services Data API (HSDA), using this single OpenAPI, describing a single HSDA path--organizations.

When you take the schemes: located at line 7, and combine it with host: at line 5, basePath: at line 6, and the path for /organizations/ at line 12 you get http://api.open.referral.adopta.agency/organizations/, which when you load in a browser will give you a JSON listing of many organizations. Line 13-29 describes how to make an API request, and line 30-36 describes what you can expect as a response.

Lines 1-38 is HSDA, and 42-71 is HSDS. Line 36 is the link between HSDA, and HSDS, providing a reference that binds the API request, with the API response. HSDS is the valid schema being returned--HSDA is not the schema, it is the surface of the API that lets you send, and in this case received valid HSDS. This is a line that we honestly haven't had the level of detail, or even the acronyms before now to even articulate HSDS/A at this level. So don't worry if what I said doesn't quite make sense--it will come. ;-)

The first reason I'm writing this story is to help myself better articulate the difference between HSDS, and HSDA, and the relationship between them. The second portion is to help other folks participating in the HSDS/A governance conversation see the separate layers between the schema and API, but also understand how they work together. I'd say a third portion is about helping folks understand the value of using OpenAPI to facilitate these types of conversations.

It might take a couple times reading this post and/or having a conversation directly with me about OpenAPI, but there is nothing in this OpenAPI definition that any engaged users can learn to work with--developers, and non-developers. I'll keep producing simple lessons like this to better articulate aspects of the HSDS/A contract using OpenAPI. I'd love to hear any feedback on how I can better articulate the great work we are doing around the Human Services Data Specification and it's API.
