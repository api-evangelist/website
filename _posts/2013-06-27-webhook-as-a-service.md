---
layout: post
title: "Webhook as a Service"
url: 'http://apievangelist.com/2013/06/27/webhooks-as-a-service/'
image: 'http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/blog/webscript-io-logo.png'
---

[<img class="c1" src="https://s3.amazonaws.com/kinlane-productions/api-evangelist/webscript/webscript-io-logo.png" alt="" align="right" />][1]

While [I was at API Days this weekend in San Francisco][2], I managed to catch a handful of talks Saturday afternoon after I landed at OAK. While listening to each talk, I kept hearing one technical API building block, over and over--[webhook][3].

Webhooks are a common way for API providers to make API integration a two ways street for consumer. Developers, or even non-developers, can setup webhooks via common API platforms, and receive notifications about different events and activities that occur.

Webhooks are also a common tool for [API automation and reciprocity platforms][4] like [Zapier][5] and [IFTTT][6]. Users can setup webhooks, that respond to just about any action across multiple, API driven platforms.

[<img class="c1" src="https://s3.amazonaws.com/kinlane-productions/api-evangelist/webscript/webscripts-io-webhook-script-example.png" alt="" width="325" align="right" />][1]

After hearing webhooks mentioned so often, I wondered if anyone out there is offering web hook as a service (WHaaS) (LOL). Sure enough, John Sheehan ([@johnsheehan][7]) pointed me to [webscript.io][1].

Webscripts are short scripts, written in Lua, that run in the cloud servers, and can respond to any HTTP requests.

Exactly what I was looking for. I had heard of webscript.io before, but for some reason it didn't stick in my mind. It is precisely the simple approach I was looking for, and has many common examples like sending emails, counters, parsing RSS and Tweeting.

I really like dead simple implementations like [webscript.io][1], that solve real world problems in such granular, yet powerful ways. Nice work [@smarx][8].

   [1]: https://webscript.io/
   [2]: http://www.apievangelist.com/2013/06/23/a-great-time-at-api-days-san-francisco/
   [3]: http://en.wikipedia.org/wiki/Webhook
   [4]: http://reciprocity.apievangelist.com/companies.html
   [5]: http://reciprocity.apievangelist.com/companies-detail.html?id=38
   [6]: http://reciprocity.apievangelist.com/companies-detail.html?id=39
   [7]: https://twitter.com/johnsheehan
   [8]: https://twitter.com/smarx
