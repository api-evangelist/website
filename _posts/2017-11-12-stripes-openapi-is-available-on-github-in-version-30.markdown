---
published: true
layout: post
title: Stripes OpenAPI Is Available On Github In Version 3.0
date: 2017-11-12T15:00:00.000Z
tags:
  - API Evangelist
  - Definitions
  - Payments
  - Github
  - Orchestration
image: ''
---
<p><a href="https://github.com/stripe/openapi"><img src="https://s3.amazonaws.com/kinlane-productions/stripe/stripes-openapi-specification-on-github.png" align="right" width="45%" style="padding: 15px;" /></a></p>I can't write about every API provider who publishes their OpenAPI to Github, there are just too many. But, I can write about the rockstar API providers who do though, and showcase what they are doing, so I can help influence the API providers who have not started publishing their OpenAPIs in this way. If you are looking for a solid example of a leading API provider publishing their OpenAPI to Github, [I recommend taking a look at the payment provider Stripe](https://github.com/stripe/openapi).

[Their repository contains OpenAPI specifications for Stripe's API](https://github.com/stripe/openapi), with multiple files available in the in the openapi/ directory:

- **spec3.{json,yaml}** - OpenAPI 3.0 spec.
- **spec2.{json,yaml}** - OpenAPI 2.0 spec. We're continuing to generate this for now, but it will be deprecated in favor of spec3.
- **fixtures3.{json,yaml}** - Test fixtures for resources in spec3. See below for more information.
- **fixtures2.{json,yaml}** - Test fixtures for resources in spec2.

It is pretty exciting to see them already embracing version 3.0. They even provide a listing of the OpenAPI vendor extensions they are using, which are specific to their API. [I'll be adding these to my OpenAPI toolbox](http://openapi.toolbox.apievangelist.com/) when I have the time, adding to the number of vendor extensions I have indexed. Stripe provides another pretty solid example of an API provider taking ownership of their OpenAPI spec, publishing to Github for their consumers to put tow rok, but clearly they are also using as part of their own internal workflows as well.

Every API provider should have a Github repository with an up to date OpenAPI [like Stripe does](https://github.com/stripe/openapi). I know many API architects envision a hypermedia API discovery landscape, where APIs are defined and discoverable by default, but I think an OpenAPI on Github is the best we can hope for at this stage in the evolution of the space. With the momentum I'm seeing in the number API providers publishing their OpenAPIs to Github, I'm feeling like Github is going to become the continuous integration, API discovery engine we've all been looking for over the last decade. Allowing us to discover, integrate and orchestrate with our APIs across the API life cycle--we just need everyone to follow Stripe's lead. ;-)
