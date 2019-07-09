---
title: On Device Machine Learning API Stack
date: 2017-05-19 12:00:00 Z
tags:
- Machine Learning
- Containers
- Devices
image: https://s3.amazonaws.com/kinlane-productions/google/tensorflow/tensorflow-lite-images.jpg
---

<p><img style="padding: 15px;" src="https://s3.amazonaws.com/kinlane-productions/google/tensorflow/tensorflow-lite-images.jpg" align="right" width="35%" /></p>
I was reading about [Google's TensorFlowLite in Techcrunch](https://techcrunch.com/2017/05/17/googles-tensorflow-lite-brings-machine-learning-to-android-devices/?ncid=rss), and their mention of [Facebook's Caffe2Go](https://code.facebook.com/posts/196146247499076/delivering-real-time-ai-in-the-palm-of-your-hand/), and I was reminded of a conversation I was having with the Oxford Dictionaries API team a couple months ago. 

The OED and other dictionary and language content API teams wanted to learn more about on-device API deployment, so their dictionaries could become the default. [I have asked when we will have containers natively on our routers a while ago](http://kinlane.com/2015/01/21/when-will-my-router-have-docker-containers-by-default/), but I'd also like to add to that request--when will we have a stack of containers on device where we can deploy API resources that can be used by applications, and augment the existing on-device hardware and OS APIs?

API providers should be able to deploy their APIs exactly here they are needed. API deployment, management, monitoring, logging, and analytics should exist by default in these micro-containerized environments on any devices. Whether it's our mobile phones, our automobiles, or the weather, solar, or other industrial device integration, we are going to new API-driven data, ML, AI, augmented, and other resources on-device, in a localized environment.