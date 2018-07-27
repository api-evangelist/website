---
published: true
layout: post
title: The Service Level Agreement (SLA) Definition For The OpenAPI Specification
date: 2018-07-27T09:00:00.000Z
tags:
  - API Evangelist
  - Service Level Agreement
  - SLA
  - Politics of APIs
  - Management
image: >-
  https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories/legalstatue_light_dali.jpg
---
<p><img src="{{ page.image }}" width="45%" align="right" style="padding: 15px;" /></p>[I'm currently learning more about SLA4OAI, an open source standard for describing SLA in APIs](https://github.com/isa-group/SLA4OAI-Specification), which is based on the standards proposed by the OAI, adding an optional profile for defining SLA (Service Level Agreements) for APIs. "This SLA definition in a neutral vendor flavor will allow to foster innovation in the area where APIs expose and documents its SLA, API Management tools can import and measure such key metrics and composed SLAs for composed services aggregated way in a standard way." Providing not just a needed standard for the API sector, but more importantly one that is built on top of an existing standard.

SLA4OAI, provides an intersesting way to define the SLA for any API, providing a set of objects that augment and can be paired with an OpenAPI definition using an x-sla vendor extension:

- **[Context](https://github.com/isa-group/SLA4OAI-Specification/blob/master/Specification.md#522-contextobject)** - Holds the main information of the SLA context.
- **[Infrastructure](https://github.com/isa-group/SLA4OAI-Specification/blob/master/Specification.md#524-infrastructureobject)** - Required Provides information about tooling used for SLA storage, calculation, governance, etc.
- **[Pricing](https://github.com/isa-group/SLA4OAI-Specification/blob/master/Specification.md#525-pricingobject)** - Global pricing data.
- **[Metrics](https://github.com/isa-group/SLA4OAI-Specification/blob/master/Specification.md#526-metricsobject)** - A list of metrics to use in the context of the SLA.
- **[Plans](https://github.com/isa-group/SLA4OAI-Specification/blob/master/Specification.md#528-plansobject)** - A set of plans to define different service levels per plan.
- **[Quotas](https://github.com/isa-group/SLA4OAI-Specification/blob/master/Specification.md#5210-quotasobject)** - Global quotas, these are the default quotas, but they could be overridden by each plan later.
- **[Rates](https://github.com/isa-group/SLA4OAI-Specification/blob/master/Specification.md#5211-ratesobject)** - Global rates, these are the default rates, but they could be overridden by each plan later.
- **[Guarantees](https://github.com/isa-group/SLA4OAI-Specification/blob/master/Specification.md#5212-guaranteesobject)** - Global guarantees, these are the default guarantees, but they could be overridden by each plan later.
- **[Configuration](https://github.com/isa-group/SLA4OAI-Specification/blob/master/Specification.md#5218-configurationsobject)** - Define the default configurations, later each plan can be override it.

These objects provide all the details you will need to quantify the SLA for any OpenAPI defined API. In order to validate each of the SLAs, a separate Basic SLA Management Services is provided to implement the services that control, manage, report and track SLAs. Providing the reporting output you will need to understand whether or not each individual API is meeting its SLA. Providing a universal SLA format that can be used to create SLA templates, applied as individual API SLAs, and then leveraging a common schema for reporting on SLA monitoring, which can actually be used in conjunction with the API management layer of your API operations.

I'm still getting familiar with the specification, but I'm impressed with what I've seen so far. There is a lot of detail available in there, and it provides all the context that will be needed to quantify, measure, and report upon API SLAs. My only critique at this point is that I feel the pricing, metrics, plans, and quotas elements should be broken out into a separate specification so that they can be used out of the context of just SLA management, and as part of the wider API management strategy. There are plenty of scenarios where you will want to be using these elements, but not in the context of SLA enforcement (ie. driving pricing and plan pages, billing and invoicing, and API discovery). Other than than, I'm pretty impressed with the work present in the specification.

It makes me happy to see sister specifications emerge like this, rather than also baked directly into the OpenAPI. The way they've referenced the SLA from the OpenAPI definition, and the OpenAPI from the SLA definition is how these things should occur, in my opinion. It has been something I've done for years with [the APIs.json format](http://apisjson.org/), having seen a future where there are many sister or even competing specifications all working in unison. Which is why I feel the pricing and plan elements should be decoupled from the SLA object here. However, I think this is a great start to something that we are going to need if we expect this whole API thing to actually work at scale, and make sure the technology of APIs is in sync with the business of APIs. Without it, there will always been a gulf between the technology and business units, much like we've seen historically between IT and business groups across enterprise organizations today.