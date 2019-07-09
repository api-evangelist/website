---
published: true
layout: post
title: The API Portal Outline For A Project I Am Working On
date: 2017-10-24T13:00:00.000Z
tags:
  - API Evangelist
  - Portal
  - Management
image: 'https://s3.amazonaws.com/kinlane-productions/portal/api-portal-forkable.png'
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/portal/api-portal-forkable.png" align="right" width="45%" style="padding: 15px;" /></p>I am working through a project for a client, helping them deliver a portal for their API. As I do with any of my recommendations with my clients, I take my existing API research, and refine it to help craft a strategy to meets their specific needs. Each time I do this it gives me a chance to rethink some of my recommendations I've already gathered, as well as learn from new types of projects. I've taken the building blocks from my [API portal](http://portal.apievangelist.com), as well as my [API management](http://portal.apievangelist.com) research, and have taken a crack at organizing them into an outline that I can use to guide my current project.

Here is a walk through of the outline I'm recommending as part of a basic API portal implementation, to support a simple public API:

- **Overview** - / - Everything starts with a landing page, with a simple overview of what an API does.

Then you need some basics to help make on-boarding as frictionless as possible, providing everything an API consumer needs to get going:

- **Getting Started** - /getting-started/ - Handful of steps with exactly what is needed to get started.
- **Authentication** - /authentication/ - An overview of what type of authentication is used.
- **Documentation** - /documentation/ - Documentation for the APIs that are available.
- **FAQ** - /faq/ - Answer the most common questions.
- **Code** - /code/ - Provide code samples, libraries, and SDKs to get going.

Then get API consumers signed up, or able to login and get at their API keys as quickly as you possibly can:

- **Sign Up** - /developer/ - Provide a simple sign up for a developer account.
- **Login** - /developer/ - Allow users to quickly log back in after they have account.

Next, provide a wealth of communication and support mechanisms, helping make sure developers are aware of what is going on:

- **Blog** - /blog/ - A simple blog dedicated to sharing stories about the API.
- **Support** - /support/ - Offer up a handful of support channels like email and tickets.
- **Road Map** - /road-map/ - Provide a road map of what the future will hold for the API.
- **Issues** - /issues/ - Share what the known issues are for the API platform.
- **Change Log** - /change-log/ - Publish a log of everything that has changed with the platform.
- **Status** - /status/ - Provide a status page showing the availability of API services.
- **Security** - /security/ - Publish an overview of what security practices are in place.

Make sure your consumers know how to get involved at the right level, making plans, pricing, and partnership opportunities easy to find:

- **Plans** - /plans/ - Offer a single page with API access plans and pricing information.
- **Partners** - /partners/ - Share what the partnership opportunities are, as well as existing partners.

Then let's take care of the legal side of things, making sure API consumers are fully aware of the TOS, and other aspects of operations:

- **Terms of Service** - /terms-of-service/ - Make the terms of service easy to find.
- **Privacy** - /Privacy/ - Publish a privacy statement for all API consumers.
- **Licensing** - /Licensing/ - Share the licensing for API, code, data, and other assets.

I also wanted to make sure I took care of the basics for the developer accounts, flushing out the common building blocks developers will need to be successful:

- **Dashboard** - /developer/dashboard/ - Provide a simple, comprehensive dashboard for developers.
- **Account** - /developer/account/ - Allow API consumers to change their account information.
- **Applications** - /developer/applications/ - Allow API consumers to add multiple applications, and receive API keys for each application.
- **Plans** - /developer/plans/ - If there are multiple plans, allow developers to change plans.
- **Usage** - /developer/usage/ - Show history of all API usage for API consumers.
- **Billing** - /developer/billing/ - Allow API consumers to add, update, and remove billing information.
- **Invoices** - /developer/invoices/ - Share a listing, as well as detail of all invoices for use.

Then I had a handful of other looser items that I wanted to make sure were here. Some of these will be for the second phase of developoment, but I want to make sure is on the list:

- **Branding** - /branding/ - Providing a logo, branding guidelines, and requirements.
- **Embeddable** - /embeddable/ - Share a handful of butts and widgets for use by consumers.
- **Webhooks** - /Webhooks/ - Publish details on how to setup and manage webhook notifications.
- **iPaaS** - /ipaas/ - Information on Zapier, and other iPaaS integration solutions that are available.
- **Spreadsheets** - /spreadsheets/ - Share any spreadsheet plugins or connectors that are available for integration.

That concludes what I'd consider to be the essential building blocks for an API. Sure, there are some more minor APIs that can operate on a bare bones version of this list, but for any API looking to conduct business at scale, I'd recommend considering everything on this list. It reflects what I find across the leading providers like Stripe and Twilio, and reflect what I like to see from an API provider when I am getting up and running using any API.

I have Jekyll templates for each of these building blocks, which use the Bootstrap UI for the layout. I am updating it for this project, then I will publish again as a set of forkable tools that anyone can implement. I'm going to publish a new API portal that runs as an interactive outline of essential building blocks, then creates new Github repository for a user, and publishes each of the selected components to the repo. Providing a buffet of API developer portal tools anyone can put to work for their API without much work.
