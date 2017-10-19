---
published: true
layout: post
title: Using APIs To Enrich The Data You Have In Spreadsheets
date: 2017-10-19T11:00:00.000Z
tags:
  - API Evangelist
  - Spreadsheets
  - Data
  - CSV
  - Integration
image: >-
  https://s3.amazonaws.com/kinlane-productions/blockspring/blockspring-bulk-connectors.png
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/blockspring/blockspring-bulk-connectors.png" align="right" width="40%" style="padding: 15px;" /></p>As my friend John Sheehan over at [Runscope](http://apis.how/8nlsropidv) says, "the spreadsheet is the most underrated API client". The spreadsheet is where a significant amount of business gets done each day in the business world, so it make sense that we should be integrating APIs at this level whenever we possibly can. The best tool for doing this today is with [Blockspring](https://www.blockspring.com/), which provides non-developers (and developers) with the tools they need to integrate APIs into spreadsheets, either Microsoft Excel or Google Sheets--putting the power of APIs directly into the hands of average business folk.

Blockspring has over 100 APIs available for integration into your spreadsheets, but I wanted to highlight their recent release of [bulk connectors](https://open.blockspring.com/browse), which currently [provides 10 separate data enrichment features from a handful of API providers](https://open.blockspring.com/browse):

- **Bing** - Company Domain Lookups
- **Bing** - Search Query Lookups
- **FullContact** - Email Lookups
- **FullContact** - Company Lookups
- **FullContact** - Twitter Lookups
- **FullContact** - Phone Lookups
- **Mailgun** - Validate Emails
- **Clarifai** - Deep Learning Image Tagging
- **Google** - Shorten URLs
- **Google** - Expand URLs

These bulk connectors are meant to help you work with bulk data you have stored in spreadsheets and CSV files by enriching your data using these valuable API services. These connectors are all features I've custom developed as part of my internal systems, to help me monitor the world of APIs. They are simple, useful data management features, but instead of having to custom integrate with each API as I had to, anyone can use Blockspring to deliver these features within their own spreadsheets. Making the spreadsheet act as an API client, but for any average business user, not just for developers who are API savvy, and have the skills to deliver custom integration.

I'm a big advocate of companies publishing APIs. I also do a lot of pushing for API providers to make sure [their APIs are available to non-developers using Zapier](http://apievangelist.com/2017/09/25/embeddable-api-integrations-for-non-developers-with-zapier/). I consider Blockspring to be on this list of essential API services you should be working with as an API provider. This approach to consuming APIs will increasingly be how business gets done. As much as many of us developers would love for spreadsheets to go away, they ain't going anywhere. Most normal folk in the world of business live and breathe within their spreadsheets, and if we want to deliver our API services to them, it will have to be through brokers like Blockspring. Just pause for a moment and think about the potential for delivering machine learning models via APIs within the spreadsheet like this, and you'll begin to realize what an underserved aspect of API consumption spreadsheets are.
