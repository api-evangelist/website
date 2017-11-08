---
layout: post
title: 'APIs And Other Ways Of Serving Up Machine Learning Models'
date: 2017-11-08T15:00:00.000Z
tags:
  - API Evangelist
  - Machine Learning
  - Artificial Intelligence
  - Algorithms
  - Observability
  - Deployment
image: >-
  https://s3.amazonaws.com/kinlane-productions/algorotoscope/stories/crypto-machine-bletchley_copper_circuit.png
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/algorotoscope/stories/crypto-machine-bletchley_copper_circuit.png" align="right" width="45%" style="padding: 15px;" /></p>As with most areas of the tech sector, behind the hype there are real world things going on, and machine learning is one area I've been studying, learning, and playing withd what is actually possible when it comes to APIs. I've been studying the approach across each of the major cloud platforms, including AWS, Azure, and Google t push forward my understanding of the ML landscape. Recently the Google Tensorflow team released an interesting overview of how they are serving up Tensorflow models, making machine learning accessible across a wide variety of use cases. Not all of these are API specific, but I do think they are should be considered equally as part of the wider machine learning (ML) application programming interface (API) delivery approach.

Over the past year and half, with the help of our users and partners inside and outside of Google, TensorFlow Serving has advanced performance, best practices, and standards for ML delivery:

- **Out-of-the-box Optimized Serving and Customizability** - We now offer a pre-built canonical serving binary, optimized for modern CPUs with AVX, so developers don't need to assemble their own binary from our libraries unless they have exotic needs. At the same time, we added a registry-based framework, allowing our libraries to be used for custom (or even non-TensorFlow) serving scenarios.
- **Multi-model Serving** - Going from one model to multiple concurrently-served models presents several performance obstacles. We serve multiple models smoothly by (1) loading in isolated thread pools to avoid incurring latency spikes on other models taking traffic; (2) accelerating initial loading of all models in parallel upon server start-up; (3) multi-model batch interleaving to multiplex hardware accelerators (GPUs/TPUs).
- **Standardized Model Format** - We added SavedModel to TensorFlow 1.0, giving the community a single standard model format that works across training and serving.
- **Easy-to-use Inference APIs** - We released easy-to-use APIs for common inference tasks (classification, regression) that we know work for a wide swathe of our applications. To support more advanced use-cases we support a lower-level tensor-based API (predict) and a new multi-inference API that enables multi-task modeling.

I like that easy-to-use APIs are on the list. I predict that ease of use, and a sensible business model will provide to be just as important as the ML model itself. Beyond these core approaches, the Tensorflow team is also exploring two experimental areas of ML delivery:

- **Granular Batching** - A key technique we employ to achieve high throughput on specialized hardware (GPUs and TPUs) is "batching": processing multiple examples jointly for efficiency. We are developing technology and best practices to improve batching to: (a) enable batching to target just the GPU/TPU portion of the computation, for maximum efficiency; (b) enable batching within recursive neural networks, used to process sequence data e.g. text and event sequences. We are experimenting with batching arbitrary sub-graphs using the Batch/Unbatch op pair.
- **Distributed Model Serving** - We are looking at model sharding techniques as a means of handling models that are too large to fit on one server node or sharing sub-models in a memory-efficient way. We recently launched a 1TB+ model in production with good results, and hope to open-source this capability soon.

I'm working to develop my own ML models, and actively using a variety of them available over at [Algorithmia](https://algorithmia.com/). I'm pushing forward a project to help me quantify and categorize ML solutions that I come across, and when they are delivered using an API, I am generating an OpenAPI, and applying a set of common tags to help me quantify, categorize, and index all the ML APIs. While I am focused on the technology, business, and politics of ML APIs, I'm interested in understanding how ML models are being delivered, so that I can help keep pace with exactly how APIs can augment these evolving practices, making ML more accessible, as well as observable.

We are in the middle of the algorithmic evolution of the API space, where we move beyond just data and content APIs, and where ML, AI, and other algorithmic voodoo is becoming more mainstream. I feel pretty strongly that APIs are an import piece of this puzzle, helping us quantify and understand what ML algorithms do, or don't do. No matter how the delivery model for ML evolves, batches, distributes, or any other mutation, there should be an API layer for accessing, auditing, and shining a light on what is going on. This is why I regularly keep an eye on what teams like Tensorflow are up to, so that I can speak intelligently to what is happening on this evolving ML front.
