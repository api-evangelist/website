---
layout: post
title: "Business of Google APIs 2011"
url: 'http://apievangelist.com/2011/12/21/business-of-google-apis-2011/'
image: 'http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/blog/google_code.jpg'
---

[<img src="http://kinlane-productions.s3.amazonaws.com/google/google_code.jpg" alt="" width="250" align="right" />][1]

[ProgrammableWeb says Google has 94 APIs][2]. I roughly count about [75 going through Google Code][1]. I’m more concerned with public web APIs, and Google has Android, Chrome and other non-web APIs, so its hard to tell.

In any case I would consider Google to the largest public web API owner around. I don’t think any other single provider, owns the number of, as well as size of public APIs, that Google does. As with any leading API providers I think there is a lot to learn in studying their approach to API deployment and management.

With this in mind I wanted to take a look at the Business of Google APIs in 2011 as one of my year-end, API reflection posts. I think there are some important lessons to be learned from the work Google did over 2011, to get their API business in order.

Google was already setting the theme for 2011, with the [launch of Google Console in November 2010][3]. The [Google API Console][4] helps developers manage their Google API usage across all of thier sites and apps. It was clear, Google was not just looking for a way to get a handle on how they deploy and manage large numbers of APIs, they were acknowledging developers needed a way as well.

[<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/google/Google-APIs-Console-Dashboard.png" alt="" width="300" align="right" />][5]

[Google API Console][5] centralized how developers managed the Google APIs they used, traffic generated via these APIs, introduced billing management for some APIs, and provided developers with project and team building tools.  Google supports 30 APIs inside of the API Console now.

In 2011 Google also worked to make their [APIs more discoverable for developers][6] with the launch [Google API Discovery Service][7]. The [Google API Discovery Service][8] provides a set of web APIs for discovering metadata across Google APIs by delivering a JSON-based API that provides a directory of supported Google APIs, and a machine-readable discovery document for each API.

[<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/google/google-discover-file-cabinet.png" alt="" align="right" />][8]

Now developers can integrate Google API discovery into client libraries, IDE plugins and other tools, making it easier to discover the API they need. After providing an API discovery service, Google followed another 2011 trend around deploying the [Google API Explorer][9].

Like other API explorers, [Google API Explorer][10] allows users to make calls and explore REST APIs using a web interface, allowing anyone to start using an API without writing any code, even when authentication using Basic Auth or OAuth is required.

API explorers have done a lot to improve the time it takes for developers to get up and running using an API, but nothing beats good quality code samples, and Google put some serious effort into standardized code samples that can be used across Google APIs, in multiple programming languages:

  *

   [1]: http://code.google.com/more/
   [2]: http://www.programmableweb.com/apis/directory/1?company=Google (ProgrammableWeb says Google has 94 APIs)
   [3]: http://googlecode.blogspot.com/2010/11/introducing-google-apis-console-and-our.html (launch of Google Console in 2010)
   [4]: https://code.google.com/apis/console/ (Google API Console)
   [5]: http://blog.apievangelist.com/2011/05/21/google-apis-console/ (Google API Console)
   [6]: http://googlecode.blogspot.com/2011/05/google-apis-discovery-service-one-api.html (Google APIs more discoverable)
   [7]: http://code.google.com/apis/discovery/ (Google API Discovery Service)
   [8]: http://blog.apievangelist.com/2011/05/21/google-apis-discovery-service/ (Google API Discover Service)
   [9]: https://code.google.com/apis/explorer/ (Google API Explorer)
   [10]: http://blog.apievangelist.com/2011/03/08/google-api-explorer/ (Google API Explorer)
