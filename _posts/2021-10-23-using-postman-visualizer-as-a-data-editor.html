---
published: true
layout: post
title: 'Using Postman Visualizer as a Data Editor'
image: https://kinlane-productions2.s3.amazonaws.com/restaurant-json-editor.png
tags:
  - Postman
  - Data
  - Visualizer
  - Editor
---
<p>I use and abuse the Postman platform for a lot of things it wasn’t designed for. In the same way that I have used and abused the Github platform for things it wasn’t designed for over the last five years. I find Postman collections to be infinitely useful for just about anything I want to do in the world of APIs, and recently I have been using them as little API-First data stores. Meaning I have little lists of things I want to curate and make available as simple APIs, and I find collections via the Postman platform to be a perfect way to manage lots of little datasets.</p>

<p>I have a number of collections I use for data storage, but I figured I’d build my proof of concept data editor using Postman visualizer on <a href="https://www.postman.com/postman/workspace/restaurant/overview">my restaurant demo workspace</a>. This is a workspace I use multiple times a week during meetings, demos, talks, and demonstrating how you do APIs in an API-first way, and I’d like to have a simple editor for editing the underlying data, but also available for demonstrating the power of Postman visualizer. My restaurant workspace began with an OpenAPI, but then I quickly generated a Postman collection, added examples, and published as a mock API—pretty standard API-first Postman platform stuff. I can plug the URL of my mock server into my collection and see the results each time I hit send for any of the paths I have defined. Each request in my collection has one example which is used for the API documentation and the mock server, and I am looking to visualize and edit the first request, which happens to be a list of my restaurants.</p>

<p><img src="https://kinlane-productions2.s3.amazonaws.com/restaurant-json-view.png" width="100%" style="padding: 10px"></p>

<p>Then using visualizer for the request I pull the JSON and render as a table, showing two the of properties for cuisine and menu, potentially allowing me to actually edit each property in my list of restaurants. Rendering the returning JSON as HTML, and giving me a little UI editor for my example restaurant data.</p>

<p><img src="https://kinlane-productions2.s3.amazonaws.com/restaurant-json-editor.png" width="100%" style="padding: 10px"></p>

<p>Now that I have my restaurant listing editable in text fields I add a save button. When the visualizer loads it stores the JSON in a central textarea, then each time you edit one of the fields it will update the centralized JSON, and when I click the save button it grabs this JSON, pulls the collection from the Postman API, updates the example body of the collection with my changed JSON, and PUTs it back via the Postman API. Providing a pretty hacky, but interesting script for rendering, updating, and then saving data via a collection.</p>

<script src="https://gist.github.com/kinlane/a410511790a1fc308b9e386f7ffe749e.js"></script>

<p>I can definitely improve this script in a lot of ways, allowing me to add rows, delete rows, and make it more generic so it will handle any time of JSON, not just my restaurant data. I will get around to all of this. I just wanted to build the basic proof of concept and show that I could pull data from a collection, render it using visualizer, update it, and save it back via the Postman API—-mission accomplished. This means that each of my collections I am using to store data can also have a little UI for editing that data. I am perfectly happy editing the data via JSON, but sometimes it is a pain in the ass. Plus this means non-developers can get in here and potentially manage data without feeling like they will mess up the JSON.</p>

<p>Next I will retrofit a few of my example data store collections with this editor and improve on my JavaScript. Then I am going to play around with actually pulling data from an API, rendering the results to the editor via visualizer, allow for editing, filtering, curating, etc. and then allow the desired results to be saved to the underlying example or examples within the collection. This means I can pull a list of news articles from an RSS feed, allow for curation, and saving to the underlying collection for making daa available via a static API for use in other applications. I could do the same for Twitter, Github, or any other types of results I want to pull from a 3rd party API, but then store data locally within the collection. I don’t see the Postman mock feature in the same way everyone else does. I see it as a static API data server, and collections are just a key/value store, allowing me to do whatever I want in an API-first way.</p>