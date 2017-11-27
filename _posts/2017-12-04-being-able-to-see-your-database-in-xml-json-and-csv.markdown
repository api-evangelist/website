---
published: true
layout: post
title: 'Being Able To See Your Database In XML, JSON, and CSV'
date: 2017-12-04T09:00:00.000Z
tags:
  - API Evangelist
  - Database
  - Definitions
  - Data
image: >-
  https://s3.amazonaws.com/kinlane-productions/slashdb/slashdb-content-negotiation.png
---
<p><a href="https://www.slashdb.com/documentation/api-documentation/"><img src="https://s3.amazonaws.com/kinlane-productions/slashdb/slashdb-content-negotiation.png" align="right" width="45%" style="padding: 15px;" /></a></p>
_This is a sponsored post by my friends over at [SlashDB](https://www.slashdb.com/). The topic is chosen by me, but the work is funded by SlasDB, making sure I keep doing what I do here at API Evangelist. Thank you [SlashDB](https://www.slashdb.com/) for your support, and helping me educate my readers about what is going on in the API space._

I remember making the migration from XML to JSON. It was hard for me to understand that difference between the formats, and that you accomplish pretty much the same things in JSON that you could in XML. I've been seeing similarities in my migration to YAML from JSON. The parallels in each of these formats isn't 100%, but this story is more about our perception of data formats, than it is about the technical details. CSV has long been a tool in my toolbox, but it was until this recent migration from JSON to YAML that I really started seeing the importance of CSV when it comes to helping onboard business users with the API possibilities.

In my experience API design plays a significant role in helping us understand our data. Half of this equation is understanding our schema, and what the dimensions, field names, and data types of the data we are moving around using APIs. As I was working through some stories on how my friends over at SlashDB are turning databases into APIs, I saw that they were translating database, tables, and field names into API design, and that [they also help you handle content negotiation between JSON, XML, CSV](https://www.slashdb.com/documentation/api-documentation/). Which I interpret as an excellent opportunity for learning more about the data we have in our databases, and getting to know the design aspects of the data schema.

In an earlier post about what SlashDB does I mentioned that many API designers cringe at translating database directly into a web API. While I agree that people should be investing into API design to get to know their data resources, the more time I spend with SlashDB's approach to deploying APIs from a variety of databases, the more I see the potential for teaching API design skills along the way. I know many API developers who understand API design, but do not understand content negotiation between XML, JSON, and CSV. I see an opportunity for helping publish web APIs from a database, while having a conversation about what the API design should be, and also getting to know the underlying schema, then being able to actively negotiate between the different formats--all using an existing service.

While I want everyone to be as advanced as they possibly can with their API implementations, I also understand the reality on the ground at many organizations. I'm looking for any possible way to just get people doing APIs, and begin their journey, and I am not going to be to heavy handed when it comes to people being up to speed on modern API design concepts. The API journey is the perfect way to learn, and going from database to API, and kicking of the journey is more important than expecting everyone to be skilled from day one. This is why I'm partnering with companies like SlashDB, to help highlight tools that can help organizations take their existing legacy databases and translate them into web APIs, even if those APIs are just auto-translations of their database schema.

Being able to see your database as XML, JSON, and CSV is an important API literacy exercise for companies, organizations, institutions, and government agencies who are looking to make their data resources available to partners using the web. It is another important step in understanding what we have, and the naming and dimensions of what we are making available. I think the XML to JSON holds one particular set of lessons, but then CSV possesses a set of lessons all its own, helping keep the bar low for the average business user when it comes to making data available over the web. I'm feeling like there are a number of important lessons for companies looking to make their databases available via web APIs over at SlashDB, with automated XML, JSON, and CSV translation being just a notable one.
