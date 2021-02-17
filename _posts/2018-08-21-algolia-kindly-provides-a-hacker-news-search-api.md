---
published: true
layout: post
title: 'Algolia Kindly Provides A Hacker News Search API'
image: https://s3.amazonaws.com/kinlane-productions2/algolia/hacker-news-algolia-search-api.png
---

<p><img src="https://s3.amazonaws.com/kinlane-productions2/algolia/hacker-news-algolia-search-api.png" width="45%" align="right" style="padding: 15px;" />
<p>I was working on <a href="https://serverlessrepo.aws.amazon.com/applications/arn:aws:serverlessrepo:us-east-1:879370021840:applications~StreamData-IO-Hacker-News-New">a serverless app for Streamdata.io that takes posts to Hacker News and streams them into an Amazon S3 data lake</a>, and I came across the <a href="https://hn.algolia.com/api">Algolia powered Hacker News search API</a>. After being somewhat frustrated with the simplicity of the official Hacker News API, I was pleased to find <a href="https://hn.algolia.com/api">the search kindly provided by Algolia</a>.

<p>There is no search API available for the core Hacker News API, and the design leaves a lot to be desired, so the simplicity of Algolia’s API solution was refreshing. There is a lot of data flowing into Hacker News on a regular day, so providing a search API is pretty critical. Additionally,  Algolia’s ability to deliver such a simple, usable, yet powerful API on top of a relevant data source like Hacker News demonstrates the utility of what Algolia offers as a search solution–something I wanted to take a moment to point out here on the blog.

<p>I consider search to be an essential ingredient for any API. Every API should have a search element to their stack, allowing the indexing and searching of all API resources through a single path. Making Algolia a relevant API service provider in this area, enabling API providers to outsource the indexing and searching of their resources, and the delivery of a dead simple API for your consumers to tap into. This path forward is probably not for every API, as many weave specialized search throughout their API design, but for teams who are lacking in resources, and can afford to outsource this element–Algolia makes sense.

<p>Seeing Algolia in action, for a specific API I was integrating with helped bring their service front and center for me. I tend to showcase Elastic for deploying API search solutions, but it is a good to receive a regular reminder that Algolia does the same thing as a service. Their work on the Hacker News Search API provides a good example of they can do for you–sure, we can all build our own search solutions, but honestly, do you have the time? I’ll make sure and regularly highlight what Algolia is doing as part of <a href="http://search.apievangelist.com">my search API research</a>, and thanks Algolia! I really appreciate what you did for <a href="https://hn.algolia.com/api">the Hacker News API</a>, it made my work a lot easier.


