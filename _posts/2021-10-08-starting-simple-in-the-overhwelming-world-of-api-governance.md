---
published: true
layout: post
title: 'Starting Simple in the Overwhelming World of API Governance'
image: https://s3.amazonaws.com/kinlane-productions2/algorotoscope-master/35201856153_61bc075e4b-nazi-invasion.jpg
tags:
  - Governance
  - Rules
  - Design
---
The world of API governance can be pretty overwhelming when it comes to trying to figure out where to get started. Almost everyone I talk to, beginner and expert, has a difficult time getting their head around what should happen first, so I figured I’d work on establishing some blueprints for getting started. When it comes to design governance there are a lot of rabbit holes you can fall down, but I find it helps focusing on some of the most common elements we can get mixed up when designing our APIs.

### Information
The place to start with governance is to make sure we have the essential information for an API present, establishing the base of meta data that is needed to describe what an API does, being able to contact whoever is behind the API, and standardizing the licensing and terms of service being applied.

- [**Title**](https://rules.linting.org/#info-title) - Every API should have a title that properly describes what it does.
- [**Title Max Length**](https://rules.linting.org/#info-title-max-length) - The title of the API should be as concise as possible.
- [**Title Word Check**](https://rules.linting.org/#info-title-word-check) - There are some words we do not want to see in the title.
- [**Summary**](https://rules.linting.org/#info-summary) - Every API should have a summary that describes what the API does.
- [**Summary Max Length**](https://rules.linting.org/#info-summary-max-lengthinfo-summary-max-length) - The summary of the API should not be too long.
- [**Summary Word Check**](https://rules.linting.org/#info-summary-word-check) - There are some words that shouldn’t be in summary.
- [**Description**](https://rules.linting.org/#info-description) - Every API should have a detailed description of what it delivers.
- [**Description Max Length**](https://rules.linting.org/#info-description-max-length) - We don’t want the description of the API to be a novel.
- [**Description Word Check**](https://rules.linting.org/#info-description-word-check) - We want to filter out some words from the description.
- [**Contact**](https://rules.linting.org/#info-contact) - Every API should have a contact object present in the OpenAPI.
- [**Contact Name**](https://rules.linting.org/#info-contact-name) - There should be a contact person assigned to each API.
- [**Contact Email**](https://rules.linting.org/#info-contact-email) - There should be a contact emailed available for each API.
- [**Contact URL**](https://rules.linting.org/#info-contact-url) - The API should have a URL to a contact page defined.
- [**License**](https://rules.linting.org/#info-license) - The license object should be present for any that is published.
- [**License Name**](https://rules.linting.org/#info-license-name) - The license should have a name applied to each API.
- [**License URL Apache**](https://rules.linting.org/#info-license-url-apache) - The license for APIs should all be Apache.
- [**License URL MIT**](https://rules.linting.org/#info-license-url-mit) - The license for APIs should all be MIT.
- [**Terms of Service**](https://rules.linting.org/#info-terms-of-servce) - Every API should have a terms of service applied to OpenAPI.

These API governance rules provide a nice base for any team to start with when it comes to seeding your design governance rulesets and guidelines.  You aren’t even beginning to touch on the technical details of each API here, but there is a huge opportunity to enhance the discovery, onboarding, and evolution of APIs by standardizing the information available.

### Versioning
After getting a hand on the information for each API it makes sense to lay the baseline for how versioning should be applied across APIs. Providing clear guidelines and automated rules that can be applied to streamline how change management is handled across teams in a consistent way across all of the APIs being developed.

- [**Version**](https://rules.linting.org/#info-version) - Every API should have a version property assigned in OpenAPI.
- [**Version Semantic**](https://rules.linting.org/#version-semantic) - All APIs should be versioned using a semantic approach.
- [**Version Date**](https://rules.linting.org/#version-date-format) - All APIs should be versioned using a data format approach.
- [**Version Path**](https://rules.linting.org/#version-segment-second) - The version should be applied in the path for an API.
- [**Version Query Parameter**](https://rules.linting.org/) - The version should be applied in a query parameter.
- [**Version Header**](https://rules.linting.org/) - The version should be applied in the header for an API.

This area of governance is a pretty critical aspect of potentially stabilizing API Operations, getting all teams on a level playing field when it comes to managing change, but more importantly communicating it out with other teams and API consumers. This is an area that should be present in the first draft of any API design guidelines.

### Paths
API paths are probably the most difficult aspect of defining rules for API governance, and where most of the dogma and friction in the design process lies. I’ve fleshed out a handful of rules that can help stabilize a few of the most common areas, and this area of API governance will take the most amount of work to flesh out.

- [**Trailing Slash Yes**](https://rules.linting.org/#paths-trailing-slash) - You can enforce that every API path has a trailing slash.
- [**Trailing Slash No**](https://rules.linting.org/#paths-trailing-slash-none) - You can enforce that every API does not have a trailing slash.
- [**No Empty**](https://rules.linting.org/#paths-no-empty) - Making sure there are no empty segments in your API paths.
- [**No Dashes**](https://rules.linting.org/#paths-dashes) - Enforcing that there are no dashes in your API paths.
- [**Lowercase Hyphens**](https://rules.linting.org/#paths-lowercase-hyphens) - Making sure all API path segments are lowercase and hyphenated.

I will spend a lot more time looking through the design guides of top API Providers trying to find what some of the most common rules applied to the path. However, even with this needed work, there are plenty of ways we can also keep building out more governance that shape API paths across teams.

### Operations 
The operation layer is the next area ripe for standardization that will have a rippling effect across operations. The individual summary, description, tags, and operation id for each API across hundreds or thousands of APIs provides a massive opportunity for applying governance, and getting teams providing what is needed to coherently describe what each individual API path delivers.

- [**Summary**](https://rules.linting.org/#operations-summary) - Requiring that every API operation have a summary applied for documentation.
- [**Summary Max Length**](https://rules.linting.org/#operations-summary-max-length) - Making sure that your API summaries are not too long.
- [**Summary Word Check**](https://rules.linting.org/#operations-summary-word-check) - Making sure there are not certain words present in the API summary.
- [**Summary Period Check**](https://rules.linting.org/#operations-summary-period-none) - Checking to see if there is a period present in the summary.
- [**Description**](https://rules.linting.org/#operations-description) - Requiring that every API operation have a description applied for documentation.
- [**Description Max Length**](https://rules.linting.org/#operations-description-max-length) - Making sure that your API operation descriptions are not too long.
- [**Description Word Check**](https://rules.linting.org/#operations-description-word-check) - Making sure there are not certain words present in the API description.
- [**Operation ID Camel Case**](https://rules.linting.org/#operations-operationids-camel-case) - Enforcing that the operation id is always defined using camel case.
- [**Operation ID Kebab Case**](https://rules.linting.org/#operations-operationids-kebab-case) - Enforcing that the operation id is always defined using kebab case.
- [**Operation ID Pascal Case**](https://rules.linting.org/#operations-operationids-pascal-case) - Enforcing that the operation id is always defined using pascal case.
- [**Tags**](https://rules.linting.org/#operations-tags) - Making sure that every operation has a tag object present to better organize APIs.
- [**Tags One Of**](https://rules.linting.org/#operations-tags-one-of) - Requiring that there is at least one tag present for each of your API operations.

I have looked at thousands of APIs, and the summary, description, and tags represents where the most friction lies when it comes to discovering APIs, understanding what they actually do, and then onboarding and putting each operation to work. If you can standardize how API developers define their operations you are going to streamline so many things downstream, most notably the generate of SDKs and code snippets when your operation ids are all consistent.

### Parameters
Next, moving to the parameters defined for each operation, it really helps reduce friction in how APIs are produced and consumed when you have a few standardized approaches to the naming, formatting, and education resources provided with parameters. It doesn’t take much to provide a baseline of rules to apply to all query and path parameters, but is something that can reduce so much friction downstream.

- [**Name**](https://rules.linting.org/#parameters-name) - Setting the baseline that all parameters should have a name.
- [**Name Camel Case**](https://rules.linting.org/#parameters-name-camel-case) - Enforcing that parameters names are always camel case.
- [**Name Pascal Case**](https://rules.linting.org/#parameters-name-pascal-case) - Enforcing that parameters names are always pascal case.
- [**Name Snake Case**](https://rules.linting.org/#parameters-name-snake-case) - Enforcing that parameters names are always snake case.
- [**Name Max Length**](https://rules.linting.org/#parameters-name-max-length) - Restrict how long you can make your parameter names.
- [**Name Word Check**](https://rules.linting.org/#parameters-name-word-check) - Make sure certain words do not exist across parameter names.
- [**Description**](https://rules.linting.org/#parameters-description) - Making sure that every parameter has a description present.
- [**Description Max Length**](https://rules.linting.org/#parameters-description-max-length) - Helping make sure that parameter descriptions aren’t too long.
- [**Description Word Check**](https://rules.linting.org/#parameters-description-word-check) - Making sure some words are not used in parameter descriptions.
- [**In**](https://rules.linting.org/#parameters-in) - Requiring that all parameters have an in property to determine query or path.
- [**Type**](https://rules.linting.org/#parameters-type) - Making sure that all properties are defined as a valid type.
- [**Example**](https://rules.linting.org/#parameters-example) - Enforcing that there is always an example to show what a parameter does.
- [**Schema**](https://rules.linting.org/#parameters-schema) - Pushing API developers to always have a schema present for parameters.

If you just stick with one approach to casing, and make sure that each parameter has a description you are will be significantly ahead of the game when it comes to API design governance.  There can be hundreds or thousands of parameters in use across APIs, and having a baseline of governance guidance in place can go along way to making APIs look the same no matter which team developed them.

### Request Bodies
Another dimension of API design governance that is easy to tackle is making sure request bodies are properly applied across the different HTTP methods, and that they common HTTP patterns. Depending on your approach to using parameters or bodies you will have different needs here, but regardless, there are some minimum viable rules that should be in place when it comes to the bodies of your API request.

- [**GET**](https://rules.linting.org/#request-bodies-get-oas3) - Making sure that there is no request body present for GET.
- [**POST**](https://rules.linting.org/#request-bodies-post-oas3) - Making sure that all POST requests have a request body.
- [**POST Media Type**](https://rules.linting.org/#request-bodies-post-media-type-oas3) - Requiring POST bodies to have media type.
- [**PUT**](https://rules.linting.org/#request-bodies-put-oas3) - Making sure that all PUT requests have a request body.
- [**PUT Media Type**](https://rules.linting.org/#request-bodies-put-media-type-oas3) - Requiring PUT bodies to have media type.
- [**PATCH**](https://rules.linting.org/#request-bodies-patch-oas3) - Making sure that all PATCH requests have a request body.
- [**PATCH Media Type**](https://rules.linting.org/#request-bodies-patch-media-type-oas3) - Requiring PATCH bodies to have media type.
- [**DELETE**](https://rules.linting.org/#request-bodies-delete-oas3) - Making sure that there is no request body present for DELETE.

There is a lot more you can do here to make sure there are examples, schema, and other areas, but this provides another baseline for API request bodies that should be considered default as part of API guidance. Not all API designers and developers will have the basics of how HTTP and REST works, and these types of rules really help make it easy to do the right thing when you are designing, developing, or building your API.

### Responses
Moving from the request to the response, there are a handful of rules that should be in place to stabilize the way responses are returned. For RESTful APIs there are some pretty common patterns in place that often get overlooked if you aren’t familiar with common practices, and I pulled together a handful of rules that help define a simple base for handling responses in similar ways across all APIs.

- [**GET 200 Status Code**](https://rules.linting.org/#response-get-200-status-code) - All GET requests should have a 200 status code.
- [**GET 200 JSON Body**](https://rules.linting.org/#response-get-200-media-type) - All GET requests 200 responses should have JSON body.
- [**GET 500 Status Code**](https://rules.linting.org/#response-get-500-status-code) - All GET requests should have a 500 status code response.
- [**POST 201 Status Code**](https://rules.linting.org/#response-post-201-status-code) - All POST requests should have a 200 status code.
- [**POST 201 JSON Body**](https://rules.linting.org/#response-post-201-media-type) - All POST requests 200 responses should have JSON body.
- [**POST 500 Status Code**](https://rules.linting.org/#response-post-500-status-code) - All POST requests should have a 500 status code response.
- [**PUT 204 Status Code**](https://rules.linting.org/#response-put-204-status-code) - All PUT requests should have a 200 status code.
- [**PUT 204 No Body**](https://rules.linting.org/#response-put-204-media-type) - All PUT requests should have no body returned as part of responses.
- [**PUT 500 Status Code**](https://rules.linting.org/#response-put-500-status-code) - All PUT requests should have a 500 status code response.
- [**DELETE 204 Status Code**](https://rules.linting.org/#response-delete-204-status-code) - All DELETE  requests should have a 200 status code.
- [**DELETE 204 No Body**](https://rules.linting.org/#response-delete-204-no-body) - All DELETE  requests should have no body returned as part of responses.
- [**DELETE 500 Status Code**](https://rules.linting.org/#response-delete-500-status-code) - All DELETE  requests should have a 500 status code response.

Even if you understand these details, it is really easy to be inconsistent in how you actually apply these across many different APIs. These API design governance rules applied across your API responses really can assist teams in stabilizing API responses which have huge downstream effects on SDKs, integrations, and effectively developing tests that work across all of your APIs.

### Schema
The schema used across the request and responses for APIs provides a rich area to lay down some base design guidelines, standardizing how teams define schema and the properties they contain, which helps be consistent in the design of your APIs, but also will be something that allows for the validation and automated testing of API requests and responses. There are a handful of API design rules that can be applied to schema at design, develop, or build time.

- [**Name**](https://rules.linting.org/#schema-names) - All schema have to have a valid name applied to the object.
- [**Name Camel Case**](https://rules.linting.org/#schema-names-camel-case) - Enforcing that all schema names are camel case.
- [**Name Pascal Case**](https://rules.linting.org/#schema-names-pascal-case) - Enforcing that all schema names are pascal case.
- [**Name Snake Case**](https://rules.linting.org/#schema-names-snake-case) - Enforcing that all schema names are snake case.
- [**Name Max Length**](https://rules.linting.org/#schema-names-max-length) - Limiting how long you can make your schema names.
- [**Name Word Check**](https://rules.linting.org/#schema-names-word-check) - Ensuring that some words are not in schema names.
- [**Description**](https://rules.linting.org/#schema-description) - Making sure that every schema object has a description.
- [**Description Max Length**](https://rules.linting.org/#schema-description-max-length) - Limiting the length of the schema description.
- [**Description Word Check**](https://rules.linting.org/#schema-description-word-length) - Ensuring that some words are not in schema descriptions.
- [**Type**](https://rules.linting.org/#schema-type) - Making sure that every schema used in your APIs have a type.
- [**Required**](https://rules.linting.org/#schema-required) - Requiring that there is always a list of required properties.
- [**Properties**](https://rules.linting.org/#schema-properties) - Making sure that every schema object has properties.
- [**Properties Name**](https://rules.linting.org/#schema-properties-names) - Requiring that all properties have a valid name.
- [**Properties Name Camel Case**](https://rules.linting.org/#schema-properties-names-camel-case) - Making sure all property names are camel case.
- [**Properties Name Pascal Case**](https://rules.linting.org/#schema-properties-names-pascal-case) - Making sure all property names are pascal case.
- [**Properties Name Snake Case**](https://rules.linting.org/#schema-properties-names-snake-case) - Making sure all property names are snake case.
- [**Properties Name Max Length**](https://rules.linting.org/#schema-properties-names-max-length) - Limiting the length of all of your properties.
- [**Properties Name Word Check**](https://rules.linting.org/#schema-properties-names-word-check) - Filtering out some words from schema properties.
- [**Properties Description**](https://rules.linting.org/#schema-properties-descripton) - Enforcing that all schema properties have a description.
- [**Properties Description Max Length**](https://rules.linting.org/#schema-properties-descripton-max-length) - Limiting the length of schema description.
- [**Properties Description Word Check**](https://rules.linting.org/#schema-properties-descripton-word-check) - Filtering out some words on schema descriptions.
- [**Type**](https://rules.linting.org/#schema-properties-type) - Making sure that all of your schema properties have a type defined.

Like everything else here, there are many other ways in which you can establish API design guidance for your schema, but this begins to set the baseline for how your schemas should be defined, laying the foundation for your team to begin defining other ways in which schema should be crafted. Like operations and properties if you begin applying just these rules across all of your APIs across all of your teams, you will have reduced so much friction across the API lifecycle.

### Making Sure the Basics Are Covered
At this point I guarantee that anyone reading this is already thinking about what is missing from this list. This is how API people think. But it is more important to have API governance in motion than it is to have API governance be comprehensive. Like APIs, you need to start with version 1.0 of your API governance rules, then begin iterating until you find the optimal set of rules for applying at design, develop, and build time. Even once you define the set of rules you want to get started with you have to begin the lengthy journey of getting teams to comply, working with them to apply when they are designing their APIs, but also during the development and sustainment of existing APIs, or even putting in the CI/CD pipeline for future changes to APIs. It is easy for us technologists to get all caught up in the details, and never get off the finish line, or do the hard work of actually getting these API design governance guidelines out to teams for use—start small and iterate.

Next I am going to work on some base API design guides that apply these rules. It is tough to establish a single base guidelines because there are some important design choices present here. Whether or not you choose snake, pascal, or camel case for your parameters and properties will change things up significantly, so I prefer to have them more as a buffet of rules that are grouped in logical ways—then organizations can choose what matter to them. I will also be working on some next level API design rules like helping migrate teams towards the better using the components object in OpenAPI, more standardized design rules that can be applied to the API paths, and other known REST constraints that can be articulated as listing rules. I am also spending time going through many of the API design guidelines for top API Providers and seeing what else I can define as simple rules, but also start building a catalog of more advanced rules. I am pretty confident that the discovery, applying, and evolving of API design rules is going to be one of the most important areas we can invest in right now. I just want to make sure that the waves of enterprise organizations beginning their API governance journeys don’t get overwhelmed and have somewhere they can get started without a massive cognitive load or investment.