---
layout: post
title: "Can Swagger Deliver a RESTful API Discovery Service?"
url: 'http://apievangelist.com/2011/11/09/can-swagger-deliver-a-restful-api-discovery-service/'
image: 'http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/blog/Swagger-Logo.png'
---

<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/api-evangelist/swagger/Swagger-Logo.png" alt="" align="right" />

There is a lot of discussion around the growth of APIs, and what the future will look like. How will we discover and make sense of the number of available APIs, and quickly get to work integrating with the APIs that bring the most value to our apps and businesses.

One technology that comes up in every conversation I’ve had is [Swagger][1]. What is Swagger?

> **_Swagger is a specification and complete framework implementation for describing, producing, consuming, and visualizing RESTful web services._**

The goal of Swagger is to enable client and documentation systems to update at the same pace as the server. The documentation of methods, parameters and models are tightly integrated into the server code, allowing APIs to always stay in sync.

Swagger was born out of initiatives from [Wordnik][2], developed for Wordnik’s own use during the development of [developer.wordnik.com][3]. Swagger development began in early 2010 and the framework being released is used by Wordnik’s APIs, which power both internal and external API clients.

Swagger provides a declarative resource specification, allowing users to understand and consume services without knowledge of server implementation, enabling both developers and non-developers to interact with the API, providing clear insight into how the API responds to parameters and options.

I’m familiarizing myself with the specification more and playing with the various tools they provide:

<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/api-evangelist/swagger/Swagger-Screenshot-1.png" alt="" width="325" align="right" />

  * **Swagger UI** \- A dependency-free collection of HTML, Javascript, and CSS assets that dynamically generate beautiful documentation from a Swagger-compliant API
  * **Swagger Core** \- Defines Java annotations and required logic to generate a Swagger server or client.
  * **Swagger CodeGen** \- Contains a template-driven engine to generate client code in different languages by parsing your Swagger Resource Declaration.
  * **Swagger node.js** \- A Sample App is a fully-functioning, stand-alone Swagger server written in javascript which uses node.js and the express framework.
  * **Swagger Scala Sample App** \- A fully-functioning, stand-alone Swagger server written in Scala which demonstrates how to enable Swagger in your API.
  * **Swagger Java Sample App** \- A fully-functioning, stand-alone Swagger server written in Java which demonstrates how to enable Swagger in your API.

I understand that Swagger is not the one specification to rule all APIs, and it won’t make all religious API fanatics happy. But I want to start somewhere. I see three main benefits for API owners coming from adopting Swagger:

  * Automated, consistent generation of clean, beautiful, interactive API documentation
  * Generation of client code and SDK in multiple languages
  * Feeding into an industry wide API discovery language that both developers and non-developers can use

I believe strongly that consistent documentation and code samples ensure an API will get used, but as the number of APIs grows, a system like [Google API Discovery Service][4], will be essential for API adoption across industries and around the globe. I’m hoping to learn more about Swagger, and see if it can help deliver on this vision.

   [1]: http://swagger.wordnik.com/ (Swagger)
   [2]: http://www.wordnik.com/ (Wordnik)
   [3]: http://developer.wordnik.com/ (developer.wordnik.com)
   [4]: /2011/05/21/google-apis-discovery-service/ (Google API Discovery Service)
