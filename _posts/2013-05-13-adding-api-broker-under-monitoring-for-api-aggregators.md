---
layout: post
title: "Adding API Broker Under Monitoring for API Aggregators"
url: 'http://apievangelist.com/2013/05/13/adding-api-broker-under-monitoring-for-api-aggregators/'
image: 'http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/blog/payments-api-broker-spreedly.png'
---

<img src="https://s3.amazonaws.com/kinlane-productions/api-evangelist/payments-api-broker-spreedly.png" border="0" width="325" align="right" />

As I'm monitoring the API space I'm trying to create meaningful grouping for companies to belong when tracking API trends. My groupings are sometimes in alignment with what we hear in the tech blogosophere, but other times I try new definitions to help expand my monitoring definition and see if I can identify emerging patterns like I'm seeing with [BaaS][1].

Each week I do a little more exploration in concept of [API aggregation][2], and this week after [studying payment API aggregator Spreedly][3], I'm considering adding a new, overlapping area with aggregation, called API brokers. Let's see if I can make this work.

API aggregators like [Singly][4] are providing personal data access to popular SaaS platforms by aggregating APIs. You can pull a list of photos from Singly, for a user, and it could pull photos from Flickr, Instagram and Facebook. This is pretty straightforward API Aggregation.

Other providers like [Temboo][5], provide this functionality but focus more on the API interoperability or as i call it [API reciprocity][6] side of things. Temboo does aggregate multiple APIs like Singly, but focuses on providing interoperability as well as aggregation. While Singly does to, there are differences in their approach.

[Spreedly][7] has all the telltale signs of an API aggregator. They allow you to program against 48 payment gateways in 71 countries. It has aggregation, but rather than interoperability it seems to be about brokering transactions. Spreedly can help you choose the gateway based upon location, cost and availability. Which has all the elements of what I'd consider an API broker.

I envision other new API brokers emerging, in niche areas like images, video or messaging. Imagine if you could use Twilio, Tropo or other SMS API provider, but use through a broker who will give you the best availability and costs based upon various needs. This type of API aggregation is not meant for providing users with access to multiple cloud silos via APIs, it is more about brokering API resources and establishing a marketplace.

Not all APIs can be brokered, and maybe Spreedly is unique, but I bet I will find more of this behavior from other companies, once I start looking. Let me know if you know of any companies who broker API resources in a similar way to Spreedly.

   [1]: http://baas.apievangelist.com (Backend as a Service)
   [2]: http://aggregation.apievangelist.com (API aggregation)
   [3]: /2013/05/13/potential-for-api-aggregators-to-provide-valuable-industry-data/
   [4]: http://singly.com
   [5]: http://temboo.com (Temboo)
   [6]: http://reciprocity.apievangelist.com (API reciprocity)
   [7]: https://spreedly.com/
