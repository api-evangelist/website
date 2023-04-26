---
published: true
layout: post
title: 'Reverse Engineering Mobile APIs To Show A Company Their Public APIs'
date: 2019-08-02T09:00:00.000Z
tags:
  - API Evangelist
  - Mobile
  - Discovery
  - Proxy
image: https://s3.amazonaws.com/kinlane-productions2/algorotoscope-master/aws-s3-square-97-193-800-500-0-max-0-1--1-square.jpg
author:
 name: kinlane
tags:
    - None
---
One story I tell a lot when talking to folks about APIs, is how you can reverse engineer a mobile phone to map out the APIs being used. As the narrative goes, many companies that I talk with claim they do not have any public APIs when first engage with them. Then I ask them, “Do you have any mobile applications?”. To which the answer is almost always, “Yes!”.  Having anticipated this regular conversation, if I am looking to engage with a company in the area of API consulting, I will have made the time to reverse engineer their application to produce a set of OpenAPI definitions that I can then share with them, showing that they indeed have public APIs.

The process isn’t difficult, and I’ve written about this several times. To reverse engineer a mobile application, all you have to do is download the targeted application to your phone, configure your phone to use your laptop as a proxy, and be running Charles Proxy on your laptop. I’m not going to share a walkthrough of this, it is easy enough to Google and find the technical details of doing it, I’m more looking to just educate the average business person that this is possible. Once you have your mobile phone proxied through Charles, it will capture every call made home to the mother ship, logging the request and response structure of all APIs being used by the mobile application-—which uses public DNS for routing, making it a public API.

I have an API that I developed which I can upload the resulting Charles Proxy output file, and convert all the API calls into an OpenAPI. Making quick work of documenting the APIs behind a mobile application. Which, when you share with someone who is under the belief that their mobile APIs are private APIs, it can make quite a splash. Usually you get a response, like “well, we don’t allow access to the general public for our APIs”. To which I respond, any consumer of your application is a consumer of your APIs. If you use public DNS to handle the transport for your APIs-—they are public APIs. There is no secret force field created by mobile applications to keep your APIs secure or protected. Some applications have invested in SSL pinning to prevent proxying with tooling like Charles Proxy, but there is still ways around—-albeit it requires a significant more work.

As I’m spending more time crafting API discovery tooling and agents, I’m revisiting my work to reverse engineer mobile applications and generate OpenAPI from proxy logs. I’d like to find a way to emulate mobile applications and script the exploration of them. I find having to click through every option and feature within an application pretty mind numbing, and I’d like to automate it a little more. I feel like mobile, browsers, and  internet of things API discovery will be one of the next frontiers when it comes to mapping out the API landscape. I’m guessing there will always be truly public APIs launching, but the majority of APIs will continue to operate in the shadows of our browsers, mobile phones, and other devices that are becoming ubiquitous in our lives.
