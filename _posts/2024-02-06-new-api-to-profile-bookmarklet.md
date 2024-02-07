---
published: true
layout: post
title: 'New API to Profile Bookmarklet'
image: https://kinlane-productions2.s3.amazonaws.com/apis-io-maps.png
author:
    name: kinlane
tags:
- APIs.json
- Artisanal
---
I regularly come across APIs that I want to profile as part of my <a href="https://github.com/apis-json/artisanal">APIs.json "Artisanal" work</a>, but I don't always have time to actually profile the API with APIs.json and OpenAPI. So I created a bookmarklet that will take the title, description (any text I highlight on page), and URL and submit as new GitHub issue.

I had come across the Nylas API, and I wanted to quickly add it for profiling later when I am doing my work.

<p><a href="https://developer.nylas.com/"><img src="https://kinlane-productions2.s3.amazonaws.com/nylas-developer-area.png" width="100%"></a></p>

Then I produced a new bookmarklet (<a href="javascript:void(window.open('https://github.com/apis-json/artisanal/issues/new?labels=new&title=%27+encodeURIComponent(document.title)+%27&body=%27+getSelection().toString()+%27 ~ %27+encodeURIComponent(location.href)));">which you can drag to your toolbar</a>), which submits the Nylas developer portal as an issue for profiling later.

<p><a href="https://github.com/apis-json/artisanal/issues/2"><img src="https://kinlane-productions2.s3.amazonaws.com/nylas-add-for-profiling.png" width="100%"></a></p>

It is an easy way to use GitHub issues as a task list, or inbox for my <a href="https://apisjson.org">APIs.json</a> profiling work, producing new APIs for the <a href="https://apis.io">APIs.io search engine</a>. I am manually processing each of these new APIs at the moment, but automating more of the process over time.