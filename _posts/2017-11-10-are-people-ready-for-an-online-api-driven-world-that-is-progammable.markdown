---
published: true
layout: post
title: Are People Ready For An Online API-Driven World That Is Programmable?
date: 2017-11-10T11:00:00.000Z
tags:
  - API Evangelist
  - Politics of APIs
  - Design
  - Business of APIs
  - Security
image: >-
  https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories-new/van-gogh-starry-night-container-bridge-2.jpg
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories-new/van-gogh-starry-night-container-bridge-2.jpg" align="right" width="45%" style="padding: 15px;" /></p>I am struggling with helping some folks get beyond their API being just readable, and helping them understand the potential of having POST, PUT, and other writable aspects to their resources, making things much more programmable. My client has a firm grasp on the ability to GET data from their API and publish on websites. They also have the concept that they can GET other data from other 3rd party APIs, and display on their website alongside their data. Where they are struggling is that they can also add new data to their API, and update existing data they are making available via their API, and ultimately their website as well.

This hurdle isn't limited to any single project I'm working on. I find a number of people who seem to have a decent grasp on APIs in general, struggling with or completely avoiding conversations around making the data writeable. They are able to make the transition from web to API when it comes to retrieving data, but making the same jump when it comes to adding and updating data is proving to be more difficult. I think there will always be a cognitive load with jumping from read to write, as you have to think more about security, data quality, and other common concerns. However, beyond that, I'm trying to explore what might be the challenges people are facing. Many of the folks I'm working with are a bit shaky on their grasp of APIs, and aren't too confident in sharing what they don't understand.

As I do, I'll put it out to the universe and ask my audience what they've seen. On the surface, I'd say that adding or updating data into a database online is tougher to wrap your head around without some context, and some of the affordances we enjoy in the browser. Adding a Tweet through mobile application or website? No problem. POST a tweet through API, is a little tougher to envision. Updating a contact record in your administrative system? No problem. PUT via API to the /contact/ path doesn't compute as quickly. API developers can quickly see these interfaces as programmable, but for the average business user, there is more dependence on the affordances provided in the browser, and us developers are taking the importance of these affordances for granted.

Beyond that, I'm guessing there is a perceived lack of control. Anyone can add or update? How do we address quality control? IDK, just spitball'n here. The majority of APIs I come across are GET only, so I have to believe there are issues around control, and beliefs around ownership. I can't believe all of these API providers don't grasp the technical aspects of writeable APIs. It is the same in the federal government. ALL the web APIs are read only. We've started to see this ice break a little in recent years, but federal agencies are rightfully wary of the responsibility of letting the public write data to their databases. I almost feel like the Facebook and Twitters of the world are almost too open to allowing folks to write, without being thoughtful around privacy, security, and data ownership or stewardship--just to get their hands on the data.

I wondering if POST, PUT, and DELETE should be 101 concepts that I'm teaching to folks. Should I be starting out with just the safer, more straightforward reading of data, content, and algorithmic resources. Then down the road introduce the ability to add, update, and delete information. I know the concept of DELETE freaks people out pretty quickly. IDK. I'm just doing my job, and questioning things at all levels, and wondering if people are even ready for a programmable online world. I think SaaS has delivered a programmable world with a wealth of affordances that help onboard people with all of this, and us API people are failing at translating the significance of an API-driven world that is programmable to our business users.
