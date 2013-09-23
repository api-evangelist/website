---
layout: post
title: "Deploy and Manage a RESTful API with CodeIngiter and 3Scale"
url: 'http://apievangelist.com/2011/09/05/deploy-and-manage-a-restful-api-with-codeingiter-and-3scale/'
image: 'http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/blog/3scale-500.png'
---

[<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/api-service-providers/3scale-logo.jpg" alt="" width="250" align="right" />][1]At Mimeo, my API developers were running into problems integrating with our cloud print API, I needed a fast way to virtualize and deploy an API built on top of my existing REST API.  A quick and dirty way I could research and develop new APIs, launch, measure and manage without getting IT involved.  

So I [virtualized four document APIs][2] using the [CodeIgniter open-source PHP web framework][3], [Amazon EC2][4], [3Scale self-service API management service][5] and [Mimeo Connect Cloud Print API][6].

First I launched a copy of the CodeIgniter framework on my existing Amazon EC2 instance, configured mod_rewrite to handle my URLs, and wrote seven API methods dedicated to printing just one type of document, like a poster.  I now had a simple RESTful API that handled requests, and returned XML and JSON responses.

[<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/api-tools/codeigniter-logo.jpg" alt="" width="200" align="right" />][7]I need a quick way to manage access to my API and measure its usage.  So I would know who was using it, how they were using it, and if it was worth while to keep the API and put more resources into it.  I selected [3Scale API management][8], one of two free, self-service API mangement platforms out there.  The other is [Mashape][9], but they are still in BETA, so 3Scale was the only other solution I could deploy for free, and scale as I needed when things were successful.

I deployed the 3Scale PHP connector on my Amazon EC2 instance as part of the CodeIgniter REST framework.  I then launched my 3Scale self-service API area, which provides me with:

  * Self-Service Developer Registration / Login / Key Management
  * Documentation
  * Forum

   [1]: http://www.3scale.net/
   [2]: http://apievangelist.com/2011/09/05/virtualized-document-printing-apis/ (virtualized four document APIs)
   [3]: http://codeigniter.com/ (CodeIgniter)
   [4]: http://apievangelist.com/apis/amazon_ec2.php (Amazon EC2)
   [5]: http://www.3scale.net (3Scale API Management Service)
   [6]: http://developer.mimeo.com (Mimeo Connect Cloud Print API)
   [7]: http://codeigniter.com/
   [8]: http://apievangelist.com/serviceproviders/3scale.php (3Scale API Management)
   [9]: http://apievangelist.com/serviceproviders/mashape.php (Mashape)
