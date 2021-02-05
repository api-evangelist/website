---
published: true
layout: post
title: SQL Statement Pass-Through Using Web APIs
date: 2017-11-30T13:00:00.000Z
tags:
  - API Evangelist
  - Design
  - Deployment
  - Database
image: >-
  https://s3.amazonaws.com/kinlane-productions/slashdb/slashdb-sql-pass-through-mode.png
---
_This is a sponsored post by my friends over at [SlashDB](https://www.slashdb.com/). The topic is chosen by me, but the work is funded by SlasDB, making sure I keep doing what I do here at API Evangelist. Thank you [SlashDB](https://www.slashdb.com/) for your support, and helping me educate my readers about what is going on in the API space._

<p><a href="https://www.slashdb.com/how-it-works/#sql-pass-thru"><img src="https://s3.amazonaws.com/kinlane-productions/slashdb/slashdb-sql-pass-through-mode.png" align="right" width="45%" style="padding: 15px;" /></a></p>I'm closely following the approach of GraphQL when it comes to making data resources more accessible by API consumers when developing applications. I think there is some serious value introduced when it comes empowering front-end developers with the ability to get exactly the data they need using a variety of querying structures. I enjoy studying up on different approaches to making different dimensions of a database to consumers and end-users, and found a pretty scrappy one from my friends over at SlashDB, with [their SQL statement pass through](https://www.slashdb.com/how-it-works/#sql-pass-thru). It's not the most formal approach to query a database, but I think it's scrappy and simple enough, that it might work for a wide variety of technical, as well as non-technical users.

Using the SlashDB mode, an administrator, or an application backend developer can define arbitrary SQL queries which once defined, can be executed as a smple URL. The example query they provide returns customers from London: http://demo.slashdb.com/query/customers-in-city/city/London.html. It is something that will make RESTafarians pull their hair (dreads?) out, but for business users looking to get their hands on some data to populate a spreadsheet, or share with a partner when developing an application--it will be a lifesaver. As the GraphQL folks like trumpet, REST isn't the only way to get things done, and while I think we should be thinking critical about the long term impact of our API design choices, getting business done efficiently is an important aspect of doing APIs as well.

What I like about the SlashDB approach is it makes for an intuitive URL. Something business users can understand. I could see crafting these in bulk, and some becoming permanent, while others maybe being more of a temporary thing. Depending on the application you may want to standardize how you publish your URLs, using common patterns, and making sure queries aren't changing, if they are being baked into applications. I think that simple URLs that retrieve data from a database will always trump a more complex, technical solution that developers often want. Developers are always going to want more robust solutions that they can tweak and play with, but business users just want what they need, and are looking for the quickest way to solve their business problem--SQL statement pass-through is this.

I've worked at companies that have an HTML Textarea on the dashboard of the internal portal where you can hand type SQL statements, or use from a pre-configured set of statements. Allowing business users to quickly query a database and dump to spreadsheet, CSV, and import into other applications. I can see SQL pass-through being a quick and dirty solution that reflects these other approaches I've seen in the past. I could see bookmarks, quick links, and other scrappy ways of using the web to query backend databases like this. When you couple this with some sort of API key or other identifier, you can also begin to develop an awareness of who is making these types of queries, and what types of applications they are putting them to use in. Taking SQL query pass-through to the next level and going beyond just API deployment, and moving into the realms of API management.
