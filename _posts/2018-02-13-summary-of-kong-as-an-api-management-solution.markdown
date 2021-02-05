---
published: true
layout: post
title: A Summary Of Kong As An API Management Solution
date: 2018-02-13T13:00:00.000Z
tags:
  - API Evangelist
  - Management
  - Governance
image: 'https://s3.amazonaws.com/kinlane-productions/kong/get-kong-api.png'
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/kong/get-kong-api.png" align="right" width="45%" style="padding: 15px;" /></p>I was breaking down what the API management solution Kong delivers for a customer of mine, and I figured I'd take what I shared via the team portal, and publish here on the blog. It is an easy way for me to create content, and make my consulting work more transparent here on the blog. I am using Kong as part of several healthcare and financial projects currently, and I am actively employing it to ensure customers are properly managing their APIs. I wasn't the decision maker on any of these projects when it came to choosing the API management layer, I am just the person who is helping standardize how they are using API services and tooling across the API life cycle for these projects.

First, [Kong is an open source API management solution](https://konghq.com) with an easy to install [community edition](https://konghq.com/install/), and [enterprise level support when needed](https://konghq.com/kong-enterprise-edition/). They provide an [admin interface](https://konghq.com/api-admin-gui/), and [developer portal](https://konghq.com/api-dev-portal/) for the API management proxy, but there is also a growing number of community editions like [KongDash](https://ajaysreedhar.github.io/kongdash/), and [Konga](ttps://pantsel.github.io/konga/) emerging to make it a much more richer ecosystem. And of course, [Kong has an API for managing the API management layer](https://getkong.org/docs/0.12.x/admin-api/), as every API service and tooling provider should have.

Now, let's talk about what Kong does for helping in the deploying of your APIs:

- **API Routing** - The API object describes an API that's being exposed by Kong. Kong needs to know how to retrieve the API when a consumer is calling it from the Proxy port. Each API object must specify some combination of hosts, uris, and methods
- **Consumers** - The Consumer object represents a consumer - or a user - of an API. You can either rely on Kong as the primary datastore, or you can map the consumer list with your database to keep consistency between Kong and your existing primary datastore.
- **Certificates** - A certificate object represents a public certificate/private key pair for an SSL certificate.
- **Server Name Indication (SNI)** - An SNI object represents a many-to-one mapping of hostnames to a certificate.

Then it focuses on the core aspects of what is needed to help manage your APIs:

- **Authentication** - Protect your services with an authentication layer.
- **Traffic Control** - Manage, throttle, and restrict inbound and outbound API traffic.
- **Analytics** - Visualize, inspect, and monitor APIs and microservice traffic.
- **Transformations** - Transform requests and responses on the fly.
- **Logging** - Stream request and response data to logging solutions.

After that, it has a bunch of added features to help make it a scalable, evolvable solution:

- **DNS-based loadbalancing** - When using DNS based load balancing the registration of the backend services is done outside of Kong, and Kong only receives updates from the DNS server.
- **Ring-balancer** - When using the ring-balancer, the adding and removing of backend services will be handled by Kong, and no DNS updates will be necessary.
- **Clustering** - A Kong cluster allows you to scale the system horizontally by adding more machines to handle more incoming requests. They will all share the same configuration since they point to the same database. Kong nodes pointing to the same datastore will be part of the same Kong cluster.
- **Plugins** - lua-nginx-module enables Lua scripting capabilities in Nginx. Instead of compiling Nginx with this module, Kong is distributed along with OpenResty, which already includes lua-nginx-module. OpenResty is not a fork of Nginx, but a bundle of modules extending its capabilities.
- **API** - Administrative API access for programmatic control.
- **CLI Reference** - The provided CLI (Command Line Interface) allows you to start, stop, and manage your Kong instances. The CLI manages your local node (as in, on the current machine).
- **Serverless** - Invoke serverless functions via APIs.

There are a number of API management solutions available out there today. I will profile each one  I am actively using as part of my work on the ground. I'm agnostic towards which provider my clients should use, but I like having the details about what features they bring to the table readily available via a single URL, so that I can share when these conversations come up. I have many [API management solutions profiled as part of my API management research](http://management.apievangelist.com), but in 2018 there are just a handful of clear leaders in the game. I'll be focusing on the ones who are still actively investing in the API community, and the ones I have an existing relationship with in a partnership capacity. Streamdata.io is a reseller of Kong in France, making it something I'm actively working with in the financial space, and also something I'm using within the federal government, also bringing it front and center for me in the United States.

If you have more questions about Kong, or any other API management solution, feel free to reach out, and I'll do my best to answer any questions. We are also working to provide more API life cycle, strategy, and governance services along with [my government API partners at Skylight](http://skylight.digital), and through [my mainstream API partners at Streamdata.io](http://apis.how/streamdata). If you need help understanding the landscape and where API management solutions like Kong fits in, me and my partners are happy to help out--just let us know.
