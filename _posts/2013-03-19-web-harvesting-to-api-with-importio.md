---
layout: post
title: "Web Harvesting to API with Import.io"
url: 'http://apievangelist.com/2013/03/19/web-harvesting-to-api-with-import.io/'
image: 'http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/blog/import-io-logo.png'
---

[<img class="c1" src="https://s3.amazonaws.com/kinlane-productions/api-evangelist/import-io/import-io-logo.png" alt="" align="right" />][1]

I had a demo of a new [data extraction service][2] today called [Import.io][1]. The service allows you to harvest or scrape data from websites and then output in machine readable formats like JSON. This is very similar to Needlebase, a popular scraping tool that was acquired and then shut down by Google early in 2012. Except I’d say Import.io represents a simpler, yet at the same time a more sophisticated approach to harvesting of web data and publishing than Needlebase.

**Extract**
Using Import.io you can target web pages, where the content resides that you wish to harvest, define the rows of data, label and associate them with columns in table you where the system will ultimately put your data, then extract the data complete with querying, filtering, pagination and other aspects of browsing the web you will need to get at all the data you desire.

**Connect**
After defining the data that will be extracted, and how it will be store you can stop and use the data as is, or you can setup a more ongoing, real-time connection with the data you are harvesting. Using Import.io connectors you pull the data regularly, identify when it changes, merge from multiple sources and remix data as needed.

**Put The Data To Work**
Using Import.io you can immediately extract the data you need and get to work, or establish an ongoing connection with your sources of data and use via the Import.io web app or you can manage and access via the [Import.io API][3]\--giving you full control over your web harvesting connections, and the resulting data.

[<img class="c1" src="https://s3.amazonaws.com/kinlane-productions/api-evangelist/import-io/import-io-connectors.png" alt="" width="300" align="right" />][1]

When getting to work using Import.io, you have the option to build your own connectors or explore a marketplace of existing data connectors, tailored to pull from some common sources like the Guardian or ESPN. The Import.io marketplace of connectors is a huge opportunity for data consumers as well as data scraping junkies (like me) to put their talents to use building unique and desireable data harvesting scripts.

I’ve written about database to API services like [EmergentOne][4] and [SlashDB][5], I would put Import.io into the Harvest to API or ScrAPI category--allowing you to deploy APIs and machine readable datasets from any publicly available data, even if you aren’t a programmer.

I think ScrAPI services and tools will play an important role in the API economy. While data will almost always originate from a database, often times you can’t navigate existing IT bottlenecks to properly connect and deploy an API from that data source. Sometimes problem owners will have to circumvent existing IT infrastructure and harvest where the data is published on the open web.  Taking it upon themselves to generate the necessary API or machine readable formats that will be needed for the last mile of mobile and big data apps that will ultimately consume and depend on this data.

   [1]: http://import.io (Import.io)
   [2]: http://import.io
   [3]: http://docs.import.io/
   [4]: /2013/03/01/mysql,-postgresql,-rds-to-api-with-emergent-one/ (database to api with EmergentOne)
   [5]: http://apievangelist.com/2013/03/18/database-to-api-with-slashdb/ (database to api with slashdb)
