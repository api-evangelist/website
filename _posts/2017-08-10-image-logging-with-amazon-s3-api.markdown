---
title: Image Logging With Amazon S3 API
date: 2017-08-10T14:00:00.000Z
published: true
layout: post
tags:
  - API Evangelist
  - Logging
  - Images
  - Analysis
image: >-
  https://s3.amazonaws.com/kinlane-productions/algorotoscope/stories/freeway_atari_missle.jpg
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/algorotoscope/stories/freeway_atari_missle.jpg" align="right" width="40%" style="padding: 15px;" /></p>I have been slowly evolving my network of websites in 2017, overhauling the look of them, as well as how they function. I am investing cycles into pushing as much of my infrastructure towards being as static as possible, minimizing my usage of JavaScript wherever I can. I am still using a significant amount of JavaScript libraries across my sites for a variety of use cases, but whenever I can, I am looking to kill my JavaScript or backend dependencies, and reduce the opportunity for any tracking and surveillance.

While I still keep Google Analytics on my primary API Evangelist sites, as my revenue depends on it, whenever possible I keep personal projects without any JavaScript tracking mechanisms. Instead of JavaScript I am defaulting to image logging using Amazon S3. Most of my sites tend to have some sort of header image, which I store in a common public bucket on Amazon S3, all I have to do is turn on logging, and then get at logging details via the Amazon S3 API. Of course, images get cached within a user's browser, but the GET for my images still gives me a pretty good set of numbers to work with. I'm not concerned with too much detail, I just generally want to understand the scope of traffic a project is getting, and whether it is 5, 50, 500, 5,000, or 50,000 visitors.

My two primary CDNs are Amazon S3 and Github. I'm trying to pull together a base strategy for monitoring activity across my digital footprint. My business presence is very different than my personal presence, but with some of my personal writing, photography, and other creations I still like to keep a finger on the pulse of what is happening. I am just looking to minimize the data gathering and surveillance I am participating in these days. Keeping my personal and business websites static, and with a minimum footprint is increasingly important to me. I find that a minimum viable static digital footprint protects my interests, maximize my control over my work, and minimizes the impact to my readers and customers.  
