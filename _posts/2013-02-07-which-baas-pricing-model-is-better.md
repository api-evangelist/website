---
layout: post
title: "Which BaaS Pricing Model Is Better?"
url: 'http://apievangelist.com/2013/02/07/which-baas-pricing-model-is-better/'
image: 'http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/blog/baas-trends.png'
---

<img src="https://s3.amazonaws.com/kinlane-productions/api-evangelist/trends/baas-trends.png" alt="" width="225" align="right" />

I’ve been processing a [conversation over at Branch][1], that was triggered by a story in TechCrunch by Sarah Perez([@sarahintampa][2]) called, “[StackMob Ratchets Up The Competition: Makes API Calls Free, Launches A Marketplace For Third-Party Mobile Services][3]”.

There are several layers to the convSteersation, the part I’m focusing on is about how BaaS providers are structuring their pricing, in which Sarah Perez writes:

> _StackMob is now making API calls free. This latter news will impact the competitive landscape, which includes startups like Parse, Kinvey and others, all of which have traditionally charged developers as API calls increase alongside an app’s popularity._

Making the argument that:

> _Today, developers have to have an understanding of how many API calls they make, and if an app becomes really successful, developers are penalized for that with increased pricing._

Sarah quotes StackMob CEO Ty Amell, saying that:

> _“this isn’t really all that fair, explaining that it doesn’t matter to StackMob how many API calls the app makes – the cost to them doesn’t really go up. “It doesn’t matter to us whether someone’s making a million API calls or 20 million API calls – the cost is fairly manageable on our parts. So we felt like this was a blocker to innovation on the developer’s side,” he explains. “And we feel like API calls are starting to become a commodity, where it’s really how can you provide value beyond that?”_

The conversation immediately begins on Twitter, with:

> **Steve Gershnik([@StackMobSteve][4]) of Stackmob** \- @stackmob doesn't charge for 'active users' either. No success tax for you.

> **Joe Chernov ([@jchernov][5]) of Kinvey** \- but you charge for features. In the end, everyone charges for something. It's business!

After this, the conversation moves to Branch. I’m not including full comments, because there is a lot of banter back and forth, discussing various claims BaaS providers make, that I feel are irrelevant to the more important, pricing story.

The conversation continues:

> ****Joe Chernov ([@jchernov][5]) of Kinvey**:**
If a developer prefers to pay by number of users, our model may work for them; if someone would rather buy features, then StackMob may make more sense. It's all good. Everyone has their own twist on pricing. Vendors should strive to highlight their own value without misrepresenting others'. Fair? Steve Gershnik (StackMob):
We don't charge per user. We don't charge per API call. We think those are outdated and archaic pricing models.

> **Miko Matsumura ([@mikojava][6]) of Kii:**
I respect what @StackMob is doing but in looking at their pricing page, isn't it just segmenting everyone into a free tier and a "custom" Enterprise tier?

> **Steve Willmott([@njyx][7]) of 3Scale:**
Which model is best in our experience depends a lot on what type of market you're serving - individual developers tend to like by the drop because (start cheaply and scale). Large companies tend to like predictability so they can budget properly.

> Box.net is a storage company - yet, for all their enterprise accounts storage is unlimited. Variable scared their customers. Instead they charge by number of seats/users - something their enterprise customers CAN predict.

> Thinking more abstractly: If a developer is successful, there will be some sort of increase in volume. Unless the PAAS service is truly magical that means extra cost for the PAAS provider.

> You can call this a success tax, but in my view what matters is not if there is more cost to the developer but if the unit cost goes down over time. I.e. As I succeed, I'm happy to pay you a bit more as long as you are not getting an increasing %age of the pie (and ideally if the %age is decreasing). If that %age increases I'll most likely ditch you for someone who offers me better terms at that point.

> **QuickBlox([@QuickBlox][8]):**
Our pricing model is per API calls as well, we do it like that because it is clear for developers (and for our business model), also allows to create apps and prototypes that, in case they are not successful, the developers won't be charged. according to @jchernov

Only Stackmob, Kinvey, Kii and Quickblox are represented in the [conversation on Branch][1]. So I wanted to see how each of the 20 BaaS providers I’m tracking on, structure their pricing:

  * [APIOMAT][9] \- Beta, can't find
  * [Appcelerator][10] \- Events, Notifications, API Calls, Storage, Emails, Support
  * [Applicasa][11] \- Beta, can't find
  * [Buddy][12] \- API Calls
  * [CloudMine][13] \- User
  * [CloudyRec][14] \- App, API Calls, File Storage
  * [FeedHenry][15] \- Can't Find
  * [Flurry][16] \- Beta, can't find
  * [Geoloqi][17] \- API Calls
  * [iKnode][18] \- API Calls, Data Storage
  * [Kii][19] \- API Calls, Data Storage, Push Notifications
  * [Kinvey][20] \- Users, API Calls
  * [MobDB][21] \- API Calls, Push Notifications, Data Storage
  * [Parse][22] \- API Calls, Push Notifications, Data Storage
  * [Proxomo][23] \- API Calls
  * [Quickblox][24] \- API Calls
  * [ScottyApp][25] \- Apps, Users, Database Size, Emails
  * [Sencha.io][26] \- Can't Find, Beta
  * [Stackmob][27] \- Features
  * [Urban Airship][28] \- Push Messages

I couldn’t find pricing for five of the BaaS providers, because they are in beta, but pricing by API call is definitely the preferred way for the rest of them, with 11 of the 15 using this approach. The rest of them charge based upon a mix of number of users, number of apps, data and file storage, push messages, and email messages. With Stackmob going with pricing based upon feature, add-on or premium services, which can also be from 3rd party services via the [StackMob marketplace][29].

Personally I don’t think there is one approach to API or BaaS pricing. Seems to me, that different models will work for different industries, companies and even at the application level. But I wanted to document this conversation for my [larger research project around the BaaS space][30]\--maybe I will have more opinions after I dive in deeper.

Let me know what you think about BaaS pricing.

   [1]: http://branch.com/b/apicalls-successtax
   [2]: https://twitter.com/sarahintampa
   [3]: http://techcrunch.com/2012/11/13/stackmob-ratchets-up-the-competition-makes-api-calls-free-launches-a-marketplace-for-third-party-mobile-services/
   [4]: https://twitter.com/StackMobSteve
   [5]: https://twitter.com/jchernov
   [6]: https://twitter.com/mikojava
   [7]: https://twitter.com/njyx
   [8]: https://twitter.com/QuickBlox
   [9]: http://www.apiomat.com/
   [10]: http://www.appcelerator.com/plans-pricing/
   [11]: http://www.applicasa.com/
   [12]: http://buddy.com/pricing/
   [13]: https://cloudmine.me/pricing/signup
   [14]: http://cloudyrec.com/welcome/pricing
   [15]: http://www.feedhenry.com/
   [16]: http://www.flurry.com/flurry-appCloud.html
   [17]: https://geoloqi.com/pricing
   [18]: http://iknode.io/pricing/
   [19]: http://www.kii.com/en/technology/Price
   [20]: http://www.kinvey.com/pricing
   [21]: https://www.mobdb.net/pricing
   [22]: https://parse.com/plans
   [23]: http://www.proxomo.com/Pricing
   [24]: http://quickblox.com/pricing/
   [25]: http://scottyapp.com/pricing
   [26]: http://www.sencha.com/products/io/
   [27]: https://www.stackmob.com/pricing/
   [28]: https://go.urbanairship.com/accounts/register/
   [29]: https://marketplace.stackmob.com/
   [30]: /trends/baas.php
