---
published: true
layout: post
title: The National Transit Database (NTD) Needs To Be An API
date: 2018-01-02T09:00:00.000Z
tags:
  - API Evangelist
  - Transit
  - Federal Government
image: >-
  https://s3.amazonaws.com/kinlane-productions/government/federal-transit-agency/the-national-transit-database.png
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/government/federal-transit-agency/the-national-transit-database.png" align="right" width="45%" style="padding: 15px;" /></p>I've been looking for sources of transit data as part of some research I'm doing with Streamdata.io. Like most industries I study as part of my API research, it is a mess. There is no single source of truth, lack of robust open source solutions, government PDFs acting as databases, and tech companies extracting as much value as they can, and giving as little in return as they possibly can. Todays frustration centers around the unfortunately common federal government PDF database, or more specifically, [the National Transit Database (NTD)](https://www.transit.dot.gov/ntd).

In 2017, when you publish something to the web as a "database", it should be machine readable. There is some valuable data in the agency profile reports for the 800+ transit agencies available in the database, but this information is locked up in PDFs. You can find machine readable, historic versions of this data up to 2015 in data.gov, but for 2016, and 2017, the data is only available in individual PDFs for each agency profile. To make things more difficult, the listing of transit agencies uses some Ajax voodoo for its pagination and detail pages, making it even harder to scrape, on top of rendering each agencies detail useless by storing it as a PDF.

I understand why government is stuck in this mode. The systems they use only provide them with PDF as a their primary output. Staff hasn't been trained on the importance of making data available in machine readable formats. People just don't understand the negative impact they are making on the life of their data, and how it restricts people putting it to work. In some cases, people are fully aware of this, and want to limit how the data gets used, interpreted, keeping them as the definitive source of truth. I'm not saying this is what the Federal Transit Agency (FTA) is up to, but I'm saying it is the effect of their actions, which is having a chilling effect on folks like me using the valuable data to help communities served by these transit agencies.

I emailed the FTA asking if they have a machine readable copy of the database. This information should be published by default as CSV to the agencies Github account. I'm sure the data is available in a spreadsheet somewhere, before it becomes a PDF. It wouldn't be very hard to save this data as CSV and publish to Github, which could then be easily converted into JSON, or other machine readable formats. I'm happy with CSV. I'm just not happy with PDF being called a database. Database implies that I can put the data to work, and in its current format the National Transit Database (NTD) is't usable as data--hence not a database. It is just too much work to get out of the PDFs and make usable again, forcing me to step away from my project to understand how communities are investing in transit--I am hoping I can find the data some other place.
