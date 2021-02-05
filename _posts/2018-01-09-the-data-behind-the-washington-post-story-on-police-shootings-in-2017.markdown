---
published: true
layout: post
title: The Data Behind The Washington Post Story On Police Shootings in 2017
date: 2018-01-09T10:00:00.000Z
tags:
  - API Evangelist
  - Data
  - Journalism
  - News
  - Policing
image: >-
  https://s3.amazonaws.com/kinlane-productions/washington-post/washington-post-fatal-force-story.png
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/washington-post/washington-post-fatal-force-story.png" align="right" width="45%" style="padding: 15px;" /></p>I was getting ready to write my usual, "wish there was actual data behind this story about a database" story, while reading [the Fatal Force story in the Washington Post](https://www.washingtonpost.com/graphics/national/police-shootings-2017/), and then I saw the link! Fatal Force, 987 people have been shot and killed by police in 2017. [Read about our methodology](https://www.washingtonpost.com/national/how-the-washington-post-is-examining-police-shootings-in-the-united-states/2016/07/07/d9c52238-43ad-11e6-8856-f26de2537a9d_story.html). [Download the data](https://github.com/washingtonpost/data-police-shootings). I am so very happy to see this. An actual prominent link to a machine readable version of the data, published on Github--this should be the default for ALL data journalism in this era.

I see story after story reference the data behind, without providing any links to the data. As a database professional this practice drives me insane. Every single story that provides data driven visualizations, statistics, analysis, tables, or any other derivative from data journalism, should provide a link to the Github repository which contains at least CSV representations of the data, if not JSON. This is the minimum for ALL data journalism going forward. If you do not meet this bar, your work should be in question. Other analysts, researchers, and journalists should be able to come in behind your work and audit, verify, validate, and even build upon and augment your work, for it to be considered relevant in this time period.

Github is free. Google Sheets is free. There is no excuse for you not to be publishing the data behind your work in a machine readable format. [It makes me happy to see the Washington Post using Github like this, especially when they do not have an active API or developer program](https://github.com/washingtonpost). I'm going to spend some time looking through the other repositories in their Github organization, and also begin tracking on which news agencies are actively using Github. Hopefully, in the near future, I can stop ranting about reputable news outlets not sharing their data behind stories in machine readable formats, because the rest of the industry will help police this, and only the real data-driven journalists will be left. #ShowYourWork
