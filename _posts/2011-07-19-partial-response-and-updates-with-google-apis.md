---
layout: post
title: Partial Response and Updates with Google APIs
url: http://apievangelist.com2011/07/19/partial-response-and-updates-with-google-apis/
source: http://apievangelist.com2011/07/19/partial-response-and-updates-with-google-apis/
domain: apievangelist.com2011
image: 
---
{% include JB/setup %}<p>Last year google launched support for partial response and updates to a couple of the Google APIs.The goals was to significantly reduce network, memory, and CPU resources needed to work with Google APIs.Now Google is adding support for partial response, and an improved version of partial update, called patch, to a number of newer APIs including: Google Buzz API Google URL Shortener API Google Tasks API All APIs available in the Google APIs Discovery Service and the APIs Explorer supporting partial response and updates.The partial response algorithm works by supplying a fields query parameter to any API call that returns data, you can request specific fields.Here is an example request that returns only titles and timestamps of a users public Buzz activities: https://www.</p>
<center><p><a href="http://apievangelist.com2011/07/19/partial-response-and-updates-with-google-apis/" style='padding:25px; font-sze:18px; font-weight: bold;'>Read Full Story</a></p></center>
