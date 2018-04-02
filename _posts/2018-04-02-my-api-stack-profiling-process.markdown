---
published: true
layout: post
title: My API Stack Profiling Process
date: 2018-04-02T09:00:00.000Z
tags:
  - API Evangelist
  - Discovery
  - Definitions
image: >-
  https://s3.amazonaws.com/kinlane-productions/api-stack/logos/the-api-stack-entities-snapshot.png
---
<p><img src="{{ page.image }}" width="45%" align="right" style="padding: 15px;" /></p>I am escalating conversations I'm having with folks regarding how I profile and understand APIs as part of my [API Stack](http://theapistack.com) work. It is something I've been evolving for 2-3 years, as I struggle with different ways to attack and provide solutions within the area of API discovery. I want to understand what APIs exist out there as part of my industry research, but along the way I want to also help others find the APIs they are looking for, while also helping API providers get their APIs found in the first place. All of this has lead me to establish a pretty robust process for profiling API providers, and document what they are doing.

As I shift my [API Stack](http://theapistack.com) work into 2nd gear, I need to further formalize this process, articulate to partners, and execute at scale. Here is my current snapshot of what is happening whenever I'm profiling an API and adding it to my API Stack organization, and hopefully moving it forward along this API discovery pipeline in a meaningful way. It is something I'm continuing to set into motion all by myself, but I am also looking to bring in other API service providers, API providers, and API consumers to help me realize this massive vision.

**Github as a Base**<br />
Every new "entity" I am profiling starts with a Github repository and a README, within [a single API Stack organization for providers](https://github.com/api-stack-providers). Right now this is all automated, as I'm transition to this way of doing things at scale. Once in motion, each provider I'm profiling will become pretty manual. What I consider an "entity" is fluid. Most smaller API providers have a single repository, while other larger ones are broken down by line of business, to help reduce API definitions and conversation around APIs down to the smallest possible unit we can. Every API service provider I'm profiling gets its own Github repository, subdomain, set of definitions, and conversation around what is happening. Here are the base elements of what is contained within each Github repo.

- **OpenAPI** - A JSON or YAML definition for the surface are of an API, including the request, responses, and underlying schema using as part of both.
- **Postman Collection** - A JSON Postman Collection that has been exported from the Postman client after importing the complete OpenAPI definition, and full tested.
- **APIs.json** - A YAML definition of the surface area of an API's operation, including home page, documentation, code samples, sign up and login, terms of service, OpenAPI, Postman Collection, and other relevant details that will matter to API consumers.

The objective is to establish a single repository that can be continuously updated, and integrated into other API discovery pipelines. The goal is to establish a complete (enough) index of the APIs using OpenAPI, make it available in a more runtime fashion using Postman, and then indexing the entire API operations, including the two machine readable definitions of the API(s) using APIs.json. Providing a single URL in which you can ingest and use to integrate with an API, and make sense of API resources at scale.

**Everything Is OpenAPI Driven**<br />
My definition still involves OpenAPI 2.0, but it is something I'm looking to shift towards 3.0 immediately. Each entity will contain one or many OpenAPI definitions location in the underscore openapi folder. I'm still thinking about the naming and versioning convention I'm using, but I'm hoping to work this out over time. Each OpenAPI should contain complete details for the following areas:

- **info** - Provide as much information about the API.
- **host** - Provide a host, or variables describing host.
- **basePath** - Document the basePath for the API.
- **schemes** - Provide any schemes that the API uses.
- **produces** - Document which media types the API uses.
- **paths** - Detail the paths including methods, parameters, enums, responses, and tags.
- **definitions** - Provide schema definitions used in all requests and responses.

While it is tough to define what is complete when crafting an OpenAPI definition, every path should be represented, with as much detail about the surface area of requests and responses. It is the detail that really matters, ensuring all parameters and enums are present, and paths are properly tagged based upon the resources being made available. The more OpenAPI definitions you create, the more you get a feel for what is a "complete" OpenAPI definition. Something that becomes real once you create a Postman Collection for the API definition, and begin to actually try and use an API.

**Validating With A Postman Collection**<br />
Once you have a complete OpenAPI definition defined, the next step is to validate your work in Postman. You simply import the OpenAPI into the client, and get to work validating that each API path actually works. You make sure you have an API key, and any other authentication requirements, and work your way through each path, validating that the OpenAPI is indeed complete. If I'm missing sample responses, the Postman portion of this API discovery journey is where I get them. Grabbing validated responses, anonymizing them, and pasting them back into the OpenAPI definition. Once I've worked my way through every API path, and verified it works, I then export a final Postman Collection for the API I'm profiling.

**Indexing API Operations With APIs.json**<br />
I upload my OpenAPI, and Postman Collection to the Github repository for the API entity I am targeting. Then I get to work on an APIs.json for the API. This portion of the process is about documenting the OpenAPI and Postman I just created, but then also doing the hard work of identifying everything else an API provider offers to support their operations, and will be needed to get up and running with API integration. Here are a handful of the essential building blocks I'm documenting:

- **Website** - The primary website for an entity owning the API.
- **Portal** - The URL to the developer portal for an API.
- **Documentation** - The direct link to the API documentation.
- **OpenAPI** - The link to the OpenAPI I created on Github.
- **Postman** - The link to the Postman Collection I created on Github.
- **Sign Up** - Where do you sign up for an API.
- **Pricing** - A link to the plans, tiers, and pricing for an API.
- **Terms of Service** - A URL to the terms of service for an API.
- **Twitter** - The Twitter account for the API provider -- ideally, API specific.
- **Github** - The Github account or organization for the API provider.

This list represents the essential things I'm looking for. I have almost 200 other building blocks I document as part of API operations ranging from SDKs to training videos. The presence of these building blocks tell me a lot about the motivations behind an API platform, and send off a wealth of signals that can be tuned into by humans, or programmatically to understand the viability and health of an API.

**Continuously Integratable API Definition**<br />
Now we should have the entire surface area of an API, and it's operations defined in a machine readable format. The APIs.json, OpenAPI, and Postman can be used to on-board new developers, and used by API service providers looking to provides valuable services to the space. Ideally, each API provider is involved in this process, and once I have a repository setup, I will be reaching out to each provider as part of the API profiling process. Even when API providers are involved, it doesn't always mean you get a better quality API definition. In my experience API providers often don't care about the detail as much as some consumers and API service providers will. In the end, I think this is all going to be a community effort, relying on many actors to be involved along the way.

**Self-Contained Conversations About Each API**<br />
With each entity being profiled living in its own Github repository, it opens up the opportunity to keep API conversation localized to the repository. I'm working to establish any work in progress, and conversations around each APIs definitions within the Github issues for the repository. There will be ad-hoc conversations and issues submitted, but I'll be also adding path specific threads that are meant to be an ongoing thread dedicated to profiling each path. I'll be incorporating these threads into tooling and other services I'm working with, encouraging a centralized, but potentially also distributed conversation around each unique API path, and its evolution. Keeping everything discoverable as part of an API's definition, and publicly available so anyone can join in.

**Making Profiling A Community Effort**<br />
I will repeat this process over and over for each entity I'm profiling. Each entity lives in its own Github repository, with the definition and conversation localized. Ideally API providers are joining in, as well as API service providers, and motivated API consumers. I have a lot of energy to be profiling APIs, and can cover some serious ground when I'm in the right mode, but ultimately there is more work here than any single person could ever accomplish. I'm looking to standardize the process, and distribute the crowdsourcing of this across many different Github repositories, and involve many different API service providers I'm working with to ensure the most meaningful APIs are being profiled, and maintained. Highlighting another important aspect of all of this, and the challenges to keep API definitions evolving, soliciting many contributions, while keeping them certified, rated, and available for production usage.

**Ranking APIs Using Their Definitions**<br />
Next, I'm ranking APIs based upon a number of criteria. [It is a ranking system I've slowly developed over the last five years](http://apievangelist.com/2015/10/31/how-are-we-going-to-create-the-standard-and-poors-and-moodys-for-the-api-economy/), and is something I'm looking to continue to refine as part of this API Stack profiling work. Using the API definitions, I'm looking to rate each API based upon a number of elements that exist within three main buckets:

- **API Provider** - Elements within the control of the API provider like the design of their API, sharing a road map, providing a status dashboard, being active on Twitter and Github, and other signals you see from healthy API providers.
- **API Community** - Elements within the control of the API community, and not always controlled by the API provider themselves. Things like forum activity, Twitter responses, retweets, and sentiment, and number of stars, forks, and overall Github activity.
- **API Analyst** - The last area is getting the involvement of API analysts, and pundits, and having them provide feedback on APIs, and get involved in the process. Tracking on which APIs are being talked about by analysts, and storytellers in the space.

Most of this ranking I can automate through there being a complete APIs.json and OpenAPI definition, and machine readable sources of information present in those indexes. Signals I can tap into using blog RSS, Twitter API, Github API, Stack Exchange API, and others. However some it will be manual, as well as require the involvement of API service providers. Helping me add to my own ranking information, but also bringing their own ranking systems, and algorithms to the table. In the end, I'm hoping the activity around each APIs Github repository, also becomes its own signal, and consumers in the community can tune into, weight, or exclude based upon the signals that matter most to them.

**Streamdata.io Stream Rank**<br />
Adding to my ranking system, I am applying my partner [Streamdata.io's ranking system for APIs](https://streamdata.io/blog/benchmark-quantifying-api-performance/), looking to determine that activity surrounding an API, and how much opportunity exists to turn an API event a real time stream, as well as identify the meaningful events that are occurring. Using the OpenAPI definitions generated for each API being profiled, I begin profiling for Stream Rank by defining the following:

- **Download Size** - What is the API response download size when I poll an API?
- **Download Time** - What is the API response download time when I poll an API?
- **Did It Change** - Did the response change from the previous response when I poll an API?

I poll an API for at least 24-48 hours, and up to a week or two if possible. I'm looking to understand how large API responses are, and how often they change--taking notice of daily or weekly trends in activity along the way. The result is a set of scores that help me identify:

- **Bandwidth Savings** - How much bandwidth can be saved?
- **Processor Savings** - How much processor time can be saved?
- **Real Time Savings** - How real time an API resource is, which amplifies the savings?

All of which go into what we are calling a Stream Rank, which ultimately helps us understand the real time opportunity around an API. When you have data on how often an API changes, and then you combine this with the OpenAPI definition, you have a pretty good map for how valuable a set of resources is based upon the ranking of the overall API provider, but also the value that lies within each endpoints definition. Providing me with another pretty compelling dimension to the overall ranking for each of the APIs I'm profiling.

**APIMetrics CASC Score**<br />
Next I'm partnering with [APIMetrics to bring in their CASC Scoring](https://apimetrics.io/2017/04/21/casc-score/) when it makes sense. They have been monitoring many of the top API providers, and applying their CASC score to the overall API availability. I'd like to pay them to do this for ALL APIs in my API Stack work. I'd like to have every public API actively monitored from many different regions, and posses active, as well as historical data that can be used to help rank each API provider. Like the other work here, this type of monitoring isn't easy, or cheap, so it will take some prioritization, and investment to properly bring in APIMetrics, as well as other API service providers to help me rank things.

**Event-Driven Opportunity With AsyncAPI**<br />
Something I've only just begun doing, but I wanted to include on this list, is adding a fourth definition to the stack when it makes sense. If any of these APIs possess a real time, event-driven, or message oriented API, I want to make sure it is profiled using [the AsyncAPI specification](https://www.asyncapi.com/). The specification is just getting going, but I'm eager to help push forward the conversation as part of my API Stack work. The format is a great sister specification for OpenAPI, and something I feel is relevant for any API that I profile with a high enough Stream Rank. Once an API possesses a certain level of activity, and has a certain level of richness regarding parameters and the request surface area, the makings for an event-driven API are there--the provider just hasn't realized it. The map for the event-driven exists within the OpenAPI parameter enums, and tagging for each API path, all you need is the required webhooks or streaming layer to realize an existing APIs event-driven potential--this is where [Streamdata.io](http://streamdata.io) comes in. ;-)

**One Stack, Many Discovery Opportunities**<br />
I am doing this work under my [API Stack](http://theapistack.com) research. However it is all being funded by [Streamdata.io](http://streamdata.io). It is also being stimulated by my work with Postman, the OpenAPI Initiative, APIs.io, APIs.json, API Deck, APIs.guru, and beyond. The goal is to turn API Stack into a workbench, where anyone can contribute, as well as fork and integrate API definitions into their existing pipelines. All of this will take years, and a considerable amount of investment, but it is something I've already invested several years into. I'm also seeing the API discovery conversation reaching a critical mass thanks to the growth in the number of APIs, as well as adoption of OpenAPI and Postman. Making API discovery a more urgent problem. The challenge will be that most people want to extract value from these kind of effort, and not give back. While I feel strongly that API definitions should be open and freely accessible, the nature of the industry doesn't alway reflect my vision, so I'll have to get creative about how I incentivize folks, and reward or punish certain behaviors along the way.
