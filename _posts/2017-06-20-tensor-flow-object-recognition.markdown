---
title: API Wrappers To Help Bring Machine Learning Into Focus
date: 2017-06-20 16:00:00 Z
tags:
- Machine Learning
- API Evangelist
- Transparency
- Algorithms
image: https://s3.amazonaws.com/kinlane-productions/tensorflow/kites_detections_output.jpg
---

<p><img src="https://s3.amazonaws.com/kinlane-productions/tensorflow/kites_detections_output.jpg" align="right" width="40%" style="padding: 15px;" /></p>I was taking a look a[t the Tensorflow Object Detection API](https://github.com/tensorflow/models/tree/master/object_detection), and while I am interested in the object detection, the usage of API is something I find more intriguing. It is yet another example of how diverse APIs can be. This is not a web API, but an API on top of a single dimension of [the machine learning platform TensorFlow](https://www.tensorflow.org/).

"The TensorFlow Object Detection API is an open source framework built on top of TensorFlow that makes it easy to construct, train and deploy object detection models." It is just a specialized code base helping abstract away the complexity of one aspect of using TensorFlow, specifically for detecting objects in images. You could actually wrap this API with another web API and run on any server or within a single container as a proper object recognition API.

For me, it demonstrates one possible way of wrapping a single or cross section of a machine learning implementation to abstract away the complexity and helping you train and deploy ML models in this particular area. This approach to deploying an API on top of ML shows that you can use to APIs to help simplify and abstract ML for developers. This can be done to help satisfy business, regulatory, privacy, security, and other real or perceived concerns when it comes to artificial intelligence, machine learning, or any other digital voodoo that resembles magic. 

No matter how complex the inputs and outputs of an algorithm are, you can always craft an API wrapper, or series of API wrappers that help others make sense of those inputs, from a technical, business, or even political perspective. I just wanted to highlight this example of ML being wrapped with an API, even if it isn't for all the same reasons that I would be doing it. It's just part of a larger toolbox I'm looking to create to help me make the argument for [more algorithmic transparency in the machine learning platforms](http://apievangelist.com/2016/08/04/pushing-for-more-algorithmic-transparency-using-apis/) we are developing.