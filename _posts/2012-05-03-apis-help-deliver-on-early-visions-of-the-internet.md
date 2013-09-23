---
layout: post
title: "APIs Help Deliver on Early Visions of the Internet"
url: 'http://apievangelist.com/2012/05/03/apis-help-deliver-on-early-commerce-visions-of-the-internet/'
image: 'http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/blog/elasticpath-logo.jpg'
---

<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/internet-commerce.jpg" alt="" width="250" align="right" />

As my professional career moved online during the years between 1995 and 2000, I had numerous visions about what the World Wide Web could do for businesses. I think I shared these visions with millions of other individuals, fueling what we now know as the first Internet bubble.

I saw e-commerce driving entirely new businesses that could operate entirely online, and strengthen existing brick and mortar businesses allowing anyone to buy and sell goods and services from anywhere, instantly.

What we ended up with was still important, but the web 1.0 world was not quite as grand as I think some of us had envisioned. [E-Bay][1], [Amazon][2] and Paypal definitely went further than many e-commerce platforms and service providers, and I firmly believe their embrace of web APIs was the reason for this.

While e-commerce has undeniably grown and evolved, other new concepts like social and cloud computing took center stage in creating an entirely new vision of the Internet, concepts we didn’t even conceive in the early days of the World Wide Web.

Years later, driven by APIs, I think we are just now beginning to deliver on the early visions of commerce on the Internet. [E-commerce APIs like ElasticPath][3] are delivering on this vision by offering up a mature and robust [e-commerce engine][4] completely accessible by a truly RESTful API.

[<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/api-evangelist/elasticpath/elasticpath-logo.jpg" alt="" align="right" />][5]

Using ElasticPath you can define and execute against any vision of commerce whether it involves physical or virtual goods, with any type of pricing, offers or subscriptions that enable purchasing of these products on truly any platform or any device, in a myriad of ways only limited by your imagination.

ElasticPath delivers by starting with a hardened and complete e-commerce engine that drives clients like Google and Sony, and proven by driving extreme online and offline commerce scenarios like the [Vancouver 2010 Winter Olympics][6]. Next ElasticPath bundles a robust Level 3 REST API with the their e-commerce engine, providing not just programmatic access to every aspect of the e-commerce engine, but a hypermedia driven experience ensuring developers can deliver on the business logic and user experience defined by any company that deploys their e-commerce platform using ElasticPath.

[<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/api-evangelist/elasticpath/elasticpath-api.png" alt="" align="right" />][5]

If you’re not familiar with Level 3 REST also known as [Hypermedia as the Engine of Application State][7] (HATEOAS), it is an enhancement to REST, that enables a client to have no prior knowledge about how to interact with any particular application or server beyond a generic understanding of hypermedia. So in the context of e-commerce, when a developer requests a product the API, you get back the usual JSON describing the product, but you also get supporting media types for these “products”, and supporting link relations. So if purchasing the product means streaming in media player you will get media types as well as link to load into player, where if it is a product that you can add to shopping cart, you will get the link to add to cart, and so on.

I’m still learning about the technical details and benefits of HATEOAS REST, but i can see the benefits when bundled with ElasticPath’s very mature e-commerce engine. It allows you to not only build robust product catalogs that drive your website, but an e-commerce engine that can drive digital commerce across multiple platforms and devices, without developers having to fully understand the business rules and logic set forth by your company, leaving them to do what they do best, while ensuring your products, information and brand are reflected wherever your conducting e-commerce.

I guess e-commerce isn’t the only vision of the Internet, but it definitely is a large part of it, and I think APIs have been fueling the growth of e-commerce since the first part of the last decade, and now with platforms like [ElasticPath][8] we will truly see this vision mature and allow us to sell physical and digital goods anywhere in the world, in real-time.

   [1]: /2011/01/26/history-of-apis-ebay/ (E-Bay History of APIs)
   [2]: /2011/01/28/history-of-apis-amazon-e-commerce/ (Amazon History of APIs)
   [3]: http://www.elasticpath.com/ (E-commerce APIs like ElasticPath)
   [4]: http://www.elasticpath.com/products/features (e-commerce engine)
   [5]: http://www.elasticpath.com/
   [6]: http://www.elasticpath.com/company/news/2007/vancouver-2010-olympics (Vancouver Winter Olympics)
   [7]: http://en.wikipedia.org/wiki/HATEOAS
   [8]: http://www.elasticpath.com/ (ElasticPath)
