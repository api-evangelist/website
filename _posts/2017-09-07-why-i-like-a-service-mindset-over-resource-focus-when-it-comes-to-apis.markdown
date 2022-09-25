---
published: true
layout: post
title: Why I Like A Service Mindset Over A Resource Focus When It Comes To APIs
date: 2017-09-07T13:00:00.000Z
tags:
  - API Evangelist
  - Microservices
  - Design
image: >-
  https://s3.amazonaws.com/kinlane-productions/human-services/human-services-docs-screenshot.png
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/human-services/human-services-docs-screenshot.png" align="right" width="40%" style="padding: 15px;" /></p>I am currently crafting a set of services as part of [my Human Sevices Data API (API) work](http://org.open.referral.adopta.agency/). The core set of services for organizations, locations, and services are grouped together as a single service, as this is what I was handed, but all the additional APIs I introduce will be bundled as separate set of individual services. Over the last couple of weeks I've introduced seven new services, with a handful more coming in the near future. I'm enjoying this way of focusing on services, over the legacy way that is very resource focused, as I feel like it lets me step back and look at the big picture.

When I was defining the core API for this work I was very centered on the resources I was making available (organization, locations, and services), but once I took on a service mindset I began to see a number of things I was missing. With each service I find myself thinking about the full life cycle, not just the APIs that deliver the service. I'm thinking about the easy ones like design, deployment, and management, but I'm also thinking about monitoring, testing, and security. Then I'm delivering documentation, support, communications, and thinking about my monetization strategy, and access plans. I'm not just doing this once, I am thinking about it in the context of each individual service, as well as across all of them, taking care of the business of the services I'm delivering, not just the technical.

While some folks I talk to look at some of this as repeat work across my projects, I just see them as common patterns, that I should be reusing, refining, and delivering in consistent ways. I'm thinking about delivering the technology in a consistent way, and the operational, but I'm beginning to think about education, training, and how I can help folks on the provider and consumer side of things learn how things are working. I'm not just doing the technical heavy lifting to deliver APIs and then walking away, I'm bundling each search with what is needed to be valuable and successful as an actual service, that is API driven from start to finish. The service is accessible via an API, but it is also delivered, managed, and supported using APIs--everything has an API.

The Human Services Data APIs (HSDA) I am delivering aren't just a single API, or set of service. They are an open source set of services that I'm putting out there for others to adopt and deliver as part of their own operations. I don't want these to just be plug and play APIs, and want them to be plug and play services that deliver the information people need to find vital services in their community. Thinking of my APIs as services, and breaking them up into independent microservices helps me address the technical, business, and politics of delivering the technical components cities and organizations are needing. I've been pushing the business and politics of APIs since I've started, and trying to doing things in as small pieces as I can since the beginning, but the microservices conversations I've been tuning into have helped me think beyond the tech, the size, and actually consider how I'm doing this to deliver services to humans--it just an interesting twist that my primary project is all about delivering human service microservices. ;-)
