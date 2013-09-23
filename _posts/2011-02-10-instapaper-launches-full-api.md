---
layout: post
title: "Instapaper Launches Full API"
url: 'http://apievangelist.com/2011/02/10/instapaper-launches-full-api/'
image: ''
---

[<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/instapaper.png" alt="" width="175" align="right" />][1][Instapaper][1] just launched a [Full API][2] giving developers access to web pages that Instagram users have saved to read later.

The API provides full Instapaper account access, but can only access web page bookmarks from paid-subscriber accounts.

Those who haven't paid the $1/month fee for an Instapaper account will still be able to submit to Instapaper using the [Instapaper Simple API][3].

The API uses oAuth 2.0 for authentication and provide a set of helper libraries to get going.

Instapaper API services and endpoints are:

**Account / Authentication**

  * /api/1/oauth/access_token
  * /api/1/account/verify_credentials
**Web Page Bookmarks**

  * /api/1/bookmarks/list
  * /api/1/bookmarks/update_read_progress
  * /api/1/bookmarks/add
  * /api/1/bookmarks/delete
  * /api/1/bookmarks/star
  * /api/1/bookmarks/unstar
  * /api/1/bookmarks/archive
  * /api/1/bookmarks/unarchive
  * /api/1/bookmarks/move
  * /api/1/bookmarks/get_text
**Folders**

  * /api/1/folders/list
  * /api/1/folders/add
  * /api/1/folders/delete
  * /api/1/folders/set_order
Instapaper has provided some insight on its blog regarding [why it chose to provide Full API access to data from paid accounts][4]. It's a new and interesting perspective to the classic arguement of freemium versus paid accounts.

The first application developed using the Full API is [Stacks for Instapaper][5], a Windows Phone 7 client. developed by Matthieu Guyonnet-Duluc. More applications are sure to come.

   [1]: http://www.instapaper.com/
   [2]: http://www.instapaper.com/api/full
   [3]: http://www.instapaper.com/api/simple
   [4]: http://blog.instapaper.com/post/3208433429
   [5]: http://wp7wonders.wordpress.com/stacks-for-instapaper/
