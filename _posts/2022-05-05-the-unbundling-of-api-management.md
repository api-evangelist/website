---
published: true
layout: post
title: 'The Unbundling of API Management'
image: https://s3.amazonaws.com/kinlane-productions2/algorotoscope-master/containership-containership-copper-circuit.jpg
tags:
- Postman
- Management
- Documentation
- Gateway
- Authentication
- Policies
- Portals
- Docs
- Analytics
---
When you ask people involved in API operations what API management is you’ll get a whole mix of answers. [API management as we are sold it emerged out of the SOA world around 2006](https://apievangelist.com/2013/06/10/history-of-apis-mashery/). Over the years it picked up momentum [until a number of acquisitions occurred and Apigee IPO’d in 2015](https://apievangelist.com/2015/03/24/reflecting-on-api-management-and-the-apigee-ipo/), resulting in a bundling of various services API producers are in need of packaged as a single solution to what the enterprise needed. The bundling of API management capabilities was more about what API management vendors needed than it was ever about what API producers actually needed. Then around the same time API management providers were peaking, a new generation of API gateway providers were emerging to shift what the cornerstone of API management was all about, but also begin delivering the other bundled services as well.

The core set of services enterprise organizations were purchasing from API management vendors over the years looked much like this:

- **Gateway** - Providing the front door, or if you will, the front gate for your API estate.
- **Auth** - Handling onboarding, authentication, authorization, and access to APIs.
- **Policies** - Plans, rate limits, scopes, rules, and other policies applied at runtime.
- **Portals** - The human landing page for all things API within enterprise or community.
- **Docs** - Help standardize and automate the publishing of API documentation and resources.
- **Analytics** - Providing a dashboard or reports showing usage, errors, and other data.

Just as the old guard of API management providers were peaking, a next generation of API service providers were delivering features to unbundle what we know as API management:

- **Gateway** - Kong, Tyk, Hashicorp, KrakenD
- **Auth** - Auth0, Okta
- **Policies** - Who????
- **Portals** - Postman, APIMATIC, Readme, Provonix
- **Docs** - Postman, APIMATIC, Readme, Redocly
- **Analytics** - Moesif, Resurface Labs

Developers were needing almost all of the features API management providers were peddling, they just didn't need them all bundled together. You see, when you are a startup and begin selling to the enterprise you hear, “we need one solution to solve all of our problems across the entire API lifecycle” A LOT. There is a reason it is called “Full Lifecycle API Management”. Ultimately, with the API gateway a commodity that is baked into the fabric of the cloud (AWS, Azure, Google), and also now baked into the fabric of the web (CloudFlare), it isn’t where the action is. Granted, it is still a cornerstone of the API lifecycle, but this ain’t your grandfathers API operations, and there is most likely multiple gateways in use across the average enterprise organization.

For me, API management was the original intent behind starting API Evangeist in 2010 — [I wanted to understand the API management space](https://apievangelist.com/blog/page38/). It seemed logical to me from 2010 through 2015 that all of these services should be bundled together. However, I think API service providers aren’t immune from the business realities that push the average enterprise organization to be API-first, redefining the digital resources and capabilities you offer as more modular, distributed, and unbundled sets of services that can be stitched together to do whatever a developer wants. If you live by API, you die by API. If you are doing business in 2022 in any business sector, you have to have an API. API service providers who sell to the entire API lifecycle, or to any specific stop along the API lifecycle has to have an API, so people can use exactly what they need.