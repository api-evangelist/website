---
published: true
layout: post
title: 'Benefits of Good API Design at the Gateway Layer'
image: https://s3.amazonaws.com/kinlane-productions2/algorotoscope-master/braceros-domingo-ulloa-walk-through-garden-tunnel.jpg
author:
 name: kinlane
tags:
- Gateways
- Design
- OpenAPI
- Resources
---
You can see the benefits of good API design practices all across the API ecosystem, but also across all of the web and mobile applications we use each day. If you suffer from the same condition I do, then you see these frustrating signals across the landscape. However, one of the most critical ways in which poor API design affects how we deliver technology is the API design for our API gateway APIs. Like every other API, the design of APIs for API gateways provide a very honest take of what capabilities a gateway offers. Let me show you with two separate examples:

- **Azure API Management** - APIs, Authorization, Backends. Certificates, Groups, Identity Providers, Loggers, OpenID Connect Providers, Policies, Portals, Products, Properties, Quotas, Reports, Subscriptions, Templates, Tenant, Users
- **NGINX Plus** - Alerts, Apps, Authentication Provider, Catalogs, Certs, Components, Controller, Definitions, Environments, Error Sets, Events, Forwarders, Gateways, Global Settings, Groups, Identity Provider, Instance Api, Instance Groups, Instance Templates, Integrations, License, Locations, Login Providers, Login, Metrics, Nodes, Policies, Portals, Published Apis, Reset Password, Roles, Services, Strategies, Users, Verify Authorization

While I can provide you with the same set of resources derived from other API gateway providers, both Azure and NGINX had their resources neatly tagged or organized using OpenAPI — meaning there was an OpenAPI available for each of these resource areas, which reflects a thoughtful approach to API design. I’ve generated OpenAPIs for other gateways, and will be massaging them to provide a neat list of the resources they make available, but these were pretty low hanging fruit because the gateways themselves have done the work—so they get the spotlight in this story.

