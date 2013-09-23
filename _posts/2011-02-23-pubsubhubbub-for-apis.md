---
layout: post
title: "PubSubHubbub for APIs"
url: 'http://apievangelist.com/2011/02/23/pubsubhubbub-for-apis/'
image: ''
---

[Superfeedr][1] is now supporting [PubSubHubbub for data APIs][2]. [PubSubHubbub][3] was initially created for [XML][4] to alleviate the number of times a feed is polled versus how many times it actually has an update. [<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/api-evangelist/Superfeedr.png" alt="" align="right" />][1] The bandwidth consumption and server load of an API can be reduced greatly by adding a PubSubHubbub layer on a data API.

Primary areas of a Superfeedr PubSubHubbub deployment are:

  * **Resource Identification** \- Identify what services your developers / applications are polling the most. Identify how many requests are made against how many times information was returned.
  * **Push Discovery -** Indication to any applications polling your API that the content being polled is available in a push fashion by adding an HTTP header to the API responses which mentions the Superfeedr hub.
  * **Secure Subscriptions -** Define a subscription callback URL where Superfeedr will echo all subscriptions to the API content, including the [HTTP headers][5] and any additional parameter provided by the subscriber.
  * **Notifications -** Superfeedr needs to know when content is updated so they can notify users. This is done in two ways:
    * **Fat pings -** An API owner can push content to Superfeeder and they will parse the content and push it forward to subscribers.
    * **Light pings -** Provide URL that has been updated and Superfeedr will update poll and update users.
Superfeedr PubSubHubbub is providing a layer to existing data APIs that will alleviate bandwidth and server load.

We are seeing similar layers being built for functional APIs such as the XMPP print jobs notification for the [Google Cloud Print (GCP) Services Interface][6].

   [1]: http://www.superfeedr.com/
   [2]: http://disqus.com/forums/superfeedr-thoughts/superfeedr_pubsubhubbub_for_apis/trackback/
   [3]: http://code.google.com/p/pubsubhubbub/
   [4]: http://en.wikipedia.org/wiki/XML (XML)
   [5]: http://en.wikipedia.org/wiki/List_of_HTTP_header_fields (List of HTTP header fields)
   [6]: http://code.google.com/apis/cloudprint/docs/proxyinterfaces.html
