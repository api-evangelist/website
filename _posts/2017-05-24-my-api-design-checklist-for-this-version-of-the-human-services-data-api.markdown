---
title: My API Design Checklist For This Version Of The Human Services Data API
date: 2017-05-24 09:00:00 Z
tags:
- Design
- HSDS
- HSDA
image: https://s3.amazonaws.com/kinlane-productions/bw-icons/bw-design-checklist.png
---

<p><img src="https://s3.amazonaws.com/kinlane-productions/bw-icons/bw-design-checklist.png" align="right" width="25%" style="padding: 15px;" /></p>I am going through my [API design](http://design.apievangelist.com) checklist for the [Human Services Data API](https://openreferral.github.io/api-specification/) work I am doing. I'm trying to make sure I'm not forgetting anything before I propose a v1.1 OpenAPI draft, so I pulled together a simple checklist I wanted to share with other stakeholders, and hopefully also help keep me focused.

First, to support my API design work I got to work on these areas for defining the HSDS schema and the HSDA definition:

* **JSON Schema** - I generated a JSON Schema from the [HSDS documentation](https://openreferral.readthedocs.io/en/latest/reference/#objects-and-fields). 
* **OpenAPI** - I crafted an [OpenAPI for the API](https://openreferral.github.io/api-specification/definition/yaml/), generating GET, POST, PUT, and DELETE methods for 100% of the schema, and reflective its use in the API request and response.
* **Github Repo** - I published it all in a Github repository for sharing with stakeholders, and programmatic usage across any tooling and applications being developed.

Then I reviewed the core elements of my API design to make sure I had everything I wanted to cover in this cycle, with the resources we have:

* **Domain(s)** - Right now I'm going with api.example.com, and developer.example.com for the portal.
* **Versioning** - I know many of my friends are gonna give me grief, but I'm putting versioning in the URL, keeping things front and center, and in alignment with the versioning of the schema.
* **Paths** - Really not much to consider here as the paths are derived from the schema definitions, providing a pretty simple, and intuitive design for paths--will continue adding guidance for future APIs.
* **Verbs** - A major part of this release was making sure 100% of the surface area of the HSDS schema add the ability to POST, PUT, and DELETE, as well as just GET a response. I'm not addressing PATCH in this cycle, but it is on the roadmap.
* **Parameters** - There are only a handful of query parameters present in the primary paths (organizations, locations, services), and a robust set for use in /search. Other than that, everything is mostly defined through path parameters, keeping things cleanly separated between path and query.
* **Headers** - I'm only using headers for authentication. I'm also considering using the HTTP Prefer Header for schema filtering, but nothing else currently.  
* **Actions** - Nothing to do here either, as the API is pretty CRUD at this point, and I'm awaiting more community feedback before I add any more detailed actions beyond what is possible with the default verbs--when relevant I will add guidance to this area of the design.
* **Body** - All POST and PUT methods use the body for request transport. There are no other uses of the body across the current design.
* Pagination - I am just going with what is currently in place as part of v1.0 for the API, which uses page and per_page for handling this.
* **Data Filtering** - The parameters for core resources (organizations, locations, and services all have a query parameter for filtering data, and the search path has a set of parameters for filtering data returned in response. Not adding anything new for this version.
* **Schema Filtering** - I am taking [Irakli Nadareishvili's advice and going to go with  RFC 7240 - Prefer Header for HTTP](http://www.freshblurbs.com/blog/2015/06/25/api-representations-prefer.html), and craft some different representations when it comes to filtering the schema is returned.
* **Sorting** - There is no sorting currently. I did some research in this area, but not going to make any recommendations until I hear more requests from consumers, and the community.
* **Operation ID** - I went with camelCase for all API operation IDs, providing a unique reference to be included in the OpenaPI.
* **Requirements** - Going through and making sure all the required fields are reflected in the definitions for the OpenAPI.
* **Status Codes** - Currently I'm going to just reflect the 200 HTTP status code. I don't want to overwhelm folks with this release and I would like to accumulate more resources so I can invest in a proper HTTP status code strategy.
* **Error Responses** - Along with the status code work I will define a core set of definitions to be used across a variety of responses and HTTP statuses.
* **Media Types** - While not a requirement, I would like to encourage implementors to offer four default media types: application/json, application/xml, text/csv, and text/html.

After being down in the weeds I wanted to step back and just think about some of the common sense aspects of API design:

* **Granularity** - I think the API provides a very granular approach to getting at the HSDS schema. If I just want a phone number for a location, and I know its location id I can get it. It's CRUD, but it's a very modular CRUD that reflects the schema.
* **Simplicity** - I worked hard to keep things as simple as possible, and not running away with adding dimensions to the data, or adding on the complexity of the taxonomy that will come with future iterations and some of the more operational level APIs that are present in the current metadata portion of the schema.
* **Readability** - While lengthy, the design of the API is readable and scannable. Maybe I'm biased, but I think the documentation flows, and anyone can read and get an idea of the possibilities with the human *services API.
* **Relationships** - There really isn't much sophistication in the relationships present in the HSDA. Organizations, locations, and services are related, but you need to construct your own paths to navigate these relationships. I intentionally kept the schema flat, as this is a minor release. Hypermedia and other design patterns are being considered for future releases--this is meant to be a basic API to get at the entire HSDS schema.

[I have a functioning demo of this v1.1 release](http://developer.open.referral.adopta.agency/documentation/), reflecting most of the design decisions I listed above. While not a complete API design list, it provides me with a simple checklist to apply to this iteration of the Human Services Data API (HSDA). Since this design is more specification than actual implementation, this API design checklist can also act as guidance for vendors and practitioners when designing their own APIs beyond the HSDS schema.

Next, I'm going to tackle some of the API management, portal, and other aspects of operating a human services API. I'm looking to push [my prototype](http://developer.open.referral.adopta.agency/documentation/) to be a living blueprint for providers to go from schema and OpenAPI to a fully functioning API with monitoring, documentation, and everything else you will need. The schema and OpenAPI are just the seeds to be used at every step of a human services API life cycle.