---
title: My Google Sheet Driven Product API And Web Page
date: 2017-05-18 15:00:00 Z
tags:
- Products
- Deployment
- Google Sheets
- Github
- Jekyll
image: http://apievangelist.com/images/product-square.png
---

<p><img src="http://apievangelist.com/images/product-square.png" align="right" width="35%" /></p>I am in the process of eliminating the MySQL backend behind much of my research, eliminating a business expense, as well as an unnecessary complexity in my architecture. There really is no reason for the data I use in my business to be in a database. Nothing I track on tends to go beyond 10K rows, with most of the tables actually being less than 100 rows--perfect for spreadsheets, and my new static approach to delivering APIs, and websites for my research.

The time had come to update some of the products on my website, and I thought my product page was a perfect candidate for this approach, providing me with the following elements:

**[Products Google Sheet](https://docs.google.com/spreadsheets/d/1K5GTYo3McA4WNYcvv_WPRKxp5Q8emkyKlaXKATGhQFM/pubhtml)** - I have a simple spreadsheet with all of my products in it.
**[Jekyll YAML Data Stor](https://github.com/kinlane/api-evangelist/blob/gh-pages/_data/products/index.yaml)e** - I have a YAML data store in the _data folder for API Evangelist.
**Google Sheet to YAML Sync** - I have a JavaScript function that pulls the data from the Google Sheet, converts it to YAML, and writes to the _data folder in the Jekyll repository.
**[Products Web Page](http://apievangelist.com/products/)** - I have a page that lists all the products in the YAML file as HTML using Liquid.
**[Products API](http://apievangelist.com/apis/products/)** - I have a JSON page that lists all the products in the YAML file as JSON using Liquid.

This simple approach to publishing static APIs using Google Sheets and Github is working well for little data like this--I am all about the little data, while everyone else is excited about big data. ;-) I even have the beginning of some [documentation](http://apievangelist.com/documentation/) and an updated [APIs.json](http://apievangelist.com/apis.json) for my website.

Next, I'll work through the rest of my projects, organizations, tools, and other data I track on as part of my API research. I'll be publishing a complete snapshot of this data at API Evangelist, as well as subsets of it at each of the individual research projects. When I'm done I'll have a nice static stack of APIs for all of my research, easily managed via Google Sheets, and YAML on Github. 