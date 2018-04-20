---
published: true
layout: post
title: Delivering Large API Responses As Efficiently As Possible
date: 2018-04-20T09:00:00.000Z
tags:
  - API Evangelist
  - Real Time
  - Performance
  - Hypermedia
  - Definitions
  - Design
  - HTTP/2
image: >-
  https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories/carryload_dali_three.jpg
---
<p><img src="{{ page.image }}" width="45%" align="right" style="padding: 15px;" /></p>I'm participating in a meeting today where one of the agenda items will be discussing the different ways in which the team can deal with increasingly large API responses. I don't feel there is a perfect response to this question, and the answer should depend on a variety of considerations, but I wanted to think through some of the possibilities, and make sure the answers were on the tip of my tongue. It helps to exercise these things regularly in my storytelling so when I need to recall them, they are just beneath the surface, ready to bring forward.

**Reduce Size Pagination**<br />
I'd say the most common approach to send over large amounts of data is to break things down into smaller chunks, based upon rows being sent over, and paginate the responses. Sending over a default amount (ie. 10,25,100), and require consumers either ask for larger amount, as well as request each additional page of results in a separate API request. Providing consumers with a running count of how many pages, what the current page is, and the ability to paginate forward and backward through the pages with each request. It is common to send pagination parameters through the query parameters, but some providers prefer handle it through headers (ie. Github).

**Organizing Using Hypermedia**<br />
Another approach, which usually augments and extends pagination is using common hypermedia formats for messaging. To paginate results, many API providers use hypermedia media types as a message format, because the media types allow for easy linking to paginate results, as well as providing the relevant parameters in the body of the response. Additionally, hypermedia would further allow you to intelligently break down large responses into different collections, beyond just simple pagination. Then use the linking that is native to hypermedia to provide meaningful links with relations to the different collections of potential responses. Allowing API consumers to obtain all, or just the portions of information they are looking for.

**Exactly What They Need With Schema Filtering**<br />
Another way to break things down, while putting the control into the API consumers hands, is to allow for schema filtering. Providing parameters and other ways for API consumers to dictate which fields they would like to return with each API response. Reducing or expanding the schema that gets returned based upon which fields are selected by the consumer. There are simpler examples of doing this with a fields parameter, all the way to more holistic approaches using query languages like GraphQL that let you provide a schema of which response you want returned via the URL or the parameter of each API request. Providing a very consumer-centric approach to ensuring only what is needed is transmitted via each API call.

**Defining Specific Responses Using The Prefer Header**<br />
Another lesson known approach is to use the Prefer Header to allow API consumers to request which representation of a resource they would prefer, based upon some pre-determined definitions. Each API request would pass in a value for the Prefer Header, providing definitions like simple, complete, or other variation of response defined by the API provider. Keeping API responses based upon known schema and scopes defined by the API provider, but still allowing API consumers to select from the type of response they would like to receive. Balancing the scope of API responses between both the needs of API providers, and API consumers.

**Using Caching To Make Response More Efficient**<br />
Beyond breaking up API calls into different types of responses, we can start focusing on the performance of the API, and making sure HTTP caching is used. Keeping API responses as standardized as possible while leveraging CDN, web server, and HTTP to ensure that each response is being cached as much as it makes sense. Ensuring that an API provider is thinking about, measuring, and responding to how frequent or infrequent data and content is changing. Helping make each API response as fast as it possibly can by leverage the web as a transport.

**More Efficiency Through Compression**<br />
Beyond caching, HTTP Compression can be used to further reduce the surface area of API responses. DEFLATE and GZIP are the two most common approaches to compression, helping make sure API responses are as efficient as they possibly can. Compressing each API call to make sure only the least amount of bytes are transmitted across the wire.

**Breaking Things Down With Chunked Responses**<br />
Moving beyond breaking things down, and efficiency approaches using the web, we can start looking at different HTTP standards for making the transport of API responses more efficient. Chunked transfers are one way to send API responses in not just a single API response, but break it down into an appropriate number of chunks, and send them in order. API consumers can make a request and receive large volumes of data in separate chunks that are reassembled on the client side. Leveraging HTTP to make sure large amounts of data is able to be received in smaller, more efficient API calls.

**Switch To Providing More Streaming Responses**<br />
Beyond chunk responses, streaming using HTTP with standards like Server-Sent Events (SSE) can be used to deliver large volumes of data as streams. Allowing volumes of data and content to be streamed in logical series, with API consumers receiving as individual updates in a continuous, long-running HTTP request. Only receiving the data that has been requested, as well as any incremental updates, changes, or other events that have been subscribed to as part of the establishment of streams. Providing a much more real time approach to making sure large amounts of data can be sent as efficiently as possible to API consumers.

**Moving Forward With HTTP/2**<br />
Everything we've discussed until now leverages the HTTP 1.1 standard, but there are also increased efficiencies available with the HTTP/2 release of the standard. HTTP/2 has delivered a number of improvements on caching and streaming, and handling the threading of of multiple messages within a single API request. Allowing for single, or bi-directional API requests and responses to exist simultaneously. When combined with existing approaches to pagination, hypermedia, and query languages, or using serialization formats like Protocol Buffers, further efficiency gains can be realized, while staying within the HTTP realm, but moving forward to use the latest version of the standard.

This is just a summary look at the different ways to help deliver large amounts of data using APIs. Depending on the conversations I have today I may dive in deeper into all of these approaches and provide more examples of how this can be done. I might do some round ups of other stories and tutorials I've curated on these subjects, aggregating the advice of other API leaders. I just wanted to spend a few moments thinking through possibilities so I can facilitate some intelligent conversations around the different approaches out there. While also sharing with my readers, helping them understand what is possible when it comes to making large amounts of data available via APIs.
