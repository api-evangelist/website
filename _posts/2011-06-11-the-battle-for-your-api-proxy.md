---
layout: post
title: "The Battle for Your API Proxy"
url: 'http://apievangelist.com/2011/06/11/the-battle-for-your-api-proxy/'
image: ''
---

Every Web API is designed to receive requests from and respond to the outside world.

Every day an API can receive thousands or potentially millions of calls. Before the API can process these requests and returns a response, it has to potentially tackle a huge laundry list of functionalities: <img src="http://kinlane-productions.s3.amazonaws.com/api-evangelist/traffic-lights.jpg" alt="" width="300" align="right" />

  * Identity / Authentication
  * Traffic Controls
  * Rate Limiting
  * Performance
  * Security
  * Scalability
  * Filtering
  * Encryption
  * Logging
Once all these items are handled, then the API can do what it is designed to do -- process its payload and return a response.

Many API owners tackle all these layers of the API themselves. But there are also several service providers out their looking to do this for them.

The first group of API service providers in this area use what I call the Proxy Flow Through, and this includes [Mashery][1] and [Apigee][2]. Mashery and Apigee deliver these service by routing all calls to an API through their proxy. Each call actually is made to [Mashery][3] and [Apigee][4], then they route the request to the actual API for a response.

<img class="aligncenter" src="http://kinlane-productions.s3.amazonaws.com/api-evangelist/ProxyFlowThrough.png" alt="" width="500" align="center" />

The second group of API service providers in this area, use what I call the Proxy Connector, and this includes [3Scale][5] and [Mashape][6]. [3Scale][7] and [Mashape][8] deliver these services by providing a connector your API can use to communicate with the proxy during each call.

<img class="aligncenter" src="http://kinlane-productions.s3.amazonaws.com/api-evangelist/ProxyConnector.png" alt="" width="500" align="center" />

[<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/api-evangelist/apigee-logo.jpg" alt="" width="150" align="right" />][2]All of these service providers end up delivering a similar set of services. This proxy, whether flow through or connector tackle the needs listed above, but then also provide much needed data on API operations. Apigee, Mashery, and 3Scale provide you with tools for monitoring and analyzing this operational data.

There is a lot at stake here. The next wave of Internet growth will pass through these proxies. More API owners are turning to these providers to deliver this layer, where all usage of the API from web apps, mobile apps, and other devices developed internally, by partners and the public will pass through these proxies.

[<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/api-evangelist/Mashery-Logo.gif" alt="" width="150" align="right" />][1]These proxies are becoming brokers in the API economy. Each service provider is competing, for the ability to proxy your web API and be your broker in this new economy.

Mashery, Apigee, and 3Scale all provide some very robust services via their proxy, Apigee even offers their proxy technology as an on-premise appliance.

Newcomer Mashape does not provide a full suite of services via their proxy, like the others, but Mashape is taking a different approach, by introducing an add-on layer within their proxy. There are only two add-ons available (billing, rate limit) currently, but this concept opens up an entirely new type of marketplace for the entire API industry, not just a single API. Developers can now build specialized tools to sell, and push forward whats possible within a proxy. This proxy add-on layer also has potential for allowing a more a la carte set of services available to API owners.[<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/api-evangelist/3Scale-Logo.jpg" alt="" width="150" align="right" />][7]

The demand for API proxies is growing, and each service provider is pushing the definition of what it means to proxy your API. Mashery, Apigee, 3Scale, Mashape and others are working hard to define the space, push it forward, while also winning market-share.

[<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/mashape-logo.png" alt="" width="150" align="right" />][8]One might compare this playing field to the competition between database service providers of the last two decades, where companies like Microsoft and Oracle battled it out for market share. There are many differences for sure, but with the amount of information and value running through APIs, the parallels to database choices are there -- except I still don't see the MySQL of API proxies as of yet.

######  Related articles

  * [Open Source API Billing and Traffic Control][9] (apievangelist.com)
  * [API Metrics and Analytics][10] (apievangelist.com)
  * [Whats Next for APIs?][11] (apievangelist.com)

   [1]: http://www.mashery.com/
   [2]: http://www.apigee.com/
   [3]: http://blog.apievangelist.com/2010/10/10/mashery-api-services/ (Mashery)
   [4]: http://blog.apievangelist.com/2010/10/10/apigee-api-services/ (Apigee)
   [5]: http://blog.apievangelist.com/2010/10/10/3scale-api-services/ (3Scale)
   [6]: http://blog.apievangelist.com/2011/03/04/mashape-api-service-provider/ (Mashape)
   [7]: http://www.3scale.net/
   [8]: http://www.mashape.com/
   [9]: http://blog.apievangelist.com/2011/05/21/open-source-api-billing-and-traffic-control/
   [10]: http://blog.apievangelist.com/2011/03/31/api-metrics-and-analytics/
   [11]: http://blog.apievangelist.com/2011/05/24/whats-next-for-apis/
