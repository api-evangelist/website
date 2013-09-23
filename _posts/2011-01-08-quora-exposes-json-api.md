---
layout: post
title: "Quora Exposes JSON API"
url: 'http://apievangelist.com/2011/01/08/quora-exposes-json-api/'
image: ''
---

<img src="http://kinlane-productions.s3.amazonaws.com/quora-logo.jpg" alt="" width="250" align="right" />Quora has exposed a [JSON][1]-based data API that allows users to access data about a currently logged-in user.

To request particular fields about the currently logged-in user, you can add fields to a query string and append to [http://api.quora.com/api/logged_in_user][2].

Currently supported fields include:

  * Inbox
  * Followers
  * Following
  * Notifs
Here is an example call: 

This will return Inbox and Notification related information for the authenticated user.

This is not a full-blown API release by Quora. Quora engineer Edmond Lau posted information on Quora about the API, stating that it is in its alpha stage and is only meant to support existing [Quora Chrome][3] and [Quora Firefox extensions][3].

Even though it doesn't have all the supporting elements of an official API release, the fact that the Q

   [1]: http://www.apievangelist.com/definition-json.php
   [2]: Quora%20Exposes%20JSON%20API
   [3]: http://www.quora.com/Is-anyone-working-on-a-Quora-Chrome-extension
