---
layout: post
title: "Freshbooks API  Add-Ons, Billing, and Webhooks"
url: 'http://apievangelist.com/2011/04/13/freshbooks-api-add-ons-billing-and-webhooks/'
image: ''
---

[<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/Freshbooks_610x564.png" alt="" width="250" align="right" />][1]I am slowly working my way through [hundreds of APIs][2] and doing business reviews of their approach to delivering their APIs.

At API Evangelist I'm focused on the business of APIs, with a minor focus on the technology behind those APIs. So when I publish a business review of an API, I will add it to my API database, then move on.

That is, unless I identify a story -- an innovative approach, monetization strategy, or anything that I feel needs to be talked about in more detail.

While reviewing the [Freshbooks API][3] I found three notable building blocks:

  * **[Application Billing][4]** \- A built in billing and payment framework for Freshbook applications and beyond
  * **[Webhooks][5]** \- Framework for enabling application callbacks, URLs where the Freshbook system can send notifications to third party applications
  * **[FreshBooks Add-on Stor**e][6] \- Application store and development platform for developers to build custom apps, showcase, and sell to Freshbook customers.
[Self-Service Application Frameworks][7] like the Freshbooks Add-On Store are growing more common. I've talked about similar systems from [Box.net][8] and [Google Apps Marketplace][9]. The Freshbooks Add-On store is not 100% self-service, but it is close. [<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/freshbooks-leaf.jpg" alt="" width="250" align="right" />][1] Webhooks are nothing new, but Freshbook offers a standardized approach to deploying web-hooks that makes them easy for developer to use.

A built in payment system is definitely a notable [API building block][10]. Providing developers with a baked-in payment system for handling application monetization is very innovative.

Where do these three building blocks fit into the big picture? I try to build profiles for common API building blocks, I don't have profiles for self-service application frameworks, webhooks, and payment systems, but as I evaluate more I will define these as more innovative building blocks for API owners to use.

I will definitely be keeping an eye on the [Freshbook][11] approach to their API.

   [1]: http://www.freshbooks.com/
   [2]: http://www.programmableweb.com/apis/directory (hundreds of APIs)
   [3]: http://developers.freshbooks.com/ (Freshbooks API)
   [4]: http://developers.freshbooks.com/billing/ (Application Billing)
   [5]: http://developers.freshbooks.com/webhooks/ (Webhooks)
   [6]: http://community.freshbooks.com/addons/ (Freshbooks Add-On Store)
   [7]: http://blog.apievangelist.com/2011/04/08/anatomy-of-a-self-service-application-platforms/ (Self-Service Application Frameworks)
   [8]: http://blog.apievangelist.com/2011/04/08/box-net-openbox/ (Box.net)
   [9]: http://blog.apievangelist.com/2011/04/08/google-apps-marketplace/ (Google Apps Marketplace)
   [10]: http://www.apievangelist.com/ecosystem-building-blocks.php (API Building Block)
   [11]: http://www.freshbooks.com/ (Freshbook)
