---
published: true
layout: post
title: How I Use Postman for Algorotoscope — API-First, No UI Needed'
image: https://kinlane-productions2.s3.amazonaws.com/algorotoscope-postman-collection-visualizer.png
author:
name: kinlane
tags:
- Machine Learning
- Postman
- Collections
- Visualizer
---
One of the things I really like about [Postman as a platform](https://www.postman.com/) is that I really can go cheap on the user interface. I have several APIs in which I do not have any UI. I only need the data managed via API, and anytime I do need some sort of output for my storytelling, I use [Postman visualizer](https://learning.postman.com/docs/sending-requests/visualizer/) to get what I need. One example of this in action is my [Algorotoscope work](https://algorithmic.rotoscope.work/), which I apply machine learning models to my photography and use across my storytelling. I do this to help shine a light on how technology is being used to manipulate how we see the world today, but also reinvent the past that supports whatever story we need. I am the only one who creates, searches, and works with my images, and while I need an API to help me manage the thousands of images, I do not really need any web or mobile interface.

Every couple of months I fire up a big ol phat GPU instance on AWS and get to work training new ML models and apply my existing models to the increasing number of photos I am taking each day. I have around fifteen models derived from different propaganda posters, art, and other works, and I think I am up to 350+ photos I apply these models to. I needed a system to help me automate the management of my ML models and the application across new and existing photos, which was perfect as a simple API. I programmatically manage my images every time I fire up a GPU instance, but once it shuts down, I only need to query my images whenever I write a new story on API Evangelist or Kin Lane. To do this, I created a simple search API, and I use Postman to query the API and render the results using the Postman visualizer. This is a super cheap and easy way to visualize the results of an API responses HTML, without having to actually host an application—I just use Postman.

For me, this is the right balance of API and UI. I feel like most APIs I develop for myself move faster than any UI can keep up with, which is why quick and scrappy little UIs delivered with Postman visualizer works the best. If the API evolves, I can quickly update the visualizer API along with the iteration—minimal effort required. For Algorotoscope I am just needing to search for images by keyword and render as a list of images so I can see the different images, find the one that best fits the story I am telling, copy and paste the link to the image, and I am done. Nobody but me is using the API, and even if there were other people using it, I could easily let them fork the collection, and use the same visualizer delivered response via their own Postman. I know a lot of folks are really into micro apps right now, and this is the future of how we apply our digital resources and capabilities, but for me, a Postman collection + visualizer works for about 75% of the API + UI needs I have.
