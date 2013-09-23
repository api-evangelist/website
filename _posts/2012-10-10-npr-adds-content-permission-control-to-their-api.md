---
layout: post
title: "NPR Adds Content Permission Control to their API"
url: 'http://apievangelist.com/2012/10/10/npr-adds-content-permissions-control-to-their-api/'
image: 'http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/blog/npr-logo.jpeg'
---

[<img class="c1" src="https://s3.amazonaws.com/kinlane-productions/api-evangelist/npr/npr-logo.jpeg" alt="" width="200" align="right" />][1]

NPR is defining new models for content distribution. One that other media providers can follow, when designing their API driven content delivery platforms.

The [NPR Story API][2] provides digital access to NPR content and to other station content--allowing both NPR and stations to contribute and consume local and national news stories.

In an effort to provide NPR stations with more control over the content they contribute to the platform for distribution, [NPR Digital Services has introduced content permissions control via the NPR story API][3].

Currently content stored on the Story API’s platform can be retrieved by anyone with an API key--allowing content pushed across the network to be consumedd in 3 ways:

  * **Create Once, Publish Everywhere** \- Stations and npr.org push content into the API and then pull the content onto other platforms, such as other station-owned web properties and mobile apps
  * **Station Networks** \- Content is shared between multiple stations in a content network, both on web sites and mobile apps
  * **National** \- Station content is featured on npr.org and NPR mobile apps with links back to station digital properties

Using the new content permissions, stations can now control who is allowed to pull their content from the API. The permissions work by allowing stations pushing content to specify whether the content should be:

  * Public to all
  * Public to the NPR station network
  * Public to a group of stations listed in a whitelist
  * Public to everyone except for stations on a blacklist

The new changes allow stations to set these permissions at the individual story level, as well as create permission groups to add multiple stories to.

NPR's approach is a great model for how APIs can facilitate content exchange across a large network of providers, allowing for the widest distribution possible-while also allowing content owners control over who has access to their valuable content in a very granular way.

<img class="c2" src="https://s3.amazonaws.com/kinlane-productions/api-evangelist/npr/NPR-Digital-Services.png" alt="" width="450" />

APIs are all about providing access to valuable content and resources, but should also be designed to give the proper amount of access, so your content doesn’t end up being consumed, distributed in ways you don’t find appropriate.

   [1]: http://www.npr.org/ (NPR)
   [2]: http://dev.npr.org/
   [3]: http://digitalservices.npr.org/post/npr-api-content-permissions-control
