---
published: true
layout: post
title: 'My URL Shortener Is Just An API With Postman As My Client'
image: https://s3.amazonaws.com/kinlane-productions2/bw-icons/bw-url-square.png
---

<p><img src="https://s3.amazonaws.com/kinlane-productions2/bw-icons/bw-url-square.png" align="right" width="25%" style="padding: 15px;" />
<p>I have my own URL shortener for API Evangelist called apis.how. I use it to track the click through rates for some of my research projects, and partner sponsorships. I’ve had the URL shortener in operation for about two years now, and I still do not have any type of UI for it, relying 100% on Postman for adding, searching, and managing the URLs I am shortening, and tracking on.

<p>My URL shortener just hasn’t raised to a level of priority where I’ll invest any time into an administrative interface, or dashboard for my URL shortener. I used Bitly and Google for a while, but I really just needed a simple shortening with basic counts, nothing more. When I bought the domain I launched a handful of API endpoints to support, allowing me to add, update, search, and remove URLs, as well as track the click throughs, and query how many clicks a link received for each mont. I can easily accomplish all of this through the Postman interface, making basic calls to my simple API–no over-engineering necessary.

<p>I have been considering running a daily job that pulls view counts for URLs and publishing to Github as YAML, where I can drive a simple visualization, but honestly I’m not that numbers oriented. I like what API clients like <a href="https://www.postman.com/">Postman</a> and <a href="https://restlet.com/">Restlet</a> provide. Even though I’m equipped to make calls using JavaScript, PHP, or CURL, I prefer just accessing via my web client–no coding necessary. I wouldn’t manage all my systems in this way, but for really basic ones like my URL shortener, I’m not sure I will ever actually evolve it beyond just being a simple API.


