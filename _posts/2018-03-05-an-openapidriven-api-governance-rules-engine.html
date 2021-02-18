---
published: true
layout: post
title: 'An OpenAPI-Driven, API Governance Rules Engine'
image: https://s3.amazonaws.com/kinlane-productions2/rules/9968073905_95ce575233_z.jpg
---

<p><img src="https://s3.amazonaws.com/kinlane-productions2/rules/9968073905_95ce575233_z.jpg" align="right" width="45%" style="padding: 15px;" />
<p>Phil Sturgeon (<a href="https://twitter.com/philsturgeon">@philsturgeon</a>) alerted me to a pretty cool project he is cooking up, called <a href="https://github.com/wework/speccy">Speccy</a>. Which provides a rules engine for validating your OpenAPI definitions. “Taking off from where <a href="https://twitter.com/PermittedSoc/">Mike Ralphson</a> started with linting in <a href="https://github.com/Mermade/swagger2openapi/">swagger2openapi</a>, Speccy aims to become the <a href="https://github.com/bbatsov/rubocop">rubocop</a> or <a href="https://eslint.org/">eslint</a> of OpenAPI”, and to “sniff your files for potentially bad things. “Bad” is objective, but you’ll see validation errors, along with special rules for making your APIs better.” Helping make sure your API definitions are as consistent as they possibly can be, and deliver on your API governance strategy (you have one right?)

<p>With Speccy, there are a default set of rules, things like ensuring you have a summary or a description for each API path:

<div class="highlighter-rouge"><div class="highlight"><pre class="highlight"><code>{
	"name": "operation-summary-or-description",
	"object": "operation",
	"enabled": true,
	"description": "operation should have summary or description",
	"or": ["summary", "description"]
}
</code></pre></div></div>

<p>Or making sure you add descriptions to your parameters:

<div class="highlighter-rouge"><div class="highlight"><pre class="highlight"><code>{
	"name": "parameter-description",
	"object": "parameter",
	"enabled": true,
	"description": "parameter objects should have a description",
	"truthy": "description"
}
</code></pre></div></div>

<p>Or making sure you include tags for each aPI path:

<div class="highlighter-rouge"><div class="highlight"><pre class="highlight"><code>{
	"name": "operation-tags",
	"object": "operation",
	"enabled": true,
	"description": "operation should have non-empty tags array",
	"truthy": "tags",
	"skip": "isCallback"
}
</code></pre></div></div>

<p>Then you can get more strict by requiring contact information:

<div class="highlighter-rouge"><div class="highlight"><pre class="highlight"><code>{
	"name": "contact-properties",
	"object": "contact",
	"enabled": true,
	"description": "contact object should have name, url and email",
	"truthy": [ "name", "url", "email" ]&lt;br /&gt;
}
</code></pre></div></div>

<p>And make sure youi have a license applied to your API:

<div class="highlighter-rouge"><div class="highlight"><pre class="highlight"><code>{
	"name": "license-url",
	"object": "license",
	"enabled": true,
	"description": "license object should include url",
	"truthy": "url"
}
</code></pre></div></div>

<p>Speccy is available <a href="https://www.npmjs.com/package/speccy">as a Node package</a>, which you can easily run at the command line. Speccy is definitely what is needed out there right now, helping us validate the growing number of OpenAPI definitions in our life. As many companies are thinking about how they can apply API governance across their operations, they should be looking at contributing to <a href="https://github.com/wework/speccy">Speccy</a>. It is something I’ve been talking with API service providers about for some time, but haven’t seen an open source answer emerge, that can help us develop rules for what we expect of our OpenAPI definitions.
<p><img src="https://s3.amazonaws.com/kinlane-productions2/openapi/openapi-logo.png" align="right" width="25%" style="padding: 15px;" />
<p>My only feedback right now, is that we need lots of people using it, and helping contribute rules. Oh, and wrap it in an API, and make it available as an easy to use, and deploy containerized microservice. Then lets get to work on the Github Gist-driven marketplace of rules, where I can publish the rules I develop across the projects I’m working on, and of the clients I consult with. Let’s get to work making sure there are a wealth of rules, broken down into different categories for API providers to choose from. Then let’s get API tooling and service providers to begin baking a Speccy rules engine into their solutions, and allow for the import and management of open source rules.

<p>Speccy only works with OpenAPI 3.0, which makes sense if we are going to be moving forward with this conversation. Spreccy is how we will validate that banking APIs are PSD2 compliant. It is how we will ensure healthcare APIs support the FHIR specification. I have other suggestions for the CLI and API usage of Speccy, but I’d rather see investment in the available rules, before I make too many functional suggestions. I think the rules are where we will begin to define what we are looking for in an OpenAPI rules engine, and that should drive the Speccy features which end up on the road map.

