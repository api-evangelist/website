---
layout: post
title: With Seevl Music Discovery the Website is the API
url: http://apievangelist.com2011/05/27/with-seevl-music-discovery-the-website-is-the-api/
source: http://apievangelist.com2011/05/27/with-seevl-music-discovery-the-website-is-the-api/
domain: apievangelist.com2011
image: 
---
{% include JB/setup %}<p>Seevl, a music discovery service that provides anew way to explore the cultural and musical universe of various artists, just launched an API with the assistance of 3Scale.When deploying the API, Seevl approached it a little differently than most.Instead of providing a separate API to access data, Seevl relies on content negotiation principles to deliver alternative representations of web pages.This means the entire Seevl website is the API and you can get JSON representations of almost every page in the site.Seevl relies on HTTP headers to let developers request data using a particular content-types, and authenticate using three parameters: Accept - The content-type required X_APP_ID - Developer application ID X_APP_KEY - Developer application Key Here is an example search results for beatles using curl: This approach is meant to make it easier for to developers focus on the development and let the Seevl client libraries handle the content-negotiation.</p>
<center><p><a href="http://apievangelist.com2011/05/27/with-seevl-music-discovery-the-website-is-the-api/" style='padding:25px; font-sze:18px; font-weight: bold;'>Read Full Story</a></p></center>
