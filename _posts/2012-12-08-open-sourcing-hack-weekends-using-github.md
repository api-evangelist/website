---
layout: post
title: "Open Sourcing Hack Weekends Using Github"
url: 'http://apievangelist.com/2012/12/08/open-sourcing-hack-weekends-using-github/'
image: 'http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/blog/Tag-Cloud-Hack-Weekends-Github.png'
---

[<img src="https://s3.amazonaws.com/kinlane-productions/hackweekends/Tag-Cloud-Hack-Weekends-Github.png" alt="" width="350" align="right" />][1]

I’ve been maintaining a calendar of hackathons for all of 2012. Originally it was just a section off of [API Evangelist][2], but eventually the site needed to be its own project. Up until now its just been a blog and calendar of events I curate from Eventbrite, Twitter, Google, Eventful and event organizers.

I spend about 8-12 hours a week curating the events and stories for blog posts, and with the increase in the number hackathons over 2012, so does the time I need to maintain. I was adding an API so other users can add to calendar or event guest post, then I decided I would like to also have databases of hackathon organizers, sponsors, vendors, venues and other key building blocks of hackathons.

My goal is to create an information hub for the hackathon community. But an “open API” didn’t seem like enough. I wanted everything about it to be open and accessible, as well as community owned. I decided to publish [Hack Weekends on Github][3] and run it like an open source project.

I launched the site using [Github Pages][4] with [Jekyll][5]. These run the pages and blog for Hack Weekends.  But, I needed something to run the calendar, and other systems. I wanted them to be simple--I went with [Mustache Templates][6] JSON stores.

The implementation isn't perfect. I had problems getting search and sort tools to work, so I scaled back to a minimal viable implementation. I got the following areas up:

  * **Hackathon Calendar** \- Listing of hackathons global, sorted by city (for now)
  * **Cities Hackathon Directory** \- Breakdown of hackathons by cities
  * **Hack Weekends Blog** \- Blog running on Jekyll, which I edit using prose.io
  * **Hack Weekends News** \- Curated, relevant hackathon links from my pinboard

I will get all the bells and whistles in there soon. Before that, I’m working on a basic Github template for planning and executing a basic hackathon. I would like to see hackathon organizers using a common, open approach to planning and delivering hackathons around the globe. I’m hoping it will work in conjunction with an open approach to Hack Weekends and other hackathon community sites.

Hack Weekends is a work in progress. I went ahead and made it live, as its about 85% of what I had on the previous version. Having it running as a completely client-side and static site on Github will force me to learn to approaches to manage my content and data in a way that is open and machine readable by default.  

Feel free to fork [Hack Weekends][7] and make contributions.  You can add blog posts, news or calendar events.  I will be building other client side tools for interacting with the site as time goes on.  

   [1]: http://hackweekends.com/index.html
   [2]: http://apievangelist.com (API Evangelist)
   [3]: http://hackweekends.com/index.html (Hack Weekends)
   [4]: http://pages.github.com/ (Github Pages)
   [5]: https://github.com/mojombo/jekyll (Jekyll)
   [6]: http://mustache.github.com/
   [7]: https://github.com/kinlane/hack-weekends
