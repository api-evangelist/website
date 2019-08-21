---
published: true
layout: post
title: 'Multiple Overlapping API Life Cycle(s)'
date: 2019-08-21T09:00:00.000Z
tags:
  - API Evangelist
  - Life Cycle
  - Management
  - Deployment
  - Design
  - Documentation
image: https://s3.amazonaws.com/kinlane-productions/algorotoscope-master/stories-downtheline-dali-three.jpg
---
<img src="{{ page.image }}" width="45%" align="right" style="padding: 15px;" />
One of the toughest parts about teaching people about APIs is that there are many different views of what the API life cycle can be depending on who you are, and what your intentions are. As an advocate or evangelist for a single API you are speaking externally to the API consumption life cycle, but internally you are focused on the API delivery life cycle. As an API Evangelist for many APIs, targeting providers, consumers, and anyone else who comes along, I find it a constant challenge to properly speak to my intended audience. One problematic part of my storytelling I regularly see emerge is that I speak of a single API life cycle, where in reality there are many overlapping life cycles. So, to help me think through all of this I wanted to explore what these overlapping tracks might be—coming up with four distinct iterations of overlapping API building blocks.

## The API Delivery Life Cycle 
The most common way we refer to the API life cycle is from the perspective of the API provider, where it is all about delivering an API. Referencing the stops along the life cycle that are most relevant to someone who is  delivering a new API, or might be moving an API forward as part of the evolution of an existing resource. From my vantage point, I consider these to be the most common stops along the API delivery life cycle.

- **Definitions** - Defining what an API does, crafting the JSON schema, OpenAPI, AsyncAPI, and other machine readable definitions of what is potentially being delivered, initializing the contract that will guide an API through the life cycle.
- **Design** - Stepping back and considering the healthiest API Design practices to apply, working from a diverse API toolbox, and ensuring you have a good handle on who your audience is, and the design patterns they’ll respond to.
- **Mocking** - Generating a mock instance of an API using the contract to test out design patterns, and begin socializing amongst technical and business stakeholders so that they can begin providing critical feedback on the design.
- **Documentation** - Making sure there is auto-generated documentation available for all providers and consumers from the agreed upon API contract definition, ensuring there is machine and human readable documentation available at all times.
- **Testing** - As the API contract stabilizes, tests can be generated to ensure that the contract is not veering of the intended course, providing guardrails that can be regularly rebuilt from the API contract, and ultimately used in production.
- **Deployment** - Publishing of an API either using an open source framework, gateway, or through hand coding of the interfaces, providing a production ready instance of an individual API contract that was defined early on.
- **Management** - Making sure an API requires proper authentication, has access levels and rate limits defined, as well as logging enabled, so that its access can be properly quantified, managed, and reported upon for provider and consumer.
- **Monitoring** - Ensuring that each API is being monitored in real time from multiple regions, ensuring that an API is up and available, as well as passing all tests that have been defined as part of the development of each API contract.
- **Security** - Knowing that requiring authentication will not be enough, and that all APIs are regularly scanned, probed, and pushed for any potential vulnerabilities, providing regular accounting of the security of al APIs in operation.

I can quickly add on another 10-20 stops along the API delivery life cycle, but I want to highlight the core building blocks of delivering an API, not exhaustively document every possible building block. These are the primary steps any API provider will need to master before they can begin competently delivering API resources for consumption internally, or externally to partners and the general public. Providing a basic checklist that can be use to flesh out the details needed before an API can be called production-ready, then begin it’s life as the back-end for web, mobile, device, and network applications.

## API Consumption Life Cycle
<img src="https://s3.amazonaws.com/kinlane-productions/algorotoscope-master/subway-subway-internet-numbers.jpg" width="45%" align="right" style="padding: 15px;" />
Next, I wanted to explore the flip side of the API life cycle, and the view from the position of the API consumer. This is the second most common way I talk about the API life cycle, but I find that I often get things mixed up between provider and consumer, and I know from experience that I do not always ensure that things are made clear. To help me put myself into the shoes of API consumers, I wanted to explore what some of the stops along the API life cycle from purely a consumption standpoint—here are a few that I’m thinking about today.

- **Discovery** - Before you can consume an API you have to be able to find it, and be able to get what need to get up and running.
- **Documentation** - You will have to be able to understand the details of what an API does, and ultimately what it delivers via documentation.
- **Plans** - Once you understand what an API does, you will need to have a grasp on the tiers of access, and what you can afford to use.
- **Account** - After you decide to use an API you will need to be able to signup and obtain an account and credentials that will allow for access.
- **Authentication** - Now that you have keys, you will need to understand how you can use them as part of authentication for the APIs you need.
- **Clients** - There should always be client tooling that helps consumers get up and running without writing code, with as little friction as possible.
- **Software Development Kits (SDK)** - There should be SDKs available in a variety of programming languages allow consumers to seamlessly integrate.
- **Command Line Interface (CLI)** - Some developers will prefer using a CLI to integrate and automate using an API as part of their systems.
- **Integration** - Now we reach the point where we actually integrate with an API, something not all developers will successfully achieve as part of their own consumption life cycle.
- **Support** - Now that a consumer has integrated they will need to know where they can receive support as part of their application, and ongoing use of API resources.
- **Engagement** - There should be further opportunities for engagement beyond just the initial integration of an API, encouraging the deepening of the provider and consumer relationship.

This provides me with a simple slice of the API consumption side of things to focus on in my storytelling. Having simple, organized groups of API building blocks like this, wrapped in a variety of contexts helps me be more consistent in my writing and speaking. Using consistent wording combined with repetition is important, and thoughtfully defining the API life cycle from the provider, and well as consumer side, in ways that everyone can easily understand is very important to me.

## API Maintenance Life Cycle
We aren’t done with APIs once they are delivered and being consumed. There are regular maintenance tasks that should occur, and these are things that won’t necessarily be handed by the same team that delivers the APIs. Opening up a whole other dimension of the API life cycle that cannot be ignored, otherwise we run the risk of offering a less than quality experience for our consumers. Here are the maintenance portions of the API life cycle that I am considering, and documenting as part of this work.

- **Communication** - An API is up and running and communication between provider and consumer is critical to ensure everyone is operating and doing what they need to be doing.
- **Support** - Making sure all of the consumers are supported and getting the attention they need, providing the critical feedback loop between provider and consumer.
- **Issues** - Publishing a real time accounting of open issues that exist to help API consumers understand the current status of the system, while also helping minimize support requests for known issues.
- **Monitoring** - Understanding the overall health and status of all APIs, and making sure all monitors, tests, and the platform is meeting their SLA when it comes providing APIs.
- **Performance** - Going beyond the monitoring and testing, and making sure a certain quality of service bar is met, and we have a complete grasp of how our customers experience API access.
- **Security** - Reviewing security practices, and auditing authentication, usage, logging, scanning, and other dimensions of security across all APIs in operation.
- **Reporting** - Staying in tune with API consumption, errors, and general access and usability across all API consumers, making sure an awareness is developed in how digital resources are used.
- **Road Map** - Publishing an accounting of what the future will hold for API consumers, regularly thinking about what future plans, or lack of future plans will have on API consumers.
- **Evangelism** - What is being doing to get the word out about the value APIs deliver, establishing a strategy for how you evangelize internally, with partners, and the public and help achieve platform goals.

Abandoned APIs that do not have anyone in the drive seat are the most common type of API I come across. It is pretty easy to tell when an API provider has moved on, and just left the API up and running. In other cases, teams are just under resourced, and do not have the bandwidth available to invest in the API maintenance portion of the API life cycle. We all get excited about the design and delivery of a new API, but few of us like doing the mundane aspects of API management—this is why you should invest in a good API management solution, because nobody should be reinventing the wheel in this area.

## API Governance Life Cycle 
<img src="https://s3.amazonaws.com/kinlane-productions/algorotoscope-master/stories-supreme-court-judgement.jpg" width="45%" align="right" style="padding: 15px;" />
Lastly, and one of the most under-developed portions of the API life cycle, is the governance and oversight of things. This is the portion of the API life cycle where you go beyond the tactical day to day stuff and work to establish a strategy for how you deliver, consume, and maintain APIs. Getting formal about how we do what we do, and make sure all stakeholders, especially consumers have a good grasp on API policy, and how things get done. Here are some of the building blocks I consider at the API governance stops along the API life cycle.

- **Definition** - Which definitions are used? Where are the OpenAPI, schema, and other relevant patterns.
- **Design** - What design patterns are in play across the API definitions, and what is the meaning behind the design of all APIs.
- **Deployment** - What does deployment look like on-premise, in the cloud, and from region to region.
- **Management** - Quantify the standard approaches to managing APIs from on-boarding to analysis and reporting.
- **Plans** - How are access tiers and plans defined, providing 3rd party access to APIs, including that of aggregators and application developers.
- **Monitoring** - What does monitoring of web APIs look like, and how is data aggregated and shared.
- **Testing** - What does testing of web APIs look like, and how is data aggregated and shared.
- **Performance** - What does performance evaluation of web APIs look like, and how is data aggregated and shared.
- **Security** - What are the security practices in place for all APIs, and what is the current status of security.
- **Breaches** - When there is a breach, what is the protocol, and practices surrounding what should happen–where is the historical data as well.
- **Terms of Service** - What does terms of service across many APIs look like.
- **Privacy Policy** - How is privacy protected across API operations, and how is this impacting operations.
- **Support** - What are all the expected support channels, where are they located, and what the current metrics are.
- **Training** - A detailed training walk-through for anyone looking to understand governance.
- **Certification** - Providing certification for API publishers as well as API consumers when it comes to their platform participation.
- **Executive** - A robust walk-through of the concepts at play for an executive from the 100K view of things.

Your API delivery, consumption, and management house needs to be in order before you can begin realizing governance across everything. For many API providers it can be difficult to step back and look at things from the 100K level. However, increasingly it will become critical to make time to invest in API governance, otherwise you end up dealing with lower level fires that could have been addressed with a little more planning and coordination.

## Many API Life Cycle(s)
I’ve historically visualized the API lifecycle as a set of linear stops along a single life cycle, however over the years, as the world of APIs have come into better focus, I’m seeing the life cycle as a set of many different life cycles that work in concert for API provider as well as API consumers—cause, we all should really be both. I acknowledge that there are many different possible iterations upon the different types of API life cycles that will exist across companies, organizations, institutions, and government agencies. It will all depend on the expertise, services, tooling, and resources groups have when it comes to delivering, consuming, managing, and governing the APIs they depend on. However, I’m at least looking to define at least a handful of templates that can be used to guide API operators who are wanting to see the bigger picture.

Next, I will work on a visual to go with these API lifecycle templates. I’m going to be sticking with my transit map approach to defining the API landscape, and plot these different API life cycles as different lines within the same overall landscape map. Working to show how they overlap and interact. My biggest challenge in all of this is to be able to articulate that this lifecycle is applied across many different APIs, and potentially many different teams publishing APIs, as well as many different types of consumers putting them to work. Historically I have tried to auto-generate these API transit maps, but for this work I think I will just hand-craft the maps to reflect the API life cycles I have defined. Providing a more universal way in which to help articulate, visualize, explore and learn more about how the API life cycle(s) work.
