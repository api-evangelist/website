---
published: true
layout: post
title: >-
  Thinking Deeply About Other People Using Your API Is The Most Valuable Lesson
  Of API Design
date: 2018-07-26T09:00:00.000Z
tags:
  - API Evangelist
  - Design
  - Politics of APIs
image: >-
  https://s3.amazonaws.com/kinlane-productions/federal-government/uspto/uspto-peds-api.png
---
I am deploying a patent review API for a client, using data from [the Patent Examination Data System (PEDS)](https://ped.uspto.gov/peds/). You can download complete JSON or XML data from the United States Patent Office (USPTO), and they even have an API. So, why would I be launching yet another API? Well, because what they have is so cryptic, complex, and lacking in any schema or API design, there is value in me pushing the API conversation forward a bit by thinking deeply about how other people will potentially be using these resources--something the USPTO clearly hasn't done.

The [USPTO PEDS API](https://ped.uspto.gov/api/swagger-ui.html) (that is more acronyms than you can shake a stick at) is a great example of how much database people, and developers take for granted as they operate within their little bubbles, without much concern for how the rest of the world views their work--take a look at the screenshot of thee USPTO PEDS API.

<p align="center"><img src="https://s3.amazonaws.com/kinlane-productions/federal-government/uspto/uspto-peds-api.png" align="center" width="90%" /></p>

There is only one telling sign on this page regarding what this API does--the email address for the contact, which has a uspto.gov address. Beyond that there is not a single sign of the resources available within this API, or the value they bring to the table. Even if you can extrapolate that this is a patent API, there is nothing to tell you that you can't actually get patent data from this, you can only get meta data about the patents, reviewers, inventors, and the activity around the patent. For me, the API reflects many of the challenges developers and database people face when it comes to thinking out of their box, and effectively communicating with external consumers--which is the whole reason we do web APIs.

I'm pretty well versed consuming patent data, and it took me several hours to get up to speed with this set of resources. I opted to not deal with the API, which is just an ElasticSearch index on top of a patent file store, and went directly to the full-size zipped up download. Something the average user will not have the knowledge, skills, and resources to always do. Which is why I feel there is value in me investing some schema and API design cycles into making the USPTO PEDS API a little more coherent, accessible, and usable by a wider audience using a simple web API. Moving it beyond the realm of wizards (database and developers), and making it something normal people, say patent attorneys, and other business folk can put to use in their work.

The USTPO PEDS API reflects the divide between tech and business people. Some database people and developers will think the implementation is a good one, because it gives them the full download, as well as a customizable, ElasticSearch interface for querying what you want. Many though, will walk away, because they aren't willing to make the several hour investment getting up to speed on the schema, so they can make their first API query, or load the full download into the database backend of their choosing. This is where an investment on API design begins to pay dividends, is reaching this wider audience of potential consumers who are unwilling to make the investment getting up to speed, or do not have the resources or knowledge to work with the full download or an ElasticSearch interface. Unless of course, your in the business of keeping data out of the hands of these people, which many folks are.

I am a 30 year database professional. I get databases and querying solutions. What many GraphQL and ElasticSearch believers get wrong when they rely on these solutions for delivering publicly available APIs, is that they are unwilling to come to terms with the fact they can't see their resources through the eyes of the public. They think everyone is like them, and thus want a full blown query interface to get at a known schema. They see API design as unnecessary work, when in reality, they are just unwilling to do the heavy lifting, and they are either consciously, or unconsciously passing that work off to each individual consumer. If you are keeping your APIs available for internal use amongst controlled group of developers this isn't a problem, but if you are making your APIs available to a wider public audience, it ends up showing that you haven't taken the time to think deeply about how others will be using your APIs, or that you just doo not care.
