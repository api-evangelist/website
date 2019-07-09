---
published: true
layout: post
title: I Added A Taxonomy API To Support The Human Services Data API (HSDA)
date: 2017-11-13T09:00:00.000Z
tags:
  - API Evangelist
  - HSDA
  - Taxonomy
  - Definitions
image: ''
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/bw-icons/open-referral/human-services-taxonomy-api.png" align="right" width="45%" style="padding: 15px"></p>I have been organizing [my Human Services Data API (HSDA) specification work](http://org.open.referral.adopta.agency/) into separate microservices as part of version 1.0 for the API definition that cities and other organizations running 211 operations can pick and choose which aspects they want to run. One service I carved off of the move from version 1.0 to 1.1 of the specification was taxonomy, and how the human services are categories and organized. I saw there was more research to be done around 211 taxonomy, and I felt it had the potential to be a separate but supporting service to augment what Open Referral is already trying to do with [the Human Services Data API (HSDA) specification](http://org.open.referral.adopta.agency/#Specification).

[The HSDA Taxonomy API specification provides a handful of API paths for creating, reading, updating, and deleting taxonomy used in any HSDA implementation](http://developer.open.referral.adopta.agency/#HSDA Taxonomy). I have populated my demo API with [the Open Elegibility taxonomy](https://github.com/auntbertha/openeligibility) to help jumpstart folks, but any HSDA provider can populate with their own custom taxonomy, or other existing format. Then you can apply any taxonomy to any of the services stored within an HSDA database, and there is an API path for querying services by taxonomy. Next I'll make sure you can search by taxonomy, and see the taxonomy as part of the response body for all services returned across HSDA, HSDA Search, and HSDA Taxonomy.

HSDA Taxonomy API is a simple service, but it is one that I want to get up and running, and maturing quickly. I feel like there is a lot of opportunity around 211 taxonomy aggregation, an further standardizing and evolving on top of Open Eligibility, or establishing a separate Open Referral taxonomy that can be open source. The current 211 taxonomy dominating the landscape is the AIRS 211 format, which is a proprietary taxonomy, something that I'll address in a separate post. Have a shared vocabulary around human services is almost as important as the data itself--if you can't find meaningful services, in a consistent way across providers, the data itself becomes much less valuable.

[I have launched a demo copy of the API at my Human Services Demo API](http://developer.open.referral.adopta.agency/#HSDA Taxonomy), and next I am working on a handful of UI elements for managing, browsing, and searching for services using the HSDA Taxonomy API. My goal is to get v1.0 of the HSDA Taxonomy specification being discussed as part of the overall HSDA governance process, while I'm also hardening the API, and UI tooling via a couple of HSDA implementations I'm working on. Then I'll circle back in a couple months and see where things are, learn more about some other taxonomies, and hopefully pull together more of a strategy around how to get people sharing 211 taxonomies, and speaking a common language about how they categorize human services, as well as store and provide access to human service organizations, locations, and services.
