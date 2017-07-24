---
published: true
layout: post
title: The Hack Education Gates Foundation Grant Data Has An API
date: 2017-07-24T12:00:00.000Z
tags:
  - API Evangelist
  - Hack Education
  - Google Sheets
  - Github
  - Data
  - Education
image: >-
  https://s3.amazonaws.com/kinlane-productions/hack-education/hack-education-personalize-learning-and-the-power-of-the-gates-foundation-to-shape-education-policy.png
---
<p><a href="http://hackeducation.com/2017/07/18/personalization"><img src="https://s3.amazonaws.com/kinlane-productions/hack-education/hack-education-personalize-learning-and-the-power-of-the-gates-foundation-to-shape-education-policy.png" align="right" width="40%" style="padding: 15px;" /></a></p>I have been helping my partner in crime Audrey Watters ([@audreywatters](https://twitter.com/audreywatters)) adopt my approach to managing data project(s) using Google Sheets and Github, as part of her work on ed-tech funding. She is going through many of the leading companies, and foundations behind the funding of technology used across the education sector, and doing the hard work of connecting the dots behind how technology gets funded in this critical layer of our society.

I want Audrey (and others), to be self-sufficient when it comes to managing their data projects, which is why I've engineered it to use common services (Google Sheets, Github), with any code and supporting elements as self-contained as possible--something Github excels at when it comes to managing data, content, and code. [While Audrey is going to town creating spreadsheets and repos](https://github.com/Hack-Education-Data), I wanted to highlight a single area of her research into the grants that the Gates Foundation are handing out. She has worked hard to normalize data across many years (1998-2017) of PDF and HTML data into a single Google Sheet, [then she has published as individual YAML files which live on Github](https://github.com/Hack-Education-Data/gates-foundation/tree/master/_data)--making her work forkable and reusable by anyone.

Once published, Audrey is the first person to fork the YAML, and [put to work in her storytelling around ed-tech funding](http://hackeducation.com/2017/07/18/personalization), but each of her project repos also come with [an API for her research by default](http://funding.hackeducation.com/gates-foundation.html). Well, ok, it isn't a full-blown searchable API, but in addition to being able to get data in YAML format, she has a JSON API for each year of the Gates Foundation grants (ie. [2016](https://hack-education-data.github.io/gates-foundation/apis/2016/)). Increasing the surface area when it comes to collaborating and building on top of her work, which can be forked using Github, or accessed via the machine readable YAML and JSON files.

While she is busy creating new Google Sheets and repos for other companies, I wanted to add one more tool to her toolbox, an APIs.json index for her project APIs. [I added an apis.yaml index of all her APIs](https://github.com/Hack-Education-Data/gates-foundation/blob/master/_data/apis.yaml), which I also published to [the root of her project as an apis.json version](https://hack-education-data.github.io/gates-foundation/apis.json). Now, in addition to publishing YAML files for all the data driving her research, and enabling it all to have a JSON API, there is a single index available to quickly browse an index of machine readable feeds for all her ed-tech funding research. Did I mention, all of this on Google Sheet and Github, which both are free to use, if you leverage Github as a publicly available data project? Making it a pretty dead simple way for ANYONE to manage open data projects, and tell data-driven stories on a budget.

If you want to see the scope of what she is up to, head over to her [Hack Education Data Github organization](https://github.com/Hack-Education-Data). You can follow the storytelling side of all of this on her work at [Hack Education](http://hackeducation.com). What is scary about all of this, is that she is only getting started in this work. In August, we are moving to New York City where she is beginning [her Spencer Fellowship in Education Reporting at Columbia](http://spencerfellows.org/), where she will be focused 100% on this research. I'm looking forward to seeing what she does with [this type of data management using Google Sheets and Github](https://contrafabulists-lessons.github.io/google-sheet-to-github-website/), and working to support here where I can, but more importantly learning from how she takes the tools I've given her and evolve them to support her unique brand of data-driven storytelling in the education space.
