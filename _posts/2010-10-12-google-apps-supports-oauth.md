---
layout: post
title: "Google Apps Supports OAuth"
url: 'http://apievangelist.com/2010/10/12/google-apps-supports-oauth/'
image: ''
---

<img src="http://kinlane-productions.s3.amazonaws.com/OAuth.png" alt="" width="250" align="right" />[Google Apps][1] recently began supporting OAuth authorization when connecting to the [Google Apps API][2].

OAuth will make integration with the Google Apps platform much more secure by not requiring administrators to share their username and password with third party applications.

The advantages to using OAuth are:

  * OAuth is more secure: OAuth tokens can be scoped and set to expire by a certain date, making them more secure than using the ClientLogin mechanism.
  * OAuth is customizable: Using OAuth, you can create tokens that scripts may only use to access data of a particular scope when calling Google Apps APIs. For instance, a token set to call the Email Migration API would not be able to use your login credentials to access the Google Apps Provisioning API.
  * OAuth is an open standard: OAuth is an open source standard, making it a familiar choice for developers to work with.
The Google Apps API services that support OAuth are:
  * Provisioning API
  * Email Migration API
  * Admin Settings API
  * Calendar Resource API
  * Email Settings API
  * Audit API
OAuth for authentication is more accepted by developers, and it makes many IT administrators much more comfortable with allowing third party integration with their Google Apps Premier, Education and Government editions.

To learn more about the OAuth standard, visit .

   [1]: http://www.google.com/a/
   [2]: http://code.google.com/googleapps
