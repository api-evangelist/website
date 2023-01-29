---
published: true
layout: post
title: 'One Possible Vision for API Commons'
image: https://kinlane-productions2.s3.amazonaws.com/algorotoscope-master/bf-skinner-highway-line.jpeg
author:
name: kinlane
tags:
- API Commons
- Standards
- Governance
- Regulations
- Schema
- Frameworks
---
Everything in this world seems to occur in cycles, with many patterns I’ve wrestled with years ago coming around again. In 2014, in the heart of the Oracle vs. Google, me and my partner in crime Steve Willmott created the [API Commons](http://apicommons.org/) and [APIs.json](http://apisjson.org/) to help us make sense of the sprawling API landscape we saw emerging. I’ll dive into what each of these projects were shortly, but in short, they are machine-readable open source standards for licensing and indexing APIs. I’ve kept both of these specs alive over the years, even giving APIs.json a makeover a couple of years back, and investing in potential version 2.0 or alternate forms of the API indexing standard. I haven’t done much beyond brainstorming when it comes to API Commons, for a variety of reasons I will attempt to address in this narrative. 

## API Commons
In 2014, [the Oracle vs. Google API copyright case](https://apievangelist.com/2021/04/13/My-oracle-vs-google-api-copyright-journey/) was making its way through California courts to eventually the Supreme Court. In 2021, the ruling supported the previous court's decision that APIs were indeed copyrightable but support Google’s claim that it was fair use. In 2014 we didn’t know what the outcome would be but we didn’t want to wait and wanted to provide a methodology for declaring the license on your API, while ensuring that the license for your API was separate from your code, and the license reflected copyright--using Creative Commons, not Apache, MIT, or other licenses you see on the code behind APIs. So, we created API Commons, a simple little schema that would declare which side of the war you were on, and you made it clear that your API licensing was separate from your code. But once we had it created, where would you put it? How would you declare it? We need a way to index your API, describe what it did, and include your API Commons license as part of the index. 

```
{
    "apis": [
        {
            "name": "Name of Your APIs",
            "description": "Description of what your api does and the value it delivers.",
            "image": "https://example.com/image.png",
            "keywords": "keywords, tags, that, describe, api",
            "license": "http://creativecommons.org/licenses/by-sa/3.0/deed.en_US",
            "attribution": "Individual or Company Name",
            "url": "URL to this APIs manifest",
            "definitions": [
                {
                    "type": "[type: ie Swagger, RAML, API Blueprint]",
                    "url": "https://github.com/locationofdefinition"
                }
            ]
        }
    ],
    "tags": "api-commons-manifest",
    "updated": "11/04/2013"
}
```

## APIs.json (and YAML)
Alongside API Commons we launched [APIs.json](http://apisjson.org/) to help API producers index their APIs using a simple and flexible schema that could be used for discovery. With APIs.json you could provide a title and description for your API index, and then provide an index of one or many APIs, with a variety of supporting properties, one of which was API Commons.  I had been indexing and profiling the top APIs as part of my work as the API Evangelist for a couple of years, so I knew what the common building blocks of APIs were, and I included them as property types for the APIs.json format. We published APIs.json, convinced a handful of API Providers to publish one, and got to work on an API search engine called APIs.io. Unfortunately after Red Hat bought Steve’s company 3Scale, and while we were working to migrate the domain, IBM bought Red Hat, and the red tape became too great to pull the domain and search engine out of the company.

```
{
  "name": "Example API",
  "description": "This is an example APIs.json file, demonstrating what is possible with the API discovery specification.",
  "image": "https://kinlane-productions.s3.amazonaws.com/apis-json/apis-json-logo.jpg",
  "tags": [
    "Application Programming Interface",
    "API"
  ],
  "created": "2014-04-07",
  "modified": "2020-09-03",
  "url": "http://example.com/apis.json",
  "specificationVersion": "0.14",
  "apis": [
    {
      "name": "Example API",
      "description": "This provides details about a specific API, telling what is possible.",
      "image": "https://kinlane-productions.s3.amazonaws.com/apis-json/apis-json-logo.jpg",
      "humanURL": "http://example.com",
      "baseURL": "http://api.example.com",
      "tags": [
        "API",
        "Application Programming Interface"
      ],
      "properties": [
        {
          "type": "x-signup",
          "url": "https://example.com/signup"
        },
        {
          "type": "x-documentation",
          "url": "https://example.com/documentation"
        },
        {
          "type": "x-openapi",
          "url": "http://example.com/openapi.json"
        },
        {
          "type": "x-json-schema",
          "url": "http://example.com/json-schema.json"
        },
        {
          "type": "x-blog",
          "url": "http://example.com/blog"
        },
        {
          "type": "pricing",
          "url": "http://example.com/pricing"
        }
      ],
      "contact": [
        {
          "FN": "APIs.json",
          "email": "info@apisjson.org",
          "X-twitter": "apisjson"
        }
      ]
    }
  ],
  "include": [
    {
      "name": "Another Example API",
      "url": "http://example.com/apis.json"
    }
  ],
  "maintainers": [
    {
      "FN": "Kin Lane",
      "X-twitter": "apievangelist",
      "email": "info@apievangelist.com"
    }
  ]
}
```

I have long used the APIs.json format to index my APIs. There are still many companies who use it, and I recently heard it was being used at Microsoft to index APIs used to generate SDKs. It didn’t become a hit, or well-known standard. That is alright, I know these things take time and need to build. I just don’t think the time was right, and the fact that the project focused heavily on API search and discovery-—which sadly many do not care about. In my mind, there was so much work still be done on the APIs.json format, as well as the API Commons formatI needed to address through iterations of future versions, but I now see there were also things that needed to play out in the wider world of APIs before the time would be right. That is OK, I am patient. 

## APIs.json Property Types
I was obsessive about APIs.json being flexible and opinionated in the first version of the specification. There were just two properties: type and URL. These are meant to describe properties of an API, its OpenAPI, documentation, pricing page, or terms of service. These can be human readable properties as well as machine-readable properties of an API. APIs.json wasn’t intended to compete with Swagger, OpenAPI, AsyncAPI, Postman Collections, JSON Schema, or other specifications—-it was designed to index them as a single definition for an API. Here are the current sets of properties for the current and next proposed versions:

- 0.14 - Swagger, RAML, Blueprint, WADL, WSDL, TermsOfService, InterfaceLicense, StatusPage, Pricing, Forums, and AlertsTwitterHandle
- 0.15 - Swagger, OpenAPI, JSONSchema, PostmanCollection, AsyncAPI, RAML, Blueprint, WADL, WSDL, Documentation, Authentication, Signup, Login, TermsOfService, InterfaceLicense, PrivacyPolicy, Security, SDKs, StatusPage, Pricing, Rate Limits, Blog, BlogFeed, Forums, Support, ChangeLog, RoadMap, Contact, ErrorCodes, GitHubOrg, GitHubRepo, Twitter, AlertsTwitterHandle

After studying all of the APIs listed in [ProgrammableWeb](https://www.programmableweb.com/) one summer, and regularly monitoring the building blocks of APIs providers, I was pretty confident in what we needed to index to help make the API landscape discoverable. I overestimated the importance of API discovery to companies while doing this work, but I knew that we’d need to index not just the human readable aspects of our operations, but also the machine-readable ones if we are going to be able to automate and tame the chaos. But even this wouldn’t be enough. We’d need to evolve things from being human readable into being more machine-readable. We’d meet our pricing pages, service level agreements, our terms of service, and other building blocks to become machine-readable 

## The Great API Specification Wars
To understand this journey it helps to understand what I like to jokingly call the great API specification wars. Between 2010 and 2020 a number of API specifications emerged, displacing the ones that came before. In 2010 a new specification called Swagger displaced WADL as the way to describe the surface area of APIs. As it gained traction other formats like RAML, Blueprint, and Collections emerged. In 2015, Swagger was clearly dominant when it came to documenting and generating code for your APIs, and it was put into the Linux Foundation and renamed as OpenAPI. OpenAPI displaced RAML, Blueprint, and others, but Postman Collections kept growing and gaining adoption when it came to not just describe what is possible with an API, but it was something that was actually executable. Shortly after Swagger became OpenAPI, a new specification emerged called AsyncAPI that emulated what OpenAPI did for RESTful HTTP APIs, but for event-driven HTTP, TCP, MQTT, and other protocol APIs. The war quieted down with OpenAPI and Postman Collection coexisting, but things are heating up again with the growth and adoption of [AsyncAPI](https://www.asyncapi.com/), as well as new formats once again like [CADL](https://github.com/microsoft/cadl).

Many people have invested in OpenAPI being the one spec to rule them all, extending it, and looking to evolve it with what they needed for not just the API, but the API operations around them. However, for me, the API Commons evolution, along with APIs.json, has shown me that there shouldn’t be one spec to rule them all—-there should be many. There shouldn’t be just many, there should be ever evolving waves of specifications that keep things lively and competitive. Oh, and did I mention [JSON Schema](https://json-schema.org/)? It is a format for modeling and validating your schema, which both OpenAPI and AsyncAPI both use. We haven’t even talked about GraphQL, Protocol Bufgers, Avro, Thrift, and other formats for describing the bits and bytes we are passing around via APIs. As it stands today, OpenAPI is the de facto format for describing what is possible with an HTTP API, and AsyncAPI is rapidly becoming the format for event-driven multi-protocol APIs. Postman Collection is the favorite of developers when it comes to collaborating, automating, documenting, mocking, and testing their APIs, working alone, or along with an accompanying OpenAPI. With JSON Schema as the quiet format for defining and validating the objects being passed back and forth across multi-protocol, multi-pattern APIs. 

## OpenAPI
OpenAPI is the leading specification for defining the surface area of your HTTP RESTful API, defining the paths, operations, parameters, headers, requests, responses, and schema you need to use—here is an example OpenAPI.

```
openapi: '3.0.0'
info:
  version: '1.0.0'
  title: 'Sample API'
  description: Buy or rent spacecrafts

paths:
  /spacecrafts/{spacecraftId}:
    parameters:
      - name: spacecraftId
        description: The unique identifier of the spacecraft
        in: path
        required: true
        schema:
          $ref: '#/components/schemas/SpacecraftId'
    get:
      summary: Read a spacecraft
      responses:
        '200':
          description: The spacecraft corresponding to the provided `spacecraftId`
          content:
            application/json:
              schema:
                $ref: '#/components/schemas/Spacecraft'
        404:
          description: No spacecraft found for the provided `spacecraftId`
          content:
            application/json:
              schema:
                $ref: '#/components/schemas/Error'
        500:
          description: Unexpected error
          content:
            application/json:
              schema:
                $ref: '#/components/schemas/Error'
components:
  schemas:
    SpacecraftId:
      description: The unique identifier of a spacecraft
      type: string
    Spacecraft:
      type: object
      required:
        - id
        - name
        - type
      properties:
        id:
          $ref: '#/components/schemas/SpacecraftId'
        name:
          type: string
        type:
          type: string
          enum:
            - capsule
            - probe
            - satellite
            - spaceplane
            - station
        description:
          type: string
    Error:
      type: object
      required:
        - message
      properties:
        message:
          description: A human readable error message
          type: string
  securitySchemes:
    ApiKey:
      type: apiKey
      in: header
      name: X-Api-Key
security:
  - ApiKey: []
```

OpenAPI uses JSON Schema for the schema portion, and often gets confused with its previous version Swagger. OpenAPI has many shortcomings as made evident by competing and complementary formats like AsyncAPI and the most recent format CADL. 

## AsyncAPI
AsyncAPI is a sister specification for defining the surface area of your event-driven APIs. It is fast becoming the specification associated with high volume, event-driven, and next generation APIs, providing what is needed to map this noisy and fast-growing landscape.

```
asyncapi: 2.0.0
info:
  title: Email Service
  version: '1.0.0'
  description: |
    Sends emails upon certain events
  license:
    name: Apache 2.0
    url: https://www.apache.org/licenses/LICENSE-2.0

servers:
  production:
    url: mqtt://test.mosquitto.org
    protocol: mqtt
    description: Test MQTT broker

channels:
  user/signedup:
    publish:
      operationId: onUserSignUp
      message:
        $ref : '#/components/messages/UserSignedUp'

components:
  messages:
    UserSignedUp:
      name: userSignedUp
      title: User signed up event
      summary: Inform about a new user registration in the system
      contentType: application/json
      payload:
        $ref: '#/components/schemas/userSignedUpPayload'

  schemas:
    userSignedUpPayload:
      type: object
      properties:
        firstName:
          type: string
          description: "foo"
        lastName:
          type: string
          description: "bar"
        email:
          type: string
          format: email
          description: "baz"
        createdAt:
          type: string
          format: date-time
          description: "foo"
```

AsyncAPI also uses JSON Schema for the schema portion, but is expanding and shifting this approach to support binary and other formats often used by real-time systems like Protocol Buffers, Avro, and Thrift, going beyond JSON Schema, but still in a compatible realm.

## JSON Schema
JSON is the ubiquitous format for validating all of the digital objects we are passing around online. It is designed purely for validation, but of many this is synonymous with modeling your data, because they kind of go hand in hand, providing what we need to shape and see things.

```
"$id": https://example.com/person.schema.json
"$schema": https://json-schema.org/draft/2020-12/schema
title: Person
type: object
properties:
  firstName:
    type: string
    description: The person's first name.
  lastName:
    type: string
    description: The person's last name.
  age:
    description: Age in years which must be equal to or greater than zero.
    type: integer
    minimum: 0
```

JSON Schema will be how all API Commons is defined, automated, and governed. It provides the shape and the validation of every schema that passes through. JSON Schema is one of the more important schemas in the stack, but won’t be considered that way by many.

## Collections
Postman Collections is an open source format that is owned by a proprietary company. Like OpenAPI and JSON Schema it is ubiquitous. It is the executable unit of value for APIs amongst developers. It provides many of the same capabilities as OpenAPI, but designed for runtime.

```
{
	"variables": [],
	"info": {
		"name": "Sample Postman Collection",
		"_postman_id": "35567af6-6b92-26c2-561a-21fe8aeeb1ea",
		"description": "A sample collection to demonstrate collections as a set of related requests",
		"schema": "https://schema.getpostman.com/json/collection/v2.0.0/collection.json"
	},
	"item": [
		{
			"name": "Newman: GET request",
			"event": [
				{
					"listen": "test",
					"script": {
						"type": "text/javascript",
						"exec": [
							"pm.test('expect response be 200', function () {",
							"    pm.response.to.be.ok",
							"})",
							"pm.test('expect response json contain args', function () {",
							"    pm.expect(pm.response.json().args).to.have.property('source')",
							"      .and.equal('newman-sample-github-collection')",
							"})"
						]
					}
				}
			],
			"request": {
				"url": {
					"raw": "https://postman-echo.com/get?source=newman-sample-github-collection",
					"protocol": "https",
					"host": [
						"postman-echo",
						"com"
					],
					"path": [
						"get"
					],
					"query": [
						{
							"key": "source",
							"value": "newman-sample-github-collection",
							"equals": true,
							"description": ""
						}
					],
					"variable": []
				},
				"method": "GET",
				"header": [],
				"body": {},
				"description": ""
			},
			"response": []
		},
		{
			"name": "Newman: POST request",
			"request": {
				"url": "https://postman-echo.com/post",
				"method": "POST",
				"header": [
					{
						"key": "Content-Type",
						"value": "text/plain"
					}
				],
				"body": {
					"mode": "raw",
					"raw": "Duis posuere augue vel cursus pharetra. In luctus a ex nec pretium..."
				},
				"description": ""
			},
			"response": []
		},
		{
			"name": "Newman: POST request with JSON body",
			"request": {
				"url": "https://postman-echo.com/post",
				"method": "POST",
				"header": [
					{
						"key": "Content-Type",
						"value": "application/json"
					}
				],
				"body": {
					"mode": "raw",
					"raw": "{\"text\":\"Duis posuere augue vel cursus pharetra. In luctus a ex nec pretium...\"}"
				},
				"description": ""
			},
			"response": []
		}
	]
}
```

OpenAPI and AsyncAPI are the source of truth for an API, with Collections act as a derivative of that truth across the API lifecycle. Collections are the API client for APIs. Collections are the documentation for APIs. Collections can provide mock and virtualized instances of an API. Collections provide a wide variety of testing for APIs. Most importantly, it can be run, scheduled, and baked into CI/CD pipelines, automating our API operations.

## The Technology, Business, and Politics
I’ve been immersed in the technology, business, and politics of all of this since full time since 2010. I’ve seen how hard it is to do this. I’ve seen how much influence tech companies have over these seemingly open source specifications and the APIs they power. I am not excluded from this as I orchestrate the evolution of almost all of these specifications as we speak as part of Postman Open Technologies. I get the technical side of doing this. I understand what the business motivations are or aren’t. I also get the politics, egos, and the very human side of all of this. Specs aren’t easy. The human beings who contribute to them are often very smart, very opinionated, and very hard headed folks who believe the way they do, for a number of reasons. This is just the way it is. This isn’t exclusive to the API specification space, and represents the challenges any API architect, designer, developer, technical writer, and product or engineering manager would recognize across their operations. 

Many days I want to throw up my hands and walk away from this space because of what I see in this dimension. I’ve done it a couple of times. I keep coming back. I keep stirring the pot. Causing trouble. While working to be one of the leading voices in the conversation. This well spring is one area I am pulling from when it comes to this narrative I am crafting right now. This is why I want to reinvent API Commons to provide us with a more resilient scaffolding for this big circus tent. I am taking what I’ve learned over the last 12 years performing as almost every sideshow and act, and sometimes the ringmaster for this very important circus. In my mind, these aren’t just API specifications, these are the guiding templates for our professional and personal lives. These are the templates that shape our messages, images, videos, payments, and everything else in our lives that are moving online today. I am impressed at what we’ve all been able to accomplish in the last decade when it comes to APIs powering our world, but we are going to have get more organized and standardized when it comes to doing this, and we need to stop reinventing the wheel with the known building blocks, and innovate on what is actually unique.

## Getting More Opinionated On the LIfecycle
Over the years I also have gotten more opinionated about the API lifecycle. I am not getting more opinionated about a single definition of the API lifecycle, but I am getting opinionated about being opinionated about the API lifecycle and having a common definition for what it is across any organizational domain. Early last year I identified this as one of the biggest reasons we do not see the forward motion and velocity we envision across our API operations, and I got to work on trying to understand how we can better define the lifecycle around our APIs. Like we work hard to define the surface areas of our APIs using OpenAPI and AsyncAPI, as well as the objects we pass around using JSON Schema, I have been working on several drafts for what I’d consider to be one possible API common. 

```
# An extension for OpenAPI
x-lifecycle:

  # Navigating Change
  version:
      current: 'http://example.com/next'
      next: 'http://example.com/next'
      previous: 'http://example.com/next'

  # Development
  # Staging
  # Production
  environments: 

      # Environment for development
      - name: Development
        url: 'https://www.postman.com/environment'  
        variables:
            base_url: 'http://example.com/development'       
            api_key: 'xe3847d3J78393jkdm1123'  

      # Environment for production
      - name: Production
        url: 'https://www.postman.com/environment'  
        variables:
            base_url: 'http://example.com/production'       
            api_key: 'xe3847d3J78393jkdm1123'                

  # Design
  # Pre-Release    
  # Active
  # Recommended
  # Retired
  # Deprecated
  maturity: 'Active'

  # Public
  # Internal
  # Group
  # Partner
  visibility: 'Public'

  # Essential Building Blocks of the API Lifecycle
  buildingBlocks:

      # All Documentation
      documentation:

          # Reference Documentation
          - type: reference
            title: Reference Documentation
            url: 'https://example.com/documentation'
            collection: 'https://www.postman.com/collection'

          # Workflow Documentation
          - type: workflow
            title: Workflow Documentation
            url: 'https://example.com/documentation'
            collection: 'https://www.postman.com/collection'

      # All Tests
      tests:

          - type: contract
            title: Contract Testing
            url: 'https://example.com/contract-testing'
            collection: 'https://www.postman.com/collection'

          - type: performance
            title: Performance Testing
            url: 'https://example.com/performance-testing'
            collection: 'https://www.postman.com/collection'

          - type: security
            title: OWASP Top 10
            url: 'https://example.com/owasp-security-testing'
            collection: 'https://www.postman.com/collection'

      # All Mocks
      mocks:

          - type: sandbox
            title: Mock Server
            url: 'https://example.com/mock'
            collection: 'https://www.postman.com/collection'

      # All Monitors
      monitors:

          - type: uptime
            title: Uptime Monitor
            url: 'https://example.com/monitor'
            collection: 'https://www.postman.com/collection'
            environment: 'https://www.postman.com/environment'

          - type: performance
            title: Regional Performance Monitor
            url: 'https://example.com/monitor'
            collection: 'https://www.postman.com/collection'
            environment: 'https://www.postman.com/environment'

      # All Reports
      reports:

          - type: overview
            title: Dashboard
            url: 'https://example.com/monitor' 
            collection: 'https://www.postman.com/collection'           

  # Milestones for the API
  milestones:

      # Design
      - type: design
        description: 'Design agreed upon by stakeholders.'
        date: '2021-05-01'

      # Review
      - type: review
        description: 'Wentn through architectural review.'
        date: '2021-06-01'          

      # Staging
      - type: staging
        description: 'Left staging phase of development.'
        date: '2021-07-01'

      # Active
      - type: active
        description: 'Put into production as active API.'
        date: '2021-07-15'  
```

I am not saying that this is the lifecycle that everyone should follow. This is the first response I get to this from people I’ve shared it with. I am saying that this is one possible surface area for our API lifecycle, providing a scaffolding for defining, but also evolving, iterating, and forking the lifecycle surrounding our APIs. OpenAPI and AsyncAPI have been getting us on the same regarding what an API does, and I am looking to do the same for the API lifecycle across many different APIs, using all of the artifacts we use across the API lifecycle to collaborate, automate, and govern our API operations in more reliable ways. I am going to submit this as a draft API.json definition, but I am still deciding whether it should replace the current definition or introduce a difference of APIs.json artifact, going indexing and getting more opinionated about the API lifecycle.

## Bringing Governance Into the Picture
Most people like a single artifact to rule them all. People don’t like complexity, especially when it is distributed. I get it. But then we should apply the same logic to the number of APIs created. Until then, we need ways to automate the governance of our APIs, enabling us to do more with less, and make sense of the sprawling landscape. When it comes to the governance of our APIs, the leading specification for doing this is [Spectral](https://github.com/stoplightio/spectral). 99% of the attention on Spectral right now is focused on governing the surface area of our APIs defined with OpenAPI. Spectral is a rules-based language allowing you to define YAML or JSON rules that will pass or fail when applied to an OpenAPI, revealing whether the pattern we are looking to present exists or not—governing the surface area of our APIs. 

Governing simple things like, whether an OpenAPI has a description:

```
openapi-v3-info-description:
  description: Ensures that all OpenAPIs have a information description.
  message: The info object should have a description.
  given: $.info
  severity: error
  recommended: true
  type: style
  formats:
    - oas3
  then:
    field: description
    function: truthy
``

Or whether or not the OpenAPI has contact information:

```
openapi-v3-info-contact:
  description: Ensures that all APIs have contact information.
  message: API must have a contact information available.
  given: $.info
  severity: error
  recommended: true
  type: style
  formats:
    - oas3
  then:
    field: contact
    function: truthy
```

Or more complicated things like parameters being snake case:

```
openapi-v3-components-parameters-snake-case:
  description: Ensuring that all components parameters are using snake case for the name.
  message: The component parameters name needs to be snakeCase.
  given: >-
    $.components.parameters..[?(@.in==='query' || @.in==='path' ||
    @.in==='cookie')]
  severity: warn
  then:
    field: name
    function: casing
    functionOptions:
      type: snake
```

Rules can be organized into rulesets to look for things that cover multiple areas of an OpenAPI. Almost anything you can describe with an OpenAPI, you can lint and govern using a Spectral rule. These rules grouped into policy definitions that matter to business are being applied at API design time, and enforced at build time as part of CI/CD pipelines. It is being used to enable developers to design more consistent APIs and to ensure that new APIs being pushed into production are as consistent as possible. While we are in the early days of applying Spectral, Spectral holds a lot of promise when it comes to governing the design of our APIs, but we are going to need a lot more investment in meaningful and thoughtful rulesets that translate into business value, but also the services and tooling we are using to help us manage the complexity of adopting and applying yet another artifact to help us govern our APIs.

## Beyond Just API Design Governance
While the realm of API design governance continues to stabilize, like other areas of APIs, I am pushing forward with applying rules to other parts of the API lifecycle and operations. OpenAPI is simply an YAML or JSON artifact that describes the surface area of our RESTful HTTP APIs, and can be used to govern AsyncAPI, but I’d like to expand to the lifecycle, operations, and API discovery using apis.json. My partner in crime on this [Arnaud Laurent](https://apihandyman.io/) is playing around with storytelling using Spectral rules. This is something I am extremely optimistic about, as Arnaud works overtime to move rules from the realm of policing, enforcement, and governance into the realm of storytelling, guiding, and incentivizing. I’ll avoid going into too much detail here about what I am up to, but I am looking to expand listing across every stage of the API lifecycle and every nook and cranny of API operations. We just have to have an accurate map of the landscape for enterprise API operations, industries, and other bounded contexts within the API universe.

* Caching
* Cross-Origin Resource Sharing (CORS)
* Keys
* Logging
* Models
* Plans
* Rate Limits
* Request Transformation
* Request Validation
* Response Status Codes
* Response Transformation
* Paths
* Stages
* Tags
* Tracing
* TimeOuts
* Versioning

Every stop along the API lifecycle, and every detail of a digital product have JSON outputs that can be governed. OpenAPI is just an output (or input) of the API design process. Policies and rules can be applied to every stage of the life cycle, while also helping translate between tech and business, and back again. Nobody cares about API governance but just a handful of people, to everyone else it just needs to look like enablement, nudging, and guardrails that move you in the logical direction. And when policies and rules are just yet another schema that is managed by a group of stakeholders, applying voting and consensus over time to manage change, you end up with some pretty interesting approaches to automating this circus.

## Operational Narratives
One thing I have discovered lately is that policies combined with rules don’t have to just look like linting errors, and the governance they are part of. Rules can tell a story, and be accompanied by plain language and possess the education necessary to bring people up to speed on why a particular policy matters and even do the work for by applying rules and templates. Rules when done well have the potential of walking through many possible stories leading to an outcome that has been vetted by people who have been down this road. We are just getting started with API design governance, helping API architects, designers, and developers deliver more consistently behaving APIs, we just need to begin applying them to our operations, as well as the evolution of our specifications and standards, as well as the policies and rules themselves.

## API Commons 2.0
Similar to how APIs.json enabled API Commons in the early days by giving us a place to hang a machine-readable interface license, I am looking for API Commons to become the factory floor for all the small, medium, and large schema objects we are needing across API operations in any business sector. Let’s see if I can successfully articulate what I am envisioning here. I can see all the bits in my head, but turning it into something coherent enough to share with other people isn’t so easy.  Plus, this is just in the idea stage, and I’d ultimately have to get the buy-in of my partner in crime Steve Willmott, as well as get feedback from the community. I have a lot of work to do to actually get this anywhere close to reality, but this narrative is part of bringing in other folks to help, because this is much bigger than just me. 

## Schema All over the Place
I see schema everywhere. I see schema describing the surface area of our APIs, the operations around them, as well as being passed back and forth to these APIs in production. We have simple to complex, and we have immature to mature. We have formal specifications like OpenAPI, JSON Schema, and AsyncAPI. We have rules like Spectral. We have the mess of objects we are throwing around. We have new ones being created thoughtfully, and being evolved and versioned at a measured pace. We have new ones being created without any thought and iterated upon without any thought to breaking changes and other considerations. We have to allow for all of this to exist in the same realm, while always working to standardize and govern the schema we depend on the most. We need our simple street address objects well defined, as well as the way up to needing our more complex API lifecycle landscape objects to be well defined—-with as minimal work possible, in as open a way as possible.

## Schema At Multiple Levels
When it comes to enterprise API operations, we have team, line of business, enterprise, industry, and Internet scope schema standards, with all levels of maturity and hardness of these schema standards. There are legacy organizations overseeing some standards, which startups rapidly create new standards through simply leading the pack. I want API commons to be a graph of all of this. I want it to be where you find, contribute, and iterate upon Banking Industry Architecture Network (BIAN), Schema.org, or your team's own unique ML model object definition. I want API Commons to be where you go for your schema, how your standardized schema finds you wherever you work. I want to make it dead easy for anyone to use common standards, and for standards to move forward, even if their governing body doesn’t move as fast as what is needed. I want to be able to define a new schema that I need and put it on the conveyor belt to be evolved, without having to be the one to own it and do all the hard work to manage the specification.

It is schema all the way down. JSON Schema has a JSON Schema. OpenAPI and AsyncAPI both use JSON Schema to define objects for both modeling and validation, but there are also JSON Schema to validate both of these formats. Few are aware just how ubiquitous JSON Schema is. Every stage of the API lifecycle from design to deprecation produces some sort of artifact that is defined and validated with JSON Schema. We use JSON Schema to validate the request and responses for synchronous APIs, and publish and subscribe to asynchronous APIs. PSD2 for banking, FHIR for healthcare, TMForum for telecom, and many other industry standards have OpenAPI, AsyncAPI, and JSON Schema for their offerings. It can be dizzying to understand just how pervasive APIs are across industries and government, but also how desperately enterprise organizations are working right now to map the landscape of schema at all levels using these open source API specifications.

## Federated Governance
I really am not good at all the governance part of defining specifications. It isn’t my strength. But I respect the need for it and those who are good at it. I think it is something that is essential to the growth of specifications big and small, and after playing this game for a while, helping put OpenAPI, AsyncAPI, and JSON Schema into the Linux Foundation, I have learned a lot about what I don’t know, and what works and doesn’t work when it comes to moving a specification forward. [I’ve spent a lot of time studying the components of these API specifications](https://blog.postman.com/managing-next-generation-of-api-specifications/), and some of the tools they enable, immersed in m investment in OpenAPI, AsyncAPI, JSON Schema, and Postman Collections, but also trying to align with the GraphQL, GRPC, and other communities. Adding to the mix, I’d like to put APIs.json and API Commons into some sort of governance, but honestly I am not sold that the Linux Foundation would be where they should be, but there is no other better alternative that truly gets APis.

I envision the governance for the API Commons to be defined by the API Commons, providing the scaffolding and conveyor belts for defining and governing itself, beginning with a handful of digital resources potentially needed to manage standards, specifications, and schema.

* Stakeholders - A resource for managing everyone who is involved with moving a spec forward.
* Change - The details of all changes made to each spec, with everything you need to know.
* Messages - The messages sent by all stakeholders when it comes to moving a spec forward.
* Policies - The human readable purposes behind each element of operations and governance.
* Rules - The human readable rules that automate operations and governance using policies.
* Standards - A high-quality, rigorously developed, highly used schema with many stakeholders.
* Votes - The actual votes of stakeholders, providing the architecture decision records for consensus.
* Notifications - The automated notifications that go out to stakeholders around schema change.

I am sure there are numerous other schema and supporting APIs that will be needed to support the API Commons, but this provides a handful of the lego building blocks that will be needed to do this. For lack of a better model I am talking about the Mastodon version of API standards, specifications, and schema work. I even intend for the social element to be in there. You should be able to deploy the core building blocks in any environment, and get to work building through a common set of APIs, using common schema. You should be able to add building blocks into the mix, deliver entirely new building blocks, and plug and play these with other 3rd party and open source APIs. API Common schemas should be used anywhere, but the governance of the schema should also be something you can engage with anywhere.

## Guided Enablement
I want the technical, business, and politics of managing my specs, from the simple to the complicated to be guided from day one. I want any schema I put on the conveyor belt of API Commons to be guided in the right direction. I want to be able to choose at each turn which direction I want to be headed. With each decision I want to have just enough education on the subject, while knowing that the entire API Commons community has been providing feedback and iterating upon the guidance I myself and applying right now. Each element I apply has all of the references and dependencies available for me to understand the scope of any policy I am considering applying to my schema. I want as little, or as much guidance, enablement, and ultimately governance as I want in the moment. I don’t want to have to go find it, I want it to find and nudge me all along the way, even sending me emails or notifications when extremely relevant to my situation.

## Education Built-In
Every policy available to be as part of API Commons should have the right amount of education included. Simple narratives. Well-documented. Explainer videos. I don’t want to become an expert in any single area, but when it comes to the policies I am using to build my open source schema, I need to know just enough. Education should be built into each specification, as well as the process. No step should be taken without being informed. Every stakeholder in a specification should know what they need to contribute. Anyone should be able to drive-by and contribute in a meaningful way, finding the information they need in moments. Every bit of policy applied should be simple and well thought out, keeping the building blocks of API Commons simple and easy to use.

## Schema of Differing Qualities
I am not saying that every standard, specification, and schema should be of an equal quality. API Commons should assume that many schemas will never mature to the point where they‘ll be used by many consumers. However, there should be incentives and easy tracks to get on when it comes to maturing, hardening, and evolving simple schema into full fledged specifications, and standards. For this story I am considering schema any old schema for any object defined using JSON Schema—-without much rigor in how it is formed, used, and iterated upon. A specification is a much more rigorous schema with more stakeholders, policies, rules, and governance applied, and can be applied universally across almost any API, or a specific type of APIs. A standard is a much more rigorous schema with more stakeholders, policies, rules, and governance applied, and can be applied to a specific industry or area of business. I am confident I’ll get questioned on this, but for now it is my baseline. 

## Visible Rating System
Built into API Commons should be a rating system that measures what matters to stakeholders. Each policy and rule applied to a schema successfully should transfer some votes. Each engaged stakeholder with a schema should transfer some votes. Meaningful change, messaging, and other activities should transfer points. Adoption of specifications, standards, and schema should be the ultimate vote, with engaged and activity feedback loops amplifying the rating of each schema. Ratings should be visible as part of the API Commons graph, allowing anyone to see and dig into what is behind the rating, and even weigh what matters to them when searching and putting schema to use. Stakeholders should be incentivized to invest in their rating, even gamify it when it makes sense. To be able to make sense of the commons in any given moment, a rating system will be needed to find the signal in the noise.

## Signal in the Noise
There are many theories for how you should deliver APIs and the applications that use them. Holistic approaches to API design, lifecycle, and governance are popular with people who want to do this well, and follow a well-planned API strategy. In reality, APIs are getting deployed everywhere to support applications and integrations in the moment. Many companies are producing or consuming APIs without any overarching strategy for the APIs—-viewing them as just an implementation detail, not a formal catalog of their enterprise digital resources, capabilities, and experiences. The average enterprise digital landscape is a sprawling digital landscape of APIs of different sizes, shapes, and quality. The digital resources, capabilities, and experiences they provide are largely just noise without any centralized or coordinated orchestration across the enterprise. This noise is reflected outside the enterprise within the industries they operate in, making for a very noisy business landscape online. API Commons can help perpetually find the signal within this noise, introducing common schema whenever possible, standardizing APIs, but also how they are made available and work together.

## Transparency by Default
One of the common illnesses I see across API specifications, standards, and schema, is a lack of transparency. Even when standards bodies are delivering open-source solutions, they rarely operate any form of open-source governance. Every aspect of API Commons should be transparent. It should all happen out in the open. Even when we get around to talking about budgets, sponsorship, and other financial aspects, these should be open. I am talking about blockchain level transparency without blockchain. There should be no reason that any specifications, standards, or schema in the API Commons should be moved forward behind closed doors. Sure, we can’t stop private conversations from happening, but any forward motion for the schema itself should be transparent. I am sure there are aspects of operations that will eventually be determined of concern by each individual instance, and we can address these aspects when they arise. Transparency should be the default, unless otherwise agreed upon by stakeholders.

## Organically Social
Another deficiency I see in existing API specifications, standards, and schema, is that they aren’t naturally social and nurturing to their communities in consistent ways. Some standards bodies I work with are great at being part of their community, communicating at every turn, while others leave much to be desired. I wouldn’t say it is because of any ill will, most just are pretty geeky people who aren’t always good at it. I suffer from approaching the social and communicating in waves, where I am very good for some periods, but depending on how deep I go down the technical rabbit hole, I get much worse at being social and communicating around change and other activities. Like governance, communication and being social within the community should be built-in, something that nudges and happens in the background. I want to be reminded every time I forget to communicate around change. I want to be reminded of how long voting periods are when I engage with stakeholders seeking consensus for change--social should be organic.

## Dealing With The Egos
I want API Commons to deal with egos. Mine included. I want it to dispel dogma. People who contribute to specs tend to be really smart people with big personalities. I want to not only accommodate this reality, but I want to figure out how to bring more stakeholders into the conversation. The consumers of common API specifications, standards, and schema are wide, but the people who are involved in contributing to them are usually very narrow. We need to close the divide that exists between these two groups, and make the contribution process easy for anyone to understand and get involved. One of the most common ways I see standards bodies become inaccessible to normal people is the egos and personalities involved in governance, and building within the community. API Commons should acknowledge this is a reality as something that should be baked in, helping perpetually develop models for how to minimize the impact of ego on schema development.

## Embracing the Drive-Bys
If you have worked with open source specifications, standards, or tooling you have witnessed the drive-bye who show up to tell you what needs to be done. I want to encourage this. I want API Commons to have ready-to-go work for these drive-byes to pick up. I want it to be very, very clear what work needs to happen, and if you have great ideas for what work should happen, there is a very clear and simple set of actions you can take to set it in motion. Any proposal should be balanced with equal amounts of investment by the owner to get the attention of stakeholders, demonstrate the changes they wish to see, and be a strong voice for being the change they want to set in motion. While not all drive-by incidents will rise to the occasion, there shouldn’t be any obstacles in the way when it comes to submitting a proposal for anything rating from fixing a typo on the website to adding a property to a specification or standard. Anyone should be able to get involved, no matter what skills they possess.

## Dealing with the Tech Giants
API Commons should be welcoming to any size of company, institution, organization, or government agency, while preventing them from obtaining any outsized control over the governance and direction of any specification, standard, or schema. Tech companies make excellent benefactors for open source standards, but they have also mastered how they influence the conversation when doing as part of some of the existing open-source standards bodies that exist today. While this isn’t bad by default, it is something to be hyper aware of, and build into how the API Commons works. Tech companies should be able to provide money, act as stakeholders, but their involvement should never be greater than any other single stakeholder. There should be numerous opportunities for tech companies of all shapes and sizes to get involved, there just needs to be sufficient controls and transparency to ensure their impact is as positive as possible for the entire community.

## Specifications and Tooling
The API Commons should just be schema defined as JSON and YAML, expressed as JSON Schema, and made accessible via OpenAPI, AsyncAPI, and Collection-defined artifacts.  Open-source tooling will be essential to all of this, but programming language dogma introduces a significant burden to this discussion. While tooling will be kept separate from the API Commons, leaning on external tooling solutions, feedback loops with tooling providers will be essential to moving most schema forward in any meaningful way. Tooling stakeholders will play a central role in helping guide each iteration of schema, and voting on the changes that are made to each schema, helping govern forward motion. There may be some core tooling solutions eventually established as part of operations, but external tooling and service providers will be engaged with via stakeholder management aspects of governance.  The API Commons is just about the specifications, standards, and schema they are using, but avoid delivering tooling solutions on top of these solutions.

## Everything is API-First
The next iteration of the API Commons will be API-First. All schema will be defined, designed, mocked, documented, and tested, before any tooling is developed inside or outside of the commons. Feedback loops with stakeholders will be used in the design-first only reality, only reaching development, deployment, and distribution using external actors. The commons will operate via a set of core APIs, a handful of 3rd party APIs, exposed via API workspaces, collections, and a few web-only user interfaces. The emphasis of the API Commons is on the schema and API, and not on any tool or service. Everything will be API-first to help us find the signal within the noise of our undeniably code-first reality that exists across enterprise. While I’d like everyone to adopt an API-first approach to how they do APIs, I just don’t see it happening. People have been trained for years to be coders. There will always be some teams who adopt an API design first approach, but I suspect it will always be about code-first in most organizations.

## A Logical Conclusion
[Like the piece I wrote trying to step through this with my How to Draw an Owl analogy](https://apievangelist.com/2023/01/21/draw-an-owl-api-edition-part-one/), I didn’t bring it home with this post. This is more verbose and narrative than I want to actually explain what API Commons should be. The API Commons should be the federated, automated, consensus building assembly line for teams, enterprise organizations, industries, and Internet standards bodies. API Commons is open source, it should strive for consensus and transparency. API Commons should dance with the tech giants, but hold concerts, musicals, and performances outside the current tech halls of power. API Commons should provide the technical, business, and political narratives you need to guide you through the process of delivering the best possible schema, standards, and specifications possible, providing you with the guardrails you need for success. API Comons should provide guardrails that have been designed by people who know and care, and where there is always the provenance you need to trust the guidance you are applying. API Commons should embrace the noise that exists out there and always strive for clarity and establish a signal that is meaningful to human beings, not just corporations, government, and other actors.