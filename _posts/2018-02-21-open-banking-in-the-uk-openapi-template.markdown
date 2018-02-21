---
published: true
layout: post
title: An Open Banking in the UK OpenAPI Template
date: 2018-02-21T12:00:00.000Z
tags:
  - API Evangelist
  - Definitions
  - Banking
  - Standards
image: >-
  https://s3.amazonaws.com/kinlane-productions/open-banking/open-banking-openapi.png
---
After learning more about [what Open Banking is doing for APIs in the UK](https://www.openbanking.org.uk/), I realized that I needed an OpenAPI template for the industry specification. There are six distinct schema available as part of the project, and I wanted a complete OpenAPI to describe which paths were available, as well as the underlying response schema. I got work crafting one from the responses that were available within [the Open Banking documentation](https://www.openbanking.org.uk/open-data-apis/).

Open Banking had schema available for their API definitions, but OpenAPI is the leading API and data specification out there today, so it makes sense that there should be an OpenAPI available, helping all participating banking API providers take advantage of all the tooling available within the OpenAPI community. To help support, I have published my Open Banking OpenAPI definition as a Github Gist:

<script src="https://gist.github.com/kinlane/57c720c18e4d0ad370ad92c0ab9613f7.js"></script>

I've applied this OpenAPI definition to the 17 banks they have listed, and will be including them in the next publishing of [my API Stack project](http://theapistack.com). Open Banking provides a common definition that can be used across many banks, and an OpenAPI template allows me to quickly apply the common template to each individual bank. Generating bank specific documentation, SDK and code samples, monitoring, tests, and other client tooling. Helping me put the valuable data being made available via each API to work.

I'd like to see more organizations like Open Banking emerge. I'd also like to help ensure they all make OpenAPI templates available for any API and schema specifications they establish. The API lifecycle is increasingly OpenAPI defined, and when you make your guidance available in the OpenAPI format, you are enabling actors within any industry to quickly get up and running with designing, deploying, managing, testing, monitoring, and almost every other stop along a modern API lifecycle. Increasing the chances of adoption for any API standards you are putting out there.
