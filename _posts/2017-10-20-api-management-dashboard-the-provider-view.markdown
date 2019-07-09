---
published: true
layout: post
title: 'API Management Dashboard: The Provider View'
date: 2017-10-20T15:00:00.000Z
tags:
  - API Evangelist
  - Management
image: >-
  https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories/cargo-ship-on-sea_atari_missle.jpg
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories/cargo-ship-on-sea_atari_missle.jpg" align="right" width="45%" style="padding: 15px;" /></p>I'm helping some clients think through their approach to API management. These projects have different needs, as well as different resources available to them, so I'm looking to distill things down to the essential components needed to get the job done. I've taken a look at the API consumer account basics as well as their usage, and next I want to consider the view of all of this from the API provider vantage point. For both of my current projects, I'm needing to think about the UI elements that deliver on API management elements from the API provider perspective.

To help me think though the UI elements needed for helping manage the essential elements of managing APIs I wanted to create a simple list of each screen that will be needed to get the job done. So far, I have the following X UI elements as part of my API management base:

- **Creation** - The landing page for account creation. Ideally, these are using OpenID / OAuth for major providers, eliminating the need for passwords.
- **Login** - The page for logging back in after a user has registered. Ideally, these are using OpenID / OAuth for major providers, eliminating the need for passwords.
- **Dashboard** - The landing page once an API provider is logged in -- providing access to all aspects of API management.
- **APIs** - A list of APIs, with detail pages for managing each individual API definition.
- **Plans** - A list of API plans, with detail pages for managing each individual API plan definition.
- **Accounts** - A list of API consumer accounts, with detail pages for managing each individual API consumer.
- **Usage** -  - A list of API calls from logs, with tools for breaking down by API, plan, or consumer.
- **Invoices** - A list of all invoices that have been generated for a specific time period, across specific consumers. With a detail page for seeing individual invoice details.

There may be more of these added to my current projects. Things like forgot password, and other aspects, but this gives me this visibility into the API consumer account, and usage aspects of the API management I'm trying deliver. These are the basic features any API management provider delivers, and represent the default areas of control an API provider should have over API consumption. It doesn't have to be pretty, and have all the bells and whistles, but it should give enough to help API providers understand what is going on in real-time, and over a variety of time periods. 

My clients I refer to 3Scale, Tyk, Restlet and the other API management services that are available won't have to reinvent the wheel here. It is my clients who are using AWS API Gateway, and developing seamless custom integrations I'm having to specify things at this level. My advice is to make use of existing providers whenever you can, but for this round of projects I'm putting AWS API Gateway to work, so I'm going to need to do a little more custom work on the API management front. When I come out of this I should have a suite of API definitions that can be imported into the AWS API Gateway, as well as some Jekyll page templates for delivering the UI functionality listed above. Augmenting the AWS API Gateway with essential API management features that should be present within any API operations.
