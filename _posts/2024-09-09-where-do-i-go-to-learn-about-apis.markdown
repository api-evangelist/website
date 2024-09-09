---
published: true
layout: post
title: 'Where Do I Go To Learn About APIs?'
tags:
- Blogs
- Discovery
- Newsletters
- Podcasts
image: https://kinlane-productions2.s3.amazonaws.com/algorotoscope-master/bf-skinner-nyc-public-library.jpeg
---
It is the top question I get--where do I go to learn about APIs? I've long had a list of the blogs, directories, podcasts, and other resources for learning about APIs--the trick is to keep it up to date and always properly reflect what is truly happening. I've reworked my previous work on this subject while at Postman as a YAML powered blog post that I will dynamically update on a regular basis.

I recommend beginning with the top blogs and newsletter, and tune into the podcasts as you have time. Then make sure you explore the directories and catalogs to look at the different types of APIs, and get more familiar with the space. Then as you develop more awareness you can engage more within the community, digest the various reports, and find what types of API knowledge and information interests you the most.

## API Blogs and and News Sites
These are the blogs I tune into and recommend you subscribe to when looking for a way to tune  into the API space.

{% assign index = site.data.knowledge %}
{% assign show_tag = "Blog" %}
{% include api-listing.html %}

## API Catalogs, Directories, Networks, and Discovery
Places where you can actually find APIs that you can use.</p>

{% assign index = site.data.knowledge %}
{% assign show_tag = "Discovery" %}
{% include api-listing.html %}

## API Newsletters
These are the email newsletters I stay tuned into to get regular updates about what is happening weekly across the API space.

{% assign index = site.data.knowledge %}
{% assign show_tag = "Newsletter" %}
{% include api-listing.html %}

## API Podcasts
These are some of the API podcasts out there--a few have gone dormant, but they still provide relevant info and may wake up again.

{% assign index = site.data.knowledge %}
{% assign show_tag = "Podcasts" %}
{% include api-listing.html %}

## API Reports
These are the reports people are producing that help us make sense of the API space, and provide some grounding year after year.

{% assign index = site.data.knowledge %}
{% assign show_tag = "Reports" %}
{% include api-listing.html %}

## Developer Communities
These are a handful of places you can hang out and talk about APIs, augmenting the webistes for blog, newsletters, and podcasts.

{% assign index = site.data.knowledge %}
{% assign show_tag = "Developers" %}
{% include api-listing.html %}

## API Events
This is where you can tune into the conferences and events occurring across the space and rub elbows with folks who are doing APIs.

{% assign index = site.data.knowledge %}
{% assign show_tag = "Events" %}
{% include api-listing.html %}

Some of these images need updating, and it was interesting to see which sites had gone away or went dormant. I will spend some more time curating what is here, and I think I will add OpenAPI, JSON Schema, AsyncAPI, and the leading API specifications to the list. They have communities, newsletters, etc. that are worth tuning into. I am also going to work to try and get outside the echo chamber a bit and see if I can't find other avenues for driving API discussion amongst the normals.

If you [see a mistake, something you'd like to fix or add, feel free to submit a pull request on the YAML powering](https://github.com/api-evangelist/website/blob/gh-pages/_data/knowledge.yml) this page, or [submit an issue](https://github.com/api-evangelist/website/issues). I'll regularly update this blog post, a recurring theme I am seeing, where I need to treat some posts as evergreen and power using YAML, keeping them up to date with what I am seeing, rather than launching a new landing page or micro site. If you have a questions don't hesitate to ask, and if I have a resource to share I will make sure to add to my list.