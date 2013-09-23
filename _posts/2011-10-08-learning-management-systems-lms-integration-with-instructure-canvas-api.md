---
layout: post
title: "Learning Management Systems (LMS) Integration with Instructure Canvas API"
url: 'http://apievangelist.com/2011/10/08/learning-management-systems-(lms)-integration-with-instructure-canvas-api/'
image: 'http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/blog/Instructure_logo.jpg'
---

[<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/api-evangelist/instructure/Instructure_logo.jpg" alt="" width="250" align="right" />][1]

I had a great response to my [Learning Management System (LMS) APIs round-up][2] last week after [Startup Weekend Seattle EDU][3]. After posting I quickly updated with another LMS suggestion I got for [Sakai][4]. Then a couple days ago the PR director for [Instructure][1] introduced me to their [LMS platform, Canvas][5].

Canvas is a open-source LMS created by Instructure and released under the AGPLv3 license. Instructure also provides a cloud version, with all the features of the open source version of Canvas, but comes with hosting, mobile apps, services integration, and automated provisioning.

[<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/api-evangelist/instructure/Instructure-LMS-Classroom.png" alt="" width="250" align="right" />][1]

The [Canvas LMS includes a REST API][6], using OAuth for authentication, enforces SSL, with all API responses in JSON. The API is currently under development and many areas of the application are still unavailable via the external API, but there are still quite a few methods available for the LMS already, and more to come.

The Canvas solution appears to have all the latest features of a modern software as a service platform. They provide an open-source version, as well as a hosted platform.  Its built with Ruby, on a PostGres database, and runs on the Amazon Cloud.  The API is simple, and they intend to expose all features of the core LMS via the API, with all documentation hosted at Github.

When the API is complete, I’d definitely say that the Instructure Canvas and API is the most robust LMS solution I’ve come across so far. When they finish their API, and pull together a community around the API, they will definitely be a strong force in the LMS space.

   [1]: http://www.instructure.com/ (Instructure)
   [2]: /2011/10/02/learning-management-system-(lms)-apis/ (Learning Management System API Roundup)
   [3]: http://blog.programmableweb.com/2011/09/30/40-education-apis-for-startup-weekend-seattle-edu/ (Startup Weekend Seattle EDU)
   [4]: https://confluence.sakaiproject.org/dosearchsite.action?queryString=api (Sakai)
   [5]: http://www.instructure.com/ (LMS Platform Canvas)
   [6]: https://canvas.instructure.com/doc/api/index.html (Canvas MLS includes a REST API)
