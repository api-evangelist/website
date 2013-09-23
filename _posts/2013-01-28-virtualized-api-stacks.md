---
layout: post
title: "Virtualized API Stacks"
url: 'http://apievangelist.com/2013/01/28/virtualized-api-stacks/'
image: 'http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/blog/Virtualized-API-Stacks.png'
---

<img class="c1" src="https://s3.amazonaws.com/kinlane-productions/api-evangelist/Virtualized-API-Stacks.png" alt="" width="325" align="right" />

Up until now we tend to think of APIs individually--we approach integration in terms of the Twilio API, Twitter API or the Facebook API. But as the number of [public APIs has grown beyond 8K][1], and an [unknown amount of internal and partner APIs][2] become available, we are seeing new patterns of [aggregation][3] and [interoperability][4] emerge from companies like [Singly][5], but also seeing [automation][6] be added into the mix by companies like [Temboo][7], and entire backend stacks from providers like Parse.

These new aggregated or backend stacks of API driven resources can be as general as object and key-value stores, user management and other developer commodities we see [backend as a service providers][8] (BaaS) bring to the table, or they can be very personal like the photos Singly is aggregating across Flickr, Facebook and Instagram and with friends and followers across Facebook, Twitter and LinkedIn.

As I see these new aggregate and BaaS providers emerge, at an ever increasing pace, I can’t help but think--this still isn’t fast enough (its my nature, you should try being me). If I want common mobile developer resources I can adopt one of these new BaaS platforms like [Kinvey][9] or [Parse][10], or if I need personal and social resources, which have [become part of the fabric of web and mobile apps][11], I can go to Singly. But what if I want a more specialized network, say just for [education][12]? I might need user management, object storage, key-value storage, access to commons social tools like friends and photos across multiple social networks, but I also need access to open courseware, teacher and student directories all via a very secure, auditable, efficient stack tailored just for K-12? I will have to wait, for the next wave of startups to emerge.

While in NYC on Friday I had a great discussion with Temboo about virtualization. Not just the virtualization we’ve come to depend on with cloud computing--which is the virtualization of compute, storage, and database resources, but the [virtualization of network resources][13] and [software defined networking][14]. Companies like [Nicira][15], [Pluribus Networks][16], [Anuta Networks][17], [Arista][18], [and Vyatta][19] are emerging with new products that are allowing the virtualization of networking resource into new and meaningful network stacks for any possible implementation that you can imagine.

After these conversation with the Temboo team, over the weekend I continued to think about the potential of virtualized API stacks. Why can’t I assemble my own API stack? Why do I have to go to each API individually, or wait for new Singlys' to emerge in other verticals? Why can’t I assemble Parse, Singly, Twilio, Schoology, SendGrid into a virtualized API stack that provides not just ease of use, but the security I need to deploy a backend tailored just for K-12 education?

In this vision of the future, API providers could focus on what they do best, and not worry about every use case out there. Providers like Singly, Temboo, Parse can build abstracted layers on top of this. With this abstraction I wouldn’t be limited to just the friends and followers features on Twitter or Facebook, I could take advantage of the next generation of friend discovery tools like what Singly is delivering--in addition to the value of individual API providers.

<img class="c1" src="https://s3.amazonaws.com/kinlane-productions/api-evangelist/trends/interoperability-trends.png" alt="" width="250" align="right" />

With a virtualized approach, I could build the stack that is most meaningful for my internal, partner or public developers and if one piece of my stack is proving unreliable, I can replace it with another. APIs resources would be further commoditized, required to provide JSON definitions of their interfaces (or die a quick death), which virtual API stack platforms could use to discover and offer API resources. [API ranking][20] algorithms would emerge allowing anyone to make sure they were discovering, selecting and using the best of breed API resources in the areas that matter for any vertical.

With a virtualized API stack I could launch any specialized set of resources that I desired from the best of breed providers out there. I could blend private and public resources together and in return offer them for use in private or public environments, further blurring the lines of what is an API and how they are consumed.

As we see APIs continue to become a driving force in government, healthcare and education and bridge the online and physical worlds via our [automobiles][21], homes, [buildings][22] and further grow within healthcare via the [quantified self][23], potentially [disrupt manufacturing with 3D printing][24] and drive everything around us with the [internet of things][25]\--the manual assembling of individual or even aggregated API stacks won’t be enough. We will need the ability to virtualize APIs stacks for any purpose within hours, not months or years.

   [1]: http://www.programmableweb.com/apis/directory
   [2]: /2013/01/24/estimating-the-number-of-non-public-apis/ (unknown amount of internal and partner APIs)
   [3]: /trends/aggregation.php (aggregation)
   [4]: /trends/interoperability.php (interoperability)
   [5]: http://singly.com (Singly)
   [6]: /trends/automation.php (automation)
   [7]: http://temboo.com (Temboo)
   [8]: /trends/baas.php (backend as a service)
   [9]: http://kinvey.com
   [10]: http://parse.com (Parse)
   [11]: http://blog.apievangelist.com/2012/11/13/the-api-fabric-for-next-generation-of-apps/ (fabric of mobile and web apps)
   [12]: http://hackeducation.com (education)
   [13]: http://en.wikipedia.org/wiki/Network_virtualization (virtualization of network resources)
   [14]: http://en.wikipedia.org/wiki/Software-defined_networking (software defined networking)
   [15]: http://nicira.com/
   [16]: http://www.pluribusnetworks.com/
   [17]: http://www.anutanetworks.com/
   [18]: http://www.aristanetworks.com/en/solutions/network-virtualization
   [19]: http://www.vyatta.com/solutions/virtual
   [20]: http://theapistack.com/ranking.html (API Ranking)
   [21]: http://blog.apievangelist.com/trends/automobiles.php (automobiles)
   [22]: http://blog.apievangelist.com/trends/buildings.php (buildings)
   [23]: http://blog.apievangelist.com/trends/quantified-self.php (quanitfied self)
   [24]: http://blog.apievangelist.com/trends/3d-printing.php (disrupt manufacturing with 3D printing)
   [25]: http://blog.apievangelist.com/trends/internet-of-things.php (internet of things)
