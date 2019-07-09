---
published: true
layout: post
title: 68 Stops In A Comprehensive API Strategy Transit Map
date: 2018-03-16T09:00:00.000Z
tags:
  - API Evangelist
  - Lifecycle
  - API Transit
image: ''
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/transit/calcagno-2017-01-01.png" align="right" width="45%" style="padding: 15px;" /></p>I am refining my comprehensive list of stops that I highlight as part of the API lifecycle, or what I call [API Transit](https://apievangelist.com/2017/08/17/testing-out-the-concept-of-api-transit-instead-of-api-lifecycle/)--the stops that each of the services we deliver will have "pass through" at some point. I'm sharing this list with other team members as part of existing consulting arrangements I'm engaged in with Streamdata.io, as well as baking into my API transit work for some workshops I'm doing in April. All of these are available on [the API lifecycle section of API Evangelist](http://apievangelist.com/api-lifecycle/), but I will be pushing them to become a first class citizen on the home page of API Evangelist once again.

Here are 68 potential stops I'd consider for any microservice to be exposed to, as part of a larger API transit strategy map:

- **Definitions** - From the simplest definition of what a service does, all the way to the complete OpenAPI definition for each service.
- **Design** - The consistent design of each service leverage existing patterns, as well as the web to deliver each service.
- **Versioning** - Plan for handling changes, and the inevitable evolution of each service, its definitions, and supporting code.
- **DNS** - The domain addressing being used for routing, management and auditing of all service traffic.
- **Database** - The backend database schema, infrastructure, and other relevant information regarding how data is managed.
- **Compute** - How is the underlying compute delivered for each service using containers, serverless, cloud, and on-premise infrastructure.
- **Storage** - What does storage of all heavy objects, media, and other assets involved with the delivery of services.
- **Deployment** - Details services developed, and deployed, including frameworks and other libraries being used.
- **Orchestration** - Defining what the build, syndication, and orchestration of service deployments and integrations look like, and are executed.
- **Dependencies** - Identifying all backend service, code and infrastructure dependencies present for each service.
- **Search** - Strategy for understanding what search will look like for each individual service, and play a role in larger, more comprehensive search across services.
- **Proxy** - What proxies are in place to translate, cache, stream, and make services more efficient and secure?
- **Gateway** - What gateways are in place to defend, protect, route, translate, and act as gatekeeper for service operations?
- **Virtualization** - Details how how services and their underlying data are mocked, virtualized, sandboxed, and made available for non-production usage.
- **Authentication** - What is involved with authentication across all services, including key-based approaches, basic authentication, JWT, and OAuth solutions.
- **Management** - Information about how services are composed, limited, measured, reported upon, and managed consistently across all services.
- **Logging** - What is being logged as part of service operations, and what is required to participate in overall logging strategy?
- **Portal** - The strategy for how all services are required to be published to one or many public, private, and partner developer portals.
- **Documentation** - The requirements for what documentation is expected as part of each service presence, defining what the services delivers.
- **Support** - Relevant support channels, points of contact, and best practices for receiving support as an API consumer.
- **Communications** - Information about the communication strategy around each service, and how blogs, social, and other channels should be leveraged.
- **Road Map** - Details on a services road map, and what the future will hold, providing individual service, as well as larger organizational details on what is next.
- **Issues** - Expectations, communications, and transparency around what the current bugs, issues, and other active problems exist on a platform.
- **Change Log** - Translating the road map, and issues into a log of activity that has occurred for each service, providing a history of the service.
- **Monitoring** - What is required when it comes to monitoring the availability and activity of each individual service.
- **Testing** - The tactical, as well as strategic testing that is involved with each service, ensuring it is meeting service level agreements.
- **Performance** - How is the performance of each service measured and report upon, providing a benchmark for the quality of service.
- **Observability** - What does observability of the service look like, providing transparency and accountability using all of its existing outputs?
- **Caching** - What caching exists at the server, CDN, and DNS layers for each service to provide a higher level of performance?
- **Encryption** - Details regarding what is expected regarding encryption on disk, as well as in transport for each service.
- **Security** - Detailed strategy and processes regarding how each service is secured on a regular basis as part of operations.
- **Terms of Service (TOS)** - Considerations, and legal requirements applied to each service as part of the overall, or individual terms of services.
- **Privacy** - Details regarding the privacy of platform owners, developers, and end users as it pertains to service usage.
- **Service Level Agreements (SLA)** - Details regarding what service levels are required to be met when it comes to partner and public engagements.
- **Licensing** - Information about backend server code, API surface area, data, and client licensing in play.
- **Branding** - What branding requirements are in place for the platforms and its partners when it comes to the service.
- **Regulation** - Information regarding regulations in place that effect service operations, and are required as part of its usage.
- **Discovery** - How are services catalogued and made discoverable, making them accessible to other systems, developers, as well as to internal, partner, or public groups.
- **Client** - Information about clients being used to interface with and work with the service, allowing it to be put to use without code.
- **Command Line Interface** - The command line interface (CLI) tooling being used to developer or consume a service.
- **SDKs** - What software development kits (SDK) are generated, or developed and maintained as part of a service's operation?
- **Plugin** - What platform plugins are developed and maintained as part of a services operations, allowing it to work with other platforms and services.
- **IDE** - Are there integrated development environment (IDE) integrations, libraries, plugins, or availability considerations for each service?
- **Browsers** - Are there any browser plugins, add-ons, bookmarklets and integrations used as part of each service's operation?
- **Embeddable** - Information about any embeddable badges, buttons, widgets, and other JavaScript enabled solutions built on top of a service?
- **Bots** - What type of automation and bot implementations are in development or being supported as part of a service's operation?
- **Visualization** - Are there specific visualizations that exist to help present the resources available within any service?
- **Analysis** - How are logs, APIs, and other aspects of a service being used as part of wider analysis, and analytics strategy?
- **Aggregation** - Are there any aggregation solutions in place that involve the service, and depend on its availability?
- **Integration** - What 3rd party integrations are available for working with a service in existing integration platforms like IFTTT, and Zapier.
- **Network** - Information about networks that are setup, used, and allocated for each service governing how it can be accessed and consumed.
- **Regions** - Which regions does a service operate within, making it available in specific regions, and jurisdictions--also which regions is it not allowed to operate within.
- **Webhooks** - Are there webhooks employed to respond to events that occur via the service, pushing data, and notification externally to consumers?
- **Migration** - What solutions are available for migrating an API between regions, cloud environments, and on-premise?
- **Backup** - What types of backups are in place to bring redundancy to the database, server, storage, and other essential aspects of a service's operations?
- **Real Time** - Are there Server-Sent Events (SSE), Websocket, Kafka, and other real time aspects of a service's delivery?
- **Voice** - Are there any voice or speech enablement, integrating services with Alex, Siri, Google Home, or other conversational interface?
- **Spreadsheets** - What types of spreadsheet integrations, connectors, and publishing solutions are available for a service?
- **Investment** - Where do the funds for operating a service come from within a company, from external organizations, or VC funds?
- **Monetization** - What does it cost to operate a service, breaking down the one time and recurring costs involved with delivering the service.
- **Plans** - Outline of plans involved with defining, measuring, reporting, and quantifying value generated around a service's operation.
- **Partners** - An overview of partner program involved with a service's operation, and how a wider partner strategy affects a service's access and consumption.
- **Certification** - Are there certification channels available for applications and developers, defining the knowledge required to competently operate and integrate a service.
- **Evangelism** - What does internal, public, and partner evangelism efforts and requirements look like for a service, and its overall presence?
- **Showcase** - How are developers and applications using a service showcased, and presented to the community, demonstrating the valuable around a service?
- **Deprecation** - What are the plans for deprecating a service, involved the road map and communication around the individual and overall deprecation of service(s).
- **Training** - What training materials need to be developed, or already exist to support the service.
- **Governance** - How are all steps measured, quantified, aggregated, reported upon, and audited as part of a larger quality of service effort for each service.

I struggle calling this a lifecycle, as most of these do not occur in any sort of linear fashion. This is why I'm resorting to using the API Transit approach, as it is something that reflects the ever-changing, but also hopefully eventually more consistent nature of delivering microservices. Ideally, every microservice passes through each of these stops in a consistent fashion, making sure that they operate in concert with a larger API platform strategy. However, I know what the reality on the ground is, and know that not all of these relevant to each organization I am talking with, requiring me to trim down and change the order in which I present these.

If you'd like to talk about how these stops apply to your API operations, feel free to reach out. I'm doing more API lifecycle and governance strategy consulting with my partners Streamdata.io, and I'm happy to help your company, organization, institution, or government agency develop your own API transit map, which can be used across your API operations.
