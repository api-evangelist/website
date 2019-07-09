---
published: true
layout: post
title: API Foraging And Wildcraft
date: 2017-08-21T11:00:00.000Z
tags:
  - API Evangelist
  - Deployment
  - Github
image: 'https://s3.amazonaws.com/drone-recovery/diamond04.jpg'
---
<p><img src="https://s3.amazonaws.com/drone-recovery/diamond04.jpg" align="right" width="40%" style="padding: 15px;" /></p>I was in Colorado this last week at a CA internal gathering listening to my friend Erik Wilde talking about APIs. One concept he touched on was what he called API gardening, where different types of API providers approached the planting, cultivating, and maintenance of their gardens in a variety of different ways. I really like this concept, and will be working my way through the slide deck from his talk, and see what else I can learn from his work.

As he was talking I was thinking about a project I had just published to Github, which leverages the Google Sheets API, and the Github API to publish data as YAML, so I could publish as a simple set of static APIs. I'd consider this approach to be more about foraging and wildcrafting, then it is about tending to my API garden. My API garden just happens spread across a variety of services, often free and public space, in many different regions. I will pay for a service when it is needed, but I'd rather tend smaller, wilder, APIs, that grow in existing spaces--in the cracks.

I use free services, and build upon the APIs for the services I am already using. I publish calendars to Google Calendar, then pull data and public APIs using the Google APIs. I use the Flickr and Instagram APIs for storing, publishing, sharing, and integrating with my applications using their APIs. I pull data from the Twitter API, Reddit API, and store in Google Sheets. All of these calendar, image, messaging, and link data will ultimately get published to Github as YAML, which then is shared as XML, JSON, Atom, CSV via static APIs. I am always foraging for data using public services, then planting the seeds, and wildcrafting other APIs--in hopes something will eventually grow.

Right now Github is my primary jam, but since I'm just publishing static JSON, XML, YAML, and other media types, it can be hosted anywhere. Since it's Github it can be integrated anywhere, directly via the static API paths I generate, or by actually cloning the underlying Github repository. I have a Jekyll instance that I can run on AWS EC2 instance or Docker container, and will be experimenting more with Dropbox, Google Drive, and other free, or low cost storage solutions that have a public component. I'm looking to have a whole toolbox of deployment options when it comes to publishing my data and content APIs across the landscape. Most of these are low use, long tail usage data and content I'm using across my storytelling, so I'm not worried about things being heavily manicured, just providing fruit in a sustained way for as low of a price as I possibly can.
