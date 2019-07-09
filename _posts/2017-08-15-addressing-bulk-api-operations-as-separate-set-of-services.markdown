---
published: true
layout: post
title: Addressing Bulk API Operations As Separate Set Of Services
date: 2017-08-15T09:00:00.000Z
tags:
  - API Evangelist
  - Bulk
  - Design
image: >-
  https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories/cargo-ship-zoomed-in-on-sea_light_dali.jpg
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories/cargo-ship-zoomed-in-on-sea_light_dali.jpg" align="right" width="40%" style="padding: 15px;" /></p>Part of the feedback I've received from [the Human Services Data API (HSDA) evolution from v1.0 to v1.1](https://openreferral.github.io/api-specification/definition/) was that the API didn't allow for volume or bulk GET, POST, PUT, or DELETE. This was intentionally in the incremental release which focused on just making sure the API reflected 100% of the surface are for the Human Services Data Specification (HSDS). I wanted to separate out the needs of bulk API consumers, so that I could think about it separately from the more simple, micro-use integrations the default Human Services Data API would accommodate. I don't want the industrial grade needs of database and system administrators overriding the simple access needs of other individual API consumers.

To kick off my human services bulk API definition I wanted to spend some time looking at other bulk implementations from a handful of leading providers:

- [Intercom](https://developers.intercom.com/v2.0/page/bulk-api-overview)
- [ElasticSearch](https://www.elastic.co/guide/en/elasticsearch/reference/current/docs-bulk.html)
- [SalesForce](https://developer.salesforce.com/page/File:Bulk_overview.png)
- [Diffbot](https://www.diffbot.com/dev/docs/bulk/)

As I went through these implementations, and searched through Stack Overflow about bulk HTTP POSTs, I really didn't see much difference on the technical front. Bulk APIs are primarily about acknowledging heavy duty data consumption, and primarily used HTTP POST for allowing the submission of either a) large individual POST, or b) large number of POST. Technically there isn't much to them, where you start finding the nuance of bulk APIs over regular APIs is in the process surrounding the API implementation, things like having tasks, jobs, history, notifications, webhooks, email, and logging. Meaning there is just a lot more process and expectation around these APIs, which also most likely translates into more robust background architecture, and rules regarding the process involved with access.

Bulk APIs seem more about a separation of concerns. Bulk GET and POSTs require more infrastructure, and to do it properly you need process, and checks and balances to make sure a bulk operation is successfully executed, and there is sufficient history, notifications, and other events around bulk transactions. I'd say that bulk API operations should always be approached as a separate concern from the more mainstream web, mobile, single page application, embeddable, and spreadsheet applications. Providing a separate API subdomain, or paths allowing for the separation of infrastructure concerns, to make sure the API meets the availability concerns of both API provider and consumer. Next, I'll spend some more time mapping out the task or job oriented structure of bulk APIs, but also for other API operations, to help make sure I do not reinvent the wheel when it comes to the design of my bulk API operations.
