---
layout: post
title: "Virtualized Document Printing APIs"
url: 'http://apievangelist.com/2011/09/05/virtualized-document-printing-apis/'
image: 'http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/blog/mimeo-logo-400.png'
---

[<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/mimeo-logo.jpg" alt="" width="200" align="right" />][1]Even though I cover the entire industry around APIs here on [API Evangelist][2], I also am the API Evangelist for [Mimeo Connect][3].   Mimeo is a printing API that allows you to print a wide variety of business documents, using your Mimeo.com account.  Its pretty powerful stuff, if you think about it, an API that is connected to 3 print facilities.  

The API seems pretty straightforward at first glance, but developers seem to be encountering three major obstacles:

  * **Mimeo.com Accounts** \- Users don’t like having to get a developer account as well as sandbox and live Mimeo.com accounts to work with the API
  * **Mimeo Documents** \- Developers don’t really have time to build and define the documents before integration, they just want to print a specific document, and pass some settings to change it up.
  * **Sandbox and Live Environments** \- It is great that Mimeo has sandbox and live environments, but developers were expected to maintain two separate environments, just to use the system.

[<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/mimeo/posters-sample.png" alt="" width="150" align="right" />][4] These three areas proved to be the difference between some users adopting, and others walking away.  There was too much work in navigating the world of Mimeo accounts and documents.  This isn’t hard if your already a Mimeo web to print user, but if your a developer you just want to print.  

So I created four virtualized print APIs.   I took a REST framework and deployed four separate “[document printing APIs][5]”:

  * [Poster Printing API][6]
  *

   [1]: http://www.mimeo.com/
   [2]: http://www.apievangelist.com (API Evangelist)
   [3]: http://developer.mimeo.com (Mimeo Connect)
   [4]: http://mimeoconnect.3scale.net/wiki/poster-printing-api
   [5]: http://mimeoconnect.3scale.net/ (Document Printing APIs)
   [6]: ../../2011/09/05/api-stack-large-format-printing-with-the-mimeo-connect-poster-printing-api/ (Poster Printing API)
