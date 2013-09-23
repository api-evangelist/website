---
layout: post
title: "Mashape Provides Tools to Distribute, Discover and Hack APIs"
url: 'http://apievangelist.com/2011/06/30/mashape-provides-tools-to-distribute-discover-and-hack-apis/'
image: ''
---

[<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/api-service-providers/mashape-logo.png" alt="" width="250" align="right" />][1]I'm exploring the [Mashape API Platform][2], trying to break things down and understand everything in more detail. Blogging about a topic does this for me.

So let's start with deploying an API with Mashape.

With the [Mashape PHP Library][3] you can deploy an API on your infrastructure. You [download the library from Github][4], deploy on your server, and then add the methods for your API by extending the Mashape PHP component class.

If you already have an API that returns JSON responses, you can just register it as a Mashape API for distribution, without deploying the Mashape PHP Library.

If you've deployed your API without the Mashape PHP Library you will need to accomplish one more step. You will need to implement the [Mashape Connector][5] by adding one line of code to your API, which is required to connect your API to the Mashape Platform and handle user authorization, billing, and rate-llimiting.

Whichever way you deploy your API, you can now distribute it using Mashape. The first step for distributing an API is to create an XML file that describes what the API does. This XML file gets deployed on your server and needs to be updated as your API evolves.

Once your API is deployed and published to Mashape, the platform distributes your API to the [Mashape Marketplace][6] and provides a detail page with title, description, documentation, test console and [PHP][7], [Python][8], [Ruby][9], [Java][10] and [Objective C][11] client libraries.

Mashape then provides a way for developers to sign-up and start hacking on any API in the Mashape Marketplace with a single developer account and key. There are also social features allowing users to follow and contact other users.

All APIs that are published using Mashape will connect and communicate with Mashape through an API Proxy. This is the proxy that handles the authorization of users, implementation of billing, rate limiting and other functions described above.

<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/api-service-providers/mashape/Mashape-Manage-Your-API.png" alt="" width="350" align="right" />Right now the proxy is primarily available via the Mashape platform, but you can also find an [open-source version of the Mashape API proxy][12] on Github. The API Proxy is intended to be downloaded and installed on your servers, which will increase the performance and security of your API.

In addition to being able to register your API and use the [Mashape API Proxy][13] in the cloud, you can [download and install][14] on-premise. Since it is open-source, you could also fork the code and potentially add in your own modifications to the API proxy, which is written in JavaScript and runs on the latest version of node.js

I'm playing around with deploying one small and one large data-set as two separate APIs using the Mashape PHP Library, so I can get more familiar with how the platform works. I just wanted to work through some thoughts about what they provide here on the blog. More to come on [Mashape][15]...

   [1]: http://www.mashape.com/
   [2]: http://www.mashape.com/ (Mashape API Platform)
   [3]: https://github.com/Mashaper/mashape-php-library (Mashape PHP Library)
   [4]: https://github.com/Mashaper/mashape-php-library (download the library from Github)
   [5]: http://www.mashape.com/guide/publish/xml#authentication (Mashape Connector)
   [6]: http://www.mashape.com/explore/ (Mashape Marketplace)
   [7]: https://github.com/Mashaper/mashape-php-client-library (Mashape PHP Client Library)
   [8]: https://github.com/Mashaper/mashape-python-client-library (Mashape Python Client Library)
   [9]: https://github.com/Mashaper/mashape-ruby-client-library (Mashape Ruby Client Library)
   [10]: https://github.com/Mashaper/mashape-java-client-library (Mashape Java Client Library)
   [11]: https://github.com/Mashaper/mashape-objectivec-client-library (Mashape Objective C Client Library)
   [12]: http://blog.apievangelist.com/2011/06/30/open-source-version-of-the-mashape-api-proxy/ (Open-Source version of the Mashape API Proxy)
   [13]: http://blog.apievangelist.com/2011/06/30/open-source-version-of-the-mashape-api-proxy/ (Mashape API Proxy)
   [14]: https://github.com/Mashaper/Mashape-API-Proxy (download and install)
   [15]: http://blog.apievangelist.com/2011/03/04/mashape-api-service-provider/ (Mashape)
