---
published: true
layout: post
title: 'An Observable Regulatory Provider Or Industry API Management Gateway'
date: 2019-08-15T09:00:00.000Z
tags:
  - API Evangelist
  - Gateway
  - Management
  - Observability
  - Regulation
image: https://s3.amazonaws.com/kinlane-productions/algorotoscope-master/35201856153_61bc075e4b-nazi-invasion.jpg
---
<img src="{{ page.image }}" width="45%" align="right" style="padding: 15px;" />
I wrote a separate piece on an API gateway specification standard recently, merging several areas of my research and riffing on a recent tweet from Sukanya Santhanam (@SukanyaSanthan1). I had all these building blocks laying around as part of my research on API gateways, but also from the other areas of the API lifecycle that I track on. Her tweet happened to coincide with other thoughts I had simmering, so I wanted to jump on the opportunity to publish some posts, and see if I could slow jam a conversation in this area. Now, after I defined what I’d consider to be a core API gateway set of building blocks, I wanted to take another crack at refining my vision for how we make it more observable and something that could be used as a tech sector regulatory framework.

Copying and pasting from my API gateway core specification, here is what my v1 draft vision for an API gateway might be:

- **Paths** - Allowing many different API paths to exist.
- **Schema** - Allowing me to manage all of my schema.
- **Integrations** - Providing backend lego architecture.
    - **Resource** - Allow for integration with other APIs.
    - **Database** - Provide a stack of database integrations.
    - **Other** - Define whole buffet of integration definitions.
- **Requests** - Define all of my HTTP 1.1 requests
    - **Methods** - Providing me with my HTTP verbs.
    - **Path Parameters** - Able to define path parameters.
    - **Query Parameters** - Able to define query parameters.
    - **Bodies** - Providing control over the request body.
    - **Headers** - Full management of HTTP request headers.
    - **Encoding** - Defining the media types in in use for requests.
    - **Validate** - Providing validation for all incoming requests.
    - **Mappings** - Allowing for mapping of requests to backend.
    - **Transformations** - Transformation before sending to backend..
    - **Examples** - Ensuring there are samples for each request.
    - **Schema** - Able to reference all schema used in requests.
    - **Tags** - Being able to organize API requests using tags.
- **Responses** - Define all of my HTTP 1.1 responses.
    - **Status Code**s - Providing the ability to define HTTP status codes.
    - **Headers** - Full management of all HTTP response headers.
    - **Encoding** - Defining the media types in in use for responses.
    - **Schema** - Able to reference all schema used in responses.
    - **Examples** - Ensuring there are samples for each response.
- **Stages** - Able to stage APIs under any platform defined environment.
- **Publishing** - Allowing for conscious publishing of APIs into production.
- **Versioning** - Providing semantic versioning as header or in the path.
- **Policies** - Defining policies for API, and schema access by consumers.
- **Licensing** - Ensure that data and APIs are properly licensed for consumption.
- **Plans** - Crafting a handful of standard access tiers for different consumers.
- **Rate Limiting** - Define the rate limits for all APIs within each plan offered.
- **Domains** - Allow for default and custom domains associated with APIs.
- **Certificates** - Provide management and usage of certificates for encryption.
- **Tags** - Allow APIs, as well as their individual paths, and requests to be tagged.
- **Dependencies** - Inform on the dependencies between APIs, including 3rd party.
- **Regions** - Allow for multi-region deployment of APIs, with full DNS support.
- **Contact** - Ensure there is contact information for every API owner.
- **Logging** - Standardize the logging for all API traffic to one or many locations.
- **Monitoring** - Provide basic monitoring of all APIs from alternate locations.
- **Status** - Offer a real time status dashboard and notification for all APIs.
- **Terms of Service** - Allow for the publishing of one or many TOS applying to APIs.
- **Authentication** - Provide a handful of standard authentication mechanisms.
- **Authorization** - Enable fine grade authorization across APIs and schema.
- **Consumers** - Allow for consumers to sign up and maintain access accounts.
- **Keys** - Require consumers define their applications and use API keys with API calls.
- **Documentation** - Automatically publish documentation for all APIs that are published.
- **Reporting** - Provide reporting on all gateway activity across each API and the lifecycle.
    - **Platform** - Deliver platform specific API consumption report.
    - **Consumer** - Provide consumer specific API consumption reports.

That is a pretty long list. I know there are other building blocks missing, but this represents my first pass through my API research. It reflects the building blocks I want available when I put an API gateway to work in any cloud, on-premise, or on-device use case. However, in this post I wanted to go beyond what I’d consider the core API gateway, and talk about how we make it more observable, and something that could be applied to regulate an industry. Not something that happens behind the scenes, but something that happens out in the open, bringing in some sunlight, and pulling back the curtain on the black boxes some companies enjoy operating. While this won’t solve all our problems, I think it will provide a pretty good first step towards bringing some much needed observability to the tech sector, using common solutions that already exist. Here are a handful of building blocks I think could contribute to this conversation.

- **Open Source** - Ensure that the gateway is open source, and something that is developed out in the open, and can be forked an operated by anyone.
- **Organizational** - Provide the suggested framework for the operating organization, and what staffing and other resources are required to operate an instance of this model, providing a (hopefully) neutral entity to bring to life.
- **Provider Directory** - Require that all providers who have APIs published as part of the platform be profiled and available within a single directory, breaking down the resources they have published, as well as usage, monitoring, and other relevant information.
- **Consumer Directory** - Require that all consumers who have access to the platform publish a profile, share how their are using APIs, and offer a summary of their authentication, authorization, usage levels, and data points.
- **Research Access** - Provide access to researchers as part of the consumer management, but offering wider access to platform data and consumption based upon agreed upon plans.
- **Media Access** - Allow for access my media organization who are looking to understand what is happening across a platform, and the impact on consumers via applications.
- **Industry Access** - Provide access to industry analysts as part of the consumer management, but offering wider access to platform data and consumption based upon agreed upon plans.
- **Auditor Access** - Provide complete auditor access to the entire platform, allowing certified auditors to come in and review resources, consumers, logs, and any other aspects of the gateway operations.
- **Schema Catalog** - A complete catalog of all the types of data that is tracked and made available across all APIs, and used in desktop, web, mobile, and device applications.
- **Monetization** - Allow for the monetization of provider participation, consumer, researcher, and industry access, allowing for well defined plans, rate limits, and observability into revenue that is generated.
- **Issues** - Provide the ability for the public, consumers, researchers, and industry to submit issues in a safe, moderated, and accessible space, ensuring there is observability into all issues across the gateway.
- **Disputes** -  Ensure there are trained professionals to help address disputes on the platform rising from issues reported by the public, consumers, researchers, and industry analysts using the gateway.
- **Reporting** - Provide reporting to key stakeholders.
    - **Private** - Provide comprehensive reporting accessible to trusted internal stakeholders.
    - **Public** - Publish a line of regular public reports on platform usage and consumption.
    - **Researcher** - Provide a set of reports just for researchers based upon plans and agreements.
    - **Media** - Provide a rich set of reports that help keep media understanding what is going on.
    - **Auditors** - Give auditors a full set of reports, including summary and detail access.

This model isn’t without precedent. Last year I spent a couple months studying the approach by UK regulators to bring more observability into the banking sector, and the formation of Open Banking organization (https://www.openbanking.org.uk/). Learning more about what open banking was in the UK (http://apievangelist.com/2018/02/21/what-is-open-banking-in-the-uk/),  how it provides a common API definition (http://apievangelist.com/2018/02/21/open-banking-in-the-uk-openapi-template/), who the common stakeholders were (http://apievangelist.com/2018/02/26/the-banking-api-actors-in-the-uk/), and exploring how I could emulate this approach as an open source API industry template (http://open.banking.blueprint.apievangelist.com/). In 2019, I want to go even further with this open source API Blueprint, understand how it can be used to define a common open source API gateway specification, while adding the necessary building blocks to ensure there is observability at the industry level.  

I am proposing that this model be defined, standardized, and applied at the single provider, or industry level. If required, an independent entity can be setup to operate the API gateway as an independent platform, funded by regulators, and the monetization layer that leverages a mix of providers, consumers, researchers, and industry analyst access to the platform. While there will be private layers of the platform, the goal is to provide as much as possible out in the open, operating as many public API platforms have been operating for the last 20 years. Ironically, some of the worst behaved technology platforms have operated using this model in the past, but sadly have been actively tightening down access levels. I’m proposing we take their formula, open source it, and operate it independently, out in the open, and make them pay for it.

As I said before, this will not solve all problems. However it will define a layer that ALL desktop, web, mobile, and device applications can be required to go through. Requiring that provides only develop applications on top of APIs deployed within regulated API gateways. Requiring that all internal, partner, and 3rd party public consumers access API via the single, or regionally distributed gateways. If auditors ever find that an API provider is leverage APIs not listed in the API gateway directory, or their partners and the public have access to data that is not defined in schema within the API gateway—then there is a problem, and enforcement can follow. Of course, all of this isn’t as simple as proposed in this post, but it provides the scaffolding and blueprint for how it can be applied. There is no reason this can’t be applied to regulate technology companies, and applied to existing industries that are already regulated, helping bring more observability into already existing regulatory practices.

Nothing I’m proposing here is rocket science, or theoretical. It is based upon proven practices of tech companies. All I’m saying now, is rather than just advising companies, organizations, institutions, and government follow these best practices, I’m saying that we should begin working to establish a standard, and craft policy that requires everyone to participate. I know many tech folks don’t like the idea of regulation, but for certain industries, and certain platforms, it might be a positive thing to inject some regulation into the equation, and begin doing things out in the open, rather than behind the curtain. If you have any questions or comments on this blueprint, feel free to email me at info@apievangelist.com, or submit an issue on the GitHub repository for this blueprint.
