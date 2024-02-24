---
published: true
layout: post
title: 'What We Will Need To Automate API Consumption'
image: https://kinlane-productions2.s3.amazonaws.com/algorotoscope-master/bf-skinner-iron-horse-close.jpeg
author:
    name: kinlane
tags:
- Automation
- Consumption
- Integration
---
I know a lot of folks think we are going to automate API consumption using AI. I am sure there are some layers of business and some APIs that will fit this profile. However, I know the API landscape too well, and know that there are a lot of business, political, and very human obstacles in the way of automating the integration of APIs into new desktop, web, mobile, device, network, and artificial intelligence applications. I want to take a moment to consider what is needed to automate API consumption, and use APIs.json, API Commons, and other machine-readable artifacts to provide the governor we need to automate all of this at scale across many different industries. 

Based upon my experience as the API Evangelist, developing [APIs.json](https://apisjson.org/), [APIs.io](https://apis.io), and with Postman, these are the properties of our APIs, but more importantly our API operations that we will need to be machine-readable if we expect to be able to automate the consumption of APIs:

- **Discovery** - Our search for internal and external APIs.
- **OpenAPI** - Describing the surface of HTTP APIs.
- **AsyncAPI** - Describing the surface of asynchronous APIs.
- **Accounts** - The creation and management of accounts.
- **Pricing** - Understanding the pricing of API resources.
- **Authentication** - Obtaining and rolling over your keys.
- **Terms of Service** - The legal aspects of API consumption.
- **Privacy Policy** - How is privacy being addressed or not.
- **Licensing** - Understanding the license for each API.
- **Security** - Validating the security of the APIs being used.
- **Usage** - Knowing how much you are using an API.
- **Billing** - Handling of the billing for your API consumption.
- **Support** - Obtaining support when you need it now.
- **Status** - Being able to tell if an API is up or down.
- **Change Log** - Understanding what has changed.
- **Road Map** - Preparing for what will change in future.
- **Deprecation** - Being able to properly deprecate APIs.

If you want to fully automate API integration, you need all of those areas of our API operations to be machine readable, and ideally using common interfaces. We’ve managed to make the first two machines readable, and there are efforts in a handful of other areas. There are also APIs for the leading cloud and API gateway providers that will give you programmatic interfaces, and machine readable output for some of these areas.
I have been tracking the common building blocks of API operation since 2010. I have been mapping the human and machine readable properties of API operations using APIs.json since 2014. I know we all are looking for that easy button with AI, but there is a ton of work that needs to occur if we are going to collectively get to the automatic vision of API consumption we all have in our heads. To be able to intelligently connection, consume, switch, disconnect, and work with not just hundreds, but thousands of APIs, we are going to need these areas to be standardized and machine-readable.

I’d say we are about 30-40% of the way towards where we need to be. We are going to need to stop seeing APIs and the API infrastructure behind them as special snowflakes, and embrace standardization. We aren’t even talking about standardization of the API resources like messages, images, videos, payments, and other essential resources. I am just talking about the fundamental building blocks of putting those API resources to work in desktop, web, mobile, device, network, and artificial intelligence applications. Otherwise your low-code / no-code, AI driven goodness just will not work as intended—we gotta get more of the business and political bits standardized first.