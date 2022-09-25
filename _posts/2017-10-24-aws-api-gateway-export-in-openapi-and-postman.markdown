---
published: true
layout: post
title: AWS API Gateway Export In OpenAPI and Postman Formats
date: 2017-10-24T11:00:00.000Z
tags:
  - API Evangelist
  - Gateway
  - Deployment
  - Definitions
  - Management
image: 'https://s3.amazonaws.com/kinlane-productions/amazon/aws-api-gateway-export.png'
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/amazon/aws-api-gateway-export.png" align="right" width="40%" style="padding: 15px;" /></p>[I wrote about being able to import an OpenAPI into the AWS API Gateway to jumpstart your API the other day](http://apievangelist.com/2017/10/19/importing-openapi-definition-to-create-api-with-aws-gateway/). OpenAPI definitions are increasingly used for every stop along the API life cycle, and being able to import an OpenAPI to start a new API, or update an existing in your API gateway is a pretty important feature for streamlining API operations. OpenAPI is great for defining the surface area of deploying and managing your API, as well as potentially generate client SDKs, and interactive API documentation for your API developer portal.

Another important aspect of this API lifecycle is being able to get your definitions out in a machine readable format as well. All service providers should be making API definitions a two-way street, just like Amazon does with the AWS API Gateway. Using the AWS Console you can export an OpenAPI definition for any API. What makes things interesting is you can also export an OpenAPI complete with all the OpenAPI extensions they use to customize each API within the API Gateway. Also, they provide an export to OpenAPI, but with Postman specific extensions, allowing you to use use in the desktop client tooling when developing as well as integrating with any API.

I've said it before, and I'll say it again. Every API service provider should allow for the importing and exporting of common API definition formats like OpenAPI and Postman. If you are selling services and tooling to API designers, developers, architects, and providers, you should ALWAYS provide a way for them to generate a static definition of what is going on--bonus, if you allow them to publish API definitions to Github. I know some API service providers like to allow for API import, but worry about customers abandoning their service if there is an export. Too bad, offer better services, and affordable pricing models, and people will stick around.

Beyond selling services to folks with day jobs, having the ability to import and export an OpenAPI allows me to play aorund with tools more. Using the AWS API Gateway I am setting up a number of APIs, then exporting them, and saving the blueprints for when I need to tell as part of a story, or use in a clients project. Having the ability to import and export an OpenAPI helps me better deliver actual APIs, but it also helps me tell better stories around what is possible with an API service or tool. If I can't get in there and actually test drive, play with and see how things work, it is unlikely I will be telling stories about it, or have in my toolbox when I come across a project where I'll need to apply a specific service or tool.

If you are having trouble making your API service or tool speak  OpenAPI, Postman, or other formats, make sure and check out [API Transformer](https://apimatic.io/transformer), which provides an API you can use to convert between the format. So if you can support one format, you can support them all. They even have the ability to take a .har file and generate an OpenAPI. I recommend natively supporting the importing and exporting of OpenAPI, then using API Transformer you can also allow for the importing and exporting in other formats. When you handle the import, you'll always just make sure it speaks OpenAPI before you ingest. When a service supports OpenAPI import and export, it is much more likely I'm going to play with more, as well as increases the chance I'm going to be baking it into the life cycle for one of the projects I'm working on for a client. I'm sure other folks are thinking along the same lines, and are grateful when they can get their API definitions in and out of your platform.
