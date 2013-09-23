---
layout: post
title: "Providing Full Data Download vs API"
url: 'http://apievangelist.com/2013/07/19/providing-full-data-download-vs-api/'
image: 'http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/blog/download.png'
---

<img class="c1" src="https://s3.amazonaws.com/kinlane-productions/bw-icons/download.png" alt="" width="250" align="right" />

I've had so many discussions on this topic, I felt like I had written a post on it, but when the topic came up again today, I realized I hadn't. This is a regular conversation I get into with open data folks, regarding whether you should deploy open data as download vs an API.

I'll spare you having to read my entire rant, the answer is if you can, both. You should always provide a full data download, and additionally API access when the resources are available. There is no versus argument, there are scenarios where both are valuable and offer benefits over the other.

As a developer, I just want quick, complete access to data. I'm always in a hurry to just get to work, and I have the skills to parse, store, transform this data for whatever reason I will need. So let's just get to work. Give me a download and get the hell out of my way. Pretty straight forward logic. This is all true, but it is a very short-sighted, narrowly focused perspective and shouldn't impede larger, long term goals around data acquisition, management and access.

Taking your data, keying it up, and asking users to request a key and access via an API, might be a wall for the eager alpha dev, but there are many that could benefit from well thought out API end points, search