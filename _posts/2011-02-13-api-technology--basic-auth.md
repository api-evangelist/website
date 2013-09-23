---
layout: post
title: "API Technology - Basic Auth"
url: 'http://apievangelist.com/2011/02/13/api-technology-basic-auth/'
image: ''
---

<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/basic-auth.png" alt="" width="250" align="right" />Basic Auth is a way for a web browser or application to provide credentials in the form of a username and password.

Because Basic Auth is integrated into [HTTP protocol][1] it is the easiest way for users to authenticate with a [RESTful API][2].

Basic Auth is easily integrated, however if [SSL][3] is not used, the username and password are passed in plain text and can be easily intercepted on the open Internet.

OAuth is a much better choice for RESTful API authentication, but Basic Auth is perfectly suited for APIs that are intended for a wider audience and do not give access to sensitive information.

######  Related articles

  * [Instapaper Launches Full API][4] (apievangelist.com)
  * [Google Adds API For URL Shortener and Link Analytics][5] (programmableweb.com)
  * [API Status Dashboard with Pingdom][6] (apievangelist.com)

   [1]: http://en.wikipedia.org/wiki/Hypertext_Transfer_Protocol (Hypertext Transfer Protocol)
   [2]: http://en.wikipedia.org/wiki/Representational_State_Transfer (Representational State Transfer)
   [3]: http://en.wikipedia.org/wiki/Transport_Layer_Security (Transport Layer Security)
   [4]: http://blog.apievangelist.com/2011/02/10/instapaper-launches-full-api/
   [5]: http://blog.programmableweb.com/2011/01/11/google-adds-api-for-url-shortener-and-link-analytics/
   [6]: http://blog.apievangelist.com/2011/02/12/api-status-dashboard-with-pingdom/
