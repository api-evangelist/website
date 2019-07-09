---
published: true
layout: post
title: "Keeping Things One Dimensional To Go From API To Spreadsheet In One Step"
date: 2017-09-06T09:00:00.000Z
tags:
  - API Evangelist
  - Spreadsheets
  - Design
  - HSDA
image: >-
  https://s3.amazonaws.com/kinlane-productions/bw-icons/bw-api-to-spreadsheet.png
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/bw-icons/bw-api-to-spreadsheet.png" align="right" width="40%" style="padding: 15px;" /></p>I have been working on the next version of [my human services work](http://org.open.referral.adopta.agency/), which provides a way for cities to make information about organizations, locations, and services available on the web. Part of the feedback from the community around what was missing from the last version, was the number of API calls you needed to make to get a complete representation of a resource, and its sub-resources, as each API response was one dimensional. An example would be that you could get a list of locations, but to get at the list of services you had to make a separate API call. This wasn't a lapse in API design, it was a result of the schema being born out of a CSV format, and me working to stay true to the original design, and usage of the schema.

In the latest version, I did release a handful of paths that provide a complete representation of each resource and it's sub-resources. However, I have maintained the original one dimension representation of each resource and sub-resources, allowing me to offer an XML, JSON, as well as CSV representation for each API call. This allows API consumers to pull CSV lists of organizations, locations, services, and their sub-resources like address and phone lists. While not something that would be useful in all API implementations, I feel like the audience for municipal level human services data will benefit significantly being able to go from API to spreadsheet in a single step. All the GET paths for organizations, locations, and services are publicly available by default, not requiring authentication, making CSV data available via a single URL--something anyone can make happen.

While weighing API design decisions as part of my Human Services Data API (HSDA) work I am having to consider not just the technical of how I should be doing this. I am also deeply considering how the API will be put to use, and who will be doing that. While I am thinking about the heavy system to system integration needs of human service providers, as well as the web, mobile, and other applications. I am also thinking about the individual user who might just need a list of the names of organizations, or the addresses of services in a simple CSV format, so that they can work with the data in their most familiar format--the spreadsheet. I am just focusing on the API side of things at the moment, but once I'm done with the latest version I am going to think about some simple linking, and embeddable tooling that allows users to put CSV data from the API to work in a single click using Google Sheets, and Microsoft Excel.
