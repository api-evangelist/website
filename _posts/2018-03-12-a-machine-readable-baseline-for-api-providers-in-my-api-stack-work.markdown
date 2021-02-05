---
published: true
layout: post
title: A Machine Readable Baseline For API Providers In My API Stack Work
date: 2018-03-12T09:00:00.000Z
tags:
  - API Evangelist
  - Definitions
  - Discovery
image: 'https://s3.amazonaws.com/kinlane-productions/api-definitions-api-stack.png'
---
<p><img src="{{ page.image }}" width="45%" align="right" style="padding: 15px;" /></p>I'm rebooting [my API Stack](http://theapistack.com/) work as part of my partnership with [Streamdata.io](http://streamdata.io). I'm spending a significant portion of my day profiling API providers, documenting what it is they bring to the table. Historically I've published the resulting APIs.json and OpenAPI definition(s) to a single Github repository driving theapistack.com. The primary folder was already getting too big, and since I'm looking at adding at least a thousand more API providers to the stack, I am going to need to shard things out a bit.

To help accommodate the increased scale, I'm breaking up the API Stack into two separate Github organizations. One for individual API providers called [api-stack-providers](https://github.com/api-stack-providers), and a second for individual topics called [api-stack-topics](https://github.com/api-stack-topics). I've began publishing individual repositories for each API provider that I am monitoring, establishing a self-contained, continuously deployable, and integratabtle set of definitions for each API. I'm needing each API provider to be independent from each other, and I'm even publishing individual API definitions for each API path, distilling things down to the smallest possible unit of compute possible.

Each repository contains three main API definitions, using [the ParallelDots machine learning API](https://github.com/api-stack-providers/paralleldots) as an example:

- [APIs.json](https://github.com/api-stack-providers/paralleldots/blob/master/apis.yaml) - The entire index of the API provider's operation.
- [OpenAPI](https://github.com/api-stack-providers/paralleldots/blob/master/openapi/complete.yaml) - The definition of the surface area of entire API.
- [Postman Collection](https://github.com/api-stack-providers/paralleldots/blob/master/postmancollections/complete.json) - An execute-time ready definition for the Postman client.

I'm also publishing an individual OpenAPI for each API path within a listings folder, allowing me to provide the detailed execute-time definition I'm needing to work with each API. I'm also considering how I can do this with the Postman Collections. Next, I'm looking to understand how I can include the multiple source definitions within the repository, providing original copies of API definitions that I'm pulling from sources like [APIs.guru](http://apis.guru), [Any API](https://any-api.com/), and directly from API providers. Sharing the entire history behind how each set of API definitions has come together, and hopefully encouraging others to submit pull requests with fresh copies.

Ideally, each API provider is maintaining their own set of definitions in their own Github repository, like [Box](https://apievangelist.com/2017/05/22/box-goes-all-in-on-openapi/), [NY Times](https://apievangelist.com/2017/03/01/new-york-times-manages-their-openapi-using-github/), and [Slack](http://apievangelist.com/2017/11/06/an-example-of-how-every-api-provider-should-be-using-openapi-out-of-the-slack-platform/) do, which I'll just keep in sync with. However, for the rest, I'm looking to maintain an independent Github repository for each API providers, providing a single repo, URL, and set of issues for discussing the evolution of the OpenAPI, Postman, and APIs.json indexes. Each project will also have [its own portal landing page](http://paralleldots.stack.network/), with generated API docs. It's a lot to maintain, but it is something I'm already doing behind the scenes in a database, and I might as well continue the work out in the open where I can solicit the help of the community, and build on the hard work of existing projects.
