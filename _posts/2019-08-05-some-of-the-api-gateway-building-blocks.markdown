---
published: true
layout: post
title: 'Some Of The API Gateway Building Blocks'
date: 2019-08-05T09:00:00.000Z
tags:
  - API Evangelist
  - Gateway
  - Management
image: https://s3.amazonaws.com/kinlane-productions/algorotoscope-master/udnie-IMG_8312.jpg
---
<img src="{{ page.image }}" width="45%" align="right" style="padding: 15px;" />
The inspiration for this post wasn't fully mine, I’m borrowing and building upon what Sukanya Santhanam (@SukanyaSanthan1) <a href="https://twitter.com/SukanyaSanthan1/status/1151424256300859392">tweeted out the other day</a>. It is a good idea, and something that should be open sourced and moved forward. I’ve been studying with API management since 2010, and using gateways for over 15 years. I’ve watched gateways evolve, and partnered regularly with API management and gateway providers (Shout out to Tyk). Modern API gateways aren’t your grandfather’s SOA tooling, they’ve definitely gone through several iterations. While I still prefer hand rolling and forging my APIs out back in my woodshed on an anvil, I find myself working with a lot of different API gateways lately.

I’ve kept feeling like I needed to map out the layers of what I’d consider to be a modern API gateway, and begin providing links to the most relevant API gateways out there, and the most common building blocks for an API gateway. Now that you can find API gateways baked into the fabric of the cloud, it is time that we work to standardize the definition of what they can deliver. I’m not looking to change what already is. Actually, I’m looking to just document and build on what already is. As with every other stop along the API lifecycle I’m looking to just map out the common building blocks, and establish a blueprint going forward the might influence existing API gateway providers, as well as any newcomers.

After going through my <a href="http://gateway.apievangelist.com/">API gateway research</a> for a while, I quickly sketched out these common building blocks for helping deploy, manage, monitor, and secure your APIs:

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

I’m going to add these to my API gateway research. I’m sure there are other building blocks out there, but I think this is a good start. It reflects what I think makes API gateways different from API management. It has the design, deployment, and backend integration portion of the conversation, as well as the key API management features expected. I see API gateways as a Venn diagram of API lifecycle features. Providing a single blueprint, tooling, and appliance that will help you deliver, manage, distribute, and scale your API infrastructure.

<a href="https://github.com/api-evangelist/api-gateway-blueprint">You can find this outline published over at GitHub</a>. I will me managing it as a living document and opening up to feedback via GitHub issues. I’m going to evolve this as a core API gateway specification—eventually defining APIs and schema for each layer of the stack. This will take some time because I will have to profile several of the existing API gateway APIs and mine them for logical patterns. Borrowing from their API designs, and schema, layering them together to create a common set of building blocks. I’m going to also begin iterating upon what I’d call an observable regulatory set of API gateway building blocks to augment this existing list. Establishing my vision of not just an API gateway standard, which can be used internally, as well as openly as part of an industry-wide effort to deliver consistent APIs for a collective purpose.
