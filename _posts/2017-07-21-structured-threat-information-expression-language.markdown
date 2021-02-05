---
published: true
layout: post
title: Structured Threat Information Expression (STIX)
date: 2017-07-21T13:00:00.000Z
tags:
  - API Evangelist
  - Security
image: 'https://s3.amazonaws.com/kinlane-productions/stix/stix-logo.png'
---
<p><a href="https://oasis-open.github.io/cti-documentation/"><img src="https://s3.amazonaws.com/kinlane-productions/stix/stix-logo.png" align="right" width="35%" style="padding: 15px;" /></a></p>
[I wrote about the opportunity around developing an aggregate threat information API](http://apievangelist.com/2017/07/10/opportunity-to-develop-a-threat-intelligence-apis-json/), and got some interest in both creating, as well as investing in some of the resulting products and services that would be derived from this security API work. As part of the feedback and interest on that post, I was pointed in the direction of the [Structured Threat Information Expression (STIX)](https://oasis-open.github.io/cti-documentation/), as one possible schema for definining and sharing the information I'm talking about. Here is a quick summary of STIX is from the website:

> Structured Threat Information Expression (STIX™) is a language for describing cyber threat information in a standardized and structured manner to enable the exchange of cyber threat intelligence (CTI). STIX characterizes an extensive set of CTI to include indicators of adversary activity, as well as contextual information characterizing cyber adversary motivations, capabilities, and activities and best courses of action for defense and mitigation.

I haven't dug into STIX too much, so I'm not making recomendations on the value it brings to the table yet, but I want to make sure we take a look at any existing work that was already on the, and make sure we aren't reinventing the wheel with any part of an aggregated threat information API. At first glance STIX looks like a pretty damn good start for a potential API schema, that speaks a common language, and is seeing adoption with other existing threat information storage and sharing providers.

I am adding STIX to my research into threat information sharing, and wider [API security research](http://security.apievangelist.com/). [I am currently diving deeper into API security thanks to investment from Elastic Beam, and I will be publishing a guide, as well as an API security white paper](https://apievangelist.com/2017/06/21/i-am-working-with-elastic-beam-to-help-define-api-security/) as part of the work. I'm going to try and provide some intelligence to a group of folks who expressed interest in developing an aggregate threat information sharing API. I'm hoping to better flesh out my thoughts on how API security and threat information sharing might feed into an overall API industry ranking scoring system that would help us understand which APIs are secure and observable enough to warrant usage, or not.
