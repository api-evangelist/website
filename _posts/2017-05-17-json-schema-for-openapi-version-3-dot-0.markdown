---
title: JSON Schema For OpenAPI Version 3.0
date: 2017-05-17 09:00:00 Z
image: https://s3.amazonaws.com/kinlane-productions/json/json-schema.png
---

<p><img style="padding: 15px;" src="https://s3.amazonaws.com/kinlane-productions/json/json-schema.png" align="right" width="40%" /></p>
We are inching closer to a final release of version 3.0 for the OpenAPI specification, with the official version currently set at 3.0.0-rc1. We are beginning to see tooling emerge, and services like [APIMATIC are already supporting version 3.0 when it comes to SDK generation](https://apimatic.io/), as well their [API Transformer conversion tool](https://apimatic.io/transformer). 

I am working on an OpenAPI validation solutions tailored specifically for municipal API deployments and was working with [the JSON Schema for version 2.0 of the API specification](https://github.com/OAI/OpenAPI-Specification/blob/master/schemas/v2.0/schema.json).  I wanted to help make my work be as ready for the future of the API specification and wanted to see if there was a JSON Schema for version 3.0 of the OpenAPI specification. I couldn't find anything in the new branch of the repository, so I set out seeing if anyone else has been working on it.

While I was searching I saw [Tim Burks](https://github.com/timburks) share that he and [Mike Ralphson](https://github.com/MikeRalphson) were [working on one over at the Google Gnostic project](https://github.com/googleapis/gnostic/blob/openapi-v3.0.0-rc2/OpenAPIv3/openapi-3.0.json). It looks like it is still a work in progress, but it provides us with a starting point to work from.

I will keep an eye out on the OpenAPI repo for when they add an official JSON Schema for version 3.0. As I've learned more about JSON Schema, the more I'm learning about how it helps harmonize and stabilizing tooling being developed around any schema. Without it, you get some pretty unreliable results, but with it, you can achieve some pretty scalable consistency across API tooling and services--something the API space needs as much as it can get in 2017.