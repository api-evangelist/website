---
layout: post
title: "Building Your Business Around Google or Any Other APIs"
url: 'http://apievangelist.com/2011/05/28/building-your-business-around-google-or-any-other-apis/'
image: ''
---

I'm reading all the starred items in my Google Reader about [Google's latest closing of APIs][1], most notably [Google Translate API][2]. There are some pretty sensational headlines:<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/api-evangelist/pitchforks-torches-mob.jpg" alt="" width="250" align="right" />

  * [Google pulls the rug out from under web service API developers, nixes Google Translate and 17 others][3]
  * [GOOGLE IS NOT YOUR DADDY (OR LONG TERM RELIANCE ON APIS IS AS BAD AS OUTSOURCING)][4]
  * [Google Translate API to Go Kaputt in December][5]
I don't feel the need to defend Google here, I wish to only defend APIs against people blaming them for what is the fault or responsibility of developers and API owners. I see this same line of attacks on APIs anytime an API company makes a change in their strategy, and developers freak out!

**First**, let's start with the claims that developers are having the rug pulled out from under them, and you can't build a business on APIs!

<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/TweetDeck-Screenshot.png" alt="" width="250" align="right" />This week I was fortunate enough to hear [Mark Suster of GRP Partners][6] talk at [Gluecon on Cloud Computing: Challenges and Opportunities over the Next Five Years][7]. One important point he made about business platforms and startups (ie. TweetDeck) is **you need to have multiple data sources**. Without expanding to LinkedIn, Buzz, and Facebook TweetDeck would have been left with only a single data source, and left completely vulnerable.

This is a pretty basic concept when it comes to business. If I start a corner deli, and buy my food from a single food distribution company that delivers every Thursday by truck. Then one Thursday the truck doesn't come, and i'm left for the weekend without any food for my restaurant. Is it valid for me to claim that food distribution companies are no way to build a restaurant?

Even in the case of TweetDeck, using a very unique API (ie. Twitter), they had to diversify with other services. If your building a business around Google Translate API, what sort of plan B and C do you have built into your code? Are you using any of the free or paid solutions out there like [Translated.net][8], [WordLingo][9], [Microsoft Translator][10], [Apertium][11], or [ICanLocalize][12]?

Please don't blame APIs because developers don't have a business strategy, or because bloggers are looking for a sensational headline.

**Second**, let's take a look at Google's approach to Google Translate API. The primary reason Google gave for depracting Google Translate API was:

> _Due to the substantial economic burden caused by extensive abuse, the number of requests you may make per day will be limited and the API will be shut off completely on December 1, 2011._

I can't help but think, this problem could have been curbed, by bringing Google Translate API under metered billing using the [Google Console][13],as other APIs appear to be heading. This would give a low ceiling of free daily calls on the API, then make users pay for more access.

Except I really don't think Google wants to make its money from translation services, they are focused on where translation supports their core business. World Domination! Wait, no maybe it is search.

If you notice translation is still available in other areas like Google Docs API for translating documents on upload, and in Gmail for translating emails, and Chrome for translating web pages. And of course you can still use the [web interface for Google Translate][14].

<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/google/google-translate.png" alt="" width="200" align="right" />So you will still see Google Translate in use where it supports Google's core business. I can see just about any other business making a similar decision.

Also, Google did reach out to communicate the impending deprecation, they called my girlfriend [Audrey Watters][15], and briefed her on the plan. I assume they reached out to others as well.

I would add, that Google could do a better job of communicating their roadmap of various APIs and how they will work to support the core Google set of services, or be offered as a service by themselves. As I watch the Google API ecosystem being pulled together and organized, I still can't quite tell whether the vision is to purely serve the primary Google vision, or provide a wide set of APIs that developers can build businesses on, as recent moves with Google Console might suggest.

######  Related articles

  * [Google API House Cleaning][16] (apievangelist.com)
  * [The Google Translate API has been officially deprecated][17] (code.google.com)

   [1]: http://googlecode.blogspot.com/2011/05/spring-cleaning-for-some-of-our-apis.html (Goog'es latest closing of APIs)
   [2]: http://code.google.com/apis/language/ (Google Language APIs)
   [3]: http://www.zdnet.com/blog/burnette/google-pulls-the-rug-out-from-under-web-service-api-developers-nixes-google-translate-and-17-others/2284 (Google pulls the rug out from under web service API developers, nixes Google Translate and 17 others)
   [4]: http://www.webiphany.com/2011/05/27/google-is-not-your-daddy-or-long-term-reliance-on-apis-is-as-bad-as-outsourcing/ (Google is not your daddy or long term reliance on APIs is as bad as outsourcing)
   [5]: http://blog.programmableweb.com/2011/05/27/google-translate-api-to-go-kaputt-in-december (Google Translate aPI to Go Kaputt in December)
   [6]: http://www.youtube.com/watch?v=04AG3UHUIJE (Mark Suster)
   [7]: http://gluecon.com/2011/?page_id=16 (Glue Conference Mark Suster)
   [8]: http://www.translated.net/en/translation-api (Translated.net)
   [9]: http://www.worldlingo.com/en/products/worldlingo_api.html (Wordlingo)
   [10]: http://www.microsofttranslator.com/dev/ (Microsoft Translator)
   [11]: http://wiki.apertium.org/wiki/Apertium_web_service (Apertium)
   [12]: http://www.icanlocalize.com/site/ (ICanLocalize)
   [13]: http://blog.apievangelist.com/2011/05/21/google-apis-console/ (Google Console)
   [14]: http://translate.google.com/ (web interface for Google Translate)
   [15]: http://www.hackeducation.com (Audrey Watters)
   [16]: http://blog.apievangelist.com/2011/05/27/google-api-house-cleaning/
   [17]: http://code.google.com/intl/de-DE/apis/language/translate/overview.html
