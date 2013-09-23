---
layout: post
title: "Google APIs Discovery Service"
url: 'http://apievangelist.com/2011/05/21/google-apis-discovery-service/'
image: ''
---

<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/google/google-apis-discovery-filing-cabinet.png" alt="" align="right" />The[Google APIs Discovery Service][1] provides a set of web APIs for discovering metadata across Google APIs.

The discovery service delivers a JSON-based API that provides a directory of supported Google APIs, and a machine-readable discovery document"for each of the supported APIs that includes:

  * List of API resource schemas based on JSON Schema
  * List of API methods and available parameters for each method
  * Available OAuth 2.0 scopes for each API
  * Inline documentation of methods, parameters and available parameter values
Developers can use the Google APIs Discovery Service to build client libraries, IDE plugins and other tools that interact with supported Google APIs.

The Google APIs Discovery Service delivers two things for each supported API:

  * **APIs Directory Resource**
    * Identification and description information, including name, version, title, and description.
    * Documentation information, including icons and a documentation link.
    * Status information, including status labels, and an indication as to whether or not this is the preferred version of the API.
    * Discovery document link, the URI of the discovery document for this API
  * **Discovery Document Resource**
    * Schemas, which is a list of API resource schemas that describe the data you have access to in each API
    * Methods, including a list of API methods and available parameters for each method.
    * OAuth scopes, which identifies the list of OAuth scopes available for this API.
    * Inline documentation, which provides brief descriptions of schemas, methods, parameters and available parameter values.
The Google APIs Discovery Service is part of a larger effort by Google to get a handle on their growing number of APIs. Developers find themselves potentially using multiple Google APIs across many application or client projects.

The Google APIs Discovery Service allows developers to find new APIs available in the directory and programmatically discover how the API authenticates, what methods, and parameters are available.

Not many companies have the number of APIs that Google has, and would need an API discovery service. But with the recent growth in web APIs there will be more of a need for API discovery services within specific areas or industries.

   [1]: http://code.google.com/apis/discovery/index.html (Google APIs Discovery Service)
