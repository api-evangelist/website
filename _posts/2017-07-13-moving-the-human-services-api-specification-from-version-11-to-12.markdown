---
published: true
layout: post
title: Moving The Human Services API Specification From Version 1.1 to 1.2
date: 2017-07-13T09:00:00.000Z
tags:
  - API Evangelist
  - Definitions
  - HSDA
  - Design
image: >-
  https://s3.amazonaws.com/kinlane-productions/open-referral/hsda-organizations-documentation.png
---
<p><a href="http://developer.open.referral.adopta.agency/documentation/"><img src="https://s3.amazonaws.com/kinlane-productions/open-referral/hsda-organizations-documentation.png" align="right" width="40%" style="padding: 15px;" /></a></p>I am preparing for the recurring governance meeting for the Open Referral Human Services Data API standard--which I'm the technical lead for. I need to load up every detail of my Human Services Data API work into my brain, and writing stories is how I do this. I need to understand where the definition is with v1.1, and encourage discussion around a variety of topics when it comes to version 1.2.

### Constraints From Version 1.0 To v1.1
I wasn't able to move as fast as I'd like from 1.0 to 1.1, resulting in me leaving out a number of features. The primary motivation to make sure as much of the version 1.1 of Human Services Data Specification (HSDS) was covered as possible--something I ended up doing horizontally with new API paths, over loading up the core paths of /organizations, /locations, and /services. There were too many discussion on the table regarding the scope and filtering of data, and schema for these core paths. Something which led to a discussion, about /search--resulting in me pushing off API design discussions on how to expand vertically at the core API path level to future versions.  

There were just too many decisions to make at the API request and response level for me to make a decision in all the areas--warranting more discussion. Additionally, there were other API design discussion regarding operational, validation, and more utility APIs to discuss for inclusion in future versions expanding the scope and filtering discussions to the API path, and now API project level. In preparation for our regular governance meeting I wanted to run through all of the open API design issues, as well as additional projects the community needs to be thinking about.

## API Design
As part of my Human Services Data API (HSDA) work we have opened up a pretty wide API design conversation regarding where the API definition could (should) be going. I've tried to capture the conversations going on across the Slack, and Google Group using GitHub issues for the HSDA GitHub repository. I will be focusing in on 16 of these issues for the current community discussions.

### [Versioning](https://github.com/openreferral/api-specification/issues/8)
We are moving forward the version of the API specification from 1.0 to 1.1. This version describes the API definition, to help quantify the compliance of any single API implementation. This is not guidance regarding how API providers should version their API--each implementation can articulate their compliance using an OpenAPI definition, or just in operation by being compliant. I purposely dodged providing versioning guidance of specific API implementations--until I could open up discussion around this subject.

If you need a primer on API versioning I recommend [Troy Hunt's piece](https://www.troyhunt.com/your-api-versioning-is-wrong-which-is/) which helps highlight:

- URL: We put the API version into the URL: https://example.com/api/v1.1/organizations/
- Custom request header: Using a header such as “api-version: 1.1”
- Accept header: Using the accept header to specify the version “Accept: application/vnd.hsda.v1.1+json - which relates to content negotiation discussions.
- No Versioning - We do not offer any versioning guidance and let each API implementation decide for themselves with no version being a perfectly acceptable answer.

API versioning discussions are always hot topics, and there is no perfect answer. If we are to offer API versioning guidance for HSDA compliant API providers I recommend putting it in the URL, not because it is the right answer, but it is the right answer for this community. It is easy to implement, and easy to understand. Although I'm not 100% convinced we should be offering guidance at all.

I would like to open it up to the community, and get more feedback from vendors, and implementors. I'm curious what folks prefer when they are building applications. This decision was one that was wrapped up with potential content negotiation, hypermedia, and schema scope discussions to make without more discussion.

### [Paths](https://github.com/openreferral/api-specification/issues/27)
The API definition provides some basic guidance for HSDA implementations when it comes to naming API paths, providing a core set or resources, as well as sub-resources. There are a number of other API designs waiting in the wings to be hammered out, making more discussion around this relevant. How do we name additional API paths? Do we keep evolving a single stack of resources (expanding horizontally), or do we start grouping them and evolve using more sub-resources (expanding vertically)?

Right now, we are just sticking with a core set of paths for /contacts, /locations, /organizations, and /services, with /search somewhat of an outlier, or I guess wrapper. We have moved forward with sub-resource guidance, but should standard API design guidance when it comes to crafting new paths, as well as sub-paths, including the actions discussion below. This will be an ongoing discussion when it comes to API design across future versions, making it an evergreen thread that will just keep growing as the HSDA definition matures.

### [Verbs](https://github.com/openreferral/api-specification/issues/26)
HTTP verbs usage was another aspect of the evolution of the HSDA specification from v1.0 to v1.1--the new specification uses its verbs. Making sure POST, PUT, and DELETE were used across all core resources, as well as sub-resources, making the entire schema open for reading and writing at all levels. This further expanded the surface of the API definition, making it manageable at all levels.

Beyond this expansion we need to open up the discussion regarding OPTIONS, and PATCH. Is there a need to provide partial updates using PATCH, and providing guidance on using OPTION for providing requirements associated with a resource, and the capabilities of the server behind the API. Also we should be having honest conversations about which verbs are available for sub-resources, especially when it comes to taking specific actions using HSDA paths. There is a lot more to discuss when it comes to HTTP verb usage across the HSDA specification.

### [Actions](https://github.com/openreferral/api-specification/issues/24)
I want to prepare for the future when we have more actions to be taken, and talk about how we approach API design in the service of taking action against resources. Right now HTTP verbs are taking care of the CRUD features for all resources and sub-resources. While I don't have any current actions in the queue to discus, we may want to consider this as part of the schema scope and filtering discussion--allowing API consumers to request partial, and complete representations of API resources using action paths. For example: /organization/simple, or /organizations/complete.

As the HSDA specification matures this question will come up more and more, as vendors, and implementations require more specialized actions to be taken against resources. Ideally, we are keeping resources very resource oriented, but from experience I know this isn't always the case. Sometimes it becomes more intuitive for API developers to take action with simple, descriptive API paths, than adding more complexity with parameters, headers, and other aspects of the APIs design. I will leave this conversation open to help guide future versions, as well as the schema scope and filtering discussions.

### [Parameters](https://github.com/openreferral/api-specification/issues/24)
Currently the numbers parameters in use for any single endpoint is pretty minimal. The core resources allow for querying, and sorting, but as of version 1.1, parameters are still pretty well-defined and minimal. The only path that has an extensive set of parameters is /search, which possesses category, email, keyword, language, lat_lng, location, org_name, page, per_page, radius, service_area, and status. I'd like to to continue the discussion about which parameters should be added to other paths, as well as used to help filter the schema, and other aspects of the API design conversation.

I'd like to open up the parameter discussion across all HSDA paths, but I'd also like to establish a way to regularly quantify how many paths are available, as well as how loaded they are with default values, and enumerators. I'd like to feed this into overall API design guidance, helping keep API paths reflecting a microservices approach to delivering APIs. Helping ensure HSDA services do one thing, and do it well, with the right amount of control over the surface area of the request and response of each API path.

### [Headers](https://github.com/openreferral/api-specification/issues/5)
Augmenting the parameter discussion I want to make sure headers are an equal part of the discussion. They have the potential to play a role across several of these API design questions from versioning to schema filtering. They also will continue to emerge in authentication, management, security, and even sorting and content negotiation discussions.

It is common for there to be a lack of literacy in developer circles when it comes to HTTP headers. A significant portion of the discussion around header usage should always be whether of not we want to invest in HTTP literacy amongst implementors, and their developer communities, over leveraging other non-header approaches to API design. HTTP Headers are an important building block of the web that developers should understand, but educating developers around their use can be time intensive and costly when it comes to guidance.

### [Body](https://github.com/openreferral/api-specification/issues/25)
There is an open discussion around how the body will be used across HSDA compliant implementations. Currently the body is default for POST and PUT, aka add and update. This body usage has been extended across all core resources, as well as sub-resource, requiring the complete, or sub resource representation to be part of each POST or PUT request.

There is no plan for any other APIs that will deviate from this approach, but we should keep this thread open to make sure we think about when the usage of the body is appropriate and when it might not be. We need to make sure that developers are able to effectively use the body, alongside headers, as well as parameters to get the desired results they are looking for.

### [Data Scope / Filtering](https://github.com/openreferral/api-specification/issues/22)
Currently the only filtering beyond pagination that is available is the query parameter available on /contact, /organizations, /locations, and /services resources. After that search is where the heaviest data scope and filtering can be filtered and defined. We need to discuss the future of this. Should the core resources have similar capabilities to /search, or should /search be a first class citizen with the majority of the filtering capabilities?

There needs to be more discussion around how data will be available bia default, and how it will be filtered as part of each API request. Will search be carrying most of the load, or will each core resource be given some control when it comes to filtering data. Whatever the approach it needs to be standardized across all existing paths, as well as applied to new API designs, keeping data filtering consistent across all HSDA designs. As this comes into focus I will be making sure there is a guide that provides guidance when it comes to data filtering practices in play.

### [Schema Scope / Filtering](https://github.com/openreferral/api-specification/issues/21)
This is one of the top issues being discussed as part of the migration from v1.1 to v1.2, regarding how to not just filter data that is returned as part of API responses, but how do you filter what schema gets returned as part of the response. When it came to v1.0 to v1.1 I didn't want to shift the response structure so that I can reduce any breaking changes for existing Ohana implementations, and open up with the community regarding the best approach for allowing schema filtering.

My current recommendation when it comes to the filtering of how much or how little of the schema to return with each request is to allow for schema templates to be defined and named, then enable API consumers to specify which template they'd like returned. This should be specified through either through a [prefer header](https://apievangelist.com/2017/05/24/considering-http-prefer-header-instead-of-field-filtering-for-my-api/), as part of the path structure as an action, or possibly through a parameter--all would accept the name of a schema template they desire (ie. simple, complete, etc.).

This approach to enabling schema templating could be applied at the GET, and could be also applied to POST or PUT requests. I personally recommend using a [prefer header](https://apievangelist.com/2017/05/24/considering-http-prefer-header-instead-of-field-filtering-for-my-api/), but I also emphasize the ease of use, and ease of defining the usage as part of documentation, and the OpenAPI definition--which it might make sense to allow for schema enablement as pat of the path name as an action. I'll leave it to the community to ultimately decide, as with the rest of this API design and project list, I'm just looking to provide guidance, and direction, built on the feedback of the community.

### [Path Scope / Filtering](https://github.com/openreferral/api-specification/issues/38)
Next up in the scope and filtering discussion is regarding how we define, group, and present all available API paths included in the HSDA specification. With the current specification I see three distinct groups of API paths emerging: 1) core resources (/contacts, /organizations, /locations, /services), and 2) sub resources (/physical-address, /postal-address, /phones, and more), then the more utility aspects of meta data, taxonomy, and eventually webhooks.

When a new user lands on the API documentation, they should see the core resources, and not be burdened with the cognitive load associated sub resources or the more utility aspects of HSDA consumption. However, once ready more advanced API paths are available. The grouping and filtering of the API paths can be defined as part of the OpenAPI definitions for the API(s), as well as the APIs.json index for the site. This path grouping will allow for API consumers to limit scope and filter which API paths are available in the documentation, and possibly with SDKs, testing, and other aspects of integration.

There are additional API projects on the table that might warrant the addition of new API groups, beyond core resources, sub resources, and utility paths. The approval, feedback, and messaging discussions might require their own group, allowing them to be separated in documentation, code, testing, and other areas--reducing the load for new users, while expanding the opportunities for more advanced consumers. Eventually there might be a one to one connection between API path groups, and the API projects in the queue, allowing for different groups of APIs to be moved forward at different rates, and involve different groups of API consumers and vendors in the process.

### [Project Scope / Filtering](https://github.com/openreferral/api-specification/issues/40)
Adding the fourth dimension to this scope / filtering discussion, I'm proposing we discuss how projects are defined and isolated, which can allow them to move forward at different rates, and be reflected in documentation, code, and other resources--allowing for filtering by consumers. This will drive the path filtering described above, but apply beyond just the API, and influencing documentation, SDKs, testing, monitoring, validation, and other aspects of API operations.

With this tier I am looking to decouple API projects from one another, and from the core specification. I want the core HSDS/A specification to stay focused on doing one thing well, but I'd like to establish a clear way to move forward complimentary groups of API definitions, and supporting tooling independently of the core specification. As we prepare to begin the journey from version 1.1 to 1.2, there are a number of significant projects on the table, and we need a way to isolate and decouple each additional API project in the same we we do with individual API resources--keeping them clearly defined, focused on specific problem set, and a buffet of resources that the community can choose where they'd like to participate.

### [Pagination](https://github.com/openreferral/api-specification/issues/10)
This is the discussion around how results will be paginated, allowing for efficient or complete requests to be requested, and navigate through large volumes of human services data. We need to be discussing how we will evolve the current approach to using page= and per_page= to articulate pagination. This approach is a common, well understood way to allow developers to paginate, but we need to keep discussion open as we answer some of the other API design questions on the table.

The pagination topic overlaps with the hypermedia and response structure discussion. Eventually we may offer pagination as part of a response envelope, or relational links provided as part of the response when using JSON API, HAL, or other media type. Right now we will leave pagination as it is, but we should be thinking about how it will evolve alongside all other API design conversations in this list.

### [Sorting](https://github.com/openreferral/api-specification/issues/12)
According to the current Ohana API implementation, which is the HSDA v1.0 definition, the guidance for sorting availability is as follows:

> Except for location-based and keyword-based searches, results are sorted by location id in ascending order. Location-based searches (those that use the lat_lng or location parameter) are sorted by distance, with the ones closest to the search query appearing first. keyword searches are sorted by relevance since they perform a full-text search in various fields across various tables.

This guidance follows the API definition from version 1.0 to 1.2, but for future versions we should be considering providing further guidance regarding sorting of results. I'd like to get more feedback from the community on how they are providing data sorting capabilities for API consumes, or even as part of web and mobile applications.

### [Response Structure](https://github.com/openreferral/api-specification/issues/6)
Right now the API responses for HSDA are pretty flat, like the schema. As part of the move from version 1.1 to 1.2 we need to be expanding on them, allowing for sub-resources to be included. This conversation will be heavily influenced by the schema filtering conversation above, as well as potentially the hypermedia and content negotiation discussions below. If we are gong to expand on the the schema being returned with API response we should be discussing all possible changes to the schema at once.

This conversation is meant to bring together the API schema filtering, hypermedia, and content negotiation conversations into a single discussion regarding the overall structure of a response, by default, as well as through filtering at the path, parameter, or header levels. I'd like to see  HSDA responses expand to accommodate sub resources, but also the relationships between resources, as well as assisting with pagination, sorting, and other aspects of data, schema, and path filtering. I am looking to make sure the expansion of the response structure be more inclusive beyond just talk of sub resource access.

### [Hypermedia](https://github.com/openreferral/api-specification/issues/7)
I really want to see a hypermedia fork in the HSDA definition, allowing more advanced users to negotiate and hypermedia version of the specification, instead of the more simpler, or even advanced default versions of the API. I recommend the adoption of HAL, Siren, or JSON API, as an alternate edition of an HSDA implementation. This expansion of the design of the HSDA specification would not impact the current version, but would allow for another dimension of API consumption and integration.

The relationships between human services data, and the semantic nature of the data really begs for a hypermedia solution. It would allow more meaningful API responses, and defining of relationships between resources, and emphasis of the taxonomy. I will be encouraging a separate, but complimentary version of HSDA that uses one of the leading hypermedia media types. I'd like to ensure there is community awareness of the potential of this approach, and support for investing in this as part of the HSDA design strategy.

### [Status Codes](https://github.com/openreferral/api-specification/issues/3)
One of the areas of design around version 1.1 of the HSDA specification that was put off until future versions is guidance when it comes to API response status and error codes. Right now the OpenAPI definition for version 1.1 of the HSDA specification only suggests a 200 successful response, returning a reference to the appropriate HSDS schema. A project needs to be started that would provider further guidance for 300, 400, and 500 series status codes, as well as error responses.

Each HSDA path should provide guidance on all relevant HTTP Status Codes, but should also provide guidance regarding the error object schema returned as part of every possible API response. Helping standardize how errors are communicated, and provide further guidance on how to help API consumers navigate a solution. Currently there is no guidance when it comes to HTTP responses and errors, something that should be considered in version 1.2 or 1.3, depending on available resources.

### [Content Negotiation](https://github.com/openreferral/api-specification/issues/39)
Augmenting other conversations around schema filtering, API response structure, and hypermedia, I want to make sure content negotiation stays part of the conversation. This aspect of API design will significantly impact API integration, and the evolution of the API specification. I want to make sure vendors, and other key actors are aware of it as an option, and can participate in the conversation regarding the different content types.

This conversation should begin with making CSV and HTML representations of the data available as part of the API response structure alongside the current JSON representations. API consumers should have the option to get raw HTML, CSV, and JSON through content negotiation--with JSON remaining as the default. Then the conversation should evolve to consider HSDA specific content type designation, as well as implementation of a leading hypermedia media type like JSON API, HAL, or Siren.

Content negotiation plays an important role in versioning the HSDA specification, as well as providing different dimensions for dealing with more complex integrations, as well as other aspects of operations like pagination, sorting, access to sub resources, other actions and even data, schema, and path filtering. Like headers, the mainstream developer community tends to not all be aware of content negotiation, but the benefits of adopting far outweigh the overhead involved with bringing developers up to speed.

That concludes the list of API design conversations that are occurring as part of the move from version 1.0 to 1.1, and will set the stage for the move towards 1.2, and beyond. It is a lot to consider, but it is a manageable amount for the community to think about as part of the version 1.1 feedback cycle. Allowing us to make a community informed decision regarding what should be focused on with each release--delivering what matters to the community.

## API Projects
As the version 1.0 to 1.1 migration occurred several projects were identified, or suggested for consideration. I want to make sure all these projects are on the table as part of the evolution of HSDA, beyond just the current API design discussion occurring. These are the projects we added to the specification that are moving forward but will have varying degrees of impact on the core API definition.

### [Taxonomy](https://github.com/openreferral/api-specification/issues/19)
There are two objects included in version 1.1 of the Human Services Data Specification (HSDS) that deal with taxonomy, the service_taxonomy object, and the core taxonomy object. I purposely left these aspects of the schema out of version 1.1 of HSDA. I wanted to see more discussion regarding taxonomy before we included in the specification. This is one of the first areas that influenced the above discussions regarding path scope and filtering, as well as project scope and filtering.

I'd like to see taxonomy exist as a separate set of paths, as a separate project, and out of the core specification. In addition to further discussion about what is HSDA taxonomy, I'd like to see  more consideration regarding what exactly is acceptable levels of HSDA compliant taxonomy. Ideally, the definition allows for multiple taxonomy, and possibly even a direct relationship between the available content types and a taxonomy, allowing for a more meaningful API response.

I will leave open a Github issue to discuss taxonomy, and either move forward as entirely separate schema, or inclusion in version 1.2, 1.3 of the core HSDA definition. One aspect of this delay is to ensure that my awareness of available taxonomies is up to snuff to help provide guidance. I'm just not aware of everything out there, as well as an intimacy the leading taxonomies in use--I need to hear more from vendors and implementors on this subject before I feel confident in making any decision.

### [Metadata](https://github.com/openreferral/api-specification/issues/28)
The metadata, and the meta_table_description objects v1.1 of HSDA were two elements I also left out of version 1.1 of HSDA. I felt like there should be more discussion around API management, logging, and other aspects of API operations that feed into this area, before we settled in on an API design to satisfy the HSDA metadata conversation. I'd like to hear more from human services implementors regarding what metadata they desire before we connect the existing schema to the API.

The metadata conversation overlaps with the approval and feedback project. There are aspects of logging and meta data collection and storage that will contribute to the transactional nature of any approval and feedback solution. There is also conversation going on regarding privacy concerns around API access to HSDS data, and logging, auditing that occurs at the metadata level. This thread covers these conversations, and is looking to establish a separate group of API paths, and separate project to drive documentation, and other aspects of API operations.

### [Approval & Feedback](https://github.com/openreferral/api-specification/issues/34)
One of the projects that came up recently was about working to define the layer that allows developers to add, update, and delete data via the API. Eventually through the HSDA specification we to encourage 3rd party developers, and external stakeholders to help curate and maintain critical human services data within a community, through trusted partners.

HSDA allows for the reading and writing of organizations, locations, and services for any given area. I am looking to provide guidance on how API implementors can allow for POST, PUT, PATCH, and DELETE on their API, but require approval before any changing transaction is actually executed. Requiring the approval of an internal system administrator to ultimately give the thumbs up or thumbs down regarding whether or not the change will actually occur.

A process which immediately begs for the ability to have multiple administrators or even possibly involving external actors. How can we allow organizations to have a vote in approving changes to their data? How can multiple data stewards be notified of a change, and given the ability to approve or disprove, logging every step along the way? Allowing any change to be approved, reviewed, audited, and even rolled back. Making public data management a community affair, with observability and transparency built in by default.

I am doing research into different approaches to tackling this, ranging from community approaches like Wikipedia, to publish and subscribe, and other events or webhook models. I am looking for technological solutions to opening up approval to the API request and response structure, with accompanying API and webhook surface area for managing all aspects of the approval of any API changes. If you know of any interesting solutions to this problem I’d love to hear more, so that I can include in my research, future storytelling, and ultimately the specification for the Open Referral Human Services Data Specification and API.

### [Universal Unique IDs](https://github.com/openreferral/api-specification/issues/35)
How will we allow for a universal unique ID system for all organizations, locations, and services, providing some provenance on the origin of the record. There is a solid conversation started about how to approach a universal ID system to live alongside, or directly as part of the core HSDA specification--depending on how we decide to approach project scope. Ideally, a universal ID system isn't pat of being compliant, but could add a healthy layer of certification for some leading providers.

More research needs to be done regarding how universal IDs are handled in other industries. An exhaustive search needs to be conducted regarding any existing standards and guidance that can help direct this discussion. This approach to handling identifiers will have a significant impact on individual API implementations, as well as the overall HSDA definition. More importantly, it will set the stage for future HSDA aggregation and federation, allowing HSDA implementations to work together more seamlessly, and better serve end-uses.

### [Messaging](https://github.com/openreferral/api-specification/issues/37)
I separated this project out of the approval and feedback project. I am suggesting that we isolate the messaging guidance for APIs, setting a standard for how you communicate within a single implementation as well across implementations. There are a number of messaging API standards and best practices available out there, as well as existing messaging APIs that are already in use by human services practitioners, including social channels like Facebook and Twitter, but also private channels like Slack.

HSDA compliant messaging channels should live as a separate project, and set of API path specifications. It should augment the core HSDA definition, overlaying with existing contact information, but it should also be dovetailed with new projects like approval and feedback system. More research needs to be conducted on existing messaging API standards, and leading channels that existing human services implementations and their software vendors are already using.

### [Webhooks](https://github.com/openreferral/api-specification/issues/35)
I want to begin separate project for handling an important aspect of any API operations, and not just being their to receive requests, but can also push information externally, and respond to scheduled, or event driven aspects of API operations. Webhooks will play a role in the approval and feedback system, as well as the metadata, and messaging projects--eventually touching all aspects of the core HSDA resources, and separate projects.

Alongside the approval and feedback, universal id, and messaging projects, webhooks will set the stage for the future of HSDA, where individual city and regional implementations can work together, share information, federate and share responsibility in updates and changes. Webhooks will be how each separate implementation will work in concert, making the deliver of human services more real time, and orchestrated across providers, achieving API the vision of Open Referral founder Greg Bloom.

## What Is Next?
We have a lot on the table to discuss currently. We need to settle some pretty important API design discussions that will continue to have an impact on API operations for a long time. I want to help push forward the conversation around these API design discussions, and get these API projects moving forward in tandem. I need more input from the vendors, and the community around some of the pressing discussions, and then I'm confident we can settle in on what the final version 1.1 of the API specification should be, and what work we want to tackle as part of 1.2 and beyond. I'm feeling like with a little discussion we can find a path forward to reach 1.2 in the fall of 2017.
