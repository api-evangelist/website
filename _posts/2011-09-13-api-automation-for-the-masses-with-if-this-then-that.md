---
layout: post
title: "API Automation for the Masses with If This Then That"
url: 'http://apievangelist.com/2011/09/13/api-automation-for-the-masses-with-if-this-then-that/'
image: 'http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/blog/if-this-then-that.png'
---

<img src="http://kinlane-productions.s3.amazonaws.com/ifthisthenthat/if-this-then-that.png" alt="" width="300" align="right" />I believe that [REST][1] and [JSON][2] are breaking up the web, into smaller more understandable, re-usable, mashable pieces that potentially anyone can use, even non-developers.

I have written several posts on how tools like [API explorers][3] and standards like [oEmbed][4] are making APIs accessible by non-developers.  And I’m always on the look out for new ideas, for new ways to arm the masses with tools that take advantage of APIs.

Evolving on a piece I wrote a couple a months ago about a [Widget Builder Environment for APIs][5], I was envisioning taking Yahoo Pipes to the next level, add in better API support with OAuth, and make it much more simpler to use.  I did not get much time to think about it before [Audrey][6] introduced me to [if this then that][7] (ifttt).  

ifttt allows you to creates tasks.  Tasks are defined like this: when something happens (this) then do something else (that).

  * **this (triggers) -** The this part of a task is the Trigger. Some example Triggers are "if I'm tagged in a photo on Facebook" or "if I tweet on Twitter." 
  * **that (actions) -** The that part of a task is the Action. Some example Actions are "then send me a text message" or "then create a status message on Facebook." 

<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/ifthisthenthat/ifttt-Dashboard.png" alt="" width="300" align="right" />Triggers and Actions come from Channels. Channels are the services and devices we use every day, such as:  Twitter, Facebook, Instagram, Email, Phone Call or Weather.

You can put one channel's trigger together with another channel's action to create a task that runs every 15 minutes and can be turned on and off.

Channels are made possible because these services have APIs.  ifttt does a remarkable job at simplifying this in a way, I never even imagined, and allows any user to take advantage of two APIs, apply meaningful business logic, and automate the task to run regularly.  

What really makes it cool is you can save tasks as “recipes” and share them with friends making this type of API usage and automation a potentially very social thing. 

Right now it appears that the ifttt team creates the new channels that are available.  Think of the possibilitis if they opened it up to developers to build their own channels and recipes, and created a marketplace of these API automation recipes?  

 [if this then that][7] (ifttt) is pretty cool!  I will be playing with more and incorporating into my daily operations, and see if we can make it stick.

   [1]: /buildingblocks/restful_api.php (REST)
   [2]: /2011/01/27/api-technology-json/ (JSON)
   [3]: /2011/03/24/explorers-open-api-access-beyond-developers/ (API Explorers)
   [4]: /2011/04/06/allow-api-users-to-embed-content-with-oembed/ (oEmbed)
   [5]: /2011/06/22/widget-builder-environment-for-apis/ (Widget Builder For APIs)
   [6]: http://www.hackeducation.com (Audrey Watters)
   [7]: http://ifttt.com/dashboard (if this then that)
