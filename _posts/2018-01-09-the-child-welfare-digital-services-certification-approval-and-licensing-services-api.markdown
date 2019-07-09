---
published: true
layout: post
title: >-
  The Child Welfare Digital Services (CWDS) Certification, Approval, and
  Licensing Services (CALS) API
date: 2018-01-09T09:00:00.000Z
tags:
  - API Evangelist
  - Child Services
  - County Government
  - State Government
  - City Government
image: >-
  https://s3.amazonaws.com/kinlane-productions/child-welfare-digital-services-california/child-welfare-digital-services.png
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/child-welfare-digital-services-california/child-welfare-digital-services.png" align="right" width="45%" style="padding: 15px;" /></p>My partner Chris Cairns([@cscairns](https://twitter.com/cscairns)) over at [Skylight](https://skylight.digital/) sent me a link to [the Child Welfare Digital Services (CWDS) Certification, Approval, and Licensing Services (CALS) API on Github](https://github.com/ca-cwds) the other day. The API isn't your traditional public API, but shows what is possible when it comes to APIs at government agencies. The group behind the API has published their [Digital Service Development Standards](https://cwds.ca.gov/digital_service_design_standards), and is actively using [a Github Wiki to layout the API strategy for the organization](https://github.com/ca-cwds/cals-api/wiki).

To give some backround, the Child Welfare Digital Services (CWDS) is for _"state and county workers who ensure that safe and quality licensed facilities and approved homes are available for the children and nonminor dependents who need them, the CALS Digital Service Team will facilitate activities related to ensuring that licensed facilities, approved homes and associated adults meet and maintain required standards."_ It makes me happy to see that they are investing so heavily in API, in support of such a worthy cause.

Looking around their wiki I found a handful of APIs:

- [**Facility**](https://github.com/ca-cwds/cals-api/wiki/Facility-Resource)
- [**Facility Children**](https://github.com/ca-cwds/cals-api/wiki/Facility-Children-Resource-v1)
- [**Facility Complaint**](https://github.com/ca-cwds/cals-api/wiki/Facility-Complaints-Resource)
- [**Facility Inspections**](https://github.com/ca-cwds/cals-api/wiki/Facility-Inspections-Resource-v1)

You can also find more about their development process, data model, and approach to security on the Github Wiki for the organization. After looking around more at their Github organization, I found a handful of other operational APIs:

- [**Modules API**](https://github.com/ca-cwds/API)
- [**Intake API**](https://github.com/ca-cwds/intake_api)
- [**Case Management API**](https://github.com/ca-cwds/case-management-api)
- [**Document Management API**](https://github.com/ca-cwds/dms-api)
- [**Forms API**](https://github.com/ca-cwds/forms-api)
- [**Geo Services API**](https://github.com/ca-cwds/geo-services-api)

There was also a [Core API](https://github.com/ca-cwds/api-core) which they use as a base across all API projects, standardizing how they do things. Smart! I also found their testing strategy worthy of noting, just so I can add to my research.

- **Integration Testing** - To run Integration tests set property cals.api.url to point to environment host. Use gradle integrationTest task. In this case token will be generated for default test user, so it's possible to test environment with Perry running in dev mode.
- **Smoke Testing** - Smoke test suite is part of integration tests. Set cals.api.url, use gradle smokeTestSuite task. Smoke test endpoint is not protected by Perry.

I like the style of the Child Welfare Digital Services (CWDS) team. They are investing heavily in APIs, and aren't afraid of doing it out in the open. As it should be. It is important that ALL government agencies do this, so that other agencies can come along and build on their work, making government more efficient, and cost effective when getting business done. All of the APIs above can, and should be forked, and put to use across other child welfare organizations. I notice they are also using OpenAPI (fka Swagger), but haven't published them as part of some of their projects. I will keep an eye on and update when they do--reuse of API definitions, is even more than reuse of code. 

If you know of any government agency who is this progressive, and publishing their API strategy, processes, definitions, and code on Github--please let me know! This type of behavior needs showcasing, and I like to have a wealth of references on my blog which I can cite as I'm traveling around speaking, and consulting with government agencies. This type of API efforts should be default across all city, county, state, and federal government agencies.
