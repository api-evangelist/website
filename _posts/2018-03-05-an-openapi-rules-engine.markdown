---
published: true
layout: post
title: 'An OpenAPI-Driven, API Governance Rules Engine'
date: 2018-03-05T13:00:00.000Z
tags:
  - API Evangelist
  - Definitions
  - Validation
  - Governance
image: 'https://s3.amazonaws.com/kinlane-productions/rules/9968073905_95ce575233_z.jpg'
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/rules/9968073905_95ce575233_z.jpg" align="right" width="45%" style="padding: 15px;" /></p>Phil Sturgeon ([@philsturgeon](https://twitter.com/philsturgeon)) alerted me to a pretty cool project he is cooking up, called [Speccy](https://github.com/wework/speccy). Which provides a rules engine for validating your OpenAPI definitions. "Taking off from where [Mike Ralphson](https://twitter.com/PermittedSoc/) started with linting in [swagger2openapi](https://github.com/Mermade/swagger2openapi/), Speccy aims to become the [rubocop](https://github.com/bbatsov/rubocop) or [eslint](https://eslint.org/) of OpenAPI", and to "sniff your files for potentially bad things. "Bad" is objective, but you'll see validation errors, along with special rules for making your APIs better." Helping make sure your API definitions are as consistent as they possibly can be, and deliver on your API governance strategy (you have one right?)

With Speccy, there are a default set of rules, things like ensuring you have a summary or a description for each API path:

``{
	"name": "operation-summary-or-description",

	"object": "operation",

	"enabled": true,

	"description": "operation should have summary or description",

	"or": ["summary", "description"]        

}``

Or making sure you add descriptions to your parameters:

``{

	"name": "parameter-description",

	"object": "parameter",

	"enabled": true,

	"description": "parameter objects should have a description",

	"truthy": "description"

}``

Or making sure you include tags for each aPI path:

``{
	"name": "operation-tags",

	"object": "operation",

	"enabled": true,

	"description": "operation should have non-empty tags array",

	"truthy": "tags",

	"skip": "isCallback"

}``
Then you can get more strict by requiring contact information:

``{
	"name": "contact-properties",

	"object": "contact",

	"enabled": true,

	"description": "contact object should have name, url and email",

	"truthy": [ "name", "url", "email" ]

}``

And make sure youi have a license applied to your API:

``{
	"name": "license-url",

	"object": "license",

	"enabled": true,

	"description": "license object should include url",

	"truthy": "url"

}``

Speccy is available [as a Node package](https://www.npmjs.com/package/speccy), which you can easily run at the command line. Speccy is definitely what is needed out there right now, helping us validate the growing number of OpenAPI definitions in our life. As many companies are thinking about how they can apply API governance across their operations, they should be looking at contributing to [Speccy](https://github.com/wework/speccy). It is something I've been talking with API service providers about for some time, but haven't seen an open source answer emerge, that can help us develop rules for what we expect of our OpenAPI definitions.
<p><img src="https://s3.amazonaws.com/kinlane-productions/openapi/openapi-logo.png" align="right" width="40%" style="padding: 15px;" /></p>
My only feedback right now, is that we need lots of people using it, and helping contribute rules. Oh, and wrap it in an API, and make it available as an easy to use, and deploy containerized microservice. Then lets get to work on the Github Gist dirven marketplace of rules, where I can publish the rules I develop across the projects I'm working on, and of the clients I consult with. Let's get to work making sure there are a wealth of rules, broken down into different categories for API providers to choose from. Then let's get API tooling and service providers to begin baking a Speccy rules engine into their solutions, and allow for the import and management of open source rules.

Speccy only works with OpenAPI 3.0, which makes sense if we are going to be moving forward with this conversation. Spreccy is how we will validate that banking APIs are PSD2 compliant. It is how we will ensure healthcare APIs support the FHIR specification. I have other suggestions for the CLI and API usage of Speccy, but I'd rather see investment in the available rules, before I make too many functional suggestions. I think the rules are where we will begin to define what we are looking for in an OpenAPI rules engine, and that should drive the Speccy features which end up on the road map.
