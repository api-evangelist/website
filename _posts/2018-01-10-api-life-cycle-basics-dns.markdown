---
published: true
layout: post
title: 'API Life Cycle Basics: DNS'
date: 2018-01-10T11:00:00.000Z
tags:
  - API Evangelist
  - DNS
image: 'https://s3.amazonaws.com/kinlane-productions/bw-icons/bw-dns.png'
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/bw-icons/bw-dns.png" align="right" width="45%" style="padding: 15px;" /></p>DNS is one of those shadowy things that tends to be managed by a select few wizards, and the rest of an organization doesn't have much knowledge, awareness, or access at this level. APIs has shifted this reality for me, and is something I'm also seeing at organizations who are adopting a microservices, and devops approach to getting things done. DNS should be a first class citizen in the API toolbox, allowing for well planned deployments supporting a variety of services, but also allow for logging, orchestration, and most importantly security, at the frontline of our API operations.

There are some basics I wanted to introduce to my readers when it comes to DNS for their API operations, but I also wanted to shine a light on where the DNS space is headed because of APIs. Some DNS and cloud providers are taking things to the next level, and APIs are central to that. Like most other stops along the API life cycle DNS is not just about doing DNS for your APIs, it is also about doing APIs for your DNS.

- **Dedicated API DNS** - I'm not in the business of telling you how to name the domain, or subdomain for your API, but you should have a plan, and be also considering having multiple subdomains, separating concerns across operations.
- **API Control Over DNS** - DNS is the frontline for your API infrastructure, even internally, and you should be able to programmatically configure, audit, orchestrate, and manage the DNS for your APIs using APIs.
- **Regional Consideration** - Begin thinking about how you name and manage your DNS with multiple zones and regions in operations--even if you aren't quite ready, you should be thinking in this way.
- [**Amazon Route 53 Releases Auto Naming API for Service Name Management and Discovery**](https://aws.amazon.com/about-aws/whats-new/2017/12/amazon-route-53-releases-auto-naming-api-name-service-management/) - Thinking about how service addressing can be automated, as well as standardized as part of the life cycle.
- [**CloudFlare**](https://www.cloudflare.com/) - You may not use them as a provider, but tune in and study the way CloudFlare does their DNS, as well as provides APIs for managing DNS.

DNS should be a prominent part of API operations, even with internal APIs. It is the first line of defense when it comes to security, as well as discovery, and allowing developers and partners to put APIs to work. DNS shouldn’t be separate from the rest of the API life cycle, and should be reachable by all developers, with logging at this layer shipped to be included within API life cycle operations. DNS needs to come out of the shadows and be something your entire team is aware of, with transparency around configuration, as well as standard practices for usage  across services.

I can't emphasize enough regarding how DNS providers like CloudFlare have shifted my view of DNS. Even if you aren't using them for your primary DNS, I recommend setting up a domain and playing around with what they have to offer. At least tune into their blog and Twitter account, as they are pushing the conversation forward when it comes to DNS, and API access to this layer. DNS in 2018 is much more than just addressing for your APIs, it is about logging, security, and much, much more. Bring it out of the background, and take another look at how it can make a bigger impact on what you are looking to achieve with APIs.
