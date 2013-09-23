---
layout: post
title: "Simple API Example: Company Listing"
url: 'http://apievangelist.com/2013/07/14/simple-api-example-company-listing/'
image: 'http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/blog/baas-trends.png'
---

I'm always looking for dead simple examples of what an API is to help average folk understand what APIs are, and how they can be applied in their worlds.

My current research on [backend as a service providers (BaaS)][1] providers a great example. On my research site i provide listing of BaaS providers for my readers:

<img src="https://s3.amazonaws.com/kinlane-productions/api-evangelist/baas/example-api-baas.png" alt="" width="500" />

This listing of companies is a pretty common occurence on the web. As a web developer, if I want to show this listing I use HTML, which is markup that provides a visual formatting for this listing:

<img src="https://s3.amazonaws.com/kinlane-productions/api-evangelist/baas/example-api-baas-html.png" alt="" width="500" />

HTML makes content presentable for humans. Now if I want to make this same content available for other web sites and applications, instead of using HTML, I will use another open format called JSON, which is easy for other computers and applications to consume.

<img src="https://s3.amazonaws.com/kinlane-productions/api-evangelist/baas/example-api-baas-json.png" alt="" width="500" />

In this particular case, I provide an HTML listing of BaaS providers, as well as a JSON listing. I actually use the JSON file to display the HTML, using a JavaScript templating library called [Mustache][2].

In addition to a static HTML and JSON listing of BaaS providers, I also provide an API which returns the same content as the JSON file, but allows you to do queries and get only the BaaS companies you are looking for. All of my data works this wa by providing:

<img src="https://s3.amazonaws.com/kinlane-productions/hacker-storytelling/machine-readable-toolbar.png" alt="" width="250" align="right" />

  * **HTML** \- An HTML listing meant for humans to view.
  * **JSON** \- A JSON listing meant for developers to use in other sites and apps.
  * **API** \- An API allowing querying, filtering and other dynamic access.

This process always starts with API driven data, and I produce the HTML from my APIs. This is the beauty of API first. You can generate your web content from it, being the first user of all your APIs. Then encourage others to syndicate content by providing them with simple scripts for displaying HTML listings, driven from JSON and / or your API.

The only difference between web site content and an API is the resulting output, if it is a website--we use HTML. If its an API--we use JSON. Both websites and APIs using the same mechanisms of the web, specifically HTTP to deliver this data.

To provide machine readable JSON version of your content, or even more dynamic representations via APIs, you don't need special technology or skills. If you are developing websites, you have the skills to make the same content machine readable and potentially much more syndicatable, re-usable and accessible with APIs.

   [1]: http://baas.apievangelist.com (BaaS)
   [2]: http://mustache.github.io/
