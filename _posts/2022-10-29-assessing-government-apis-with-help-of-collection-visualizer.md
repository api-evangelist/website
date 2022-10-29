---
published: true
layout: post
title: 'Assessing Government APIs with Help of Collection Visualizer'
image: https://kinlane-productions2.s3.amazonaws.com/postman-government-search-listing.png
author:
 name: kin
tags:
- Government
- Federal Government
- Open Data
- Inventory
- Discovery
- Assessment
- Collections
- Visualizer
---
I joined in on some conversations around data and APIs with the White House this week and it got my juices flowing again when it comes to understanding APIs. One of the biggest challenges in doing APIs anywhere, but something that is painfully evident in the federal government within the United States is when it comes to API discovery. Or more simply, knowing where all of the APIs are. We love creating APIs, and in some cases too many APIs, and in some cases not enough APIs, but no matter what, we suck at making sure our APIs are discoverable. Something I’ve been fretting about since I created [APIs.json](http://apisjson.org/) back in the day. During the two hour call this week, the subject of data and API discovery came up again, pushing me to once again be looking to conduct a quick survey of what APIs and data efforts are available out of the federal government.
 
Unfortunately there is no right way to automate this, and I know from doing it before that you learn a lot just by doing a manual google search for each of the 100+ government agencies. However, I want to reduce the amount of redundant work for me, so I employed the help of a Postman collection to assist me in conducted the searches I needed. To pull a list of all the government agencies I enlisted the help of the [US Digital Registry API from the GSA](https://open.gsa.gov/api/digital-registry/), and fired up [a collection to pull the results for me using the agencies API](http://apisjson.org/). This returned 163
Agencies which I rendered as an HTML list using the Postman visualizer. I knew I’d be doing a handful of searches for each agency so I went ahead and added a bulleted list of the five top search terms I’d be repeating over and over, resulting in an easy to use list for me to work from.
 
This is excruciating work. Very manual. However, you learn a lot while doing it. Making it really worth your time. Ideally every federal agency would publish an APIs.json index in the root of their domain, providing us with a machine readable index of all APIs, similar to what I did for the Obama administration with the data.json file. Until then I am just going to have to manually do my audits every couple of years to see what is out there. Some day, I’ll just set up my harvesting engine and get to work crawling and scraping valuable datasets that government agencies publish. The challenge is that most are not available via APIs, and most of the time data is published as Excel spreadsheets, making things really difficult to make sense of in a programmatic way. Spreadsheets are good for humans, but not for other machines.
 
We will see how much stamina I have for this work this weekend. My goal is to do a quick assessment of what is happening, and capture some of my thoughts and notes on the data and APIs coming out of the current administration. I wish I had the ability to do a diff with the other two assessments I’ve done, but just developing an awareness of the current state, and educating myself a bit more will have to be enough. I am a big believer that APIs will help fix many of the problems the government has, but also what the public has with the government, and this will be a drum I will keep beating on until I retire. After a decade of doing this work, I am more convinced than ever that a lot of this work has to occur from the outside in, but we will need policy to shift to help change the behavior of government agencies to be more API-first, otherwise we’ll never quite be able to get the data and information we need from our government.



