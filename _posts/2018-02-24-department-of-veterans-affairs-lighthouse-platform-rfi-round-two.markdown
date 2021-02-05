---
published: true
layout: post
title: Round Two Of The Department of Veterans Affairs Lighthouse Platform RFI
date: 2018-02-24T09:00:00.000Z
tags:
  - API Evangelist
  - Federal Government
  - Strategy
  - Governance
  - Platform
image: >-
  http://kinlane-productions.s3.amazonaws.com/algorotoscope/builder/filtered/23_113_800_500_0_max_0_1_-1.jpg
---
<p><img src="http://kinlane-productions.s3.amazonaws.com/algorotoscope/builder/filtered/23_113_800_500_0_max_0_1_-1.jpg" align="right" width="45%" style="padding: 15px;" /></p>I'm spending some more time thinking about APIs at the Department of Veterans Affairs (VA), in response to round two of their request for information (RFI). [A couple months back I had responded to an earlier RFI](http://apievangelist.com/2017/10/26/my-response-on-the-department-of-veterans-affairs-rfi-for-the-lighthouse-api-management-platform/), providing as much information as I could think of, for consideration as part of their API journey. As a former VA employee, and son of two Vietnam Vets (yes two), you can say I'm always willing to invest some in APIs over at the VA.

To provide a response, I have taken the main questions they asked, broken them out here, and provided answers to the best of my ability. In my style, the answers are just free form rants, based upon my knowledge of the VA, and the wider API space. It is up to the VA, to decide what is relevant to them, and should be included in their agency API strategy.

**_2. Current Scope<br />
While the acquisition strategy for Lighthouse has not yet been formalized, VA envisions that the program will consist of multiple contracts.  For example, a contract for recommending policy and standards to form governance would likely be separate from an API build team.  The key high level activities below are anticipated to be included within these contracts, and VA is requesting feedback from industry on how these activities should be aligned between multiple contracts.  The list below is not inclusive of all tasks required to support this program.  Additionally, VA intends to provide the IAM solution and the provisioning of necessary cloud resources to host the proposed technology stack.  VA’s current enterprise cloud providers are Microsoft Azure and Amazon Web Services._**

**Microservice Focused Operational & Implementation**<br />
Lighthouse should embrace a microservices way of doing things, so that the platform can avoid legacy trappings when it comes to delivering software at the VA, which have resulted in large, monolithic systems, possessing enormous budgets, and entrenched teams, that are able to develop a resistance to change and evolution. This microservices way of doing things should be adopted internally, as well as externally, then applied to the technology, business, and politics of delivering ALL Lighthouse infrastructure.

All contracts should be defined and executed in a modular way, with the only distinction between  projects being operational, or for specific project implementations. Everything should be delivered as microservices, no matter whether it is in support of operating the Lighthouse platform, or delivering services to Lighthouse-driven applications. The technology and business of each service should be self-contained, modular, and focusing on doing one thing, and doing it well. Ensuring all services executed as part of Lighthouse operations are decoupled, working independently, allowing for easily defining, delivering, managing, evolving, and deprecating of every operational and implementational service that makes Lighthouse work.

Operational services will be the first projects delivered via the platform, and will be used to establish and mature the Lighthouse project deliver workflow, but then going forward, every additional operational, as well as specific implementation focused service will utilize the same workflow and life cycle.

- **Definitions** - Everything begins as a set of definitions. Leveraging OpenAPI, JSON Schema, Dockerfiles, and other common definitions to provide a human, and machine readable definition of every project, which is ultimately delivered as a microservice.
- **Github** - Each microservice begins as either a public or private Github repository, with a README index of the definition of what a service will deliver. Providing a self-contained, continuously deployed and integration blueprint of what a service does.
- **Architecture** - Always providing a comprehensive outline all backend architecture used to support a specific service, including the technical, as well as the business, and security policy elements of what it takes to deliver the required service.
- **Tooling** - Always providing a comprehensive outline of any tools used as part of delivering a service, to provide what is needed from a front-end delivery and execution vantage point.
- **Lifecycle** - Establish a lifecycle, that each service will need to pass through, ensuring consistent delivery, and management of services that adhere to governance standards.
	- **define** - What definitions are required for services?
    - **design** - What is the API design guidance involved?
    - **mock** - How are APIs and data virtualized as part of development?
    - **portal** - Which portals are service published to, or will possess?
    - **document** - What documentation is required and delivered?
    - **test** - Where are the code, as well as interface level tests?
    - **clients** - What client environment are in use for design, development, and testing?
    - ******* - Pause there, and repeat until the desired service is realized...
    - **deploy** - How are services delivered as part of a containerized, continuous deployment pipeline?
    - **dns** - What DNS is needed to address and route traffic to services?
    - **manage** - What API management level services are in place to secure, log, limit, and report of API and service consumption?
    - **logging** - What is the logging stack, how is it shipped, analyzed, and reported upon?
    - **monitor** - What monitors are required and in place for each service?
    - **performance** - How is performance measured and reported upon?
    - **sdk** - What client libraries, SDKs, and samples in place for service integration?
    - **depenencies** - What internal service, and external API dependencies are in play?
    - **licensing** - What is the data, code, interface, and other licensing that apply?
    - **privacy** - Are privacy policies in place, and considered for the platform, partners, developers, and end-users.
    - **terms** - Are terms of service in place, and independently considered for each service?
    - **monetization** - What are the operating costs, and other monetization considerations?
    - **plans** - What API consumption plans, rate limits, and policies in place to govern service usage?
    - **support** - What support mechanisms are in place, with relevant point of contacts?    
    - **communication** - What communication channels are in place, such as blogs, social, and messaging channels?
    - **observability** - What is the observability of each service, from open source to monitoring, and CI/CD workflows, ensuring it can be audited?
    - **discovery** - What is required to register, route, and discover an API as part of overall operations?
    - **evangelism** - What is the plan for making sure a service is known, used, and evangelized amongst target audience?
- **Governance** - How is each step along the life cycle measured, reported upon, and audited as part of governance, to understand how a service is meeting platform requirements, and evolving along a maturity path--allowing for innovation to occur, and newer ideas to flourish, but also allow more hardened, secure, and mature services to rise to the top.

The OpenAPI, JSON Schema, and other definitions for each microservice will ultimately be the contract for each project. Of course, to deliver the first set of operational platform services (compute, storage, DNS, pipeline, logging, etc.) these independent contracts might need to be grouped into a single, initial contract. Something that will also occur around different groups of services being delivered at any point in the future, but each individual service should be self-contained, with its own contract definition existing in it's Github repository core.

_**Question: API Roadmap Development (Backlog, Future)**_<br />
Each service being delivered via Lighthouse will possess its own self-contained road map as part of its definition. Providing a standardized, yet scalable way to address what is being planned, is being delivered, operated, and when anything will ultimately be deprecated.

- **Github Issues** - Each Github repository has it's own issues for managing all conversations around the service road map. Tags and milestones can be used to designate the past, present, future, and other relevant segmentation of the road map.
- **Micro / Macro** - Each services posses micro level detail about the road map, which is available via Github APIs, in a machine readable way for inclusion at the macro level, serving governance, reporting, and higher level road map considerations.
- **Communication** - Each service owner is responsible for road map related communication, support, and management providing their piece of the overall road map puzzle.

The Lighthouse platform road map should work like an orchestra, with each participant bringing their contribution, but platform operators and conductors defining the overall direction the platforms is headed. At scale, Lighthouse will be thousands of smaller units, organized by hundreds of service owners and stewards, serving millions of end-users, with feedback loops in service through the stack.

_**Question: Outreach (Internal & External Parties)**_<br />
Outreach is essential to the viability of any platform, and represents the business and political challenges that lie ahead for the VA, or any government agency looking to work seamlessly with public and private sector partners, as well as the public at large. There will be many services involved with Lighthouse operations that will need to be private, but the default should always be public, allowing for as much transparency and observability as possible, which will feed platform outreach in a positive way.

- **Github Project Pages** - Each Github repository can have a public facing Github Pages static site portal and landing page. Allowing for individual service, or group portals to exist, providing a destination for all stakeholders to get involved.
- **Github Social Framework** - Github provides a wealth of outreach and communication solutions from organization and repository search, to issues and wikis, and tagging services with individual topics. All of which can be used as part of outreach and engagement in a private or public setting.
- **Twitter** - Microblogging provides a great way to publish regular updates, and provide communication around platform operations.
- **Linkedin** - Enterprise development groups, especially those in service of the government tend to use Github for establishing their profile, and maintaining their presence, which can be incorporated into all outreach efforts.
- **Blogs** - The platform should possess its own public and / or private blogs, as well as potentially more topically, service, or project based blogs that expand outreach to the long tail of platform operations.

This type of outreach around platform operations is something that scares the hell out of government folks, and the majority of government APIs operation are critically deficient in the area of outreach. This has to change. If there is no feedback loop in place, and outreach doesn't occur regularly and consistently, the platform will not succeed. This is how the API world operates.

_**Question: Management of API Request Process (Internal (VA)/External (Non-VA))**_<br />
New services will always be needed. Operational and implementation related requests should all be treated the same. Obviously there will be different prioritization mechanisms in place, but API requests should just be the birth of any new service, allowing it to begin its journey, and transit through the API lifecycle described above. Not all requests will reach deployment, and not all deployments will reach maturity, but all API requests should be treated equally.

- **Definitions** - Each API request begins with a definition. A simple description of what a service will do.
- **Github** - Each API request begins its journey as a Github repository, with a README containing its basic definition, and conversation around its viability within Github issues.
- **JSON Schema** - As part of each request, all data that will be leverage as part of service operations should be defined as JSON Schema, and included in the Github repository.
- **OpenAPI** - Additionally, the access to the service, and its underlying data and resource should be defined using a machine readable OpenaPI definition, outlining the contract of the service.
- **Certification** - Some stakeholders will have submitted API requests before, and better understand the process, and be certified owners of existing services, working as part of trusted organizations, expediting and prioritizing the request process.
- **Template(s)** - The most common service patterns to emerge should be defined as template, providing seeds and starter projects to help expedite and streamline the API request process, ensuring all the moving parts are there to make a decision, in a forkable, replicable package.

New API requests should be encourage. Anyone should be able to submit a new service, replicate, or augment an existing service, or respond to a platform API RFP. The life cycle described above should be open to everyone looking to submit an API request. Allowing them to define, design, mock, and iterate their submission. Even providing a nearly usable representation of a service, even before the idea or service is accepted. Forcing everyone to flesh out their service, deliver a viable proof of concept, that will streamline the API acceptance process.

_**Question: Propose, Implement and Manage the PaaS (technology stack)**_<br />
As mentioned before, this aspect of Lighthouse should be delivered as microservices, alongside every other service being delivered via the platform. It just so happens that this portion of the stack will be the first to be delivered, and be iterated upon, evolved, and deprecated just like any other service. To put this in perspective, I will outline the AWS, and Azure infrastructure need to support management of the platform later on in this post, while considering the fact that AWS and Azure have been on the same journey that the VA is on with Lighthouse, something that has been playing out for the last decade.

The VA wants to be the Amazon of serving veterans. They want internal groups, vendors, contractors, veteran health and service organizations, and independent developers to come build their solutions on the Lighthouse platform. The VA should uses its own services for internal service delivery, as well as supporting external projects. The operational side of Lighthouse platform should be all microservice projects, with the underlying infrastructure being Azure or AWS solutions, providing a common platform as a service stack that can be leveraged, no matter where the actual service is deployed.

<p><img src="http://kinlane-productions.s3.amazonaws.com/algorotoscope/builder/filtered/68_113_800_500_0_max_0_-1_-1.jpg" align="right" width="45%" style="padding: 15px;" /></p>

_**Question: DevOps Continuous Integration and Continuous Delivery (CI/CD) of APIs**_<br />
Every service in support of operations or implementations via the Lighthouse platform will exist as a self-contained Github repository, with all the artifacts needed to be included in any application pipeline. The basic DNA blueprint for each service should be crafted to support any single CI/CD service, or ideally even multiple types of CI/CD and orchestration solutions like AWS and Azure both support.

- **Microservices** - Lighthouse CI/CD will be all about microservice orchestration, and using a variety of pipelines to deliver and evolve initially hundreds, and eventually thousands of services in concert.
- **Github** - Github will the cellular component driving the Lighthouse CI/CD workflow, providing individual service "legos" that can be composed, assembled, disassembled, and delivered in any way.
- **Definitions** - Each microservice will contain all the artifacts needed for supporting the entire life cycle listed above, driven by a variety of CI/CD pipelines. Leveraging dockerfiles, build packages, OpenAPI definitions, schema, and other definitions to continuously deliver and integrate across platform operations.

Both AWS and Azure provide CI/CD workflows, which can be used to satisfy the portion of the RFI. I will list out all the AWS and Azure services I think should be considered below. Additionally, Jenkins, CircleCI, or other 3rd party CI/CD could easily be brought in to deliver on this aspect of platform delivery. The microservices core can be used as part of any pipeline delivery model.

_**Question: Environment Operations & Maintenance (O&M)**_<br />
Again, everything operates as microservices, and gets delivered independently as services that can be configured and maintained as part of overall platform operations and maintenance, or in service of individual services, and groups of services supporting specific implementations.

- **Microservices** - Everything is available as microservices, allowing the underlying environment operations and maintainenace to be orchestration, and optimized in real time.

Each of the AWS and Azure services listed below are APIs. They allow for the configuration and management of each service via API or CLI, allowing the architecture to be seamlessly managed as part of the overall API stack, as well as the CI/CD pipeline. Making environment operations and maintenance, just part of the continuous delivery cycle(s).

_**Question: Release Management**_<br />
Release occurs at the granular service level. With Github and CI/CD as the vehicle for moving release forward daily, versioning, defining, and communicating all the way. With the proper code and API level testing in place, release management can happen safely at scale.

- **Github** - Github version control, branches, and release management should  be used as part of the overall release management strategy.
- **Versioning** - Establishment of a service versioning strategy for minor and major code, and interface releases, allowing independent release management that can occur at the higher orchestration level
- **CI/CD Pipelines** - Everything should be a pipeline, broken down by logical operational, organization, and project boundaries, operating on a continuous release cycle.
- **Microservices** - Everything is operated independently, and released independently via containers, with approach dependency management as part of each release.
- **Definitions** - OpenAPI and JSON Schema are versioned and use to act as the contract for each release.
- **Communications** - Along with each release, comes a standard approach to notification, communication, and support.

Release management will horizontally take a significant amount of time to wrap your head around. Moving forward hundreds, and thousands of services in concert won't be easy. However it will be more resilient, and forgiving than moving forward a single monolith.

_**Question: API Analytics**_<br />
Awareness should be baked in by default to the Lighthouse platform, measuring everything, and reporting on it consistently, providing observability across all aspects of operations in alignment with security policies. Analysis should be its own set of operational services, that span the entire length of the Lighthouse platform.

- **Log Shipping** - The database, container, web server, management, and DNS logs for ALL services should be shipped, and centralized, for complete access and analysis.
- **APIs** - Centralized logs should be its own service, with programmatic access to logs for all platform services.
- **Modular** - Analytics should be modular, bit-size API-driven elements that can be mixed, composed, published, and visualized in reusable ways.
- **Embeddables** - Modular, embeddable UI elements should be developed as applications on top of platform analytics APIs, allowing for portable dashboard that can be remixed, reused, and evolved.
- **Search** - The logging and reporting layer of the platform should have a core search element, allowing all logs to searched, as well as the logs for how API consumers are analyzing logs (mind blown).
- **Continouous** - As with all other services, analytics, reporting, and visualizations should be continuous, and ever evolving and deployed on a day to day, week to week basis.

A standard logging strategy across all services is how we achieve a higher level of API analytics, going beyond just database or web server statics, and even API management analytics, providing end to end, comprehensive platform service measurement, analysis, reporting, and visualization. Allowing platform operators, consumers, and auditors to access and understand how all service are being used, or not being used.

_**Question: Approval to Operate (ATO) Support for Environments**_<br />
Every service introduced as part of the Lighthouse platform should have all the information required to support ATO, with it baked into the governance and maturity life cycle for any service. It actually lends itself well to the maturity elements of the lifecycle above, ensuring there is ATO before anything is deployed.

- **Definitions** - All definitions are present for satisfying ATO.
- **Github** - Everything is self-contained within a single place for submission.
- **Governance** - ATO is part of the governance process, while still allowing for innovation.
- **Micro / Macro** - ATO for each individual service can be considered, as well as at the project, group levels, understanding where services fit in at macro level.

ATO can be built into the templated API request and submission process discussed earlier, allowing for already approved architecture, tooling, and patterns to be used over and over, streamlining the ATO cycle. Helping service developers enjoy more certainty around the ATO process, while still allowing for innovation to occur, pushing the ATO definition and process when it makes sense.

_**Question: Build APIs including system level APIs that connect into backend VA systems**_<br />
Everything is a microservice, and there are plenty of approaches to ensure that legacy backend systems can enjoy continued use and evolution through evolved APIs. The API life cycle allows for the evolution of existing backend systems that operate in the cloud and on-premise in small, bit-size service implementations.

- **Gateway** - AWS API Gateway and Azure API management makes it easy to publish newer APIs on top of legacy backend systems.
- **Facades** - Establishing facade patterns for modernizing, and evolving legacy systems, allowing them to take on a new interface, while still maintaining existing system.
- **OpenAPI** - Map out newer APIs using OpenAPI, then importing into gateways and wiring up with backend systems.
- **Schema**- Mapping out the schema transformations from backend systems to front-end API requests and responses using JSON Path, and JSON Schema.
- **Microservices** - Delivering newer APIs on top of legacy systems in smaller, more evolvable services.

From the frontend, you shouldn't be able to tell whether a legacy VA system is in use, or newer cloud infrastructure. All applications should be using APIs, and all APIs should be delivered as individual or groups of microservices, that do one thing and does it well. As APIs evolve, the backend systems should be decoupled and evolved as well, but until that becomes possible, all consumption of data, content, and other resources will be routed through the Lighthouse API stack.

_**Question: API key management or managing third party access (authorization, throttling, etc.)**_<br />
Both theAWS API Gateway, and Azure API Management allow for the delivery of modern API management infrastructure that can be used to govern internal, partner, and 3rd party access to resources. All applications should be using APIs, and ALL APIs should be using a standardized API management approach, no matter whether the consumption is internal or external. Ensuring consistent authorization, throttling, logging, and other aspects of doing business with APIs.

- **IAM** - Leverage API keys, JWT, and OAuth in conjunction with IAM policies governing which backend resources are available to API consumers.
- **Gateway** - All API traffic is routed through the AWS API Gateway and Azure API management layers, allowing for consistent and comprehensive management across all API consumption.
- **Management** - Apply consistent logging, rate limiting, transformations, error and security at the API management level, ensuring all services behave in the same way.
- **Plans** - Establishing of a variety of API plans that dictate API levels of access, which services are accessible to different API key levels, that are in sync with backend IAM policies.
- **Logging** - Every API call is logged, and contains user and application keys, allow ALL API consumption to be audited and reported upon, and responded to in real time.
- **Security** - Providing a single point of entry, and the ability to shut down access, striking the balance between access and security which is the hallmark of doing APIs.

API management is baked into the cloud. It is a discipline that has been evolving for over a decade, and is available on both the AWS and Azure platforms. The tools are there, Lighthouse just needs to establish a coherent strategy for authentication, service composition, logging, reporting, and responding to API consumption at scale in real time. Staying out of the way of consumers, while also ensuring that they only have access to the data, content, and other resources they are allowed to, in alignment with overall governance.

_**Management of API lifecycle in cloud, hybrid, and/or on premise environments**_<br />
All operational aspects of the Lighthouse platform should be developed as independent microservices, with a common API--no matter what the underlying architecture is. The DNS service API should be the same, regardless of whether it is managing AWS or Azure DNS, or possibly any other on-premise or 3rd party service--allowing for platform orchestration using a common API stack.

- **Microservices** - Each operational service is a microservice, with possibly multiple versions, depending on the backend architecture in use.
- **Containers** - Every operational service is operated as a container, allowing it to run in any cloud environment.
- **Github** - All services live as a Github repository, allowing it to be checked out and forked via any cloud platform.

The modular, containerized, microservice approach to delivering the Lighthouse platform will allow for the deployment, scaling, and redundant implementation of services in any cloud environment, as well as on-premise, or hybrid scenarios. All services operate using the same microservice footprint, using containers, and a consistent API surface area, allowing for the entire platform stack to be orchestrated against no matter where the actual service resides.

_**Question: 3. Use Case<br />
To better provide insight into aligning activities to contracts, VA has provided the use case below. Please walk through this use case discussing each activity and the contract it would be executed under.

**Veteran Verification Sample Use Case: VA has a need for a Veteran Verification API to verify a Veteran status from a number of VA backend systems to be shared internally and externally as an authoritative data source.  These backend systems potentially have conflicting data, various system owners, and varying degrees of system uptime._**

This is a common problem within large organizations, institutions, and government agencies. This is why we work to decouple, modularize, and scale not just the technology of building applications on backend systems, but also the business, and politics of it all. Introducing a competitive element when it comes to data management access, and building in redundancy, resilience, and a healthier incentive model into how we provide access to critical data, content, and other resources.

I have personal experience with this particular use case. One of the things I did while working at the VA, was conduct public data inventory, and move forward the conversation around a set of veteran benefit web services, which included asking the question--who had the authoritative record for a veteran? Many groups felt they were the authority, but in my experience, nobody actually did entirely. The incentives in this environment weren't about actually delivering a meaningful record on a veteran, it was all about getting a significant portion of the budget. I recommend decoupling the technology, business, and politics of providing access to veterans data using a microservices approach.

- **Microservices** - Break the veterans record into separate, meaningful services.
- **Definitions** - Ensure the definitions for the schema and API are open and accessible.
- **Discovery** - Make sure that the Veteran Verification API is full discoverable.
- **Testing** - Make sure the Verification API is fully tested on a regular basis.
- **Monitoring** - Ensure that there are regular monitors for the Verification API.
- **Redundancy** - Encourage multiple implementations of the same API to be delivered and owned by separate groups in separate regions, with circuit breaker behavior in APIs and applications.
- **Balancing** - Load balance between services and regions, allowing for auto-scaled APIs.
- **Aggregation** - Encourage the development of aggregate APIs that bridge multiple source, providing aggregate versions of the veteran's record, encouraging new service owners to improve on existing services.
- **Reliability** - Incentivize and reward reliability with Verification API owners, through revenue and priority access.

There should be no single owner of any critical VA service. Each service should have redundant versions of the service, available in different regions, and managed by separate owners. Competition should be encouraged, with facade and aggregate introduced, putting pressure on core service providers to deliver quality, or their service(s) will be de-prioritized, and newer services will be given traffic and revenue priority. The same backend database can be exposed via many different APIs, with a variety of owners and incentives in place to encourage the quality of service.

APIs, coupled with the proper terms of service in place can eliminate an environment where defensive data positions are established. If other API owners can get access to the same data, and offer a better quality API, then evangelize and gain traction with application owners, entrenched API providers will no longer flourish. Aggregate and facade APIs allow for the evolution of existing APIs, even if the API owners are unwilling to move and evolve. Shifting the definition of what is authoritative, making it much more liquid, allowing it to shift and evolve, rather than just be diluted and meaningless, as it is often seen in the current environment.

<p><img src="http://kinlane-productions.s3.amazonaws.com/algorotoscope/builder/filtered/69_113_800_500_0_max_0_-1_-1.jpg" align="right" width="45%" style="padding: 15px;" /></p>

_**Question: 4. Response<br />
In addition to providing the requested content above, VA asks for vendors to respond to the following questions:**

**Describe how you would align the aforementioned activities between contracts, and the recommended price structure for contracts?_**

Each microservice would have its own technical, business, and political contract, outline how the service will be delivered, managed, supported, communicated, and versioned. These contracts can be realized individually, or grouped together as a larger, aggregate contract that can be submitted, while still allowing each individual service within that contract to operate independently.

As mentioned before, the microservices approach isn't just about the technical components. It is about making the business of delivering vital VA services more modular, portable, and scalable. Something that will also decouple and shift the politics of delivering critical services to veterans. Breaking things down into much more manageable chunks that can move forward independently at the contract level.

- **Micro Procurement** - One of the benefits of breaking down services into small chunks, is that the money needed to deliver the service can become much smaller, potentially allowing for a much smaller, more liquid and flowing procurement cycle. Each service has a micro definition of the monetization involved with the service, which can be aggregated by groups of services and projects.
- **Micro Payments** - Payments for service deliver can be baked into the operations and life cycle of the service. API management excels at measuring how much a service is accessed, and testing, monitoring, logging, security, and other stops along the API life cycle can all be measured, and payments can be delivered depend on quality of service, as well as volume of service.

Amazon Web Services already has the model for defining, measuring, and billing for API consumption in this way. This is the bread and butter of the Amazon Web Services platform, and the cornerstone of what we know as the cloud. This approach to delivering, scaling, and ultimately billing or payment for the operation and consumption of resources, just needs to be realized by the VA, and the rest of the federal government. We have seen a shift in how government views the delivery and operation of technical resources using the cloud over the last five years, we just need to see the same shift for the business of APIs over the next five years.

_**Question: The Government envisions a managed service (ie: vendor responsible for all aspects including licenses, scaling, provisioning users, etc.) model for the entire technology stack.  How could this be priced to allow for scaling as more APIs are used?  For example, would it be priced by users, API calls, etc.?_**

API management is where you start this conversation. It has been used for a decade to measure, limit, and quantify the value being exchanged at the API level. Now that API management has been baked into the cloud, we are starting to see the approach being scaled to deliver at a marketplace level. With over ten years of experience with delivering, quantifying, metering and billing at the API level, Amazon is the best example of this monetization approach in action, with two distinct ways of quantifying the business of APIs.

- **AWS Marketplace Metering Service** - SaaS style billing model which provides a consumption monetization model in which customers are charged only for the number of resources they use--the best known cloud model.
- **AWS Contract Service** - Billing customers in advance for the use of software, providing an entitlement monetization model in which customers pay in advance for a certain amount of usage, which could be used to deliver certain amount of storage per month for a year, or a certain amount of end-user licenses for some amount of time.

This provides a framework for thinking about how the business of microservices can be delivered. Within these buckets, AWS provides a handful of common dimensions for thinking through the nuts and bolts of these approaches, quantifying how APIs can be monetized, in nine distinct areas:

- **Users** – One AWS customer can represent an organization with many internal users. Your SaaS application can meter for the number of users signed in or provisioned at a given hour. This category is appropriate for software in which a customer’s users connect to the software directly (for example, with customer-relationship management or business intelligence reporting).
- **Hosts** – Any server, node, instance, endpoint, or other part of a computing system. This category is appropriate for software that monitors or scans many customer-owned instances (for example, with performance or security monitoring). Your application can meter for the number of hosts scanned or provisioned in a given hour.
- **Data** – Storage or information, measured in MB, GB, or TB. This category is appropriate for software that manages stored data or processes data in batches. Your application can meter for the amount of data processed in a given hour or how much data is stored in a given hour.
- **Bandwidth** – Your application can bill customers for an allocation of bandwidth that your application provides, measured in Mbps or Gbps. This category is appropriate for content distribution or network interfaces. Your application can meter for the amount of bandwidth provisioned for a given hour or the highest amount of bandwidth consumed in a given hour.
- **Request** – Your application can bill customers for the number of requests they make. This category is appropriate for query-based or API-based solutions. Your application can meter for the number of requests made in a given hour.
- **Tiers** – Your application can bill customers for a bundle of features or for providing a suite of dimensions below a certain threshold. This is sometimes referred to as a feature pack. For example, you can bundle multiple features into a single tier of service, such as up to 30 days of data retention, 100 GB of storage, and 50 users. Any usage below this threshold is assigned a lower price as the standard tier. Any usage above this threshold is charged a higher price as the professional tier. Tier is always represented as an amount of time within the tier. This category is appropriate for products with multiple dimensions or support components. Your application should meter for the current quantity of usage in the given tier. This could be a single metering record (1) for the currently selected tier or feature pack.
- **Units** – Whereas each of the above is designed to be specific, the dimension of Unit is intended to be generic to permit greater flexibility in how you price your software. For example, an IoT product which integrates with device sensors can interpret dimension “Units” as “sensors”. Your application can also use units to make multiple dimensions available in a single product. For example, you could price by data and by hosts using Units as your dimension. With dimensions, any software product priced through the use of the Metering Service must specify either a single dimension or define up to eight dimensions, each with their own price.

These dimensions reflect the majority of API services being sold out there today, we don't find ourselves in a rut with measuring value, like just paying per API call. Allowing Lighthouse API plans to possess one or more dimensions, beyond any single use case.

- **Single Dimension** - This is the simplest pricing option. Customers pay a single price per resource unit per hour, regardless of size or volume (for example, $0.014 per user per hour, or $0.070 per host per hour).
- **Multiple Dimensions** – Use this pricing option for resources that vary by size or capacity. For example, for host monitoring, a different price could be set depending on the size of the host. Or, for user-based pricing, a different price could be set based on the type of user (admin, power user, and read-only user). Your service can be priced on up to eight dimensions. If you are using tier-based pricing, you should use one dimension for each tier.

This provides a framework that Lighthouse can provide to 3rd party developers, allowing them to operate their services within a variety of business models. Derived from many of the hard costs they face, and providing additional volume based revenue, based upon how may API calls of any particular service receives.

Beyond this basic monetization framework, I'd add in an incentive framework that would dovetail with the business models proposed, but then provide different pricing levels depending on how well the services perform, and deliver on the agreed upon API contract. There are a handful of bullets I'd consider here.

- **Design** - How well does a service meet API design guidelines set forth in governance guidance.
- **Monitoring** - Has a service consistently met its monitoring goals, delivering against an agreed upon service level agreement (SLA).
- **Testing** - Beyond monitoring, are APIs meeting granular interface testing, along a regular testing & monitoring schedule.
- **Communication** - Are service owners meeting expectations around communication around a service operations.
- **Support** - Does a service meet required support metrics, making sure it is responsive and helpful.
- **Ratings** - Provide a basic set of metrics, with accompanying ratings for each service.
- **Certification** - Allowing service providers to get certified, receiving better access, revenue, and priority.

All of the incentive framework is defined and enforced via the API governance strategy for the platform. Making sure all microservices, and their owners meet a base set of expectations. When you take the results and apply weekly, monthly, and quarterly against the business framework, you can quickly begin to see some different pricing levels, and revenue opportunities around all microservices emerge. You deliver consistent, reliable, highly ranked microservices, you get paid higher percentages, enjoy greater access to resources, and prioritization in different ways via the platform--if you don't, you get paid less, and operate fewer services.

This model is already visible on the AWS platform. All the pieces are there to make it happen for any platform, operating on top of the AWS platform. The marketplace, billing, and AWS API Gateway connection to API plans exists. When you combine the authentication and service composition available at the AWS API Gateway layer, with the IAM policy solutions available via AWS, an enterprise grade solution for delivering this model securely at scale, comes into focus.

_**Question: Is there a method of paying or incentivizing the contractor based on API usage?**_<br />
I think I hit on this with the above answer(s). Keep payments small, and well defined. Measured, reported upon, and priced using the cloud model, connecting to a clear set of API governance guidance and expectations. The following areas can support paying and incentivizing contractors based upon not just usage, but also meeting the API contract.

- **Management** - API management puts all microservices into plans, then log, meter, and track on value exchanged at this level.
- **Marketplace** - Turning the platform into a marketplace that can be occupied by a variety of internal, pattern, vendor, 3rd party, and public actors.
- **Monetization** - Granular understanding of all the resources it takes to deliver each individual service, and understand the costs associated with operating at scale.
- **Plans** - A wealth of API plans in place at the API gateway level, something that is tied to IAM policies, and in alignment with API governance expectations.
- **Governance** - Providing a map, and supporting guidance around the Lighthouse platform API governance. Understanding, measuring, and enforcing consistency across the API lifecycle--platform wide.
- **Value Exchange** - Using the cloud model, which is essentially the original API management, marketplace, and economy model. Not just measuring consumption, but used to maximize and generate revenue from the value exchanged across the platform.

When you operate APIs on AWS and Azure, the platform as a service layer can utilize and benefit from the underlying infrastructure as a service monetization framework. Meaning, you can use AWS's business model for managing the measuring, paying, and incentivizing of microservice owners. All the gears are there, they just need to be set in motion to support the management of a government API marketplace platform.

_**Based on the information provided, please discuss your possible technology stack and detail your experience supporting these technologies.**_<br />
Both Amazon Web Services and Azure provide the building blocks of what you need to execute the above. Each cloud platform has its own approach to delivering infrastructure at scale. Providing an interesting mix of API driven resources you can jumpstart any project.
<p><img src="http://kinlane-productions.s3.amazonaws.com/algorotoscope/builder/filtered/27_113_800_500_0_max_0_-1_-1.jpg" align="right" width="45%" style="padding: 15px;" /></p>
**AWS**
First, let's take a look at what is relevant to this vision from the Amazon Web Services side of things. These are all the core AWS solutions on the table, with dashboard, API, and command line access to get the job done.

**Compute**
- <a href="https://aws.amazon.com/ec2/?hp=tile&amp;so-exp=below">Amazon EC2</a> - Virtual Servers in the Cloud
- <a href="https://aws.amazon.com/ec2/autoscaling/?hp=tile&amp;so-exp=below">Amazon EC2 Auto Scaling</a> - Scale Compute Capacity to Meet Demand
- <a href="https://aws.amazon.com/ecs/?hp=tile&amp;so-exp=below">Amazon Elastic Container Service</a> - Run and Manage Docker Containers
- <a href="https://aws.amazon.com/eks/?hp=tile&amp;so-exp=below">Amazon Elastic Container Service for Kubernetes</a> - Run Managed Kubernetes on AWS
- <a href="https://aws.amazon.com/ecr/?hp=tile&amp;so-exp=below">Amazon Elastic Container Registry</a> - Store and Retrieve Docker Images
- <a href="https://aws.amazon.com/lightsail/?hp=tile&amp;so-exp=below">Amazon Lightsail</a> - Launch and Manage Virtual Private Servers
- <a href="https://aws.amazon.com/fargate/?hp=tile&amp;so-exp=below">AWS Fargate</a> - Run Containers without Managing Servers or Clusters
- <a href="https://aws.amazon.com/batch/?hp=tile&amp;so-exp=below">AWS Batch</a> - Run Batch Jobs at Any Scale
- <a href="https://aws.amazon.com/lambda/?hp=tile&amp;so-exp=below">AWS Lambda</a> - Run your Code in Response to Events
- <a href="https://aws.amazon.com/serverlessrepo/?hp=tile&amp;so-exp=below">AWS Serverless Application Repository</a> - Discover, Deploy, and Publish Serverless Applications Auto Scaling

**Storage**
<a href="https://aws.amazon.com/s3/?hp=tile&amp;so-exp=below">Amazon S3</a> - Scalable Storage in the Cloud
<a href="https://aws.amazon.com/ebs/?hp=tile&amp;so-exp=below">Amazon EBS</a> - Block Storage for EC2
<a href="https://aws.amazon.com/efs/?hp=tile&amp;so-exp=below">Amazon Elastic File System</a> - Managed File Storage for EC2
<a href="https://aws.amazon.com/glacier1/?hp=tile&amp;so-exp=below">Amazon Glacier</a> - Low-cost Archive Storage in the Cloud
<a href="https://aws.amazon.com/storagegateway/?hp=tile&amp;so-exp=below">AWS Storage Gateway</a> - Hybrid Storage Integration

**Database**
- <a href="https://aws.amazon.com/rds/aurora/?hp=tile&amp;so-exp=below">Amazon Aurora</a> - High Performance Managed Relational Database
- <a href="https://aws.amazon.com/rds/?hp=tile&amp;so-exp=below">Amazon RDS</a> - Managed Relational Database Service for MySQL, PostgreSQL, Oracle, SQL Server, and MariaDB
- <a href="https://aws.amazon.com/dynamodb/?hp=tile&amp;so-exp=below">Amazon DynamoDB</a> - Managed NoSQL Database
- <a href="https://aws.amazon.com/elasticache/?hp=tile&amp;so-exp=below">Amazon ElastiCache</a> - In-memory Caching System
- <a href="https://aws.amazon.com/redshift/?hp=tile&amp;so-exp=below">Amazon Redshift</a> - Fast, Simple, Cost-effective Data Warehousing

**Authentication**
- <a href="https://aws.amazon.com/iam/?hp=tile&amp;so-exp=below">AWS Identity &amp; Access Management</a> - Manage User Access and Encryption Keys
- <a href="https://aws.amazon.com/cognito/?hp=tile&amp;so-exp=below">Amazon Cognito</a> - Identity Management for your Apps
- <a href="https://aws.amazon.com/single-sign-on/?hp=tile&amp;so-exp=below">AWS Single Sign-On</a> - Cloud Single Sign-On (SSO) Service
- a href="https://aws.amazon.com/cloudhsm/?hp=tile&amp;so-exp=below">AWS CloudHSM</a> - Hardware-based Key Storage for Regulatory Compliance

**Management**
- <a href="https://aws.amazon.com/api-gateway/?hp=tile&amp;so-exp=below">Amazon API Gateway</a> - Build, Deploy, and Manage APIs
- <a href="https://aws.amazon.com/autoscaling/?hp=tile&amp;so-exp=below">AWS Auto Scaling</a> - Scale Multiple Resources to Meet Demand
- <a href="https://aws.amazon.com/cloudformation/?hp=tile&amp;so-exp=below">AWS CloudFormation</a> - Create and Manage Resources with Templates

**Logging**
- <a href="https://aws.amazon.com/cloudwatch/?hp=tile&amp;so-exp=below">Amazon CloudWatch</a> - Monitor Resources and Applications
- <a href="https://aws.amazon.com/cloudtrail/?hp=tile&amp;so-exp=below">AWS CloudTrail</a> - Track User Activity and API Usage

**Network**
- <a href="https://aws.amazon.com/vpc/?hp=tile&amp;so-exp=below">Amazon VPC</a> - Isolated Cloud Resources
- <a href="https://aws.amazon.com/cloudfront/?hp=tile&amp;so-exp=below">Amazon CloudFront</a> - Global Content Delivery Network
- <a href="https://aws.amazon.com/route53/?hp=tile&amp;so-exp=below">Amazon Route 53</a> - Scalable Domain Name System

**Discovery**
- <a href="https://aws.amazon.com/application-discovery/?hp=tile&amp;so-exp=below">AWS Application Discovery Service</a> - Discover On-Premises Applications to Streamline Migration
- <a href="https://aws.amazon.com/servicecatalog/?hp=tile&amp;so-exp=below">AWS Service Catalog</a> - Create and Use Standardized Products

Migration
- <a href="https://aws.amazon.com/dms/?hp=tile&amp;so-exp=below">AWS Database Migration Service</a> - Migrate Databases with Minimal Downtime
- <a href="https://aws.amazon.com/server-migration-service/?hp=tile&amp;so-exp=below">AWS Server Migration Service</a> - Migrate On-Premises Servers to AWS

**Orchestration**
- <a href="https://aws.amazon.com/codedeploy/?hp=tile&amp;so-exp=below">AWS CodeDeploy</a> - Automate Code Deployment
- <a href="https://aws.amazon.com/codepipeline/?hp=tile&amp;so-exp=below">AWS CodePipeline</a> - Release Software using Continuous Delivery
- <a href="https://aws.amazon.com/config/?hp=tile&amp;so-exp=below">AWS Config</a> - Track Resource Inventory and Changes
- <a href="https://aws.amazon.com/systems-manager/?hp=tile&amp;so-exp=below">AWS Systems Manager</a> - Gain Operational Insights and Take Action

**Monitoring**
- <a href="https://aws.amazon.com/trustedadvisor/?hp=tile&amp;so-exp=below">AWS Trusted Advisor</a> - Optimize Performance and Security
- <a href="https://aws.amazon.com/premiumsupport/phd/?hp=tile&amp;so-exp=below">AWS Personal Health Dashboard</a> - Personalized View of AWS Service Health

**Security**
- <a href="https://aws.amazon.com/guardduty/?hp=tile&amp;so-exp=below">Amazon GuardDuty</a> - Managed Threat Detection Service
- <a href="https://aws.amazon.com/certificate-manager/?hp=tile&amp;so-exp=below">AWS Certificate Manager</a> - Provision, Manage, and Deploy SSL/TLS Certificates
- <a href="https://aws.amazon.com/shield/?hp=tile&amp;so-exp=below">AWS Shield</a> - DDoS Protection
- <a href="https://aws.amazon.com/waf/?hp=tile&amp;so-exp=below">AWS WAF</a> - Filter Malicious Web Traffic

**Analytics**
- <a href="https://aws.amazon.com/athena/?hp=tile&amp;so-exp=below">Amazon Athena</a> - Query Data in S3 using SQL
- <a href="https://aws.amazon.com/cloudsearch/?hp=tile&amp;so-exp=below">Amazon CloudSearch</a> - Managed Search Service
- <a href="https://aws.amazon.com/redshift/?hp=tile&amp;so-exp=below">Amazon Redshift</a> - Fast, Simple, Cost-effective Data Warehousing

**Integration**
- <a href="https://aws.amazon.com/step-functions/?hp=tile&amp;so-exp=below">AWS Step Functions</a> - Coordinate Distributed Applications
- <a href="https://aws.amazon.com/sqs/?hp=tile&amp;so-exp=below">Amazon Simple Queue Service (SQS)</a> - Managed Message Queues
- <a href="https://aws.amazon.com/sns/?hp=tile&amp;so-exp=below">Amazon Simple Notification Service (SNS)</a> - Pub/Sub, Mobile Push and SMS
- <a href="https://aws.amazon.com/amazon-mq/?hp=tile&amp;so-exp=below">Amazon MQ</a> - Managed Message Broker for ActiveMQ

I'm a big fan of the AWS approach. Their marketplace, and AWS API gateway provide unprecedented access to backend cloud, and on-premise resources, which can be secured using AWS IAM. Amazon Web Services products a robust infrastructure as a services, adequate enough to deliver any platform as a services solutions.

**Azure**

Next, let's look at the Azure stack to see what they bring to the table. There is definitely some overlap with the AWS list of resources, but Microsoft has a different view of the landscape than Amazon does. However, similar to Amazon, most of the building blocks are here to deliver on the proposal above.

**Compute**
- <a href="https://azure.microsoft.com/en-us/services/virtual-machines/">Virtual Machines</a> - Provision Windows and Linux virtual machines in seconds
- <a href="https://azure.microsoft.com/en-us/services/app-service/">App Service</a> - Quickly create powerful cloud apps for web and mobile
- <a href="https://azure.microsoft.com/en-us/services/functions/">Functions</a> - Process events with serverless code
- <a href="https://azure.microsoft.com/en-us/services/batch/">Batch</a> - Cloud-scale job scheduling and compute management
- <a href="https://azure.microsoft.com/en-us/services/container-instances/">Container Instances</a> - Easily run containers with a single command
- <a href="https://azure.microsoft.com/en-us/services/service-fabric/">Service Fabric</a> - Develop microservices and orchestrate containers on Windows or Linux
- a href="https://azure.microsoft.com/en-us/services/virtual-machine-scale-sets/">Virtual Machine Scale Sets</a> - Manage and scale up to thousands of Linux and Windows virtual machines
- <a href="https://azure.microsoft.com/en-us/services/container-service/">Azure Container Service (AKS)</a> - Simplify the deployment, management, and operations of Kubernetes
- <a href="https://azure.microsoft.com/en-us/services/cloud-services/">Cloud Services</a> - Create highly-available, infinitely-scalable cloud applications and APIs
- <a href="https://azure.microsoft.com/en-us/services/virtual-machines/linux-and-open/">Linux Virtual Machines</a> - Provision virtual machines for Ubuntu, Red Hat, and more
- <a href="https://azure.microsoft.com/en-us/services/">Windows Virtual Machines</a> - Provision virtual machines for SQL Server, SharePoint, and more

**Storage**
- <a href="https://azure.microsoft.com/en-us/services/storage/">Storage</a> - Durable, highly available, and massively scalable cloud storage
- <a href="https://azure.microsoft.com/en-us/services/backup/">Backup</a> - Simple and reliable server backup to the cloud
- <a href="https://azure.microsoft.com/en-us/services/storsimple/">StorSimple</a> - Lower costs with an enterprise hybrid cloud storage solution
- <a href="https://azure.microsoft.com/en-us/services/site-recovery/">Site Recovery</a> - Orchestrate protection and recovery of private clouds
- <a href="https://azure.microsoft.com/en-us/services/data-lake-store/">Data Lake Store</a> - Hyperscale repository for big data analytics workloads
- <a href="https://azure.microsoft.com/en-us/services/storage/blobs/">Blob Storage</a> - REST-based object storage for unstructured data
- <a href="https://azure.microsoft.com/en-us/services/storage/unmanaged-disks/">Disk Storage</a> - Persistent, secured disk options supporting virtual machines
- <a href="https://azure.microsoft.com/en-us/services/managed-disks/">Managed Disks</a> - Persistent, secured disk storage for Azure virtual machines
- <a href="https://azure.microsoft.com/en-us/services/storage/queues/">Queue Storage</a> - Effectively scale apps according to traffic
- <a href="https://azure.microsoft.com/en-us/services/storage/files/">File Storage</a> - File shares that use the standard SMB 3.0 protocol
<p><img src="http://kinlane-productions.s3.amazonaws.com/algorotoscope/builder/filtered/27_113_800_500_0_max_0_-1_-1.jpg" align="right" width="45%" style="padding: 15px;" /></p>
**Deployment**
- <a href="https://azure.microsoft.com/en-us/services/app-service/api/">API Apps</a> - Easily build and consume Cloud APIs

**Containers**
- <a href="https://azure.microsoft.com/en-us/services/app-service/">App Service</a> - Quickly create powerful cloud apps for web and mobile
- <a href="https://azure.microsoft.com/en-us/services/batch/">Batch</a> - Cloud-scale job scheduling and compute management
- <a href="https://azure.microsoft.com/en-us/services/container-registry/">Container Registry</a> - Store and manage container images across all types of Azure deployments
- <a href="https://azure.microsoft.com/en-us/services/container-instances/">Container Instances</a> - Easily run containers with a single command
- <a href="https://azure.microsoft.com/en-us/services/service-fabric/">Service Fabric</a> - Develop microservices and orchestrate containers on Windows or Linux
- <a href="https://azure.microsoft.com/en-us/services/container-service/">Azure Container Service (AKS)</a> - Simplify the deployment, management, and operations of Kubernetes

**Databases**
- <a href="https://azure.microsoft.com/en-us/services/sql-database/">SQL Database</a> - Managed relational SQL Database as a service
- <a href="https://azure.microsoft.com/en-us/services/cosmos-db/">Azure Cosmos DB</a> - Globally distributed, multi-model database for any scale
- <a href="https://azure.microsoft.com/en-us/services/sql-data-warehouse/">SQL Data Warehouse</a> - Elastic data warehouse as a service with enterprise-class features
- <a href="https://azure.microsoft.com/en-us/services/cache/">Redis Cache</a> - Power applications with high-throughput, low-latency data access
- <a href="https://azure.microsoft.com/en-us/services/sql-server-stretch-database/">SQL Server Stretch Database</a> - Dynamically stretch on-premises SQL Server databases to Azure
- <a href="https://azure.microsoft.com/en-us/services/storage/tables/">Table Storage</a> - NoSQL key-value store using semi-structured datasets
- <a href="https://azure.microsoft.com/en-us/services/postgresql/">Azure Database for PostgreSQL</a> - Managed PostgreSQL database service for app developers
- <a href="https://azure.microsoft.com/en-us/services/mysql/">Azure Database for MySQL</a> - Managed MySQL database service for app developers
- <a href="https://azure.microsoft.com/en-us/services/database-migration/">Azure Database Migration Service</a> - Simplify on-premises database migration to the cloud

**Authentication**
<a href="https://azure.microsoft.com/en-us/services/active-directory/">Azure Active Directory</a> - Synchronize on-premises directories and enable single sign-on
<a href="https://azure.microsoft.com/en-us/services/multi-factor-authentication/">Multi-Factor Authentication</a> - Add security for your data and apps without adding hassles for users
<a href="https://azure.microsoft.com/en-us/services/key-vault/">Key Vault</a> - Safeguard and maintain control of keys and other secrets
<a href="https://azure.microsoft.com/en-us/services/active-directory-b2c/">Azure Active Directory B2C</a> - Consumer identity and access management in the cloud

**Management**
- <a href="https://azure.microsoft.com/en-us/services/api-management/">API Management</a> - Publish APIs to developers, partners, and employees securely and at scale

**Logging**
- <a href="https://azure.microsoft.com/en-us/services/log-analytics/">Log Analytics</a> - Collect, search, and visualize machine data from on-premises and cloud
- <a href="https://azure.microsoft.com/en-us/services/traffic-manager/">Traffic Manager</a> - Route incoming traffic for high performance and availability

**Monitoring**
- <a href="https://azure.microsoft.com/en-us/services/monitor/">Azure Monitor</a> - Highly granular and real-time monitoring data for any Azure resource
- <a href="https://azure.microsoft.com/en-us/features/azure-portal/">Microsoft Azure portal</a> - Build, manage, and monitor all Azure products in a single, unified console

**Analytics**
- <a href="https://azure.microsoft.com/en-us/services/hdinsight/">HDInsight</a> - Provision cloud Hadoop, Spark, R Server, HBase, and Storm clusters
- <a href="https://azure.microsoft.com/en-us/services/hdinsight/apache-spark/">Apache Spark for Azure HDInsight</a> - Apache Spark in the cloud for mission critical deployments
- <a href="https://azure.microsoft.com/en-us/services/hdinsight/apache-storm/">Apache Storm for HDInsight</a> - Real-time stream processing made easy for big data
- <a href="https://azure.microsoft.com/en-us/services/sql-data-warehouse/">SQL Data Warehouse</a> - Elastic data warehouse as a service with enterprise-class features
- <a href="https://azure.microsoft.com/en-us/services/log-analytics/">Log Analytics</a> - Collect, search, and visualize machine data from on-premises and cloud
- <a href="https://azure.microsoft.com/en-us/services/data-lake-store/">Data Lake Store</a> - Hyperscale repository for big data analytics workloads
- <a href="https://azure.microsoft.com/en-us/services/data-lake-analytics/">Data Lake Analytics</a> - Distributed analytics service that makes big data easy
- <a href="https://azure.microsoft.com/en-us/services/analysis-services/">Azure Analysis Services</a> - Enterprise grade analytics engine as a service
- <a href="https://azure.microsoft.com/en-us/services/databricks/">Azure Databricks</a> - Fast, easy, and collaborative Apache Spark-based analytics platform  

**Network**
- <a href="https://azure.microsoft.com/en-us/services/cdn/">Content Delivery Network</a> - Ensure secure, reliable content delivery with broad global reach
- <a href="https://azure.microsoft.com/en-us/services/dns/">Azure DNS</a> - Host your DNS domain in Azure
- <a href="https://azure.microsoft.com/en-us/services/virtual-network/">Virtual Network</a> - Provision private networks, optionally connect to on-premises datacenters
- <a href="https://azure.microsoft.com/en-us/services/traffic-manager/">Traffic Manager</a> - Route incoming traffic for high performance and availability
- <a href="https://azure.microsoft.com/en-us/services/load-balancer/">Load Balancer</a> - Deliver high availability and network performance to your applications
- <a href="https://azure.microsoft.com/en-us/services/network-watcher/">Network Watcher</a> - Network performance monitoring and diagnostics solution  

**Orchestration**  
- <a href="https://azure.microsoft.com/en-us/services/scheduler/">Scheduler</a> - Run your jobs on simple or complex recurring schedules
- <a href="https://azure.microsoft.com/en-us/services/automation/">Automation</a> - Simplify cloud management with process automation
- <a href="https://azure.microsoft.com/en-us/services/automation-control/">Automation &amp; Control</a> - Centrally manage all automation and configuration assets  

**Integration**
- <a href="https://azure.microsoft.com/en-us/services/data-factory/">Data Factory</a> - Orchestrate and manage data transformation and movement
- <a href="https://azure.microsoft.com/en-us/services/logic-apps/">Logic Apps</a> - Automate the access and use of data across clouds without writing code
- <a href="https://azure.microsoft.com/en-us/services/event-grid/">Event Grid</a> - Get reliable event delivery at massive scale  

**Search**
- <a href="https://azure.microsoft.com/en-us/services/search/">Azure Search</a> - Fully-managed search-as-a-service

**Discovery**      
- <a href="https://azure.microsoft.com/en-us/services/active-directory-ds/">Azure Active Directory Domain Services</a> - Join Azure virtual machines to a domain without domain controllers  

**Security**
- <a href="https://azure.microsoft.com/en-us/services/security-center/">Security Center</a> - Unify security management and enable advanced threat protection across hybrid cloud workloads
- <a href="https://azure.microsoft.com/en-us/services/security-compliance/">Security &amp; Compliance</a> - Enable threat detection and prevention through advanced cloud security
- <a href="https://azure.microsoft.com/en-us/services/ddos-protection/">Azure DDoS Protection</a> - Protect your applications from Distributed Denial of Service (DDoS) attacks  

**Governance**
- <a href="https://azure.microsoft.com/en-us/services/azure-policy/">Azure Policy</a> - Implement corporate governance and standards at scale for Azure resources

**Monetization**
- <a href="https://azure.microsoft.com/en-us/services/cost-management/">Cost Management</a> - Optimize what you spend on the cloud, while maximizing cloud potential

**Experience**<br />
I have been studying Amazon full time for almost eight years. I've been watching Azure play catch up for the last three years. I run my infrastructure, and a handful of clients on AWS. I understand the API landscape of both providers, and how they can be woven into vision proposed so far.

I see the AWS API stack, and the Azure API stack, as a starter set of services that can be built upon to deliver the base Lighthouse implementation. All the components are there. It just need the first set of Lighthouse services to be defined, delivering the essential building blocks  any platform needs, things like compute, storage, dns, messaging, etc. I recommend that the VA Lighthouse team take the AWS API stack, and mold it into v1 of the Lighthouse API stack. Take the momentum from AWS's own API journey, build upon it, and set into motion the VA Lighthouse API journey.

Enable VA services to be delivered as individual, self-contained units, that can be used as part of a larger VA orchestration of veteran services. Open up the VA and let some sunlight in. Think about what Amazon has been able to achieve by delivering its own internal operations as services, and remaking not just retail, but also touching almost every other industry with Amazon Web Services. [The Amazon Web Services myth story](https://apievangelist.com/2012/01/12/the-secret-to-amazons-success-internal-apis/) provides a powerful and compelling narrative for any company, organizations, institution, or government agency like the VA to emulate.

This proposal is not meant to be a utopian vision for the VA. However it is meant to, as the name of the project reflects, shine a light on existing ways of delivering services via the cloud. Helping guide each service in its own individual journey, while also serving the overall mission of the platform--to help the veteran be successful in their own personal journey.

<p><img src="https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories/pano-lighthouse_copper_circuit.jpg" width="100%" align="center"></p>
