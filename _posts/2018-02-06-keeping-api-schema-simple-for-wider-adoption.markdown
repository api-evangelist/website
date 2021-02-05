---
published: true
layout: post
title: Keeping API Schema Simple For Wider Adoption
date: 2018-02-06T09:00:00.000Z
tags:
  - API Evangelist
  - Definitions
  - Schema
  - Design
  - CSV
image: 'https://s3.amazonaws.com/kinlane-productions/bw-icons/bw-csv.png'
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/bw-icons/bw-csv.png" align="right" width="45%" style="padding: 15px;" /></p>One aspect of [my talk at APIDays Paris this last week](http://apievangelist.com/2018/02/03/api-is-not-just-rest/), included a slide about considering to allow API consumers to negotiate CSV responses from our API. Something that would probably NEVER occur to most API providers, and probably would make many even laugh at me. I'm used to it, and don't care. While not something that every API provider should be considering, depending on the data you are serving up, and who your target API consumer ares, it is something that might make sense. Allowing for the negotiation of CSV responses represents lowering the bar for API consumption, and widening the audience who can put our APIs to work.

I was doing more work around public data recently, and was introduced to an interesting look at some lessons from developing open data standards. I'm doing a deep dive into municipal data lately as part of my partnership with [Streamdata.io](http://apis.how/streamdata), and I found [the lessons they published interesting](http://www.opennorth.ca/2017/12/21/from-development-to-adoption-lessons-from-three-open-standards.html), and something that reflects my stance on API content negotiation.

> _From the development and maintenance of the API, it quickly became clear that adjusting scripts after every election (and by-election) and website modification, was quickly becoming unsustainable. To address this issue, a simple CSV schema was developed to encourage standardisation of this data from the outset. The schema was designed to be as simple and easy to understand and implement as possible. Comprised of just 21 fields, 7 of which are recommended fields, the schema does not have hierarchical relationships between terms and can be implemented in a single CSV file. By making the standard this simple, we were able to get a number of adopters onboard and outputting their lists of elected representatives on their own open data portals._

When it comes to APIs, simplicity rules. The simpler you can make your API, the more impact you will make. Allowing for the negotiation of CSV responses from your API when possible allows API consumers to go from API to a spreadsheet in just one or two clicks. This is huge when it comes to on boarding business users with the concepts of APIs, and what they do, and allows them to easily put valuable data resources to work in their native environment--the spreadsheet. This is something many API consumers won't understand, but when it comes to seeking meaningful API adoption, it is something that expand the reach of any API beyond the developer class, putting it within reach of business users.

I am a big fan of pushing our APIs to allow for the negotiation of CSV. XML, and JSON by default, whenever possible. I'm also a fan of delivering richer experiences by allowing for the negotiation of hypermedia media types. While delivering hypermedia takes a significant amount of thought and investment, allowing for the negotiation of CSV, XML, and JSON doesn't take a lot of work. When delivering your APIs, I highly recommend thinking about who your API consumers are, and whether offering CSV responses might shift the landscape even a little bit, making your valuable data resources a little more usable by business users who won't necessarily be delivering web or mobile applications.
