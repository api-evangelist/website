---
published: true
layout: post
title: Understanding The Words We Use To Describe Machine Learning APIs
date: 2017-08-04T09:00:00.000Z
tags:
  - API Evangelist
  - Machine Learning
  - Definitions 
image: 'https://s3.amazonaws.com/kinlane-productions/mining-machine-learning.png'
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/mining-machine-learning.png" align="right" width="40%" style="padding: 15px;" /></p>I spend a lot of time trying out new APIs, working to understand what it is they do, or do not do. I have a pretty robust way of looking at APIs, profiling the company, and the APIs they offer, but when I'm wading through the marketing content, API documentation, and other resources, I am regularly stumped by the language that is used to describe what an API does. Honestly, this problem isn't exclusive to machine learning APIs, but with the recent explosion in artificial intelligence, machine learning, deep learning, cognitive and other types of algorithmic voodoo, the words being used seem to have gone to entirely new levels.

I am interested in understanding what it is an API does. I want to go from zero to understanding in 2.34 seconds. I don't want to wade through marketing, and documentation to understand what an API does. I want to find simple, concise language that properly describes an API. In the world of artificial intelligence, this can be difficult to do, and is something that varies from provider to provider. Some machine learning API providers are better at describing what they do, while others seem to prefer hype, and fluff when it comes to explaining what is actually possible.

As I continue my work profiling [Amazon](http://amazon.web.services.stack.network/), [Microsoft](http://microsoft.stack.network/), and [Google APIs](http://google.stack.network/) I want to develop an approach to helping me separate what an API does, and what a provider says it does. I am going to continue profiling each API [using OpenAPI](https://www.openapis.org/), and labeling them with a common set of tags I'm using to quantify what machine learning APIs actually do. As I'm doing this I also decided to add an extra tag field called x-hype-tags, which gives me a way to track each of the additional words I found in the marketing and documentation, that I may not be actually using to describe what the API does--maintaining much of the API providers intent.

One thing that contributes to the confusion of what is machine learning is that, very similar to APIs, it can be almost anything. While packaged in many different ways, most of the major machine learning providers have a machine learning engine for training and executing models, as well as some ready to go models that accomplish some common ML tasks for developers. Here are the primary machine learning engines I've been profiling out of the major cloud providers:

- [**Amazon Machine Learning**](https://aws.amazon.com/machine-learning/) - Amazon Machine Learning is a service that makes it easy for developers of all skill levels to use machine learning technology.
- [**Google Machine Learning**](https://cloud.google.com/ml/) - Google Cloud Machine Learning Engine is a managed service that enables you to easily build machine learning models that work on any type of data, of any size
- [**Azure Machine Learning**](https://azure.microsoft.com/en-us/services/machine-learning/) - A fully-managed cloud service that enables you to easily build, deploy, and share predictive analytics solutions.

I am going to be profiling these engines in their own way, but before I understand the infinite possibilities, I want to better understand the finite possibilities with each of these machine learning platforms. To help me develop a way of tagging, and quantifying what APIs do, and the hype around them I took a single type of machine learning API from each of these providers, and augmented their OpenAPI with more descriptive tagging.

To begin, I started with [Amazon's Rekognition API](https://aws.amazon.com/rekognition/?hp=tile&so-exp=below), crafting a basic OpenAPI that outlines the technical details of each possible API request and response, with the added tagging describing what the API does:

<script src="https://gist.github.com/kinlane/a5b721d555e92aa81cf386a6f85c8e09.js"></script>

Then I went through [Azure's Computer Vision](https://azure.microsoft.com/en-us/services/cognitive-services/computer-vision/), crafting a basic OpenAPI that outlines the technical details of each possible API request and response, with the added tagging describing what the API does:

<script src="https://gist.github.com/kinlane/cc69c6f6a25cbe6ae021941e45fb2f31.js"></script>

Then last I look at [Google's Cloud Vision API](https://cloud.google.com/vision/), crafting a basic OpenAPI that outlines the technical details of each possible API request and response, with the added tagging describing what the API does:

<script src="https://gist.github.com/kinlane/a559ae524f321167d708e229c9792e23.js"></script>

These OpenAPIs aren't 100% complete. I'm more concerned with developing the tagging schema for use across many APIs, than I am with the perfect OpenAPI. I'll publish them to Github and continue to evolve, polish, and work to make each OpenAPI as complete as possible. I'm looking to settle in on a schema, before I got to work adding the extra x-hype-tags to additional OpenAPIs, pushing beyond what OpenAPI 2.0 dictates when it comes to API tagging. I'll use the primary tags for each OpenAPI as the distilled down categorization of what each ML API does, while the x-hype-tags will give me a summary of what is used in the marketing copy, and the API documentation for each ML API provider.

It is important to me that I can quickly pull up APIs that accomplish specific business tasks--this requires each API to be tagged well. I also want to be able to apply some sort of hype score to each API, which reflects the number of adjectives and buzzwords in use in marketing and documentation. I feel these x-hype-tags reflect the hype in ML API space, and the tags reflect the realities of what ML APIs are actually capable of doing. When I profile new ML APIs I will be adding any word that catches my eye to the x-hype-tags, but I will be thinking about more deeply, and more carefully evolving the core set of more meaningful APIs I am using to categorize the ML APIs I track on.

Once I profile Amazon, Microsoft's, and Google's ML APIs in this way I am going to go through [Algorithmia](http://algorithmia.com), and other leading ML API providers and profiling their APIs, adding to both my core machine learning tagging vocabulary, as well as my machine learning hype tagging dictionary. Then I'll step back a little and think about the bigger picture of the words we are choosing to describe our ML APIs. I am looking to develop a better way to be cataloging the types of ML APIs out there, and understand the language API providers are choosing to use when they describe what it is that they deliver. We need to be able to make sense of the ML APIs we already have, as well as each of the upcoming waves of AI and ML voodoo that is being developed right now, and due to be unleashed on the world in coming years.
