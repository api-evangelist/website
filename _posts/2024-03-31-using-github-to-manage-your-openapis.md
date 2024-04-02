---
published: true
layout: post
title: 'Using GitHub To Manage Your OpenAPIs'
image: https://kinlane-productions2.s3.amazonaws.com/algorotoscope-master/every-sunday-morning-shipping-containers-cranes.jpeg
author:
    name: kinlane
tags:
- OpenAPI
- GitHub
- Source Control
---
While profiling some of the top APIs for [my APIs.json Artisanal work](https://github.com/apis-json/artisanal), which I am using to power [APis.io](https://apis.io), I have come across some interesting approaches to using GitHub for managing and publishing OpenAPIs for your API. I am going through each of their approaches, grading them, and then gathering what I feel are the common building blocks of their approaches. Just like profiling the developer portals for these API providers, I learn a lot by reviewing how these API leaders are handling their business.

- **Stripe (B)** - [https://github.com/stripe/openapi](https://github.com/stripe/openapi0)
- **OpenAI (C)** - [https://github.com/openai/openai-openapi](https://github.com/openai/openai-openapi)
- **Digital Ocean (A)** - [https://github.com/digitalocean/openapi](https://github.com/digitalocean/openapi)
- **Azure (B)** - [https://github.com/Azure/azure-rest-api-specs](https://github.com/Azure/azure-rest-api-specs)
- **Amazon Partners (B)** - [https://github.com/amzn/selling-partner-api-models](https://github.com/amzn/selling-partner-api-models)
- **Plaid (C)** - [https://github.com/plaid/plaid-openapi](https://github.com/plaid/plaid-openapi)
- **Twilio (B)** - [https://github.com/twilio/twilio-oai](https://github.com/twilio/twilio-oai)
- **Discord (B)** - [https://github.com/discord/discord-api-spec](https://github.com/discord/discord-api-spec)
- **New York Times (C)** - [https://github.com/nytimes/public_api_specs](https://github.com/nytimes/public_api_specs)
- **Box (B)** - [https://github.com/box/box-openapi](https://github.com/box/box-openapi)
- **BigCommerce (B)** - [https://github.com/bigcommerce/docs](https://github.com/bigcommerce/docs)
- **CloudFlare (C)** - [https://github.com/cloudflare/api-schemas](https://github.com/cloudflare/api-schemas)
- **GitHub (B)** - [https://github.com/github/rest-api-description](https://github.com/github/rest-api-description)
- **Adyen (B)** - [https://github.com/Adyen/adyen-openapi](https://github.com/Adyen/adyen-openapi)

I learned a lot from all of their approaches. I feel pretty strongly that GitHub, or at least Git, is how you want to manage your machine-readable API artifacts. I found Digital Ocean’s approach particularly advanced and is something I am still pondering after profiling. After spending some time looking through each one, I took down the following properties of each provided approach to managing their OpenAPIs on GitHub.

- **Repository** - They all had a dedicated GItHub repository for their OpenAPIs.
- **README** - They put a variety of efforts into their README for consumers.
- **Single OpenAPI** - Some of them would just publish a single OpenAPI.
- **Multiple OpenAPI** - Others would break down and publish multiple OpenAPis.
- **Modular OpenAPI** - Digital Ocean took a very modular approach to theirs.
- **JSON Schema** - Storing your JSON Schema separate from OpenAPI is compelling.
- **YAML** - Some of them would also provide a YAML version of their OpenAPI.
- **JSON** - Others would publish only a JSON, or a JSON to accompany the YAML.
- **Extensions** - Several providers shared the OAS extensions they put to use.
- **Quality Badges** - There were badges showing the health of each build.
- **Make File** - Some provide make files that would automate various builds.
- **GitHub Actions** - There were GitHub actions to automate the CI/CD of OpenAPIs. 
- **Testing** - Sometimes you could find test suites to make sure OpenAPI checked out.
- **Licensing** - There was always licensing for the OpenAPI specs and the code.
- **Contributing** - There is the standard contributing README for GitHub repos.
- **Directory Structure** - A few of them would provide an overview of folders.
- **Versions** - Sometimes they clearly broke out various versions of the OpenAPI.
- **Maturity** - Occasionally you would see preview and other maturity dimensions.
- **Reviews** - Microsoft had the ability to get a review of the OpenAPI being added.
- **Change Log** - There is the regular GitHub changelog markdown for repository.
- **Issues** - The GitHub issues are used as a feedback loop for the OpenAPI definitions.
- **Spectral** - There were Spectral rules, as well as build processes using them.
- **Collections** - Postman collections were oftentimes part of the build output.
- **Status** - There were various mechanisms for communicating the status of OpenAPIs.
- **Limitations** - I saw explanations of the limitations of each of the OpenAPIs.
- **Support** - Some providers were explicit about the support they would provide.
- **Contact** - I found some contact information on some of the repositories.

I find all of these building blocks very compelling in aggregate. They are the makings for a standardized proposal for how you should be using GitHub to manage your OpenAPI artifacts. However, since these are GitHub repositories I also found a fingerprint of a mix of tooling from across the API lifecycle.

- **OpenAPI Generator** - Allowing you to generate the OpenAPIs.
- **Code Generator** - Provide you with the ability to generate code.
- **OpenAPI Editor** - Linking to an OpenAPI editor to support work.
- **Documentation Generator** - Publishing markdown or other docs.

That is a pretty nice list of features, from some of the leaders in the API space. I am going to take this list and look at it through an APIs.json lens to see what I can do to expand the scope of this from the individual API level out to the API operational level. I want to inject APIs.json, and its human and machine readable properties, as well as overlays into the conversation. I’d like to inject what I am learning while profiling APIs as part of my APIs.json Artisanal work, and produce an open source blueprint for API providers to use when managing their APIs using GitHub.

A lot of the building blocks above make sense and are easy to implement, and I would like to get more opinionated on a modular approach, but I need to decide if I want to go as extreme as Digital Ocean. I like having parameters, responses, and schema broken up, but I still need to think on it. I’d also like to get more opinionated on versioning and maturity, even if I am wrong with the first implementation. It is hard stuff, but I think it is an essential area to provide guidance for API providers, and not leave to the imagination—even if it results in debate. I am looking to build an operational blueprint for managing not just OpenAPIs, but any artifact, all indexed using APIs.json.