---
published: true
layout: post
title: >-
  My Response On The Department Of Veterans Affairs (VA) RFI For The Lighthouse
  API Management Platform
date: 2017-10-26T12:00:00.000Z
tags:
  - API Evangelist
  - Federal Government
  - Veterans
  - Platform
  - Business of APIs
image: 'https://s3.amazonaws.com/kinlane-productions/veterans-affairs/va-logo.jpg'
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/veterans-affairs/va-logo.jpg" align="right" width="40%" style="padding: 15px;" /></p>I am working with my partners in the government API space ([Skylight](https://skylight.digital/), [540](https://540.co/), [Agile Six](https://agile6.com/)) to respond to a request for information (RFI) out of the Department of Veterans Affairs (VA), for what they call the [Lighthouse API Management platform](https://www.fbo.gov/index?s=opportunity&mode=form&tab=core&id=b5a3e0c29fa78545f0556dac972bac69). The RFI provides a pretty interesting look into the way the government agency which supports our vets is thinking about how they should be delivering government resource using APIs, but also how they play a role in the wider healthcare ecosystem. My team is meeting today to finalize our response to the RFI, and in preparation I wanted to prepare my thoughts, and in my style of doing things, involves publishing them here on API Evangelist.

You can read [the whole RFI](https://www.fbo.gov/index?s=opportunity&mode=form&tab=core&id=b5a3e0c29fa78545f0556dac972bac69), but I'll provide the heart of it, to help set the table for my response.

**Introduction:**
To accelerate better and more responsive service to the Veteran, the Department of Veterans Affairs (VA) is making a deliberate shift towards becoming an Application Programming Interface (API) driven digital enterprise. A cornerstone of this effort is the setup of a strategic Open API Program that is adopting an outside-in, value-to-business driven approach to create APIs that are managed as products to be consumed by developers within and outside of VA.

**Objectives:**
VA has started the process of establishing an API Management Platform, named Lighthouse.  The purpose of Lighthouse is to establish the Next Generation Open Digital Platform for Veterans, accelerating the transformation in core domains of VA, such as Health, Benefits, Burial and Memorials. This platform will be a system for designing, developing, publishing, operating, monitoring, analyzing, iterating and optimizing VA’s API ecosystem. These APIs will allow VA to leverage its investment in various digital assets, support application rationalization, and allow it to decouple outdated systems and replace them with new, commercial, off the shelf, Software as a Service (SaaS) solutions. It will enable creation of new, high value experiences for our Veterans, VA’s provider partners, and allow VA’s employees to provide better service to Veterans.

**With some insight into how they will achieve those objectives:**

* Integrate more effectively with the community care providers by connecting members of a Veteran’s “Care Team” from within and outside the Veterans Health Administration (VHA); and, generate greater opportunities for collaboration across the care continuum with private sector providers,
* Effectively shift technology development to commercial electronic health record (EHR) and administrative systems vendors that can integrate modular components into the enterprise through open APIs, thus allowing VA to leverage these capabilities to adopt more efficient and effective care management processes,
* Foster an interoperable, active, innovation ecosystem of solutions and services through its Open API Framework that contributes to the next generation of healthy living and care models that are more precise, personalized, outcome-based, evidence-based, tiered and connected across the continuum of care regardless of where and how care is delivered,
* Create an open, accessible platform that can be used not only for Veterans care but also for advanced knowledge sharing, clinical decision support, technical expertise, and process interoperability with organizations through the U.S. care delivery system. By simplifying access to the largest data set of clinical data anywhere, albeit de-identified, it will accelerate the discovery and development of new clinical pathways for the benefit of the Veterans and the community at large.

They include some bullets for what they see as the road map for the Lighthouse API management platform:

* The API Gateway, through creating the facades for common, standard Health APIs will allow multiple EHRs to freely and predictably interoperate with each other as VA deploys the COTS EHR through the enterprise and finds itself with multiple EHR's during the transition and stabilization phases of the implementation.
* Establish the Single Point of Interoperability with health exchanges and EHR systems of Community Care Providers.
* The development of APIs across the enterprise spanning additional domains following a federated development approach that can see an exponential growth in the number APIs offered by the platform.  
* Operate at scale to support the entire population of Veterans, VA Employees and Community Providers that provide a variety of services to the Veterans

This is all music to my ears. These are objectives, and a road map that I can get behind. It is an RFI that reflects where all federal agencies should be going, but it also is also extra meaningful for me to see this coming out of the VA. Definitely making it something I want to support however I can. The window for responding is short, so I wanted to be able to stop what I'm doing, and give the RFI a proper response, regardless of who ends up running the platform. I've done type of RFI storytelling several times in the past, with [the FAFSA API for Department of Education](http://ed-data.github.io/fafsa-api/), the [Recreational Information Database (RIDB) out of Department of Interior](http://apievangelist.com/2014/10/16/i-need-help-to-make-sure-the-dept-of-agriculture-leads-with-apis-in-their-parks-and-recreation-rfp/), when [Commerce hired a new Chief Data Officer](https://apievangelist.com/2014/07/15/chief-data-officer-needs-to-make-the-department-of-commerce-developer-portal-the-center-of-api-economy/), and [just in general support of the White House API strategy](https://apievangelist.com/2014/07/15/chief-data-officer-needs-to-make-the-department-of-commerce-developer-portal-the-center-of-api-economy/). This time is different, only because I have a team of professionals who can help me deliver beyond just the RFI.

**Some Background On Me And The VA**
Before I get to the questions included as part of the RFI, I wanted to give some background on my relationship to the VA, and supporting veterans. First, my biological father was career military, and the father that raise me was a two tour Vietnam veteran, exposing me to the veterans administration and hospitals at an early age. He passed away in the 1990s from cancer he developed as a result of his Agent Orange exposure. All this feeds into my passion for applying APIs in this area of our society. Additionally, I used to work for the Department of Veterans affairs, as a Presidential Innovation Fellow in 2013. I didn't stay for the entire fellowship, exiting during the government shutdown, but I have continued to work on opening up data sets, supporting VA related API conversations, and trying to keep in tune with anything that is going on within the agency. All contributing to this RFI making me pretty happy.

**My Answers To The RFI Questions**
The VA provides 20 separate questions as part of their RFI. Shining a light on some of the thinking that is occurring within the agency. I've bolded their questions, and provide some of my thought inline, sharing my official responses. My team will work to combine everyones feedback, and publish a formal response to the VA's RFI.

**1. Drawing on your experience with API platforms, how do you see it being leveraged further within the healthcare industry in such a manner as described above? What strengths and opportunities exist with such an approach in healthcare?**

An API first platform as proposed by the VA reflects what is already occurring in the wider healthcare space. With veteran healthcare spending being such a significant portion of healthcare spending in this country, the presence of an API platform like this would not just benefit the VA, veterans, veteran hospitals, and veteran service organizations (VSO), it would benefit the larger economy. A VA API platform would be the seed for a federated approach to not just consuming valuable government resources, but also deploying APIs that will benefit veterans, the VA, as well as the larger healthcare ecosystem.

Some of the strengths of this type of approach to supporting veterans via an open data and API platform, with a centralized API operations strategy would be:

- **Consistency** - Delivering APIs as part of a central vision, guided by a central platform, but echoed by the federated ecosystem can help provide a more consistent platform of APIs.
- **Agility** - An API-first approach across all legacy, as well as modern VA systems will help break the agency, and its partners into much smaller, bite-size, reusable components.
- **Scope** - API excel at decouple legacy systems that are often larger and more complex, delivering much smaller, reusable components that can be developed, delivered and deprecated in smaller chunks, that work at scale.
- **Observability** - A modern approach to delivering an API platform for government with a consistent model for API definitions, design, deployment, management, monitoring, testing, and other steps of the API lifecycle, combined with a comprehensive approach to measuring and analysis brings much needed observability to all stops along the lifecycle. Letting in the sunlight required for success at scale.
- **Feedback Loops** - An API platform at this scale, which the appropriate communication and support channels open up feedback loops for all stops along the lifecycle, benefitting from community, and partner input from design to deprecation. Making all VA systems

These platform strengths set the stage for some interesting and beneficial opportunities to emerge from within the platform community, but also the wider healthcare ecosystem that already exists, and is evolving, which sill step up and participate and engage with available VA resources. Here are some examples of how this can evolve based upon existing API ecosystem within and outside the healthcare ecosystem:

- **Practitioner Participation** - An open API platform always starts with engaging backend domain experts, allowing for the delivery of APIs that deliver access to critical resources. Second, modern API platforms help open up, and attract external domain experts, and in the case of a VA platform, this would mean more engagement with health care practitioners, further rounding off what goes into the delivery of critical veteran services.
- **Healthcare Vendor Integration** - Beyond practitioners, a public API platform for the VA would attract existing healthcare vendors, providing EHR, and other critical services. Vendors would be able to define, design, deploy, and integrate their API driven solutions outside the tractor beam of internal VA operations.
- **Partner Programs** - The establishment of formal partner program accompany the most mature API platforms available, allowing for more trusted engagement across the public and private sector. Partners will bring needed resources to the ecosystem, while benefitting from deeper access to VA resources.
- **Certification** - Another benefit of a mature API platform is the ability to certify partners, applications, and developers, establishing a much more trusted pool of vendors, and developers that the VA can benefit from, as well as rest of the ecosystem.
- **Standardization** - A centralized API platform helps aggregates common schema, API definitions, models, and blueprints that can be used across the federated public and private sector. Helping establish consistency across VA API resources, but also in the tooling, services, and other applications built on top of VA APIs.
- **Data Ecosystems** - A significant number of VA APIs available on the platform will be driven by valuable data sets. The more APIs, and the consistency of APIs across many internal data stewards, as well as trusted partner sources will establish a data ecosystem that will benefit veterans, the VA, as well as the rest of the ecosystem.
- **Community Participation** - Open API platform bring in a wide variety of developers, data scientists, healthcare practitioners, and folks who are passionate about the domain. When it comes to supporting veterans, it is essential that there is a public platform and forum for the community to engage around VA resources. Helping share the load with the community, when it comes to serving veterans.
- **Marketplace** - With an API platform as proposed by this RFI, a natural opportunity is with a marketplace. An established process and platform for internal groups to publish their APIs, as well as supporting SDKs, and other applications. This marketplace could also be made available to trusted partners, and certified developers, allowing them to showcased their verified applications, and be listed as a certified developer or agency. The marketplace opportunity will bring the most benefit to the VA, when it comes to delivering across many internal groups.

The benefits of an API platform such as the one proposed as part of this RFI is that they make the delivery of critical services a team effort. Domains within the VA can do what they do best, and benefit from having a central platform, and team to help them deliver consistent, reliable, scalable API access to their resources, for use across web, mobile, device, spreadsheet, analysis, and other applications. Externally, healthcare vendors, hospitals, practitioners, veterans, and the people that support them can all work together to put valuable API resources to work, helping make sense of data, deliver more modular, meaningful applications that all focus on the veteran.

The fact that this RFI exists shows that the VA is looking to keep pace with where the wider healthcare sector is headed. Four our of five of the leading EHR providers have existing API platforms. Demonstrating where the healthcare sector is headed, and something that reflects the vision established in this RFI. The strength and the opportunity with such an approach to delivering healthcare services for veterans will be fully realized when the VA becomes interoperable, and plug and play with the wider healthcare sector.

**2. Describe your experience with different deployment architecture supported by MuleSoft (e.g. SaaS only, On Premise Only, Private cloud, Hybrid – Mix of SaaS and Private Cloud) and in what industry or business process it was used? Please include whether your involvement was as a prime or subcontractor, and whether the work was in the commercial or government sector.**

My exposure to the Mulesoft in a production environment has been limited in recent years, especially within the last couple of years. However, during my time at the Veterans Affairs, and working in government, I was actively involved with the company, regularly engaging with their product and sales team in several areas:

- **Industry Research** - I was paid to conduct API industry research back in 2012 and 201 by Mulesoft, providing regular onsite presentations regarding my work, contributing to their road map.
- **Messaging Partner** - I worked with Mulesoft on the creation of short form and long form content around the API industry, and as part of my API industry conference.
- **Sales Process** - I have sat in on several sales meetings for Mulesoft with government agencies, enterprise organizations, and higher educaitonal institutions, and are familiar with what they offer.
- **RAML Governance** - I was part of the early discussion, formation, and feedback on the RAML API specification form, but left shortly after I left the government.

Based upon my experience working with the Mulesoft team, and through my regular monitoring of their services, tooling, and engaging with some of their clients I am confident in my ability to tailor a platform strategy that would work with their API gateway, IAM, definitions, discovery, and other solutions. I have been one of the analysts in the API sector who studies Mulesoft, and the other API management providers, and understand the strengths, and weaknesses of each of the leading vendors, as well maintain and understanding of how API management is being commoditized, standardized, and applied across all the players. I’m confident this knowledge will transfer to delivering an effective vision for the VA, involving Mulesoft solutions.

**3. Describe any alternative API Management Platforms that are offered as SaaS offerings, On Premise, Private Cloud, or Hybrid.  Please detail how these solutions can scale to VA’s needs managing approximately 56,000 transactions per second through connecting to VistA and multiple commercial and open source EHRs (conforming to US Core Profiles of the HL7 FHIR standards), multiple commercial Enterprise Resource Planning (ERP) systems, various home grown systems including Veterans Benefit Management Service (VBMS), Corporate Data Warehouse, and VA Time & Attendance System (VATAS),  and commercial real-time analytics software packages, and open source tools enabling rapid web and mobile application development.**

Monitoring and understanding API management platforms is something I've done since 2010 in a full time capacity. I've studied the evolution of the enterprise API gateway from its service oriented architecture days, into the cloud as a commodity with AWS, Google, and Azure, as well as the deployment on-premise, in hybrid scenarios, and even on-device. To support my partners, clients, and the readers of my blog, I work regularly to test drive, and understand leading API management solutions available on the market today.

While I study the proprietary and open source API gateway and management solutions out there, I also work to understand where API providers will be operating these solutions, which means having a deep understanding of how native and installed API management occurs in the cloud, hybrid, on-premise, on-device, and anywhere it needs to be in 2017.

- **Multi-Vendor** - API gateways have become a commodity and are baked into every one of the major cloud providers. AWS has the lead in this space, with Google, and Azure following up. We stay in tune with a multi-vendor gateway approach to be able to support, and deliver solutions within the context of how our customers and clients are already operating. To support the number of transactions the VA is currently seeing, as well as with future API implementation, a variety of approaches will be required to support the requirements of many different internal groups, as well as trusted partners.
- **Multi-Cloud** - As I already mentioned, always look to support multiple gateways across multiple datacenter, and cloud providers. Our goal is to understand the native opportunities on each cloud platform, the environment to deliver hybrid networks and environments, as well as how each of the leading open source and proprietary API management providers operate within a cloud environment. Making it easier to integrate with, and deliver API facades for any backend resources available within any cloud environment.
- **Reusable Models** - One key to successful API management in any environment is the establishment of reusable models, and the reuse of definitions, schema, and templates which can be applied consistently across groups. Any API gateway, and management solution should have an accompanying database, machine, or container image, and be driven using a machine readable API definition using OpenAPI, API Blueprint, or RAML. All data should possess an accompanying definition using JSON Schema, and leverage standards like JSON Path for mapping relationships, and establishing mappings between resources. Everything should be defined for implementation, reuse, and continuous deployment as well as integration.
- **API-Driven** - Every mature API management platform automates using APIs. Mulesoft, Apigee, 3Scale, AWS Gateway, all have APIs for managing the management of APIs. This allows for the seamless integration across all systems, even disparate backend legacy systems. Extending identity, service compositions, plans, rate limits, logging, analysis, and other exhaust from API management into any system it is needed. Lighthouse should be an API driven platform for defining, designing, deploying, and managing APIs the serve the VA.

In full disclosure, I've worked with almost every API management provider out there in some capacity. Similar to providing industry analysis to Mulesoft, I helped WSO2 define and evolve their open source API management solution. Engaged and partnered with 3Scale (now Red Hat), Apigee (Now Google), Mashery (now Tibco), and others. I've also engaged with NREL and their development of API Umbrella, as well as the GSA when it came to implementing in support of api.data.gov. I'm currently taking money from Tyk, 3Scale, Runscope, and Restlet--all servicing the space. It is my job to understand the API management playing field, as well as the nuts and bolts of all the leading providers.

While it is important to be able to dive deep and support specific solutions for specific project when it comes to API management, for a platform to handle the scale and scope of the Lighthouse API management platform it will have to be able to provide support for connecting to a robust set of known, and unknown backend systems. While many organizations we've worked with strive for a single gateway or API management solution, in reality many often operating multiple solutions, across many vendors, and multiple cloud or on-premise environments. The key to a robust, scalable platform is the ability to easily define, configure, and repeat regularly across environment, providing a consistent API surface area across implementations, groups, backend, and gateway infrastructure.

**4. Describe your company’s specific experience and the strategies that you have employed for ensuring the highest level of availability and responsiveness of the platform (include information about configuration based capabilities such as multi-region deployments, dynamic routing, point of presence, flexible/multi-level caching, flexible scaling, traffic throttling etc.).**

Our approach to delivering API infrastructure involves assessing scalability at every level of API management within our control. When it comes to API deployment and management we aren't always in control over every layer of the stack, but we always work to configure, optimize, and scale whenever we possibly can. Every API will be different, and a core team will enjoy a different amount of control over backends, but we always consider the full architectural stack when ensuring availability and responsiveness across API resources, looking at eight common layers:

- **Network** - When possible we work to configure the network to allow for prioritization of traffic, and isolation of resources at the network level.
- **Sytem** - We will work with backend system owners to understand what their strengths and weaknesses are, and understand how systems are currently optimize and assess what new ways are possible as part of Lighthouse API operations.
- **Database** - When there is access to the database level will will assess the scalability of instances and tables in service of API deployment. If possible we will work with database groups to deploy slave implementations that can be dedicated to supporting API implementations.
- **Serverless** - Increasingly we are using serverless technology to help carry the load for backend systems, adding another layer for optimization behind the gateway. In some situations a serverless layer can act as a proxy, cache, and redundancy for backend systems. Opening up new approaches to availability.
- **Gateway** - At the gateway level there are opportunities for scaling, and delivering performance, as well as enabling caching, and rate limiting to optimize specific types of behaviors amongst consumers. Each API will have its own plan for optimization and reliability, tailored for its precise configuration and time to live (TTL).
- **DNS** - DNS is another layer which will play a significant role in the reliability and performance of API operations. There are numerous opportunities for routing, caching, and multi-deployment optimizations at the DNS to support API operations.
- **Caching** - There are multiple levels to think about caching in API infrastructure, from the backend up to DNS. The entire stack should be considered on an API by API basis, with a robust approach to knowing when to use, and where not to use.
- **Regional** - One of the benefits of being multi-vendor, and multi-cloud, and on-premise, is the ability to deliver API infrastructure where it is needed. Delivering in multiple geographic regions is an increasingly common reason for using the cloud, as well as allowing for flexibility in the deployment, management, and testing of APIs in any US region.
- **Monitoring** - One aspect of availability and reliability is monitoring infrastructure 24x7, keeping an eye on availability and performance. Sustained monitoring, across providers, and regions is essential to understanding how to ensure APIs are available and dependable.
- **Analysis** - Extracted from monitoring, and logging, the analysis across API operations feeds into the overall availability and reliability of APIs. Real-time analysis of API availability and performance over time is critical for dependable infrastructure.
- **Partners** - I've experience the lack of dependability of VA APIs first hand. During my time at the agency I was forced to shut down APIs I had worked on during the government shutdown. Introducing me to another dimension of API reliability, where I feel external partners can help contribute to the redundancy and availability of APIs beyond what the agency can deliver on its own.

API stability isn't purely a technical game. There are plenty of tools at our disposal for scaling, optimizing, and injecting efficiencies into the API life cycle. However, the most important contributor to reliability is experience, and making sure you measure, analyze, and understand the needs of each API. This is where modern approaches to API management come into play, and understand how API consumers are putting resources to work, and optimizing each API to support this at which every layer possible.

**5. The experiences you have and the strategies that you have employed to ensure the highest level of security for the platform. Please address policy / procedure level capabilities, capabilities that ensure security of data in transit (e.g. endpoint as well as payload), proactive threat detection etc.**

API security is another dimension of the API sector I've been monitoring and studying on a regular basis. I have just finished a comprehensive guide to the world of API security, which will be the first guide of its kind when publish next week. I've been monitoring general approaches to securing infrastructure, as well as how that impacts API security. I've been taking what I've found in my research, as well as work with clients, and aggregated into 15 separate areas to consider as we develop a strategy to deliver the high levels of security.

- **Encryption** - Encryption in transport, on the disk, in storage, and in database.
- **API Application Keys** - Requiring keys for ALL API access, no matter whether internal or external.
- **Identity & Access Management (IAM)** - Establish roles, groups, users, policies and other IAM building blocks, healthy practices and guidance across API implementations and teams.
- **Service Composition** - Provide common definitions for how to organize APIs, establish and monitor API plans and usage, and use to secure and measure access to ALL API resources.
- **Common Threats** - Be vigilant for the most common threat from SQL injection, to DDoS, making sure all APIs don't fall victim to the usual security suspects.
- **Incident Response** - Establish an incident response team, and protocol, making sure when a security incident occurs there is a standard response.
- **Governance** - Bake security into API governance, taking beyond just API design, and actually connecting API security to the service level agreements governing platform operations.
- **DNS** - Leverage the front line of API security and identifying threats at the DNS layer, and establish, and maintain a frontline of defense for API security.
- **Firewall** - Building on top of existing web security practices, and deploying, and maintaining a comprehensive set of rules at a firewall level.
- **Automation** - Implement security scanning, fuzzing, and automated approaches to crawling networks and infrastructure looking for security vulnerabilities.
- **Testing & Monitoring** - Dovetail API security with API testing and monitoring, identifying malformed API requests, responses, and other illnesses that can plague API operations.
- **Isolation** - Leveraging virtualization, serverless, and other API design and infrastructure patterns to keep API resources isolated, and minimizing any damage that can occur in a breach.
- **Orchestration** - Acknowledging the security risks that come with modern approaches to orchestrating API operations, continuously deploying, and integrating across the platform.
- **Client Automation** - Develop a strategy for managing API consumption, and identifying, understanding, and properly managing bots, and other types of client automation.
- **Machine Learning** - Leveraging the development and evolution of machine learning models that help look through log files, and othe threat information sources, and using artificial intelligence to respond and address evolving security concerns.
- **Threat Information** - Subscribing to external sources of threat information, and working with external organizations to open up the learning opportunities across platforms regarding the threats they face.
- **Metrics & Analysis** - Tap into the metrics and analysis that comes with API management, and build upon the awareness introduced when you consistently manage API consumption. Translating this awareness into a responsive and agile approach to delivering API security across groups, and externally with partners.
- **Bug Bounties** - Defining and executing public and private bug bounties to help identify security vulnerabilities early on.
- **Communications** - Establish a healthy approach to communicating around platform security. Openly discussing healthy practices, speaking at conferences, and participating in external working groups. While have a regular cadence to communication in normal times, as well as protocol for communication during security incidents.
- **Education** - Develop curriculum and other training materials around platform security, and make sure API consumers, partners, and internal groups are all getting regular doses of API security education.

Our API security experience comes from past projects, working with vendors, and studying the best practices of API leaders. Increasingly API security is a group effort, with a growing number of opportunities to work with security organizations, and major tech platforms who see the majority of threats present today. Increasing the volume of information available to integrate directly into platform security operations.

**6. Please describe your experience with all the capabilities that the platform offers and the way you have employed them to leverage existing enterprise digital assets (e.g. other integration service buses, REST APIs, SOAP services, databases, libraries)**

I have been working with databases for 30 years. I began working with web services in 2000, and have worked exclusively with web APIs in a full time capacity since 2010. I've worked hard to keep myself in tune with the protocols, and design patterns in use across the public and private API sectors. Here are the capabilities I'm tuned into currently.

- **SOAP** - Making sure we are able to support web services, and established approaches to accessing data and other resources.
- **REST** - Web APIs that follow RESTful patterns is ur primary focus, leveraging low-cost web infrastructure to securely making resources available.
- **Hypermedia** - Understanding the benefits delivered by adopting common hypermedia media types, delivering more experience focused APIs that emphasize relationships between resources.
- **GraphQL** - Understanding when the use of GraphQL makes sense for some data focused APIs, delivering resources to single page adn mobile applications.
- **gRPC** - Staying in tune with being able to deliver higher performance APIs using gRPC, augmenting the the features brought by web APIs, for use internally, and with trusted partners.
- **Websockets** - Leverage websockets for streaming of data in some situations, providing more real time integration for applications.
- **Webhooks** - Developing webhook infrastructure that makes APIs a two-way street, pushing notifications and data externally based upon events or on a schedule.
- **Event Sourcing** - Developing a sophisticated view of the API landscape based upon events, and identifying, orchestrating and incentivizing event-based behavior.

This reflects the core capabilities present across the API landscape. While SOAP and REST make up much of the landscape, hypermedia, GraphQL, event sourcing, and other approaches are seeing more adoption. I emphasize every platform make REST, or web APIs the central focus of the platform, keeping the bar low for API consumers, leverage web technology to reach the widest audience possible.

**7. Please describe your experience and strategies that you have employed at enterprises to create Experience Services from mashup/aggregation/combination of other API’s, services, database calls etc.**

I've been tracking on API aggregation as a discipline for over five years now, having worked with several groups to aggregate common APIs. It is an under developed layer to the web API sector, but one that has a number of proprietary, as well as open source solutions available.

I've personally worked on a number of API aggregation project, spanning a handful of business sectors:

- **Social** - Developed an open source , as well as SaaS solution for aggregating Facebook, LinkedIn, Twitter, and other social network.
- **Images** - Extended a systems to work across image APIs, working with Flickr, Facebook, Instagram, and other image sharing solutions.
- **Wearables** - Developed a strategy for aggregating of health data across a handful of the leading wearable device providers.
- **Documents** - Partnered with a company who provides document aggregation across Box, Google Drive, and other leading document sharing platforms.
- **Real Estate** - I founded a startup that did MLS data aggregation across APIs, FTP locations, and scraped targets, providing regional, and specific zip code API solutions.
- **Advertising** - I've worked with a company that aggregates advertising APIs bringing Google, Facebook, Twitter, and other platforms together into a single interface.

These are all the reasons why I was working on API aggregation, and spending time researching the subject. Here are some of the technology, and approaches I have been using to deliver on API aggregation.

- **OpenAPI** - I heavily use the OpenAPI specification to aggregate API definitions, and leverage JSON Schema to make connections and map API and data resources together.
- **APIs.json** - After working on the data.json project with the White House, inventorying open data inventory across federal agencies, I developed an open specification for indexing APIs, and building collections, and other aggregate definitions for processing at discovery or runtime.
- **JSON Schema** - All databases and data used as part of API operations possesses a JSON schema definition, that accompanies the OpenAPI that defines access to an API. JSON Schema provides the ability to define references across and between individual schema.
- **JSON Path** - XPath for JSON, enabling the ability to analyze, transform and selectively extract data from API requests and responses.

In an API utopia, everyone would use common API definitions, media types, and schema. In the real world, everyone does things their own way. API aggregation, and tools like OpenAPI, APIs.json, JSON Schema, and JSON Path allow us to standardize through machine readable definitions that connect the dots for us. API aggregation is still very much a manual process, or something offered by an existing SaaS provider, without much innovation--the tools are out there, we just need more examples we can emulate, and tooling to support.

**8. Please describe your experience and strategies for Lifecycle Management of APIs for increasing productivity and enabling VA to deliver high value APIs rapidly, on-boarding app developers and commercial off the shelf applications.**

I feel like this overlaps with question number 14, but is more focused on on-boarding, and client perspective of the API lifecycle. Question 14 feels like lifecycle optimization from an API provider perspective, and this is about efficiencies regarding consumption. Maybe I'm wrong, but I am a big believer in the ability of a central API portal, as well as federated portals, to increase API production, because they are delivering the resources consumers need, in a way that allows them to onboard and consume across many developers and commercial software platforms.

My experiences in fulfilling an API lifecycle from the consumer perspective always begins with a central portal, but one that posses all the required API management building blocks to not just deliver aPIs rapidly, incentivize consumption, and feedback in a way that evolves them throughout their life cycle:

- **Portal** - Have a central location to discover and work with all API resources, even if there is a federated network of portals that work together in concert across groups.
- **Getting Started** - Providing clear, frictionless on-boarding for all API consumers in a consistent way across all API resources.
- **Authentication** - Simple, pragmatic authentication with APIs, that are part of a larger IAM scaffolding.
- **Documentation** - Up to date, API definition driven, interactive API documentation that demonstrates what an API does.
- **Code Resources** - Code samples, libraries, and SDKs that make integration painless, and frictionless, allow applications to quickly move from development to production.
- **Support** - Providing direct and indirect support services that funnel back through feedback loops into the product roadmap.
- **Communications** - A regular drumbeat around API Platform communications, helping API consumers navigate discovery to integration, and keeps them informed regarding what is happening across the platform.
- **Road Map** - A clear roadmap, as we as resulting change log that keeps API consumers in tune with whats next, reducing the gap that can exist between API provider and consumer.
- **Applications** - A robust directory of certified applications, browser, platform, and 3rd party plugins and connectors, demonstrating what is possible via the platform.
- **Analysis** - Logging, measuring, and analyzing API platform traffic, sign ups, logins, and other key data points, developing an awarness of what is working when it comes to API consumption, and quickly identifying where the friction is, and eliminating with future releases.

Developer Experience (DX) is something that significantly speeds up the overall API lifecycle. Backend teams can efficiently define, deliver, and evolve their APIs without API consumers on-boarding, integrating, and providing feedback on what works, and what doesn't work. A central API portal strategy for Liqhthouse API management is key to facilitating movement along the API lifecycle, reducing friction, eliminating road blocks, and reducing the chance an API will never full be realized in production.

Lighthouse API management is a central API platform portal, but could also be a forkable DX experience that can be emulated by other internal groups, adding federated edges to the Lighthouse API management platform. Providing a network of consistent API portals, across many different groups, which share a common on0boarding, authentication, documentation, support, communication, and analysis approach. Shifting the lifecycle beyond just a linear start to finish thing, and making something that works as a network of API nodes that all work together as a single platform.

**9. Please describe your experience and strategies for establishing effective governance of the APIs.**

I've been working with a variety of organizations around the topic of API governance for 2-3 years now, and with some recent advances I'm starting to see more API governance strategies mature, and become something that goes well beyond just API design.

API governance is something i've tuned into across a variety of enterprise, higher educational institutions, and government agencies. These are the areas I'm researching currently as part of my work as the API Evangelist.

- **Design Guide** - Establishing API design guide(s) for use across organizations.
- **Deployment** - Ensuring there are machine readable definitions for every deployment pattern, and they are widely shared and implemented.
- **Management** - Quantify what API management services, tooling, and best practices groups should be following, and putting to work in their API operations.
- **Testing** - Defining the API testing surface area, and provide machine readable definitions for all test patterns, while leverage OpenAPI and other definitions as a map of the landscape.
- **Communication** - Plan out the communication strategy as part of the API governance strategy.
- **Support** - What support mechanisms are in place for governance, as well as definitions for best practices for supporting indvidiaul API implementations.
- **Deprecation** - Define what deprecation looks like even before an API is defined or ever delivered, establishing best practices for deprecation of all resources.
- **Analysis** - Measuring, analyzing, and reporting on API governance. Identifying where it is being applied effectively, and where the uncharted territory lies.
- **Coaches** - Train and deploy API coaches who work with every group on establishing, evolving, incentivizing, and enforcing API governance across groups.
- **Rating** - Establishing a set of rating system for quantifying how compliant APIs are when it comes to API governance, providing an easy to understand how close an API is, or isn't.
- **Training** - The development and execution of training around API governance, working with all external groups to help define API governance, and take active role in its implementation.

Sadly, API governance isn't something I've seen consistently applied across the enterprise, at institutions and government agencies. There is no standard for API governance. There are few case studies when it comes to API governance to learn from. Slowly I am seeing larger enterprises share their strategies, and seeing some universities publish papers on the topic. Providing some common building blocks we can organize into a coherent API governance strategy.

**10. Please describe your experience and methodologies for DevOps/RunOps processes across deployments. Highlight strategies for policy testing, versioning, debugging etc.**

API management is a living entity, and we focus on delivering API operations with flat teams who have access to the entire stack, from backend to understanding application and consumer needs. All aspects of the API life cycle embraces a microservices, continuous evolution pace, with Github playing a central from from define to deprecation.

- **CI/CD** - Shared repositories across all definition, code, documentation, and other modules that make up the lego pieces of API operations.
- **Testing & Monitoring** - Ensuring every building block has a machine readable set of assertions, tests, and other artificats that can be used to verify operational integrity.
- **Microservices** - Distilling down everything to a service that will meet a platform objective, and benefit an API consumer in as small as package as possible.
- **Serverless** - Leverage functions that reflect a microservices frame of mind, allowing much smaller unit of compute to be delivered by developers.
- **Versioning** - Following a semantic versioning with version numbers reflecting a MAJOR.MINOR.PATCH, and kept in sync across backend, API, and client applications.
- **Dependencies** - Scanning and assessing for vulnerabilities in libraries, 3rd party APIs, and other ways dependencies are established across architecture.
- **Security** - Scanning and assessing security risk introduced by dependencies, and across code, ensuring that testing and monitoring reflects wider API security practices.

A DevOps focus is maintained across as many stops along an API life cycle, and reflected in API governance practices. However, it is also recognized that a DevOps will not always be compatible with existing legacy practices, and custom approaches might be necessary to maintain specific backend resources, until their practices can be evolved, and brought in alignment with wider practices.

**11. Please describe your experience and strategies employed for analytics related to runtime management, performance monitoring, usage tracking, trend analysis.**

Logging and anaysis is a fundamental component of API management, feeding an overall awareness of how API are being consumer, which contributes to the product road map, security, and overall platform reliability. The entire API stack should be analyzed from the backend, to the furthest application endpoints, whenever possible.

- **Network** - Logging, and anaysis at the packet and network level, understanding where the network bottlenecks are.
- **Instance** - Monitoring and measuring any server instance, whether it is bare metal, virtual, or containerized, providing a complete picture of how each instance in the API chain is performing.
- **Database** - When access to the database layer is present, adding the logging, and other diagnostic information to the analysis stack, understand how backend databases are doing their job.
- **Serverless** - Understanding the performance and usage of each function in the API supply chain, making sure each lego building block is accounted for.
- **Regional** - Understanding how API resources deploy in various regions are performing, but also adding the extra dimension of measuring and monitoring APIs from a variety of geographic regions.
- **Management** - Leveraging API plans at the API gateway, and understanding API consumption at the user, application, and individual resource level. Painting a picture of how APIs are performing across access tiers.
- **DNS** - Logging, measuring, and runtime responsiveness at the DNS layer, understanding any setting, configuration, or other detail that may be creating friction at the DNS layer.
- **Client** - Introducing logging, analysis, and tracking of errors at the SDK level, developing usage and performance reports from the production client vantage point.

API management has matured over the last decade to give us a standard approach to managing API access at consumption time, optimizing usage, limiting bad behavior, and incentivizing healthy behavior. API monitoring and testing practices have evolved this perspective of the health, availability, and how APIs are being used from the client perspective. All of this information gets funneled into the road map, refining API gateway plans, rate limits, and other run time systems to adjust and support desired API usage.

**12. Please describe your experience with integrating MuleSoft with Enterprise Identity Management, Directory Services and implementing Role Based access.**

I do not have any experience in this area with Mulesoft specifically, but have worked in general with IAM and directory solutions in other platforms, and heavy usage on AWS, for securing the API gateway's interaction with existing backend system.

**13. Please describe your experience with generating and documenting API’s and the type of standards they follow. Describe approaches taken for hosting these documentations and keeping them evergreen.**

API documentation is always a default aspect of the API platform, and delivered just like code as part of DevOps and CI/CD workflows using Github. With almost every stop along the API life cycle, all documentation is API definition driven, keeping things interactive, with the following elements always in play:

- **Definitions** - All documentation is driven using OpenAPI, API Blueprint, or RAML, acting as the central machine readable truth of what an API does, and what schema it uses. API definition driven API documentation contributes to them always being up to date, and reflect the freshest view of any API.
- **Interactive** - All API documentation is API driven, allowing for the documentation to be interactive, acting as an explorer, and dynamic dashboard for playing with and understanding what an API does.
- **Modular** - Following a microservices approach, all APIs should have small, modular, API definitions, that drive modular, meaningful, and useful API documentation.
- **Visualizations** - Evolving on top of interactive documentation features, we are beginning to weave in more visual, dashboard, and reporting features directly into API document.
- **Github** - Github plays a central role in the platform life cycle, with all aPI definitions and documentation running within Github repository, and integrated as part of CI/CD workflows, and DevOps frame of mind.

All platform documentation is a living, breathing, element of the ecosystem. If should be versioned, evolved, and deployed along with other supporting microservice artifacts. Mulesoft has documentation to support this approach, as well as there being a suite of open source solutions we can consider to support a variety of different types of APIs.

**14. Please describe your proposed complete process lifecycle for publishing high quality, high value APIs with highest speed to market.**

Evolving beyond question number 8, and addressing the API provider side of the coin, I wanted to share a complete (enough) view of the life cycle from the API provider perspective. Addressing the needs of backend API teams, as well as the core API team when it comes to delivering usable, reliable, APIs that are active, and enjoy health release cycles. While not entirely a linear approach, here as many of the stops along our proposed API lifecycle, as applied to individual APIs, but applied consistently across the entire platform.

- **Definitions** - Every API starts as an API definition, which follows the API throughout its life, and drives every other stop along the way.
- **Design** - Planning, applying, evolving, and measuring how API design is applied, taking the definition, and delivering as a consistent API that complies with API governance.
- **Virtualization** - Delivery of mock, sandbox, and other virtualized instances of an API allowing for prototyping, testing, and playing around with an API in early stages, or throughout its life
- **Deployment** - Deploying APIs using a common set of deployment patterns that drives API gateway behavior, connectivity with backend systems, IAM, and other consistent elements of how APIs will be delivered.
- **Management** - The employment of common approaches to API management, some of which will be delivered and enforced by the API gateway, but also through other training, and sharing of best practices made available via API governance.
- **Testing & Monitoring** - Following DevOps, CI/CD workflows when it comes to developing tests, and other artifacts that can be used to monitor, test, and assert that APIs are meeting service level agreements, and in compliance with governance.
- **Security** - Considering security at every stop along the API life cycle, scanning, testing, and baking in security best practices all along the way.
- **Client & SDK** - Establish common approaches to generating, delivering, and deploying client solutions that help API consumer get up and running using an API.
- **Discovery** - Extending machine readable definitions to ensure an API is indexed and discoverable via service directories, documentation, and other catalogs of platform resources.
- **Support** - Establishing POC, and support channels that are available as part of any single APIs operations, ensuring it has required support that meets the minimum bar for service operations.
- **Communications** - Identifying any additions to an overall communication strategy around an APIs life cycle, announcing it exists on the blog, changes and releases are on the road map, and showcasing integrations via the platform Twitter account.
- **Road Map** - Making sure there are road map, and change log entries for an API showing where it is going, and where it has been.
- **Deprecation** - Lay out the deprecation strategy for an API as soon as it is born, setting expectations regarding when an API will eventually go away.

This life cycle will play out over and over for each API published on the Lighthouse API platform. It will independently be executed by API teams for each API they produce, and replayed with each major and minor release of an API. A well defined, and well traveled API life cycle helps ensure consistency across teams, helping enforce compliance, familiarity, and reusability across APIs, no matter which team is behind the facade.

**15. Please describe your experience and approach towards establishing a 24x7 technical support team for the users, developers and other stakeholders of the platform.**

Support is an essential building block of any successful API platform, as well as a default aspect of every single APIs individual life cycle. We break API platform support into two separate distinct categories.

API support should begin with self-service support, encouraging self-sufficiency of API consumers, and minimizing the amount of platform resources needed to support operations:

- **FAQ** - Publishing a list of frequently asked questions as part of getting started and API documentation, keeping it an easy to access, up to date list of the most common questions API consumers face.
- **Knowledge Base** - Publishing of a help directory or knowledge base of content that can help API consumers understand a platform, providing access to high level concepts, as well as API specific functionality, errors, and other aspects of integration.
- **Forum** - Operate an active, moderated, and inclusive forum to assist with support, providing self-service answers to API consumers, which also allows them to asynchronously get access to answers to their questions.

Beyond self-service support all API platforms should have multiple direct support channels available to API consumers:

- **Monitoring** - Providing a live, 3rd party status page that shows monitoring status across the platform, and individual APIs, including historical data.
- **Email** - Allow API consumers to email someone and receive support.
- **Tickets** - Leveraging a ticketing system, such as Zendesk, or other SaaS or possibly open source solution, allowing API consumers to submit private tickets, and move each ticket through a support process.
- **Issues** - Leveraging Github issues for supporting each component of the API lifecycle, from API definition, to API code, documentation, and every other stop. Providing relevant issues and conversation going on around each of the moving parts.
- **SMS** - SMS notifications regarding platform events, support tickets, platform monitoring, and other relevant areas of platform operations.
- **Twitter** - Providing public support via a Twitter account, responding to all comments, and routing them to the proper support channel for further engagement.

A combination of self-service and direct support channels allows for a resource starved core API team, as well as individual backend teams to manage many developers and applications, across many API resources in an efficient manner. Ensuring API consumers get the answers they are looking for, while ensuring relevant feedback and comments end up back in the product road map, with each appropriate product team.

**16. Please describe your experience in establishing metrics and measures for tracking the overall value and performance of the platform.**

This is somewhat overlapped with question #11, but I'd say focuses in on the heart of metrics and analysis at the API management level. Understand performance and reliability through the entire stack is critical to platform reliability, but the API management core is all about developing an awareness of how APIs are being consumed, and the value generated as part of this consumption. While performance definitely impacts value, we focus on API management to help us measure and understand consumption of each resource, and understand and measure the value delivered in consumption.

I've been studying how API management establishes the metrics needed, and measures and tracks API consumption, trying to understand value generation using the following elements:

- **Application Keys** - Every API call possess a unique key identifying the application and user behind consumption. This key is essential to understanding how value is being generated in the context of each API resources, as well as across groups of resources.
- **Active Users** - New, no name, automated API users are easy to attack. It is the active, identifiable, communicative users we are shooting for, so quantifying and measuring what an active user is, and how many exist on the platform is essential to understanding value generation.
- **Active APIs** - Which APIs are the APIs that consumers are integrating with, and using on a regular basis? Not all APIs will be a hit, and not all APIs will be transformative, but there can be utility, and functional APIs that make a significant impact. API management is key to understanding how APIs are being used, as well as how they are not being used, painting a complete picture of what is valuable, and what is not.
- **Consumption** - Measuring the nuance of how API consumers are consuming APIs, beyond just the number of calls being made. What is being consumed? What is frequency of consumption? What are the limitations, constraints, and metrics for consumption, and incentives for increasing consumption?
- **Plans** - Establishing many different access tiers and plans, containing many different APIs, allowing for API service composition to evolve create different API packages, or products that deliver across many different web, mobile, and device channels.
- **Design Patterns** - Which design patterns are being used, and driving consumption and value creation. Are certain types of APIs favored, or specific types of parameters favored and backed up by API consumption numbers. Measuring successful API design, deployment, management, and testing patterns, and identifying the not so successful patterns, then incorporating these findings into the road map as well as platform governance.
- **Applications** - Considering how metrics can be applied at the client, and SDK level, providing visibility and insight into how APIs are being consumed, from the perspective of each type of actual application being used.

API management is the future of public data, content, and other resource management. Understanding API consumption, measuring, analysing, and reporting upon API consumption is required to being able to evolve healthy API resources forward, and develop viable applications, that are putting API resources to use. API management will continue to become the tax system, the royalty system, and value generation capture mechanism across government agencies and public resources in coming years.

**17. Please describe your experience and the approach you would take as the API Program Core Team to deploy an effective strategy that will allow VA to distribute the development of API’s across multiple teams and multiple contractor groups while reducing friction, risk and time to market.**

A microservice, CI/CID, DevOps approach to providing and consuming APIs has begun to shift the landscape for how API platforms are supporting the API life cycle across many disparate teams, trusted external partners, and even 3rd party application and system developers. Distilling all elements of the API supply chain to modular, well defined components, helps establish a platform that can be centralized, but encouraging a consistent way to approach the federated delivery of APIs and supporting resources.

I focus on making API operations more reusable, agile, and effective in a handful of areas:

- **Github** - Everything starts, lives, and is branched and committed to via Github, either as a public or private repository. Definitions, code, documentation, training, and all other resources exist as repositories allowing them to be versioned, forked, collaborated around, and delivered wherever they are needed.
- **Governance** - Establishing API design, deployment, management, testing, monitoring, and other governance practices, then making them available across teams as living, collaborative documents and practices, and allow teams to remain independent, but working together in concert at scale, using a common set of health practices.
- **Training** - Establishing a training aspect to platform operations, making sure materials is readily developed to support all stops along the API lifecycle, and the curriculum is circulated, evolved, and made available across teams. Ensuring that all training remains relevant, up to date, and versioned to keep in sync with all platform changes.
- **Coaching** - Cultivate a team of API coaches who are embedded across teams, but also report back and worth with the central API team, helping train and educate around platform governance, but help work with and improve a teams ability to deliver within this framework. API coaches make API compliance a two way street, feeding resources downstream to teams, but then also working with teams to ensure their needs are being met, and reducing any friction that exists with delivering in a consistent way that meets the platform objectives.
- **Modular** - Keeping everything small, modular, and limiting the time and budget needed to define, design, deploy, manage, version, and deprecate, allowing the entire platform to move forward in concert, using smaller release cycles.
- **Continuous** - API governance, training, coaching, and all other operational level support across teams is also continuously being deployed, integrated, and evolved, ensuring that teams can work independently, but also be in sync when possible. Reducing bottlenecks, eliminating road blocks, and minimizing friction between teams, and across APIs that originate from many different systems.

API operations needs to work much like each individual API. It needs to be small, modular, well defined, doing one thing well, but in a way that can be harnessed at scale to deliver on platform objectives. The API lifecycle needs to be well documented, with disparate teams well educated regarding what healthy API design, deployment, management, and testing looks like. We make operations reusable, and forkable across teams by establishing machine readable models and supporting tooling that help teams be successful independently, but in alignment with the greater platform good.

**18. Please describe the roles and skill sets that you would be assembling to establish the API Program core team.**

Our suggested team for the Lighthouse Core API management implementation reflects how a federated, yet centralized API platform team should work. There are a handful of disparate groups, each brining a different set of skills to the table. We are always working to augment and grow this to meet each projects we work on, and open to working with 3rd party developers. Bringing forward some skills we already have on staff, while also introducing some new skills to bring a well rounded set of voices to the table to support the Lighthouse API platform.

- **Architects** - Backend, platform, and distributed system architects.
- **Database** - Variety of database administration, analysts, and scientists.
- **Veterans** - Making sure the veteran perspective is representative on the platform team.
- **Healthcare** - Opening the door to some healthcare practitioner advisor roles, making sure a diverse group of end users are represented.
- **Designers** - Bringing forward the required API design talent required to deliver consistent APIs at web scale.
- **Developers** - Provide a diverse set of developer skills supporting a variety of programming languages and platforms.
- **Security** - Ensure there is necessary security operations skills to pay attention to the bigger security picture.
- **Testing** - Provide dedicated testing and quality assurance talent to round off the set of skills on the table.
- **Evangelists** - Make sure there is an appropriate amount of outreach, communication, and storytelling occurring.

As the number of APIs grow, and an awareness of what consumers are desiring additional team members will be sought to address specific platform needs around emerging areas like machine learning, streaming and real time, or other aspects we haven't addressed in this RFI.

**19. How would you recommend the Government manage performance through Service Level Agreements?  Do you have commercial SLAs established that can be leveraged?**

Each stop along the provider dimensions, as well as the consumer perspective will be quantified, logged, measured, and analyzed as part of API management practices. As part of this process, each individual area will have it's set of metrics and questions that support API governance objectives. These are some of the areas that will be quantified, and measured, for inclusion in service level agreements.

- **Database** - What are the benchmarks for the database, and what are the acceptable ranges for operation. Log, measure, and evaluate historically, establishing a common scoring for delivery of database resources.
- **Server** - Similar to the database layer. What are the units of compute available for API deployment and management, and what are the benchmarks for measuring the performance, availability, and reliability of each instance, no matter how big or small.
- **Serverless** - Establishing benchmarks for individual functions, and defining appropriate scaling, service levels for each script beyond each API.
- **Gateway** - Through gateway logging, measuring, and understanding performance and availability at the gateway level. Factoring in caching, rat limits, as well as backend dependencies, then establishing a level of service that can / should be met.
- **APIs** - Through monitoring and testing each API should have its tests, assertions, and overall level of service defined. Is the API directly meeting its service level agreement? Is an API meeting API governance requirements, as well as meeting its SLA? What is the relationship between performance and compliance?

Each stop along the API lifecycle should have its guidance when it comes to governance, and possess a set of data points for measuring monitoring, testing, and performance. All of this can be used to establish a comprehensive service level agreement definition that goes beyond just uptime and availability, ensuring that APIs are meeting the SLA, but are doing so through API governance practices that are working.

**20. If the Government required offerors to build APIs as part of a technical evaluation, what test environments and tools would be required?**

We'd be willing to build APIs in support of a technical evaluation. We are willing to do this using an existing API gateway solution, via any of the existing cloud platforms. We would need access to deploy mock and virtualized APIs using a gateway environment, as well as configure and work with IAM, and some sort of DNS layer, to access addressing and routing for all prototypes deployed.

Our team is capable of working in any environment, and suggest test environments and tool reflect existing operations, supporting what is already in motion. We can make recommendations, and bring our open cloud, SaaS, and open tooling to the table, and build a case for why another tool might be needed, and make more sense as part of the technical evaluation.

To facilitate the defining, and evolution of a technical evaluation we recommend starting a private Github repository, either initiated by the VA, or off error, where a set of requirements, and definitions can be established as a seed for the technical evaluation, as well as quickly become many seeds for actual platform implementation.

**In Conclusion**<br />
That was a title more work than I anticipated. I had scheduled about six hours to think through this, and go through my research to find relevant answers. When I started this response, I was planning on adding a whole other section for suggestions beyond the questions that were being asked, but I think they are able to get at more of the proposed strategy than I anticipated. There were some redundant areas of this RFI, as well as some foreshadowing regarding what would be possible with such an API, but I think the questions were able to get at what is needed.

I'm not sure how my responses will size up with my partners, or alongside the other responders to the RFI. My responses reflect what I see working across the wider public API space, and are based upon what I've learned opening up data, and trying to move forward other API projects across other federal agencies, all the way down to the municipal level. I'm guessing my approach will be heavier on the business and politics of API platform operations, and lighter on the reliance on the technical elements, addressing in my opinion the biggest obstacle to API success--culture, silos, and delivering consistently across disparate groups working under a common vision.

Next, I will publish this and share with my partners for inclusion in the final response for the group. I'll make it available on API Evangelist, so that others can learn from the response to the RFI. I'm not sure where this will go next, but I can't ever miss out on an opportunity to respond to inquiries about API operations at this level. This RFI was the most sophisticated API-focused vision to come out of VA in my experience. Regardless, of what happens next, it demonstrates to me that there are groups within the VA that understand the API potential, and what it can do for veterans, and the organizations, hospitals, and communities that support them.
