---
layout: post
title: Deploy and Manage a RESTful API with CodeIngiter and 3Scale
url: http://apievangelist.com2011/09/05/deploy-and-manage-a-restful-api-with-codeingiter-and-3scale/
source: http://apievangelist.com2011/09/05/deploy-and-manage-a-restful-api-with-codeingiter-and-3scale/
domain: apievangelist.com2011
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/blog/3scale-500.png
---
{% include JB/setup %}<p>At Mimeo, my API developers were running into problems integrating with our cloud print API, I needed a fast way to virtualize and deploy an API built on top of my existing REST API. A quick and dirty way I could research and develop new APIs, launch, measure and manage without getting IT involved. So I virtualized four document APIs using the CodeIgniter open-source PHP web framework, Amazon EC2, 3Scale self-service API management service and Mimeo Connect Cloud Print API.First I launched a copy of the CodeIgniter framework on my existing Amazon EC2 instance, configured mod_rewrite to handle my URLs, and wrote seven API methods dedicated to printing just one type of document, like a poster. I now had a simple RESTful API that handled requests, and returned XML and JSON responses.</p>
<center><p><a href="http://apievangelist.com2011/09/05/deploy-and-manage-a-restful-api-with-codeingiter-and-3scale/" style='padding:25px; font-sze:18px; font-weight: bold;'>Read Full Story</a></p></center>
