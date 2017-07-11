---
published: true
layout: post
title: When You Publish A Google Sheet To The Web It Also Becomes An API
date: 2017-07-11T13:00:00.000Z
tags:
  - API Evangelist
  - Deployment
  - Spreadsheet
image: >-
  https://s3.amazonaws.com/kinlane-productions/google-sheets/google-sheets-icon.jpg
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/google-sheets/google-sheets-icon.jpg" align="right" width="30%" style="padding: 15px;" /></p>When you take any Google Sheet and choose to publish it to the web, you immediately get an API. Well, you get the HTML representation of the spreadsheet (shared with the web), and if you know the right way to ask, you also can get the JSON representation of the spreadsheet--which gives you an interface you can program against in any application.

Articles I curate, the companies, institutions, organizations, government agencies, and everything else I track on lives in Google Sheets that are published to the web in this way. When you are viewing any Google Sheet in your browser you are viewing it using a URL like:

https://docs.google.com/spreadsheets/d/[sheet_id]/edit

Of course, [sheet_id] is replaced with the actual id for your sheet, but the URL demonstrates what you will see. Once you publish your Google sheet to the web you are given a slight variation on that url:

https://docs.google.com/spreadsheets/d/[sheet_id]/pubhtml

This is the URL you will share with the public, allowing them to view the data you have in your spreadsheet in their browsers. In order to get at a JSON representation of the data you just need to learn the right way to craft the URL using the same sheet id:

https://spreadsheets.google.com/feeds/list/[sheet_id]/default/public/values?alt=json

Ok, one thing I have to come clean on is that the JSON available for each Google sheet is not the most intuitive JSON you will come across, but once you learn what is going on you can easily consume the data within a spreadsheet using any programming languages. Personally, I use a [JavaScript library called tabletop.js](https://github.com/jsoma/tabletop) that quickly helps you make sense of a spreadsheet and get to work using the data in any (JavaScript) application.

The fastest, lowest cost way to deploy an API is to put some data in a Google Sheet, and hit publish to the web. Ok, its not a full blown API, it's just JSON available at a public URL, but it does provide an interface you can program against when developing an application. I take all the data I have in spreadsheets and publish to Github as YAML, and then make static APIs available using that YAML in XML, CSV, JSON, Atom, or any other format that I need. Taking the load of Google, creating a cached version at any point in time that runs on Github, in a versioned repository that anyone can fork, or integrate into any workflow.
