---
published: true
layout: post
title: The Patent Application Information Retrieval Bulk Data API
date: 2017-08-17T13:00:00.000Z
tags:
  - API Evangelist
  - Patents
  - Federal Government
image: >-
  https://s3.amazonaws.com/kinlane-productions/uspto/uspto-pair-bulk-data-api.png
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/uspto/uspto-pair-bulk-data-api.png" align="right" width="40%" style="padding: 15px;" /></p>I stumbled across [the Patent Application Information Retrieval Bulk Data API](https://pairbulkdata.uspto.gov/) from the US Patent Office the other day. It provides a much more usable approach to getting at patent information than what I am using at the moment. Right now I am downloading XML files and searching for the occurrence of a handful of keywords. If I want to make a change I have to fire up a new AWS instance, change the code, and reprocess the downloaded files. The Patent Application Information Retrieval Bulk Data API gives me a much more efficient interface to work with.

The Patent Application Information Retrieval Bulk Data API contains the bibliographic, published document and patent term extension data tabs in Public PAIR from 1981 to present, with some additional data dating back to 1931. It has leveraged COTS semantics, maintains an open architecture, and the query syntax follows the standard Apache Solr search syntax, with API responses following the Solr formats. Providing for a much more powerful interface for querying patent data, which goes back further back in time then what I've been doing currently. I'm really interested in doing an API patent search for the 1990s, or maybe even earlier.

The Patent Application Information Retrieval Bulk Data API is a well designed API, [with an attractive API portal and documentation](https://pairbulkdata.uspto.gov/swagger/index.html), driven with an OpenAPI. The USPTO provide access to the patent data in the way that I think all government agencies should be doing it. You can use the API, or get at a JSON or XML download of the data. The API is "part of the US Patent and Trademark Office's (USPTO) commitment to fostering a culture of open government as described by the 2013 Executive Order to make open and machine-readable data the new default for government information." Which is pretty cool in my book, something we desperately are needing to become a reality across all federal agencies in 2017.
