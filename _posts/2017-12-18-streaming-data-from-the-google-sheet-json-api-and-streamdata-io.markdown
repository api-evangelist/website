---
published: true
layout: post
title: Streaming Data From The Google Sheet JSON API And Streamdata.io
date: 2017-12-18T03:00:00.000Z
tags:
  - API Evangelist
  - Real Time
  - Spreadsheets
  - Data
image: >-
  https://s3.amazonaws.com/kinlane-productions/streamdata/streamdata-google-sheet.png
---
<p><a href="https://streamdata.io"><img src="https://s3.amazonaws.com/kinlane-productions/streamdata/streamdata-google-sheet.png" align="right" width="45%" style="padding: 15px;" /></a></p>I am playing with Streamdata.io as I learn how to use my new partner's service. Streamdata.io proxies any API, and uses [Server-Sent Event (SSE)](https://streamdata.io/blog/server-sent-events/) to push updates using [JSON Patch](https://tools.ietf.org/html/rfc6902). I am playing with making a variety of APIs real time using their service, and in my style, I wanted to share the story of what I'm working on, here on the blog. I was making updates to some data in a Google Sheet that I use to drive some data across a couple of my websites, and thought...can I make this spreadsheet streaming using Streamdata.io? Yes. Yes, I can.

To test out my theory I went and created a basic Google Sheet with two columns, one for product name, and one for price. Simulating a potential product pricing list that maybe I'd want to stream across multiple website, or possibly within client and partner portals. Then I published the Google Sheet to the web, making the data publicly available, so I didn't have to deal with any sort of authentication--something you will only want to do with publicly available data. I'll play around with an authenticated edition at some point in the future, showing more secure examples.

Once I made the sheet public I grabbed the unique key for the sheet, which you can find in the URL, and placed into this URL: https://spreadsheets.google.com/feeds/list/[sheet key]/od6/public/basic?alt=json. The Google Sheet key takes a little bit to identify in the URL, but it is the long GUID in the URL, which is the longest part of the URL when editing the sheet. Once you put the key in the URL, you can take the URL and paste in the browser--giving you a JSON representation of your sheet, instead of HTML, basically giving you a public API for your Google Sheet. The JSON for Google Sheets is a little verbose and complicated, but once you study a bit it doesn't take long for it to come into focus, showing eaching of the columns and rows.

Next, I created a Streamdata.io account, verified my email, logged in and created a new app. Something that took me about 2 minutes. I take the new URL for my Google Sheet and publish as the target URL in my Streamdata.io account. The UI then generates a curl statement for calling the API through the Streamdata.io proxy. Before it will work, you will have to replace the second question mark with an ampersand (&), as Streamdata.io assumes you do not have any parameters in the URL. Once replaced, you can open up your command line, paste in the command and run. Using Server-Sent Event (SSE) you'll see the script running, checking for changes. When you make any changes to your Google Sheet, you will see a JSON Patch response returned with any changes in real time. Providing a real-time stream of your Google Sheet which can be displayed in any application.

Next, I'm going to make a simple JavaScript web page that will take the results and render to the page, showing how to navigate the Google Sheets API response structure, as well as the JSON Patch using the Streamdata.io JavaScript SDK. All together this took me about 5 minutes to make happen, from creating the Google Sheet, to firing up a new Streamdata.io account, and executing the curl command. Sure, you'd still have to make it display anywhere, but it was quicker than I expected to make a Google Sheet real-time. I'll spend a little more time thinking about the possibilities for using Google Sheets in this way, and publishing some UI examples to Github, providing a forkable use case that anyone can follow when making it all work for them.

_**Disclosure:** [Streamdata.io](https://streamdata.io) is an API Evangelist partner, and sponsors this site._
