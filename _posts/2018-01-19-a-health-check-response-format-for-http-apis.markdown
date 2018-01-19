---
published: true
layout: post
title: A Health Check Response Format for HTTP APIs
date: 2018-01-19T11:00:00.000Z
tags:
  - API Evangelist
  - Reliability
  - Monitoring
  - Standards
  - Definitions
image: >-
  https://s3.amazonaws.com/kinlane-productions/irakli/health-check-response-format-for-http-apis.png
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/irakli/health-check-response-format-for-http-apis.png" align="right" width="45%" style="padding: 15px;" /></p>My friend Irakli Nadareishvili, [has published a new health check response format for HTTP APIs](https://inadarei.github.io/rfc-healthcheck/) that I wanted to make sure was documented as part of my research. The way I do this is write a blog post, forever sealing this work in time, and adding it to the public record that is my API Evangelist brain. Since I use my blog as a reference when writing white papers, guides, blueprints, policies, and other aspects of my work, I need as many references to usable standards like this.

I am going to just share the introduction from Irakli's draft, as it says it all:

> The vast majority of modern APIs driving data to web and mobile applications use HTTP [RFC7230] as a transport protocol. The health and uptime of these APIs determine availability of the applications themselves. In distributed systems built with a number of APIs, understanding the health status of the APIs and making corresponding decisions, for failover or circuit-breaking, are essential for providing highly available solutions.

> There exists a wide variety of operational software that relies on the ability to read health check response of APIs. There is currently no standard for the health check output response, however, so most applications either rely on the basic level of information included in HTTP status codes [RFC7231] or use task-specific formats.

> Usage of task-specific or application-specific rformats creates significant challenges, disallowing any meaningful interoperability across different implementations and between different tooling.

> Standardizing a format for health checks can provide any of a number of benefits, including:

>  - Flexible deployment - since operational tooling and API clients can rely on rich, uniform format, they can be safely combined and substituted as needed.
>  - Evolvability - new APIs, conforming to the standard, can safely be introduced in any environment and ecosystem that also conforms to the same standard, without costly coordination and testing requirements.
> This document defines a “health check” format using the JSON format [RFC7159] for APIs to use as a standard point for the health information they offer. Having a well-defined format for this purpose promotes good practice and tooling.

Here is an example JSON response, showing the standard in action:

<script src="https://gist.github.com/kinlane/5bea1128ccada3b26ab534b7e4bb138d.js"></script>

I have seen a number of different approaches to providing health checks in APIs, from a single ping path, to proxying of the Docker Engine API for the microservices Docker container. It makes sense to have a standard for this, and I'll reference Irakli's important work from here on out as I'm advising on projects, or implementing my own.
