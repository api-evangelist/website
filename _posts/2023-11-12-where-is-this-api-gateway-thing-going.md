---
published: true
layout: post
title: 'Where Is This API Gateway Thing Going?'
image: https://s3.amazonaws.com/kinlane-productions2/algorotoscope-master/america-immigration_dumping-ground-gatew-into-field.jpg
author:
    name: kinlane
tags:
- Gateway
- Management
- Governance
---
According to Gartner, the full lifecycle API management quadrant is going away, but acknowledges in 2023 the API gateway continues to enjoy an outsized amount of focus when it comes to internal and public API operations. The gateway is important, and tends to be where attention is focused in good times and bad, but other stops along the API life cycle are also critical to the conversation as well, and I’m looking to understand more about why, while trying to understand where things might be going.

Closing my eyes and looking back at the last 15 years of API gateways feels a lot like standing in the middle of Times Square in New York City with all the billboards flashing at you, characters working to get your attention, and an enormous amount of traffic heading north, south, east, and west. Sometimes I feel like I have a handle on where we are when it comes to the API gateway, and how we got here, but other times I feel like I am drowning in vendor and analyst narratives. I wanted to refresh my memories of all of the API gateway narrative from this century and see if I can’t make some predictions about where things are going.

At first glance I would say we are in the fourth generation of API gateway evolution this century, with three distinct geological layers of API gateway infrastructure and belief systems, and a mix of opportunity and baggage shaping where things might go. Along the way I feel like we’ve accumulated a wealth of API gateway capabilities, but it is the wider ecosystem that has emerged around API gateways that has generated most of the wealth in my opinion–the gateway just gets credit for it. Let’s roll things back to the year 2000 and start this journey, walking though how we got here, and do some speculation on where things might be headed.

## The Service-Oriented Architecture (SOA) Dinosaur Age
Our grandfather's APIs were known as Web Services, and they used XML for messaging, provided XSD for a schema, as well as a WSDL for discovery. Honestly the SOA age was better planned than this sprawling API landscape we are drowning in today, but this fact also contributed to it falling out of favor. SOA was too much. Too complex. Service Oriented Architecture, or simply SOA was master planned from the top down, and along the way we saw enterprise-grade gateways emerge specializing in general or industry specific web service implementations for the enterprise, setting the stage for the API gateway we depend on today.

Web service gateway were early proprietary web servers deployed as SOA appliances within the enterprise for internal and partner access. I would say that the real differences between API gateways today and web services of this era was really about the number of features, and awareness of the web. SOA was a legitimate attempt at solving the problem at scale, but we’d learn over the next twenty years that it takes a much looser and scrappier approach to our services. SOA is still in operation within many enterprises, and won’t likely go anywhere soon, but the API gateway has gone through several iterations since then, which I will explore in more detail below.

## Evolving From SOA to the API Gateway
I will showcase additional API gateways below, but I wanted to start this journey focusing on the three companies I feel rose to the head of the pack when it came to market share and mind share within the enterprise. Like SOA these API gateways were a top down affair, with enterprise IT leadership making the decision to implement, and developers often left out of the discussion.

- **MuleSoft** - Dominating the discussion through a strong sales legacy that landed AnyPoint into the enterprise, and leading to an acquisition by Salesforce. 
- **Axway** - Axway isn’t a leader, but has managed to keep pace while still innovating, bridging the SOA realm to the API realm in some progressive ways.
- **Apigee** - Apigee ended up a Google acquisition after IPO’ing, but has definitely taken a strong second place after Mulesoft when it came to API industry mindshare..

I’d say that when I go into most enterprises I am seeing Mulesoft or Apigee as legacy cornerstone API gateway. I’d say that I’ve seen the most innovation around Apigee, with additional abstract layers on top to weave it into platform operations. I am sure plenty of people will snicker at my decision to place these first, but from my vantage point they led the pack when it came to getting the attention of the enterprise from 2010 through 2020. 

## Baking API Gateways Into the Cloud
Mulesoft, Axway, and Apigee definitely led the conversation when it came to the evolution of the API gateway, but I’d say that the cloudification of the API gateway was the moment where I knew all of this was serious business. Microsoft had acquired Apiphany and got to work on their Azure solution(s), and Google acquired Apigee as they also invested in their own solution, and Amazon did it the Amazon way and delivered the AWS API Gateway.

- **Amazon Gateway** - AWS offers HTTP and Websocket capabilities across their regions.
- **Azure API Management** - Weaving their API management acquisition into their CI/CD flows.
- **Google (Apigee)** - Shaping their enterprise offering to behave like something you use in the cloud.

I’d say that Apigee’s offering is the most industrial grade API gateway solution baked into the cloud, but they all reflect a seismic shift in the API management landscape. The gateway was now a commodity. This moment was when we started to see API management fracture and begin to expand into a buffet of services like portals, documentation, SDKs, mocks, testing, and other essential API services. Baking APIs into the cloud made the API gateway another one of the essential commodities in the toolbox alongside storage, compute, and database. 

## The API Gateway Status Quo
As the wheels of the capitalist machine consumed the API gateway and baked into the clouds, we saw enterprise teams begin their microservices journey, and mainstream business began waking up to the API-first transformation; a new, much smaller version of the API gateway emerged to provide developers with what they needed on the ground within the enterprise. The older guard of API gateway providers were heavily focused on public APIs, while the real need within the enterprise for the exploding world of microservices were addressed through a handful of much smaller API gateways.

- **Kong** - The poster child for the modern API gateway movement, providing the open-source solution teams are needing, which is something Kong is working hard to monetize.
- **Tyk** - This was the first new modern API gateway that was developed from the ground up, providing exactly what teams were needing on the ground in a performance package.
- **NGINX** - While not a first-class API gateway, I see NGINX deploy and cobbled together in ways that end up doing a lot of the work that a gateway does, making it something to tune into.

These gateways have worked to meet the needs of developers who were ignored while enterprise leadership made their purchasing decisions with the older guard of API management solutions, meeting the specific needs you have when publishing internal APIs while avoiding the bloatware that came with listening to API management vendors. These vendors capitalized on the commodification of the API gateway, and made something that was small, but worked in a distributed and potentially federated way.

## Reflections At Where This Might Go
I suck at predicting the future, but after looking through all of the API gateways out there, you begin to get a glimpse at several possible futures. I really do not know what the markets will ultimately find interesting, but when it comes to what I find interesting, these API gateways offer what I think should be next. While I think the legacy providers will continue to shape the enterprise, and the cloud, as well as Tyk and Kong will keep defining the conversation, I think these providers are worth looking at to understand what it is we should be investing in next across our  API operations.

- **Cloudflare** - I like Cloudflare’s approach to DNS, and I think their vision of an API that is baked into the fabric of the web, making our APIs programmable at the edge is a very compelling future.
- **Easegress** - Kubernetes is definitely a trend across API gateway deployment, Easegress looks to be investing heavily in the intersection of Kubernetes and service mesh to get things done.
- **EnRoute** - EnRoute looks to be operating at the intersection of Kubernetes and cloud-native, building on the momentum of the API gateway being baked into the fabric of the cloud.
- **Envoy** - Another bedrock Kubernetes based API gateway that has grown in popularity over recent years, their expressive, extensible, and role-oriented APIs paint another potential future.
- **Gravitee** - I found Gravitee’s event-driven, visual approach to the API gateway to offer a future that I think will match the pace of industry, while making it accessible to business stakeholders.
- **KrakenD** - Emulating what I think is similar to Tyk, KrakenD has focused on a complete rewrite of the API gateway to focus on permanence, helping enterprise organizations deal with APIs at scale.
- **Kusk** - Offering a declarative OpenAPI vision merged with Kubernetes to help shape how we approach delivering and managing our APIs using a common API contract as the configuration.
- **Reactive Interaction Gateway** - This approach is building on the momentum of the microservices shift in the API gateway landscape, keeping things  modular, reusable, and distributed. 
- **Solo** - LIked Easegress, Solo is all about the Kubernetes powered service mesh vision of how we can deal with API sprawl at scale, helping us orchestrate the API vision we want to see.
- **webMethods** - I found the multi-cloud approach of webMethods worth noting, acknowledging that we don’t want everything across all clouds, but operating something across all clouds is a future many experience today.
- **Zuplo** - I really like the programmable GitOps approach Zuplo takes to delivering APIs at the edge, making our API infrastructure the modular, reusable, and federated landscape we need.

This is where I am getting my inspiration for what the future may hold, but I want to make sure and refresh my memory regarding bedrock API gateway features across everybody in the space. I didn’t just cherry pick the API gateways I was familiar with, I looked at all the gateways to help develop an awareness regarding which features were the most fundamental features, as well as the leading edge capabilities to be delivered by these leaders. 

## Honorable API Gateway Mentions
The remaining gateways I looked at size up with others when it comes to many of the core features, but I am also considering the overall mindshare as well as market share. For me, the story is what matters the most, and the features you offer are second, but I want to make sure I listed all of the providers I looked at. 

<span style="font-size: 18px; font-weight: bold; font-style: italic; text-align: center;">Akana, Ambassador Emissary-Ingress, Apinizer, APISIX, App42, IBM API Connect, Nevatech, Oracle, Sensedia, SnapLogic, Spring Cloud, Tibco, WSO2, 3Scale, API Umbrella, Boomi, Broadcom Layer7, Fiorano</span>

I considered bumping up Spring Cloud into my stack due to the ubiquitous nature of Java, and it is sad to put some solutions I’ve worked with in the past here, but ultimately I don’t see anything too innovative here, or at least innovation that isn’t seeing much adoption—maybe my mind will change over time, but for now, I don’t have time to look to closely here.

## The Core API Gateway Capabilities
Across the almost forty API gateways I spent time aggregating all of the features I came across, to help me see what capabilities across all providers. I learned a lot doing it, and was able to better understand the space better, but also standardize how I see things. I think we all have slightly different definitions of what an API gateway does. Depending on your view of things, experience in the space, and role in the API lifecycle, you will see all of these areas differently.

### Security
This is the top thing I think business leadership thinks an API gateway does, keeping our digital resources safe at scale, using a mix of policies that help secure the enterprise internally and externally across applications and integrations–providing a pretty standardized spectrum of security policies.

<span style="font-size: 18px; font-weight: bold; font-style: italic; text-align: center;">Auth0, AWS Cognito, Access, Access Control Lists (ACL), Audit Logs, Auth Z, Auth N, Auth0, Authentication Providers, Automatic HTTPS, AWS Cognito, AWS IAM, Basic Authentication, Certificate Signing Request (CSR), Certificates, Cross-Origin Resource Sharing (CORS), JWT, Keys, Mutual TLS, OAuth 1.0, OAuth 2.0, Roles</span>

This is an area you see Open Policy Agent (OPA) emerge as a way of defining policy, which I think will have to occur across all of these areas. We are going to need to standardize and harden the security at the API gateway layer across protocols, as well as the increasingly sprawling enterprise API landscape.

### Traffic
This is the second area people tend to respond when I ask them what an API gateway does for the enterprise, with most of these areas satisfying the technical needs across teams. I’d say that this area tends to provide the most business value, but provides engineering teams with the knobs and levers they need to dial everything in at scale.

<span style="font-size: 18px; font-weight: bold; font-style: italic; text-align: center;">Circuit Breaker, Clusters, Compression, Conditional Routing, Content-Based Routing, DNS, Dynamic Routing, Edge, Egress Controller, Failover, Forwarders, Global Rate Limiting, Header-based routing, Health Checks, Ingress Controller, Load Balancer Routing, Paths, Per-User Rate Limiting, Plans, Post Processing, Pre Processing, Proxy, Quota Reset, Quotas, Rate Limits, Regions, Request Size Limiting, Request Validation, Response Types, Reverse Proxy, Routes, Service Mesh, Session Persistence, Telemetry, Throttling, Timeouts, Tracing</span>

The API gateway is the freeway interchange of the digital landscape. Managing traffic consistently at scale will continue to be one of the top challenges for enterprise organizations as they continue to add applications, integrations, and need automation to get business done. This area will keep the API gateway a power center when it comes to translating digital into business value for some time to come.

### Mediation
Next, organizations are needing to mediate the flow of information inside and outside the firewall using the API gateway, without getting in the way of business. Mediation capabilities have the potential to make API gateways a bottleneck, but also make it the value generation center when done well in a consistent manner across all APIs, employing a policy-driven approach to mediating API traffic.

<span style="font-size: 18px; font-weight: bold; font-style: italic; text-align: center;">Audit Logs, Caching, Context Persistence, Cross-Origin Resource Sharing (CORS), Custom Exception Handling, Custom Request Filters, Custom Resource Definitions (CRDs), Custom Resources, Declarative Policy Engine, Edge Policy Console, gZip, Hot-Update, Ingress Controller, JSON Validation, Message Inspection, Monetization Limits, Redaction, Regex Filters, Request Size Limit, Request Termination, Request Validation, Response Status Codes, Response Templates, Retries, SOAP Validation</span>

As the need to govern and regulate API traffic grows inside and outside the enterprise, mediation is going to play a huge role in ensuring government and enterprises are able to maintain control over what is happening. The API gateway will continue to expand its power when it comes to the increased scrutiny of platforms, AI, and other digital aspects of how business gets done.

### Transformation
Transforming all or part or part of an API message is common practice. At a minimum, shifting the headers is essential, but transforming the structure and content is also a common occurrence. I don’t think that the enterprise will be able to “digitally transform” as fast as they need to keep pace, but I think that API gateways will help incrementally transform us at scale.

<span style="font-size: 18px; font-weight: bold; font-style: italic; text-align: center;">GraphQL to REST, REST to GraphQL, Mapping Templates, JSON to CSV, CSV to JSON, Request Transformation, Response Transformation, SOAP to REST, XML to JSON, XSL Transformations</span>

I could see a gateway that specializes in just transforming API payloads to and from common formats, not just XML, JSON, CSV, and YAML, but other platforms, industry standards, and other needs. Understanding the technical and business details of transformation at the API gateway level is  something I predict will continue to grow as a way to manage the chaos and sprawl.

### Virtualization
I am fascinated why the mocking of APIs isn’t more of a default  mode of gateways. It seems like API gateways should support design-first out of the gate and make it easy to virtualize based upon an API contract or on traffic. I did find evidence of it across many of the gateways I looked at, but it isn’t a core part of the API lifecycle as I would have hoped.

<span style="font-size: 18px; font-weight: bold; font-style: italic; text-align: center;">Static Mocking, Dynamic Mocking Data Virtualization</span>

I really wish that someone would do a gateway that focused exclusively on streamlining the development of new APIs, and mocking would provide an important element of this. I think if we are going to get more developers to see the benefits of design-first, we are going to have to make it as easy as possible, and generate rich  mocked experiences all along the way.

## Change Management
Managing change should be one of the top capabilities of any API gateway, yet it is still difficult to effectively manage change at scale across APIs. Every change should be clearly documented, well-versioned, and communicated by default. There are a handful of change related capabilities I noted in my review of API gateways, but not as many as there should be.

Breaking Changes, Diff, Versioning, Canary Releases, Stages, Rollback
You shouldn’t be able to introduce breaking changes via an API gateway. I just don’t get this one. I know many have focused on vertical scale, where others invested in horizontally and distributed scaling, but I’d like to learn about the providers who abstracted away the friction created when adding, updating, and deprecating our APIs.

### Code Execution
I am not a fan of gateways doing too much, they should do the core things well, and maybe specialize in one or two areas, but I am a fan of the ability to extend the gateway with custom code, scripts, and automation. I think that without the right guard rails custom code can become a liability, but when done well, it is definitely an asset.

<span style="font-size: 18px; font-weight: bold; font-style: italic; text-align: center;">Go, Java, JavaScript, Lua, Martian DSL, Node.js, Python,TypeScript, WASM</span>

I think NGINX owes its inclusion here due to its versatility, in which its customizability plays a role. I’d say I am most interested in WASM at this layer. Think of the possibilities when it gets fully backed into not just the API gateway, but a future where the API gateway is at the edge like what CloudFlare and Zuplo are doing.

I feel like security, traffic, mediation, transformation, virtualization, change management, and extensibility are the core of what a modern API gateway should do. It is the baseline. There should be standard definitions, policies, and content to support interoperability in all of these areas across different API vendors, both open source and commercial.

## The Platform API Gateway Capabilities
Next up are all of the capabilities that have been historically bundled with API gateways to sell the last decades worth of API management and Full API Lifecycle Management (FLAPIM) solutions, and are now apparently being “unbundled”. While they were confusingly bundled historically, once the commoditization of core capabilities began happening this list of capabilities began being spun off as startups, and stand-alone open-source solutions catering to API producers looking to manage their operations.

<span style="font-size: 18px; font-weight: bold; font-style: italic; text-align: center;">Accounts, Activity, Alerts, Analytics, Application Performance Management (APM), Applications, Automation, Catalogs, Dashboards, Design, Developers, Discovery, DNS, Documentation, Domains, Environments, Extensions, Gateways, Governance, Licensing, Logging, Mocking, Models, Monetization, Monitoring, Networking, Observability, Performance, Policies, Portals, Products, Projects, Reports, Repositories, Roles, SDKs, Search, Serverless, Specifications, Standards, Teams, Templates, Testing, Threat Protection, Tracing, Workspaces</span>

These capabilities exist within varying orbits of the gateway but aren’t critical to be in the run time, despite what many legacy API gateways will sell you. While they are bundled by API management providers, they can just as easily be done as add-ons, sidecars, plugins, or external API-driven platform capabilities. Each of these areas should have its own orbit and relationship with the API runtime, and should be adjacent or separate from the API gateway, but stitched together as part of a coherent API lifecycle.

## Employing API Contracts
One of the most defining characteristics of next-generation or at least progressive gateways is the way that they have adopted API contracts. The API service providers who are not very far along in their own API journey are using OpenAPI to simply publish documentation or power other platform capabilities. While other service providers have seen the power of API contracts as a configuration for the runtime, but also policy generation and enforcement in real time.

<span style="font-size: 18px; font-weight: bold; font-style: italic; text-align: center;">OpenAPI, AsyncAPI, JSON Schema, Protocol Buffers, Avro, Thrift, Spectral, Open Policy Agent (OPA), Extensions</span>

For me this layer is separate from any specific platform capability as well as the programmability of the gateway. API contracts are more about providing a declarative interface for each API, covering not just the design of the API, but also all of the policies and configuration of the gateway, shaping both upstream and downstream behavior.  Contracts are how we are going to map, iterate, and evolve the sprawling API landscape at scale across the enterprise, and the industries they operate in.

## The Upstream Protocols
When you use AWS, Azure, or Google cloud API gateways you end up with a wealth of backend services at your disposal, but commercial and open-source vendors tend to focus on these protocols to wire up the backend of their gateways to their operations. 

<span style="font-size: 18px; font-weight: bold; font-style: italic; text-align: center;">AMQP, AWS Lambda, Database, ERP, FTP, GraphQL, gRPC, HTTP 1.1, HTTP Long-Polling, HTTP/2, HTTP/3, IMAP, JMS, Kafka, MQTT, NATS, POP3, RabbitMQ, Server-Sent Events (SSE), SMTP, SOAP, TCP, UDP, WebSockets</span>

These protocols represent the ways that enterprises are wiring up their internal systems to move digital resources around and execute the capabilities needed to do business. W/hile there are many other integrations and connections to upstream resources, this reflects the baseline of what is in use today.

## The Downstream Protocols
API gateways provide a number of common protocols for downstream API consumers to engage with enterprise digital resources and capabilities made available internally, with partners, and the public. While HTTP is definitely leading the conversation in implementations, the modern enterprise API landscape is increasingly multi-protocol.

<span style="font-size: 18px; font-weight: bold; font-style: italic; text-align: center;">AMQP, GraphQL, gRPC, HTTP 1.1, HTTP Long-Polling, JMS, Kafka, MQTT, NATS, RabbitMQ, Server-Sent Events (SSE), SOAP, TCP, UDP, WebSockets, HTTP/2, HTTP/3</span>

This is an area I predict a lot of investment by enterprise API platform teams and API service providers in coming years. We will see a load-balancing of internal and external APIs across these protocols, but the standardizing of policies across each of the protocols will become one of the most critical areas we will need to see investment.

## API Gateway Extensibility
Overlapping with the execution of code at the API gateway level, but with a focus on specific service instead of just code execution. I think that API gateways directly reaching out to existing cloud services as a capability, baking in an existing open-source solution, or going full plugin and add-on goes well beyond just code execution.

<span style="font-size: 18px; font-weight: bold; font-style: italic; text-align: center;">Add-Ons, Application Dynamics, Auth0, AWS Kinesis, AWS Lambda, Azure Event Hubs, CI/CD, Consul, Database, Datadog, Dynatrace, Etcd, Grafana, HTTP Callout, Istio, LinkerD, Plugins, Prometheus, Serverless, Service Mesh, Side-Car, WASM</span>

Some of these I should be grouping as part of platform capabilities above, but I think extensibility will need more consideration about how I group things versus how the API gateway providers I reviewed are grouping things. I am more about grouping things based upon the common view for the enterprise perspective, and not just the API service provider.

## API Gateway Automation
The adoption of API contracts overlaps with and enables the increasing automation of API gateways. With a well defined contract for the surface area of an API, and the lifecycle around them, you can import, export, continuously integrate and deploy your APIs, as well as the resources and capabilities your APIs enable.

- **Import** - You can import an API contract to override the definition of an API at any stage, introducing changes into the API runtime using one or many API contracts or artifacts.
- **CI/CD** - API gateways are often the center of the build process for APIs being deployed, but also the applications and integrations that are consuming APIs, automating with CI/CD.
- **Publish** - Just as with the import of API contracts, API gateways enable the publishing of all or part of an API contract, distributing and federating the API surface area wherever it is needed.
- **Export** - The exporting of API contracts from an API gateway allows for the backing up or maintaining of API contracts via external systems, expanding API operations where needed.
- **API** - Today’s API gateway has APIs. Automating the API lifecycle around your gateway using the API gateway API is how you do more with less, while ensuring operations are repeatable.

Automating the API lifecycle around the API gateway is how the deployment and management of APIs is increasingly getting done. Gateways are getting baked into the software development lifecycle (SDLC) at enterprises, by building on existing CI/CD workflows, but also taking advantage of API contracts to make APIs more interoperable, but also using APIs to ensure our APIs are interoperable.

## The API Dimensions That Really Matter
This look into API gateways, distilling down their capabilities and policies can be grouped into several relevant areas that I feel will be shaping the next generation of API operations. I see a number of specific areas that will shape how gateways are put to work across the enterprise, and determine how to scale, optimize, and govern within and outside the enterprise as part of the wider API economy.

- **Contracts** - Machine-readable contracts will shape the runtime, and will be how we maintain alignment across the API Lifecycle.
- **Lifecycle** - A platform approach to bridging the gateway across the lifecycle will be needed to go beyond what we know as API management.
- **Multi-Protocol** - HTTP has got us here and will take us into the future, but currently there are numerous protocols we need to support.
- **Multi-Pattern** - Supporting many different patterns, synchronous & asynchronous, event-driven, and providing a diverse API toolbox.
- **Multi-Vendor** - It is common for enterprise organizations to have API gateways from multiple vendors, providing a mix of gateway solutions teams can use when securing APIs or managing access to digital resources and capabilities within a specific cloud.
- **Multi-Gateway** - As much as leadership would like to centralize the gateway, we are living in a multi-gateway reality, so deal with it.
- **Multi-Cloud** - A utopian multi-cloud reality doesn’t exist, but we will need to be able to function across almost any cloud available today.
- **Local / On-Premise** - Offering a developer that developers can use locally to do what they need, while keeping in alignment with staging, and producing through the SLDC.
- **Edge** - Delivering APIs, where they are needed to support different types of consumers, is rapidly shaping how we put API gateways to work.
- **Regions** - Overlapping with edge considerations, but specifically addressing regulatory and data sovereignty is a top consideration.
- **Orchestration** - Making to existing Kubernetes and containerization orchestrations appears to be a top approach for many operations.
- **GitOps** - Further mapping the gateway to the existing software development lifecycle and equipping teams is where things are at.
- **Policies** - Defining, standardizing, enabling, enforcing, and evolving upon policies is going to be the top way that API Operations are shaped.
- **Centralization** - Many enterprises have a single centralized gateway handling all traffic coming from outside the enterprise via a single entry point. That provides an industrial-grade way of handling traffic coming in and out of the enterprise.
- **Federation** - Enterprises will have to have a federation strategy when it comes to dealing with the API gateway across lines of business and teams.
- **Observability** - Going beyond availability and leveraging the rich operations data at runtime to inform and enable developers earlier in the life cycle.
- **Programmability** - Tomorrow’s gateway will have to be programmable to keep up with the pace of change that exists across our operations.
- **APIs** - If our gateways don’t have APIs we will find ourselves in the same place we were ten years ago with an API strategy for our applications.
- **Plugins** - The extensibility of gateways via plugins and extensions will augment gateway capabilities with what is needed by teams.
- **Declarative** - Other YAML and JSON configuration approaches will always exist outside of standards, requiring custom declaration to shape gateways and APIs.

After setting out the core and platform capabilities I see across API gateway providers I feel like these areas are what really matter the most. I don’t see the number of APIs we are deploying slowing down anytime soon, and I think these are the dimensions where the space will expand, and help us increase the velocity of our API operations.

## Multi-Gateway Governance & Policy Management
While many of these API gateway providers each speak their own dialects when it comes to the policies used to shape the core, platform, and other API gateway capabilities here, there are hints of standardization of policies, schema, and the words we use at this layer. Regardless of the realities of the moment across API providers, I am hopeful for a standardization in policy management across these areas.

- **Caching ** - Providing a standard shape to what caching means across your APIs, helping automate and improve caching at the API gateway layer, improving overall performance.
- **Cross-Origin Resource Sharing (CORS)** - Ensuring that CORS is not an area of friction for teams producing APIs, or consumers putting them to work, establishing common policies.
- **Keys** - Having consistent way to issue, apply, and turnover keys across API consumption is how the security of APIs will be automated and scaled, while keeping easy to apply everywhere.
- **OAuth** - The OAuth standard should be automated in how it is applied across API contracts, and the consumers putting those APIs to work, leveraging well defined scopes for all API resources.
- **Plans** - The plans, packages, and features available for each API should be defined using a common set of policies that reflect the business objectives of the platform in near real-time.
- **Rate Limits** - The limitations placed upon consumers across all APIs should follow a common set of policies that reflect the technical, but also business constraints applied to operations.
- **Paths** - API policies are how we shape the aisles in our digital API stories, keeping everything organized and in its place, with sensible signage always available via consistent documentation.
- **Models** - Every digital bit that passes through the gateway should fit into a specific set of predefined policies that govern the shape of models applied across all APIs in production.
- **Request Transformation** - The transformation of API requests as they are received should be informed through a standard set of policies, rules, and schema that keep everything consistent.
- **Request Validation** - The shape of every request is known, and validation should occur frequently to help ensure the high quality of data is sent in applications and integrations. 
- **Request Size** - The size of API requests should be well defined using a standard set of policies, helping the API gateway tame the scope of API requests being made across all APIs.
- **Response Size** - The size of API responses should be well defined using a standard set of policies, helping the API gateway keep API responses from taking up too many resources.
- **Response Transformation** - The transformation of API responses as they are sent should be informed through a standard set of policies, rules, and schema that keep everything consistent.
- **Pagination** - The pagination of larger data sets is standardized by establishing common policies that can be applied across teams to further shape API responses to optimize API consumption.
- **Stages** - Establishing a common set of development stages for APIs at the gateway level helps harden the technical and business aspects of APIs as they are deployed and iterated upon.
- **Tags** - Having a common vocabulary for tagging APIs, as well as apply to other elements of the API lifecycle, help improve discovery and organization of the API landscape via the gateway.
- **Logging ** - Standardizing how we log APIs across teams using the gateway helps establish policies that govern the deployment, configuration, and use of logs generated across APIs.
- **Tracing** - Establishing policies that enable and guide tracing provides API producers and consumers with a standardized way to troubleshoot and support API consumers in new ways.
- **Versioning** - To get a handle on the change occurring across a gateway, the versioning of APIs and other artifacts across the API lifecycle will need a common set of policies to enforce.

We are going to need a common vocabulary if we are going to expect to have a handle across these dimensions for hundreds, let alone thousands of APIs. How these areas are deployed, configured, and standardized across not just many APIs, but also many APIs using different protocols, patterns, vendors, and clouds. We need to keep standardizing our policies beginning with Open Policy Agent, Spectral, but also keep expanding the interoperability and reuse at this dimension.

## The Top API Gateway Differentiators
Gateways do a wide range of things. While the core gateway capabilities are fairly short, the list of policies and ways you can extend the legacy and modern gateway is quite expansive. However, there are a handful of areas that I feel really differentiate the next-generation gateways from what is the status quo. These are all of the things that differentiated the API gateway providers from each other, providing a list of things that grab my attention, but hopefully also point to some possible futures that we may want to live in..

- **Top-Down** - When an API gateway website and marketing materials speak to the C-Suite you know you are in for a different set of API capabilities that will shape what is possible.
- **Bottom-Up** - When an API gateway website speaks to developers, DevOps, and platform teams you can expect another set of capabilities, setting the table with a different set of capabilities. 
- **Multi-Cloud** - The API gateway is baked into the cloud, but deploying and managing APIs across clouds without friction won’t matter to everyone, but to those who it does, this will shape decisions.
- **Multi-Protocol** - Standardizing APIs to just work across multiple protocols, standardizing when and how we use the common set of API protocols, making an impact on how a gateway is adopted.
- **Multi-Pattern** - REST, GraphQL, gRPC, and other common patterns are applied across multiple protocols, and the gateways are where these decisions are made to support different teams.
- **Multi-Region** - When it comes to data sovereignty, the API gateway will be the broker of where an API is produced and consumed, helping shape the API landscape based upon real borders.
- **Edge** - Like multi-region, but for more business needs, the API gateway will shape the enterprise landscape by pushing APIs closer to where consumers are, optimizing performance.
- **Contracts** - API contracts are how transactions are defined in the API economy and are how enterprises will standardize how they do business across thousands of unique digital resources.
- **Policies** - Standardizing how we express and enforce policies across every API, no matter what protocol or pattern is employed, or gateway deployed will be essential to the future of APis.
- **Federation** - The ability to federate APIs across different gateways defined by region, domain, or other bounded context in consistent ways using the same policies will be crucial to doing APIs.
- **GitOps** - The API lifecycle is an expanding layer of the software development lifecycle and Git is how APIs are being continuously integrated with business and deployed to support applications.
- **Local / On-Premise** - The API gateway needs to be where it is needed, and being able to have the API gateway be on-premise and locally available is just an essential aspect of operations.
- **Programmability** - Our APIs need to be programmable just like our applications, and the digital resources and capabilities offered by our API operations will shape all of our  digital experiences. 
- **Extensibility** - Wiring up our API gateways to other services and easily extending the capabilities of what they offer will continue to define how enterprises are building their API platforms. 
- **Observability** - Our API gateways have to be as observable as any physical factory or warehouse, making this an important way that API gateway providers will obtain mindshare.
- **Products** - As APIs shift from being a technical building block to something that business is playing an active role in, the product-centered nature of an API gateway will matter a whole lot.
- **Experience** - Using an API gateway should reflect a desirable experience for teams who are producing an API, empowering them to do more, leaving them to focus on the value they bring to the table.

These are the areas that stand out from the leading and forward-thinking API gateways on the market today. These capabilities reflect the modern gateway slowly being woven into the fabric of the cloud, and more recently the web, ensuring core gateway capabilities are available where they are needed bottom-up by developers while meeting the needs of architects, security, operations, and other top-down stakeholders.

## Conclusion
Tomorrow’s gateway must help load balance the API infrastructure sprawl resulting from a mix of bottoms-up and top-down investment at the gateway layer. We need to embrace the chaotic landscape that exists today, enabling developers to do what they need to do when they need it without friction while adhering to the policies defined top-down by business and technical leadership.

The next generation needs to be contract and policy shaped while seamlessly weaving into developers' existing workflow, allowing them to rapidly deliver APIs locally, within any cloud, and at the edge using their existing source control and CI/CD pipelines. A modern API gateway will ensure all APIs are observable and properly governed by default, without requiring developers to do additional work.

Tomorrow’s API gateway is seamless, extensible, and programmable. It is just there and part of the existing developer toolbox, the infrastructure we are already using, and part of the web we all already depend on. In tomorrow’s API landscape there will be no drift between the design and development of each API and what is present in production, leveraging contracts and policies to deliver consistency at higher velocities without breaking changes.

A modern API gateway will need to be the bridge between business and engineering with a native product centered experience that closes the divide that has existed for decades with the help of a platform team. Today’s APIs are a perpetual negotiation between product and engineering that is facilitated by a platform team, which is all iterated upon with consumers stakeholders in the loop–the API gateway is central to this motion.

I know better than to think the API space is going to listen to my predictions, and while the gateway will continue to be the center of the discussion, the API gateway of the future has to exist with a small federated footprint that is programmable and extensible. This gateway has to meet the needs of the product and engineering teams who depend on them, and like APIs, respond and evolve with whatever is happening next–like we are seeing emerge with Artificial Intelligence.