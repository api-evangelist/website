---
published: true
layout: post
title: Charles Proxy Generated HAR To OpenAPI Using API Transformer
date: 2017-07-20T16:00:00.000Z
tags:
  - API Evangelist
  - Proxy
  - Definitions
  - Conversion
image: >-
  https://s3.amazonaws.com/kinlane-productions/charles-to-openapi/har-conversion.png
---
<p><a href="https://twitter.com/jpmonette/status/885545611906428928"><img src="https://s3.amazonaws.com/kinlane-productions/charles-to-openapi/har-conversion.png" align="right" width="25%" style="padding: 15px;" /></a></p>I was responding to Jean-Philippe M. (@jpmonette) tweet regarding [whether or not I had moved forward my auto generation of OpenAPIs from traffic captured by Charles Proxy](https://apievangelist.com/2015/06/21/parsing-charles-proxy-exports-to-generate-swagger-definitions-while-also-linking-them-to-each-path/). It is one of many features of my internal systems I have not gotten around to finishing, but thankfully he actually answered his own question, and found a better solution than even I had--using my friends over at API Transformer.

I had been exploring ways for speeding up the process of generating OpenAPI specs for the APIs that I'm reviewing, something that becomes very tedious when working with large APIs, as well as just profiling the sheer number of APIs I am looking profile as part of my work. I haven't been profiling many APIs lately, but the approach Jean-Philippe M. came up is petty damn easy, leaving me feeling pretty silly that I hadn't connected the dots myself. 

Here is what you do. Fire up Charles Proxy:

<p align="center"><img src="https://s3.amazonaws.com/kinlane-productions/charles-to-openapi/charles-session.png" align="center" width="80%" style="padding: 15px;" /></p>

Then open up Postman, and make any API calls. Of course you could also proxy mobile application or website API calls through your Charles Proxy, but Postman is a great way to for a majority of the APIs I depend on.

<p align="center"><img src="https://s3.amazonaws.com/kinlane-productions/charles-to-openapi/postman-apis-how.png" align="center" width="80%" style="padding: 15px;" /></p>

After you've made the calls to all the APIs you are looking to generate an OpenAPI for, save your Charles Proxy session as a .har file, which is the last option on the dropdown menu available while saving. Then you head over [to API Transformer](https://apimatic.io/transformer) and upload your .har file, and select OpenAPI (Swagger) 2.0 as the output--push convert.

<p align="center"><img src="https://s3.amazonaws.com/kinlane-productions/charles-to-openapi/api-transformer-convert.png" align="center" width="80%" style="padding: 15px;" /></p>

[API Transformer will then push a fresh OpenAPI to your desktop](https://apimatic.io/transformer), or allow you to publish via a portal, and generate an SDK using [APIMATIC](https://apimatic.io). Automated (mostly) generation of OpenAPI definitions from API traffic you generate through your browser, Postman, Restlet Client, mobile application, or other tooling.

I have abandoned my internal systems, except for my stack of APIs, and depending mostly on 3rd party services like Charles Proxy, Postman, and API Transformer. So I won't be moving forward the custom solution I had developed. However, there still might be benefit of automatically saving .har files to my Dropbox sync folder, then using the Dropbox API, and API Transformer API to automate the conversation of .har files to OpenAPI, and write them back to the appropriate Dropbox folder.
