---
layout: post
title: "With Seevl Music Discovery, the Website is the API"
url: 'http://apievangelist.com/2011/05/27/with-seevl-music-discovery-the-website-is-the-api/'
image: ''
---

[<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/api-evangelist/seevl_logo1.png" alt="" align="right" />][1][Seevl][1], a music discovery service that provides anew way to explore the cultural and musical universe of various artists, just launched an API with the assistance of [3Scale][2].

When deploying the API, Seevl approached it a little differently than most. Instead of providing a separate API to access data, Seevl relies on content negotiation principles to deliver alternative representations of web pages.

This means the entire Seevl website is the API and you can get JSON representations of almost every page in the site.

Seevl relies on HTTP headers to let developers request data using a particular content-types, and authenticate using three parameters:

  * **Accept** \- The content-type required
  * **X_APP_ID** \- Developer application ID
  * **X_APP_KEY** \- Developer application Key
Here is an example search results for beatles using curl:

This approach is meant to make it easier for to developers focus on the development and let the Seevl client libraries handle the content-negotiation.

The [Seevl API][3] provides everal methods to search and pull specific data about individual bands and artists and related information.

While this approach is nothing new, its an interesting way to provide users with HTML views and developers with the JSON representations of information stored in a database.

######  Related articles

  * [Seevl: Explore the cultural universe based on semantic web technologies][4] (semantic-web.at)
  * [Whats Next for APIs? Learning From Social APIs][5] (apievangelist.com)
  * [Google APIs Explorer][6] (apievangelist.com)

   [1]: seevl.net (Seevl)
   [2]: http://www.3scale.net (3Scale)
   [3]: http://developers.seevl.net/ (Seevl API)
   [4]: http://blog.semantic-web.at/2011/05/19/seevl-explore-the-cultural-universe-based-on-semantic-web-technologies/
   [5]: http://blog.apievangelist.com/2011/05/24/whats-next-for-apis-learning-from-social-apis/
   [6]: http://blog.apievangelist.com/2011/05/21/google-apis-explorer/
