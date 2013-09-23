---
layout: post
title: "Wisdom Shared from the Foursquare API Team"
url: 'http://apievangelist.com/2011/07/09/wisdom-shared-from-foursquare-api-team/'
image: ''
---

<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/api-evangelist/foursquare/foursquare-engineering-logo.png" alt="" align="right" />Foursquare is [sunsetting their APIv1][1], and recently spent some time sharing the lessons they learned during APIv1 and the decisions that went into APIv2.

Here are some excerpts:

  * **JSON -** This was a no brainer. Its flexible and understood by everybody.
  * **OAuth2 and HTTPS-Only -** OAuth2 is straightforward to implement on the server and client, and offloading encryption to HTTPS makes it easy to get it right.
  * **REST Lite -** It makes sense to use resourceful URLs for certain key objects, like users/USER_ID or venues/VENUE_ID, with actions and connections hanging off of them. Also avoiding deeply nested URLs like users/USER_ID/tips/TIP_ID, instead using tips/TIP_ID, leads to much simpler URLs. Finally, they avoided using the extended set of HTTP verbs beyond POST and GET, putting the action into the endpoint name, such as tips/add.
  * **Documentation -** Quality documentation combined with an API explorer is a win. Also theimplementationof a simple documentation generation system, made it easy for Foursquare engineers to keep API documentation up to date.
  * **Timestamps as Seconds Since Epoch -** Renders timestamps not readable by humans, but extremely easy to parse.
  * **Versioning -** The hardest part of designing an API is that you're stuck with a bunch of decisions you can't take back. But in some cases they needed to take them back anyway, so they came up with the idea of clients sending back a version like 20110708 and promising to be compatible with all changes up to the date.
  * **Object Level detail -** It's always hard to decide how much detail to include in an object, and Foursquare lets the clients dictate what to include where. In APIv2, they introduced compact and full JSON representations of resources.
  * **Envelope -** The decision to wrap all responses in { meta: { � }, response: {...} } was well received, along with the error details included in the meta block.
They provide a lot more wisdom in their blog post,[APIv2: Woulda, coulda, shoulda][2]. Some of the points I couldn't do justice with just an excerpt.

Some of their reflections are just reminders of the success of JSON, OAuth2 and a simple RESTful approach. But their insight about how to structure objects, envelopes, timestamps and categories has me putting some more thought into upcoming changes to my API.

   [1]: https://groups.google.com/forum/#!topic/foursquare-api/tZPFTbUTQJQ (sunsetting their APIv1)
   [2]: http://engineering.foursquare.com/2011/07/08/apiv2-woulda-coulda-shoulda/ (APIv2: Woulda, coulda, shoulda)
