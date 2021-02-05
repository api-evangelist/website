---
published: true
layout: post
title: Three Stripe OpenAPI Vendor Extensions
date: 2017-11-16T15:00:00.000Z
tags:
  - API Evangelist
  - Definitions
  - Payments
  - Github
  - Design
image: >-
  https://s3.amazonaws.com/kinlane-productions/stripe/stripes-openapi-vendor-extension.png
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/stripe/stripes-openapi-vendor-extension.png" align="right" width="45%" style="padding: 15px;" /></p>As part of my work on [my OpenAPI toolbox](http://openapi.toolbox.apievangelist.com/) I am keeping an eye out for how leading API providers are using OpenAPI. One layer of this part of my research is understanding how teams are extending the OpenAPI specification, while also encouraging other companies to understand that they can extend the specification in the first place. I'm always surprised how many people I come across that say they do not use the specification because it doesn't do everything they need. I alternatively feel like it is my responsibility to understand what the spec can do, and then bend it to do what I need it to using vendor extensions.

I have been studying how [payment provider Stripe has been crafting their OpenAPI](https://github.com/stripe/openapi) throughout the week, while also understanding how they are applying it across their platform operations. As part of their Github repository for managing the Stripe OpenAPI they share three vendor extensions they are using to evolve what is possible with OpenAPI:

- **x-expandableFields** - Resources include an x-expandableFields that contains a list of fields that are expandable by making an API request with an expand parameter. See expanding objects.
- **x-polymorphicResources** - Some API responses are "polymorphic" in that they might return multiple types of resources which is a case that OpenAPI can't handle. In these cases the spec will reference a "synthetic" resource which is an aggregate of the properties common to all the possible resources. It will also include the field x-polymorphicResources which references those resources more precisely.
- **x-resourceId** - Resources include x-resourceId which is a canonical name for each resource. It can be used in conjunction with openapi/fixtures{2,3}.{json,yaml} to look up a sample representation (otherwise known as a "fixture") of the resource.

Some interesting extensions. The expandable fields, and resource id is pretty straight forward, but the polymorphic resources opens up some interesting questions when it comes to API design. It makes me want to learn more about the how and why Stripe does this with their API. Maybe it is just me, but I find OpenAPI a very useful tool for quantifying the design decisions that go into an API. I'm eager to learn more about how consistent providers are, as well as understanding where they deviated, and I find vendor extension are useful in revealing clues behind the decisions to deviate from common API design patterns.

I am going to be spending a lot of time studying Stripe's usage of OpenAPI. It is significant that top tier providers to share their OpenAPI on Github like Stripe does. It helps us learn more about the Stripe API, and the design and documentation decisions that have gone into the payment API. I wish more API providers would share their OpenAPI definition(s) via Github, and share any vendor extensions they have defined. A machine readable API definition on Github, with easy to find vendor extensions, across many API providers sounds like the beginning of a new generation of API discovery. One that can help drive the future of the OpenAPI Initiative (OAI) through real world usage, and shaping the OpenAPI specification road map through actively defining and sharing vendor extensions.
