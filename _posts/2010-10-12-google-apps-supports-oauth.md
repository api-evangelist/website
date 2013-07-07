---
layout: post
title: Google Apps Supports OAuth
url: http://apievangelist.com2010/10/12/google-apps-supports-oauth/
source: http://apievangelist.com2010/10/12/google-apps-supports-oauth/
domain: apievangelist.com2010
image: 
---
{% include JB/setup %}<p>Google Apps recently began supporting OAuth authorization when connecting to the Google Apps API.OAuth will make integration with the Google Apps platform much more secure by not requiring administrators to share their username and password with third party applications.The advantages to using OAuth are: OAuth is more secure: OAuth tokens can be scoped and set to expire by a certain date, making them more secure than using the ClientLogin mechanism.OAuth is customizable: Using OAuth, you can create tokens that scripts may only use to access data of a particular scope when calling Google Apps APIs.For instance, a token set to call the Email Migration API would not be able to use your login credentials to access the Google Apps Provisioning API.</p>
<center><p><a href="http://apievangelist.com2010/10/12/google-apps-supports-oauth/" style='padding:25px; font-sze:18px; font-weight: bold;'>Read Full Story</a></p></center>
