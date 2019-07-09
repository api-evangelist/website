---
published: true
layout: post
title: Challenges When Aggregating Data Published Across Many Years
date: 2017-07-12T16:00:00.000Z
tags:
  - API Evangelist
  - Aggregation
  - Data
  - Scraping
  - Deployment
image: >-
  https://s3.amazonaws.com/kinlane-productions/hack-education/ed-tech-investment-research.png
---
<p><a href="http://funding.hackeducation.com/"><img src="https://s3.amazonaws.com/kinlane-productions/hack-education/ed-tech-investment-research.png" align="right" width="40%" style="padding: 15px;" /></a></p>[My partner in crime is working on a large data aggregation project regarding ed-tech funding](http://funding.hackeducation.com/). She is publishing data to Google Sheets, and I'm helping her develop Jekyll templates she can fork and expand using Github when it comes to publishing and telling stories around this data across her network of sites. Like API Evangelist, [Hack Education runs as a network of Github repositories](https://github.com/hackeducation/), with a common template across them--we call the overlap between API Evangelist, [Contrafabulists](http://contrafabulists.com/).

One of the smaller projects she is working on as part of her ed-tech funding research involves pulling the grants made by the Gates Foundation since the 1990s. Similar to my story a couple weeks ago about my friend David Kernohan, [where he was wanting to pull data from multiple sources](https://apievangelist.com/2017/06/28/i-have-two-interesting-apis-and-i-am-not-a-developer-what-do-i-do/), and aggregate into a single, workable project. Audrey is looking to pull data from a single source, but because the data spans almost 20 years--it ends up being a lot like aggregating data from across multiple sources.

A couple of the challenges she is facing trying to gather the data, and aggregate as a common dataset are:

- **PDF** - The enemy of any open data advocate is the PDF, and a portion of her research data data is only available in PDF format which translates into a good deal of manual work.
- **Search** - Other portions of the data is available via the web, but obfuscated behind search forms requiring many different searches to occur, with paginated results to navigate.
- **Scraping** - The lack of APIs, CSV, XML, and other machine readable results raises the bar when it comes to aggregating and normalizing data across many years, making scraping a consideration, but because of PDFs, and obfuscated HTML pages behind a search, even scraping will have a significant costs.
- **Format** - Even once you've aggregated data from across the many sources, there is a challenge with it being in different formats. Some years are broken down by topic, while others are geographically based. All of this requires a significant amount of overhead to normalize and bring into focus.
- **Manual** - Ultimately Audrey has a lot of work ahead of her, manually pulling PDFs and performing searches, then copying and pasting data locally. Then she'll have to roll up her sleeves to normalize all the data she has aggregated into a single, coherent vision of where the foundation has put its money.

Data research takes time, and is tedious, mind numbing work. I encounter many projects like hers where I have to make a decision between scraping or manually aggregating and normalizing data--each project will have it's own pros and cons. I wish I could help, but it sounds like it will end up being a significant amount of manual labor to establish a coherent set of data in Google Sheets. Once, she is done though, she has all the tools in place to publish as YAML to Github, and get to work telling stories around the data across her work using Jekyll and Liquid. I'm also helping her make sure she has a JSON representation of each of her data projects, allowing others to build on top of her hard work.

I wish all companies, organizations, institutions, and agencies would think about how they publish their data publicly. It's easy to think that data stewards will have ill intentions when it comes to publishing data in a variety of formats like they do, but more likely it is just a change of stewardship when it comes to managing and publishing the data. Different folks will have different visions of what sharing data on the web needs to look like, and have different tools available to them, and without a clear strategy you'll end up with a mosaic of published data over the years. Which is why I'm telling her story. I am hoping to possibly influence one or two data stewards, or would-be data stewards when it comes to the importance of pausing for a moment and thinking through your strategy for standardizing how you store and publish your data online.
