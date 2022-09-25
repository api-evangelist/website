---
published: true
layout: post
title: Adding A Lead To SalesForce Using The REST API
date: 2018-06-19T09:00:00.000Z
tags:
  - API Evangelist
  - Getting Started
  - Documentation
  - SalesForce
image: >-
  https://s3.amazonaws.com/kinlane-productions/salesforce/salesforce-rest-api.png
---
<p><a href="https://developer.salesforce.com/page/Salesforce_APIs"><img src="{{ page.image }}" width="45%" align="right" style="padding: 15px;" /></a></p>I spend a lot of time talking about [the SalesForce API](https://developer.salesforce.com/page/Salesforce_APIs), using it as a reference for where the API evolution began 18 years ago, but it has been a long time since I've actually worked with the SalesForce API. Getting up and running with any API, especially iconic APIs that we all should be familiar with, is always an enlightening experience for me. Going from zero to understanding what is going on and actually achieving the API call(s) you want, is really what this game is all about.

As part of some work I'm doing [with Streamdata.io](http://streamdata.io) I needed to be able to add new leads into SalesForce, and I thought it would be a good time for me to get back into the saddle with the SalesForce REST API--so I volunteered to tackle the integration. The SalesForce API wasn't as easy to get up and running as many simpler APIs I onboard with is, as the API docs isn't as modern as I'd expect, and what you need is buried behind multiple clicks. Once you find what you are looking for, and click numerous times, you begin to get a feel for what is going on, and the object model in use becomes a little more accessible.

In addition to finding what you need with the SalesForce REST API, you have to make sure you have a handle on the object structure and nuance of SalesForce itself. For this story, I am just working with one object--Leads. I'm using PHP to work with the API, and to begin I wanted to be able to get leads, to be able to see which leads I currently have in the system:

<script src="https://gist.github.com/kinlane/aa472c9338a491f204ce77cb9e35fecb.js"></script>

I will add pagination, and other elements in the future. For now, I just wanted to be able to get the latest leads I have in the system to help with with some checks on what is being added. Now that I can check to see what leads are in the system, I wanted to be able to add a lead, with the following script:

<script src="https://gist.github.com/kinlane/dc45901494369ca601a36ccdabc96086.js"></script>

I am only displaying some of the default fields available for this example, and you can add other custom fields based upon which values you wish to add. Once I have added my lead, I wanted to be able to update with a PATCH API call:

<script src="https://gist.github.com/kinlane/9bdb62b79b1f0f04b60a182a9ed4a743.js"></script>

Now I am able to add, update, and get any leads I'm working with via the SalesForce API. The project gave me a good refresher for what is possible with the SalesForce API. The API is extremely powerful, and something I want to be up to speed on so that I can intelligently respond to questions I get. I wish the SalesForce API team would spend some time modernizing their API portal and documentation, providing a more coherent separation between the different flavors of their API, and provide OpenAPI driven documentation, as well as Postman Collections. It would have saved me hours of working through their API docs, and playing around with different API calls in Postman before I was able to successfully OAuth, and make my first call against the accounts and leads API endpoints.

While I think SalesForce remains a worthwhile API to showcase when I talk about the history of APIs, and the power of providing web APIs, their overall documentation and approach is beginning to fall behind the times. SalesForce possesses many of the building blocks I recommend other API providers operate, and are very advanced in some of their support and training efforts, but their documentation, which is the biggest pain point for developers, leaves a lot to be desired. I'm used to having to jump through hurdles to get up and running APIs, so the friction for me was probably less than a newer API developer would experience. I could see some of the domain instance url, versioning, and available API paths proving to be a significant hurdle if you didn't understand what was going on. Something that could be significantly minimized with some simpler, more modern API docs, and OpenAPI and Postman Collections available.
