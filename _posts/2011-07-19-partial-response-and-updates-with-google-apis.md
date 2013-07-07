---
layout: post
title: 'Partial Response and Updates with Google APIs'
url: 'http://apievangelist.com2011/07/19/partial-response-and-updates-with-google-apis/'
image: ''
---
{% include JB/setup %}
<img src="http://kinlane-productions.s3.amazonaws.com/api-evangelist/puzzle-partial.png"  width="250" align="right" /><a title="last year google launched support for partial responses and updates" href="http://googlecode.blogspot.com/2010/03/making-apis-faster-introducing-partial.html">Last year google launched support for partial response and updates</a> to a couple of the Google APIs. The goals was to significantly reduce network, memory, and CPU resources needed to work with Google APIs.
Now Google is <a title="adding support" href="http://googlecode.blogspot.com/2011/07/lightning-fast-performance-tips-for.html">adding support</a> for partial response, and an improved version of <a title="partial update, called patch" href="http://code.google.com/apis/buzz/v1/performance.htmlpatch">partial update, called patch</a>, to a number of newer APIs including:
<ul >
     <li>
          <a title="Google Buzz API" href="http://code.google.com/apis/buzz/">Google Buzz API</a>
     </li>
     <li>
          <a title="Google URL Shortener API" href="http://code.google.com/apis/urlshortener/">Google URL Shortener API</a>
     </li>
     <li>
          <a title="Google Tasks API" href="http://code.google.com/apis/tasks/">Google Tasks API</a>
     </li>
</ul>All APIs available in the <a title="Google APIs Discovery Service" href="http://blog.apievangelist.com/2011/05/21/google-apis-discovery-service/">Google APIs Discovery Service</a> and the <a title="Google APIs Explorer" href="http://blog.apievangelist.com/2011/05/21/google-apis-explorer/">APIs Explorer</a> supporting partial response and updates.
The partial response algorithm works by supplying a fields query parameter to any API call that returns data, you can request specific fields.
Here is an example request that returns only titles and timestamps of a user's public Buzz activities: <a href="http://blog.apievangelist.com/2011/05/21/google-apis-explorer/">https://www.googleapis.com/buzz/v1/activities/kinlane@gmail.com/@public?alt=json&amp;pp=1&amp;fields=items(title,updated)</a>
A full response for Buzz activity would be around 53KB and the partial response is 3KB, a reduction of almost 95%!
You can try out both partial response and patch algorithms in the <a title="Google APIs Explorer" href="https://code.google.com/apis/explorer/">Google APIs Explorer</a>. In partial responses, the fields parameter is available for most methods. You can easily tell which are partial update methods by the .patch in the method name. Both the fields parameter and the patch method on the tasklist resource in the APIs explorer.
Partial response and updates are a great way to make APIs more efficient for devices with limited connectivity, as well as making API platforms operate as efficiently as they can by delivering only what information is needed.
Google is in a unique position with the number of APIs they offer, volume of API calls they manage, and wide audience they deliver to. We can all learn a lot from watching them organize their APIs, and apply elements of their approach to our own API ecosystems.
