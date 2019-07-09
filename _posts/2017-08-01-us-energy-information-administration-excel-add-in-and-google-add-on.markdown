---
published: true
layout: post
title: U.S. Energy Information Administration Excel Add-In and Google Add-On
date: 2017-08-01T13:00:00.000Z
tags:
  - API Evangelist
  - Spreadsheets
  - Federal Government
  - Energy
  - Financial
image: >-
  https://s3.amazonaws.com/kinlane-productions/federal-government/eia/eia-spreadsheet-add-ons.png
---
<p><a href="https://www.eia.gov/opendata/excel/"><img src="https://s3.amazonaws.com/kinlane-productions/federal-government/eia/eia-spreadsheet-add-ons.png" align="right" width="35%" style="padding: 15px;" /></a></p>I was looking through a number of federal government API implementations last week in preparation of a talk I did in Washington DC. The result of research like this is always a notebook full of interesting stories to tell about what federal agencies are up to with APIs. Today's story is out of the U.S. Energy Information Administration (EIA), with [their Excel Data Add-In and Google Add-On tooling](https://www.eia.gov/opendata/excel/) which allows you to download energy data from [EIA’s data API](https://www.eia.gov/opendata/) and economic data from [the St. Louis Federal Reserve’s Economic Data (FRED) API](http://research.stlouisfed.org/fred2/) directly into your spreadsheet(s).

I'm regularly looking out for innovative uses of spreadsheets when it comes to deploying, as well as consuming APIs, because I believe it is the best way we have to turn average business users into API consumers, by piping in data into the environment they are already using each day. EIA's data API contains 1.6 million energy series, and the St. Louis Federal Reserve's API contains 240,000 economic series. Making valuable federal agency maintained data available within spreadsheets like this using APIs is something ALL other agencies should be emulating. First, agencies need to be doing public APIs, then they need to make sure they are also investing in spreadsheet tooling like the EIA is.

I'm adding this example of using Microsoft Excel and Google Sheets as an API client for not just federal government, but also for such valuable commerce and energy data, to [my APIs and spreadsheets research](http://spreadsheets.apievangelist.com/). I'm also going to be on the hunt for open source solutions for delivering spreadsheet API connectivity like this. There should be a wealth of open source tooling that federal agencies can put to work when it comes to delivering data to spreadsheets, both internally, and externally with private sector partners. In a time where it is easy to get pretty depressed on a daily basis about APIs in the federal government, it makes me happy to find shining examples of APIs being put to work in such meaningful, and useful ways.
