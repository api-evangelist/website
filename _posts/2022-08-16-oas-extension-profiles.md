---
published: true
layout: post
title: 'OAS Extension Profiles'
image: /images/posts/2022-08-16-oas-extension-profiles.png
author:
  name: pascal
tags:
- API
- Extensions
- Metadata
- Featured
---
The use of [extensions](https://spec.openapis.org/oas/v3.1.0#specification-extensions) in Open API Specification (OAS) has been supported since version 2.x based on a minimalistic approach whereby anyone can define a property starting with `x-` (e.g. `x-myextension`) which can hold any information. This feature was carried over as is to version 3.x. Extensions can be used for various purposes, typically to add functionality, particular use cases, or address shortcoming of the specification.

&#10;There are numerous examples out there, such as 
[GitHub](https://github.com/github/rest-api-description/blob/main/extensions.md)
, [AWS API Gateway](https://docs.aws.amazon.com/apigateway/latest/developerguide/api-gateway-swagger-extensions.html)
, or [readme.io](https://docs.readme.com/docs/openapi-extensions) extensions.


&#10;While technically functional, OAS does not provide any mechanism for capturing information about the extension itself, which has a significant number of negative consequences as for example there no easy way for user or an application to:


- Understand the purpose of the extension
- Validate its content
- Index it in a catalog for discovery
- Preventing name clashes (multiple extensions using the same name)
- Knowing who the author or maintainer are
- etc.

And no guidelines are provided either in terms of governance.


&#10;To address these shortcomings, we are investigating options around “extension profiles” and related topics such as registration, discovery, management, or design principles.


&#10;An extension profile is a object that can be embedded in or referenced by an OpenAPI document to capture elements of information about its extensions such as:


- namespace: a URI or similar globally unique value that ensures there is no ambiguity in terms of the extension identity. The “x-myextension” property essentially being a nickname or abbreviation.
- version: information: an object that carries the extension version number and potentially additional properties such as version changes, validity period, etc. 
- description / purpose: what is this extension about, how should it be used 
- schema: a JSON schema describing the extension content (can be a reference)
- lifecycle: what is the status of this extension (dev/alpha, beta, production, deprecated, retired, etc.)
- provenance: where does this extension come from and who is the maintainer. This is a complex object that contains information about the vendor/agency/project, contact information, and any other relevant pieces of information. We suggest for this to be based on the  [PROV-O](https://www.w3.org/TR/prov-o/) specification



&#10;It addition to above, it might be desirable to: 


- Be able to differentiate between extensions from major organizations (industry vendors, government agencies, international organizations, standard setting initiatives) vs more confined extensions (from projects, individuals, students, R&amp;D).
- Understand which disciplines or domains an extension is intended for
- Have mechanisms for capturing usage / popularity and support user feedback



&#10;We are in the process of exploring the above concepts and document in a draft schema definition, which we anticipate will lead to community driven demo / proof of concepts, prototype registries, and educational materials .


&#10;Note that a similar exercise was attempted in 2017 through the [Specification Extension Metadata for OAS Annotations (Semoasa)](https://github.com/RepreZen/Semoasa) project, proposing a draft machine-readable format for specification extensions. A list of over [a thousand extensions](https://github.com/Mermade/openapi-specification-extensions/blob/main/extensions/combined.tsv") were also identified around the same time. These projects seem to have unfortunately gone idle, but offer some valuable insights and ideas.


&#10;We will naturally also investigate related topics, such as when to use extension, design guidelines, and governance (registration authorities, name resolution, etc.). Down the road, we will explore how new features supporting API extensions can be integrated into the Postman platform, which could include extension aware editors, wizards, registration, search, and other utilities.


&#10;Note that some of the issues being raised here are not only specific to OAS, but are true for other standards such as GraphQL or AsyncAPI. We therefore expect our research to extend beyond OAS. 


&#10;We're very much just getting started on this, and naturally welcome comments, thoughts, suggestions, so do not hesitate to reach out, and keep an eye out for future related posts.




