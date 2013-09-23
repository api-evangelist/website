---
layout: post
title: "Partial Response and Updates with Google APIs"
url: 'http://apievangelist.com/2011/07/19/partial-response-and-updates-with-google-apis/'
image: ''
---

<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/api-evangelist/puzzle-partial.png" alt="" width="250" align="right" />[Last year google launched support for partial response and updates][1] to a couple of the Google APIs. The goals was to significantly reduce network, memory, and CPU resources needed to work with Google APIs.

Now Google is [adding support][2] for partial response, and an improved version of [partial update, called patch][3], to a number of newer APIs including:

  * [Google Buzz API][4]
  * [Google URL Shortener API][5]
  * [Google Tasks API][6]
All APIs available in the [Google APIs Discovery Service][7] and the [APIs Explorer][8] supporting partial response and updates.

The partial response algorithm works by supplying a fields query parameter to any API call that returns data, you can request specific fields.

Here is an example request that returns only titles and timestamps of a user's public Buzz activities: [https://www.googleapis.com/buzz/v1/activities/kinlane@gmail.com/@public?alt=json][9]

   [1]: http://googlecode.blogspot.com/2010/03/making-apis-faster-introducing-partial.html (last year google launched support for partial responses and updates)
   [2]: http://googlecode.blogspot.com/2011/07/lightning-fast-performance-tips-for.html (adding support)
   [3]: http://code.google.com/apis/buzz/v1/performance.html#patch (partial update, called patch)
   [4]: http://code.google.com/apis/buzz/ (Google Buzz API)
   [5]: http://code.google.com/apis/urlshortener/ (Google URL Shortener API)
   [6]: http://code.google.com/apis/tasks/ (Google Tasks API)
   [7]: http://blog.apievangelist.com/2011/05/21/google-apis-discovery-service/ (Google APIs Discovery Service)
   [8]: http://blog.apievangelist.com/2011/05/21/google-apis-explorer/ (Google APIs Explorer)
   [9]: http://blog.apievangelist.com/2011/05/21/google-apis-explorer/
