---
layout: post
title: "Generate API Server, Docs and Client Code Using Swagger"
url: 'http://apievangelist.com/2012/09/18/generate-api-server,-docs-and-client-code-using-swagger/'
image: 'http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/blog/Swagger-Logo.png'
---

[<img src="https://s3.amazonaws.com/kinlane-productions/api-evangelist/wordnik/wordnik-logo.jpeg" alt="" width="200" align="right" />][1]

We all have our own approaches to API design and development, many of which will never see the light of day. In the API space we hear a lot about API management and API success stories, but not much about the process of designing, developing and initial deployment of APIs. I just had a little taste of how the [Wordnik][1] team approaches it, using [Swagger][2].

Often when you hear about Swagger in the industry, you hear about the UI portion. You know the sexy [interactive documentation][3] that is fast becoming a standard with APIs, but it’s just the tip of the iceberg--there is a whole lot more power to Swagger, than just interactive docs.

_“The heart of Swagger is the specification, and from that, cool shit can get done!”, say Tony Tam Wordnik CEO and technical co-founder._

To demonstrate, Tony walked me through Wordnik’s approach to designing, developming and deploying a new API driven iPad app, using a team of 3:

  * One person driving an editor writing JSON files, which are the Swagger spec for the needed API
  * The all three discussed the operations, parameters, while adding them to the JSON, and re-running the swagger spec validator after each meaningful change
  * When they were happy with the specs, they loaded the JSON files into the UI through apache installed on a local machine
  * After they inspected each API and operation again, they wrote the models in the spec files, and reviewed again to make sure everything was good
  * Then they ran the Swagger Codegen and generated a Scalatra (Scala) server from the spec files
  * Then they ran the Swagger Codegen and generated an Objective-C client from the spec files
  * The server developer went off and wired the server to the business logic
  * The front-end guy went and wired the UI to the objective-c library

The process took 2.5 hours in total, from API to interface--a technique they call interface-driven development, which focuses on modeling the perfect interface for the problem they are trying to solve using an API.

[<img class="c2" src="https://s3.amazonaws.com/kinlane-productions/api-evangelist/wordnik/Swagger-Logo.png" alt="" width="200" align="right" />][2]

To solve this particular problem, they needed a scala server for the back-end. they could have just as easily generated a Node.JS server, a Rails Sinatra server or any other based upon simple [mustache templates][4]. Additionally they could generate JavaScript, Scala, PHP or Python clients, but for this project they only needed Objective-C.

The [Wordnik][1] approach to API design and development using [Swagger][2] is interesting. For me, it demonstrates that a clean API spec should not be an afterthought, and a means by which you generate interactive API documentation, or when API discovery becomes an issue. Your entire design, development and management process should center around a meaningful API spec, which will then allow you to deploy your API server, interactive documentation, client code, while also providing API discovery.

   [1]: http://www.wordnik.com/
   [2]: http://swagger.wordnik.com/
   [3]: http://apievangelist.com/buildingblocks/interactive_documentation.php (interactive documentation)
   [4]: http://mustache.github.com/ (mustache templates)
