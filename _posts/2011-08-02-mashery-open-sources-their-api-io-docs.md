---
layout: post
title: "Mashery Open Sources Their API I/O Docs"
url: 'http://apievangelist.com/2011/08/02/mashery-open-sources-their-api-io-docs/'
image: ''
---

<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/api-service-providers/mashery/mashery-io-docs-screenshot.jpg" alt="" width="300" align="right" />Last week at OSCON, I wrote about [Mashery's release of their new I/O Docs][1]. [Mashery I/O Docs][2] are a combination of [API documentation][3] and an [API explorer][4], allowing developers to make requests on an API inline while browsing the API reference materials.

I/O Docs provides an interactive documentation system for RESTful web APIs. By defining APIs at the resource, method and parameter levels in a JSON schema, I/O Docs will generate a JavaScript client interface. API calls can be executed directly from the documentation interface, proxied through the I/O Docs server, producing formatted responses.

Mashery has [open-sourced a version of the I/O Docs on Github][5], for any API owner to deploy for their own documentation. This version of I/O docs runs on [Node.js][6] and uses [Redis][7] as a data store.

Last year Apigee launched their [API console][8] which allows users to also make calls against an API, and [earlier this year they made it freely available for any API owner][9] to deploy. The API console is a popular tool with developers to get up and going using an API, and build an understanding how an API works. Apigees move to make free was a significant market play, and definitely built awareness of their platform.

Masherys approach to API exploration reflects an alternative view from Apigees, one that integrates API discovery with API documentation, as opposed to being an entirely separate tool. Masherys move to open-source their I/O Docs on Github, is great to see. I'm sure it will definitely attract more attention to their platform and tools.

You can [download or fork the Mashery I/O Docs on Github][10], and find necessary installation info and documentation.

   [1]: http://blog.programmableweb.com/2011/07/26/mashery-delivers-smarter-api-documentation/ (Masherys Release of their API I/O Docs)
   [2]: http://mashery.com/solution/iodocs/ (Mashery I/O Docs)
   [3]: http://www.apievangelist.com/ecosystem-building-blocks-detail.php?Building_Block_ID=120 (API Documentation)
   [4]: http://www.apievangelist.com/ecosystem-building-blocks-detail.php?Building_Block_ID=209 (API Explorer)
   [5]: https://github.com/mashery/iodocs (open-sourced a version of the I/O docs on Github)
   [6]: https://github.com/joyent/node/wiki/Installation (Node.js)
   [7]: http://redis.io/download (Redis)
   [8]: http://apigee.com/about/products_togo.html (API consoe)
   [9]: http://blog.apievangelist.com/2011/03/07/apigee-api-console-is-now-free-for-everyone-to-use/ (earlier this year they made it freely available for any API owner)
   [10]: https://github.com/mashery/iodocs (download or fork the Mashery I/O docs on Github)
