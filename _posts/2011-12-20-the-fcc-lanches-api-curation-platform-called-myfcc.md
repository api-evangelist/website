---
layout: post
title: "The FCC Lanches API Curation Platform Called MyFCC"
url: 'http://apievangelist.com/2011/12/20/the-fcc-lanches-api-curation-platform-called-myfcc/'
image: 'http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/blog/My-FCC-Logo.png'
---

[<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/api-evangelist/fcc/My-FCC-Logo.png" alt="" align="right" />][1]

The FCC just launched a new platform that allows anyone to create, save and manage a customized page, built from widgets that pull content from FCC APIs, called [MyFCC][1]. 

At first glance [MyFCC][1] might look like just another dashboard or start page, but it goes much further, as an API curation platform.

To understand, you have to go back to the beginning and see the scope of the problem being solved. To deliver on its promise for a more open government, the FCC didn't just want a new website, they needed a platform. To do this the FCC embraced an API-driven methodology while building their web site, meant to standardize the way they deliver information between internal groups, government agencies and with the public.

[<img src="http://kinlane-productions.s3.amazonaws.com/api-evangelist/seabourne-inc/Seabourne.png" alt="" width="250" align="right" />][2]

At the time, the managing FCC director Steve Van Roekel, partnered with [Seabourne][2] to architect a platform that could deliver on this vision.

The new FCC web site would start with Drupal, providing a content management system (CMS) that would allow the FCC to focus on getting a handle on its content, centralizing it, preparing it to be shared with other departments, agencies and the public. The federal government is drowning in content, so the entry, storage and management of this content was the first problem to solve, and an open-source platform like Drupal, was an ideal solution.

The new Drupal web site provided public access to the content, but the FCC needed to allow sharing of content with other departments, agencies and allow the public to get at the raw data for re-use.

[<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/api-evangelist/fcc/My-FCC-Available-Widgets.png" alt="" width="250" align="right" />][1]

> _"Everyone is talking about opening up data with APIs, to me it makes more sense to focus on opening up content using APIs.", says Mike Reich, owner of Seabourne._

So Seabourne developed the [Content API module for Drupal][3], providing a plug-and-play API, not just for the FCC website, but for any Drupal driven website.

Then in April, the FCC launched their API driven content platform, stating that “[Everything should be an API][4]”. In doing so the FCC did two very significant things:

  * Got control over their content using an open-source content management tool
  * Made their content accessible inter-department, inter-agency and with the public using APIs

Now with MyFCC the FCC is providing a dashboard that allows anyone to curate content that is made available via the FCC’s API. Centralized content, opened up with APIs, bundled with curation tools opens up lot of potential for data journalists, analysts, scientists and other average users to derive deeper meaning from FCC operations.

All of this potential is made possible through a healthy dose of open source Drupal CMS, open source Drupal modules, open data, and open APIs. That is a lot of open, and shows the commitment of the FCC.

[<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/api-evangelist/fcc/My-FCC-Topic-Watcher.png" alt="" width="250" align="right" />][1]

I sat down with Mike, while in DC in October, when he first introduced me to [Cumula ][5], the framework that drives MyFCC. During their work with the FCC, they have been committing the [Cumula framework to Github][5], planting the seeds for a much larger vision of what the framework could do.

Cumula has the potential to act as curation platform for any single or group of APIs. The MyFCC implementation is very tailored to serving up the FCC content, but the platform can act as a visual builder and dashboard for any topical area. For example, the platform could be setup with widgets that pull medical content from various health, science and medical APIs, allowing users to create custom dashboards around the medical information most important and relevant to them.

[Cumula][6] is to API curation as [Apigee console][7] is to [API exploration][8], [Google API Discovery Service][9] is to [API discovery][10], and [Swagger][11] is to interactive API documentation. It has the potential to be the platform that the world uses to discover, pull, curate and make sense of the flood of content and data we are only just beginning to drown in, with this new API driven economy.

   [1]: http://my.fcc.gov/ (MyFCC)
   [2]: http://seabourneinc.com/ (Seabourne)
   [3]: http://seabourneinc.com/projects/contentapi/ (Content API Drupal Module)
   [4]: http://blog.programmableweb.com/2011/04/06/everything-should-be-an-api-says-fcc/ (Everything Should Be An API)
   [5]: https://github.com/Cumula/framework (Cumula Framework to Github)
   [6]: https://github.com/Cumula/framework (Cumulu)
   [7]: https://apigee.com/console/twitter (Apigee Console)
   [8]: /2011/03/24/explorers-open-api-access-beyond-developers/ (API exploration)
   [9]: http://code.google.com/apis/discovery/ (Google API Discovery Service)
   [10]: /2011/05/21/google-apis-discovery-service/ (API discovery)
   [11]: http://swagger.wordnik.com/ (Swagger)
