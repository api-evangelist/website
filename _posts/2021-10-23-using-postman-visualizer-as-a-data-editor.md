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
I use and abuse the Postman platform for a lot of things it wasn’t designed for. In the same way that I have used and abused the Github platform for things it wasn’t designed for over the last five years. I find Postman collections to be infinitely useful for just about anything I want to do in the world of APIs, and recently I have been using them as little API-First data stores. Meaning I have little lists of things I want to curate and make available as simple APIs, and I find collections via the Postman platform to be a perfect way to manage lots of little datasets.


I have a number of collections I use for data storage, but I figured I’d build my proof of concept data editor using Postman visualizer on [my restaurant demo workspace](https://www.postman.com/postman/workspace/restaurant/overview). This is a workspace I use multiple times a week during meetings, demos, talks, and demonstrating how you do APIs in an API-first way, and I’d like to have a simple editor for editing the underlying data, but also available for demonstrating the power of Postman visualizer. My restaurant workspace began with an OpenAPI, but then I quickly generated a Postman collection, added examples, and published as a mock API—pretty standard API-first Postman platform stuff. I can plug the URL of my mock server into my collection and see the results each time I hit send for any of the paths I have defined. Each request in my collection has one example which is used for the API documentation and the mock server, and I am looking to visualize and edit the first request, which happens to be a list of my restaurants.


![](https://kinlane-productions2.s3.amazonaws.com/restaurant-json-view.png)


Then using visualizer for the request I pull the JSON and render as a table, showing two the of properties for cuisine and menu, potentially allowing me to actually edit each property in my list of restaurants. Rendering the returning JSON as HTML, and giving me a little UI editor for my example restaurant data.


![](https://kinlane-productions2.s3.amazonaws.com/restaurant-json-editor.png)


Now that I have my restaurant listing editable in text fields I add a save button. When the visualizer loads it stores the JSON in a central textarea, then each time you edit one of the fields it will update the centralized JSON, and when I click the save button it grabs this JSON, pulls the collection from the Postman API, updates the example body of the collection with my changed JSON, and PUTs it back via the Postman API. Providing a pretty hacky, but interesting script for rendering, updating, and then saving data via a collection.

<div id="gist112545225" class="gist">
    <div class="gist-file" translate="no">
      <div class="gist-data">
        <div class="js-gist-file-update-container js-task-list-container file-box">
  <div id="file-postman-restaurant-visualizer-js" class="file my-2">
    
    <div itemprop="text" class="Box-body p-0 blob-wrapper data type-javascript  ">

        
<div class="js-check-bidi js-blob-code-container blob-code-content">

  <template class="js-file-alert-template">
  <div data-view-component="true" class="flash flash-warn flash-full d-flex flex-items-center">
  <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-alert">
    <path fill-rule="evenodd" d="M8.22 1.754a.25.25 0 00-.44 0L1.698 13.132a.25.25 0 00.22.368h12.164a.25.25 0 00.22-.368L8.22 1.754zm-1.763-.707c.659-1.234 2.427-1.234 3.086 0l6.082 11.378A1.75 1.75 0 0114.082 15H1.918a1.75 1.75 0 01-1.543-2.575L6.457 1.047zM9 11a1 1 0 11-2 0 1 1 0 012 0zm-.25-5.25a.75.75 0 00-1.5 0v2.5a.75.75 0 001.5 0v-2.5z"></path>
</svg>
  
    <span>
      This file contains bidirectional Unicode text that may be interpreted or compiled differently than what appears below. To review, open the file in an editor that reveals hidden Unicode characters.
      <a href="https://github.co/hiddenchars" target="_blank">Learn more about bidirectional Unicode characters</a>
    </span>


  <div data-view-component="true" class="flash-action">        <a href="{{ revealButtonHref }}" data-view-component="true" class="btn-sm btn">    Show hidden characters
</a>
</div>
</div></template>
<template class="js-line-alert-template">
  <span aria-label="This line has hidden Unicode characters" data-view-component="true" class="line-alert tooltipped tooltipped-e">
    <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-alert">
    <path fill-rule="evenodd" d="M8.22 1.754a.25.25 0 00-.44 0L1.698 13.132a.25.25 0 00.22.368h12.164a.25.25 0 00.22-.368L8.22 1.754zm-1.763-.707c.659-1.234 2.427-1.234 3.086 0l6.082 11.378A1.75 1.75 0 0114.082 15H1.918a1.75 1.75 0 01-1.543-2.575L6.457 1.047zM9 11a1 1 0 11-2 0 1 1 0 012 0zm-.25-5.25a.75.75 0 00-1.5 0v2.5a.75.75 0 001.5 0v-2.5z"></path>
</svg>
</span></template>

  <table data-hpc="" class="highlight tab-size js-file-line-container js-code-nav-container js-tagsearch-file" data-tab-size="8" data-paste-markdown-skip="" data-tagsearch-lang="JavaScript" data-tagsearch-path="postman-restaurant-visualizer.js">
        <tbody><tr>
          <td id="file-postman-restaurant-visualizer-js-L1" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="1"></td>
          <td id="file-postman-restaurant-visualizer-js-LC1" class="blob-code blob-code-inner js-file-line"><span class="pl-c">// Just a default assertion to make sure we aren't erroring out</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L2" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="2"></td>
          <td id="file-postman-restaurant-visualizer-js-LC2" class="blob-code blob-code-inner js-file-line"><span class="pl-s1">pm</span><span class="pl-kos">.</span><span class="pl-en">test</span><span class="pl-kos">(</span><span class="pl-s">"Status code is 200"</span><span class="pl-kos">,</span> <span class="pl-k">function</span> <span class="pl-kos">(</span><span class="pl-kos">)</span> <span class="pl-kos">{</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L3" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="3"></td>
          <td id="file-postman-restaurant-visualizer-js-LC3" class="blob-code blob-code-inner js-file-line">    <span class="pl-s1">pm</span><span class="pl-kos">.</span><span class="pl-c1">response</span><span class="pl-kos">.</span><span class="pl-c1">to</span><span class="pl-kos">.</span><span class="pl-c1">have</span><span class="pl-kos">.</span><span class="pl-en">status</span><span class="pl-kos">(</span><span class="pl-c1">200</span><span class="pl-kos">)</span><span class="pl-kos">;</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L4" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="4"></td>
          <td id="file-postman-restaurant-visualizer-js-LC4" class="blob-code blob-code-inner js-file-line"><span class="pl-kos">}</span><span class="pl-kos">)</span><span class="pl-kos">;</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L5" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="5"></td>
          <td id="file-postman-restaurant-visualizer-js-LC5" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L6" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="6"></td>
          <td id="file-postman-restaurant-visualizer-js-LC6" class="blob-code blob-code-inner js-file-line"><span class="pl-c">// pull the collection id from the collection variables</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L7" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="7"></td>
          <td id="file-postman-restaurant-visualizer-js-LC7" class="blob-code blob-code-inner js-file-line"><span class="pl-k">var</span> <span class="pl-s1">collection_id</span> <span class="pl-c1">=</span> <span class="pl-s1">pm</span><span class="pl-kos">.</span><span class="pl-c1">variables</span><span class="pl-kos">.</span><span class="pl-en">get</span><span class="pl-kos">(</span><span class="pl-s">"collection_id"</span><span class="pl-kos">)</span><span class="pl-kos">;</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L8" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="8"></td>
          <td id="file-postman-restaurant-visualizer-js-LC8" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L9" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="9"></td>
          <td id="file-postman-restaurant-visualizer-js-LC9" class="blob-code blob-code-inner js-file-line"><span class="pl-c">// pull the api id from the collection variables</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L10" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="10"></td>
          <td id="file-postman-restaurant-visualizer-js-LC10" class="blob-code blob-code-inner js-file-line"><span class="pl-k">var</span> <span class="pl-s1">api_key</span> <span class="pl-c1">=</span> <span class="pl-s1">pm</span><span class="pl-kos">.</span><span class="pl-c1">variables</span><span class="pl-kos">.</span><span class="pl-en">get</span><span class="pl-kos">(</span><span class="pl-s">"api_key"</span><span class="pl-kos">)</span><span class="pl-kos">;</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L11" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="11"></td>
          <td id="file-postman-restaurant-visualizer-js-LC11" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L12" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="12"></td>
          <td id="file-postman-restaurant-visualizer-js-LC12" class="blob-code blob-code-inner js-file-line"><span class="pl-c">// This grabs the response from this API call</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L13" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="13"></td>
          <td id="file-postman-restaurant-visualizer-js-LC13" class="blob-code blob-code-inner js-file-line"><span class="pl-k">var</span> <span class="pl-s1">jsonData</span> <span class="pl-c1">=</span> <span class="pl-s1">pm</span><span class="pl-kos">.</span><span class="pl-c1">response</span><span class="pl-kos">.</span><span class="pl-en">json</span><span class="pl-kos">(</span><span class="pl-kos">)</span><span class="pl-kos">;</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L14" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="14"></td>
          <td id="file-postman-restaurant-visualizer-js-LC14" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L15" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="15"></td>
          <td id="file-postman-restaurant-visualizer-js-LC15" class="blob-code blob-code-inner js-file-line"><span class="pl-c">// Build a string that will be our rendered Javascript</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L16" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="16"></td>
          <td id="file-postman-restaurant-visualizer-js-LC16" class="blob-code blob-code-inner js-file-line"><span class="pl-k">var</span> <span class="pl-s1">v</span> <span class="pl-c1">=</span> <span class="pl-s">`</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L17" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="17"></td>
          <td id="file-postman-restaurant-visualizer-js-LC17" class="blob-code blob-code-inner js-file-line"><span class="pl-s">&lt;script&gt;</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L18" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="18"></td>
          <td id="file-postman-restaurant-visualizer-js-LC18" class="blob-code blob-code-inner js-file-line"><span class="pl-s">function runUpdate(data){</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L19" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="19"></td>
          <td id="file-postman-restaurant-visualizer-js-LC19" class="blob-code blob-code-inner js-file-line"><span class="pl-s"></span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L20" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="20"></td>
          <td id="file-postman-restaurant-visualizer-js-LC20" class="blob-code blob-code-inner js-file-line"><span class="pl-s">    // Provide us with a visual log</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L21" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="21"></td>
          <td id="file-postman-restaurant-visualizer-js-LC21" class="blob-code blob-code-inner js-file-line"><span class="pl-s">    document.getElementById('alert').innerHTML = "Updating the data using the Postman API..."; </span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L22" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="22"></td>
          <td id="file-postman-restaurant-visualizer-js-LC22" class="blob-code blob-code-inner js-file-line"><span class="pl-s"></span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L23" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="23"></td>
          <td id="file-postman-restaurant-visualizer-js-LC23" class="blob-code blob-code-inner js-file-line"><span class="pl-s">    // Pull the local JSON store</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L24" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="24"></td>
          <td id="file-postman-restaurant-visualizer-js-LC24" class="blob-code blob-code-inner js-file-line"><span class="pl-s">    var store = document.getElementById('store').value;</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L25" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="25"></td>
          <td id="file-postman-restaurant-visualizer-js-LC25" class="blob-code blob-code-inner js-file-line"><span class="pl-s"></span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L26" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="26"></td>
          <td id="file-postman-restaurant-visualizer-js-LC26" class="blob-code blob-code-inner js-file-line"><span class="pl-s">    // Setting the body of the first rquest to our JSON store</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L27" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="27"></td>
          <td id="file-postman-restaurant-visualizer-js-LC27" class="blob-code blob-code-inner js-file-line"><span class="pl-s">    data.collection.item[0].response[0].body = store;</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L28" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="28"></td>
          <td id="file-postman-restaurant-visualizer-js-LC28" class="blob-code blob-code-inner js-file-line"><span class="pl-s"></span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L29" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="29"></td>
          <td id="file-postman-restaurant-visualizer-js-LC29" class="blob-code blob-code-inner js-file-line"><span class="pl-s">    // Set options for our pull of collection from Postman API</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L30" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="30"></td>
          <td id="file-postman-restaurant-visualizer-js-LC30" class="blob-code blob-code-inner js-file-line"><span class="pl-s">    var options = {};</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L31" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="31"></td>
          <td id="file-postman-restaurant-visualizer-js-LC31" class="blob-code blob-code-inner js-file-line"><span class="pl-s">    options['method'] = "PUT";</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L32" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="32"></td>
          <td id="file-postman-restaurant-visualizer-js-LC32" class="blob-code blob-code-inner js-file-line"><span class="pl-s">    options['headers'] = {};</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L33" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="33"></td>
          <td id="file-postman-restaurant-visualizer-js-LC33" class="blob-code blob-code-inner js-file-line"><span class="pl-s">    options['headers']['X-API-Key'] = "`</span> <span class="pl-c1">+</span> <span class="pl-s1">api_key</span> <span class="pl-c1">+</span> <span class="pl-s">`";</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L34" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="34"></td>
          <td id="file-postman-restaurant-visualizer-js-LC34" class="blob-code blob-code-inner js-file-line"><span class="pl-s">    options['body'] = JSON.stringify(data);</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L35" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="35"></td>
          <td id="file-postman-restaurant-visualizer-js-LC35" class="blob-code blob-code-inner js-file-line"><span class="pl-s"></span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L36" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="36"></td>
          <td id="file-postman-restaurant-visualizer-js-LC36" class="blob-code blob-code-inner js-file-line"><span class="pl-s">    // Post an update to the Postman API to update our collection</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L37" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="37"></td>
          <td id="file-postman-restaurant-visualizer-js-LC37" class="blob-code blob-code-inner js-file-line"><span class="pl-s">    fetch('https://api.getpostman.com/collections/`</span> <span class="pl-c1">+</span> <span class="pl-s1">collection_id</span> <span class="pl-c1">+</span> <span class="pl-s">`',options)</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L38" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="38"></td>
          <td id="file-postman-restaurant-visualizer-js-LC38" class="blob-code blob-code-inner js-file-line"><span class="pl-s">    .then(response =&gt; response.json())</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L39" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="39"></td>
          <td id="file-postman-restaurant-visualizer-js-LC39" class="blob-code blob-code-inner js-file-line"><span class="pl-s">    .then(data =&gt; {</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L40" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="40"></td>
          <td id="file-postman-restaurant-visualizer-js-LC40" class="blob-code blob-code-inner js-file-line"><span class="pl-s">    document.getElementById('alert').innerHTML = "Data was successfully saved!";</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L41" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="41"></td>
          <td id="file-postman-restaurant-visualizer-js-LC41" class="blob-code blob-code-inner js-file-line"><span class="pl-s">    })</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L42" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="42"></td>
          <td id="file-postman-restaurant-visualizer-js-LC42" class="blob-code blob-code-inner js-file-line"><span class="pl-s">    .catch((error) =&gt; {</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L43" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="43"></td>
          <td id="file-postman-restaurant-visualizer-js-LC43" class="blob-code blob-code-inner js-file-line"><span class="pl-s">    document.getElementById('alert').innerHTML = "Something went horribly wrong!";</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L44" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="44"></td>
          <td id="file-postman-restaurant-visualizer-js-LC44" class="blob-code blob-code-inner js-file-line"><span class="pl-s">    });</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L45" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="45"></td>
          <td id="file-postman-restaurant-visualizer-js-LC45" class="blob-code blob-code-inner js-file-line"><span class="pl-s">}</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L46" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="46"></td>
          <td id="file-postman-restaurant-visualizer-js-LC46" class="blob-code blob-code-inner js-file-line"><span class="pl-s"> function saveData(){</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L47" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="47"></td>
          <td id="file-postman-restaurant-visualizer-js-LC47" class="blob-code blob-code-inner js-file-line"><span class="pl-s"></span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L48" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="48"></td>
          <td id="file-postman-restaurant-visualizer-js-LC48" class="blob-code blob-code-inner js-file-line"><span class="pl-s">     // Provide us with a visual log </span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L49" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="49"></td>
          <td id="file-postman-restaurant-visualizer-js-LC49" class="blob-code blob-code-inner js-file-line"><span class="pl-s">    document.getElementById('alert').innerHTML = "Starting the process of saving the data...";</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L50" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="50"></td>
          <td id="file-postman-restaurant-visualizer-js-LC50" class="blob-code blob-code-inner js-file-line"><span class="pl-s"></span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L51" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="51"></td>
          <td id="file-postman-restaurant-visualizer-js-LC51" class="blob-code blob-code-inner js-file-line"><span class="pl-s">    // Set options for our pull of collection from Postman API</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L52" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="52"></td>
          <td id="file-postman-restaurant-visualizer-js-LC52" class="blob-code blob-code-inner js-file-line"><span class="pl-s">    var options = {};</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L53" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="53"></td>
          <td id="file-postman-restaurant-visualizer-js-LC53" class="blob-code blob-code-inner js-file-line"><span class="pl-s">    options['method'] = "GET";</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L54" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="54"></td>
          <td id="file-postman-restaurant-visualizer-js-LC54" class="blob-code blob-code-inner js-file-line"><span class="pl-s">    options['headers'] = {};</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L55" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="55"></td>
          <td id="file-postman-restaurant-visualizer-js-LC55" class="blob-code blob-code-inner js-file-line"><span class="pl-s">    options['headers']['X-API-Key'] = "`</span> <span class="pl-c1">+</span> <span class="pl-s1">api_key</span> <span class="pl-c1">+</span> <span class="pl-s">`";</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L56" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="56"></td>
          <td id="file-postman-restaurant-visualizer-js-LC56" class="blob-code blob-code-inner js-file-line"><span class="pl-s"></span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L57" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="57"></td>
          <td id="file-postman-restaurant-visualizer-js-LC57" class="blob-code blob-code-inner js-file-line"><span class="pl-s">    // Pull collection from the Postman API</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L58" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="58"></td>
          <td id="file-postman-restaurant-visualizer-js-LC58" class="blob-code blob-code-inner js-file-line"><span class="pl-s">    fetch('https://api.getpostman.com/collections/`</span> <span class="pl-c1">+</span> <span class="pl-s1">collection_id</span> <span class="pl-c1">+</span> <span class="pl-s">`',options)</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L59" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="59"></td>
          <td id="file-postman-restaurant-visualizer-js-LC59" class="blob-code blob-code-inner js-file-line"><span class="pl-s">    .then(response =&gt;response.json())</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L60" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="60"></td>
          <td id="file-postman-restaurant-visualizer-js-LC60" class="blob-code blob-code-inner js-file-line"><span class="pl-s">    .then(data =&gt; runUpdate(data))</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L61" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="61"></td>
          <td id="file-postman-restaurant-visualizer-js-LC61" class="blob-code blob-code-inner js-file-line"><span class="pl-s"> }</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L62" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="62"></td>
          <td id="file-postman-restaurant-visualizer-js-LC62" class="blob-code blob-code-inner js-file-line"><span class="pl-s"> function updateData(id){</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L63" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="63"></td>
          <td id="file-postman-restaurant-visualizer-js-LC63" class="blob-code blob-code-inner js-file-line"><span class="pl-s">    </span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L64" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="64"></td>
          <td id="file-postman-restaurant-visualizer-js-LC64" class="blob-code blob-code-inner js-file-line"><span class="pl-s">    // Provide us with a visual log</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L65" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="65"></td>
          <td id="file-postman-restaurant-visualizer-js-LC65" class="blob-code blob-code-inner js-file-line"><span class="pl-s">    document.getElementById('alert').innerHTML = "Updating data in row " + id + "..";</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L66" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="66"></td>
          <td id="file-postman-restaurant-visualizer-js-LC66" class="blob-code blob-code-inner js-file-line"><span class="pl-s"></span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L67" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="67"></td>
          <td id="file-postman-restaurant-visualizer-js-LC67" class="blob-code blob-code-inner js-file-line"><span class="pl-s">    // Pull the central store in a textarea</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L68" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="68"></td>
          <td id="file-postman-restaurant-visualizer-js-LC68" class="blob-code blob-code-inner js-file-line"><span class="pl-s">    var store = JSON.parse(document.getElementById('store').value);</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L69" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="69"></td>
          <td id="file-postman-restaurant-visualizer-js-LC69" class="blob-code blob-code-inner js-file-line"><span class="pl-s"></span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L70" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="70"></td>
          <td id="file-postman-restaurant-visualizer-js-LC70" class="blob-code blob-code-inner js-file-line"><span class="pl-s">    // Update our two fields</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L71" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="71"></td>
          <td id="file-postman-restaurant-visualizer-js-LC71" class="blob-code blob-code-inner js-file-line"><span class="pl-s">    store[id].servesCuisine = document.getElementById('servesCuisine-' + id).value</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L72" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="72"></td>
          <td id="file-postman-restaurant-visualizer-js-LC72" class="blob-code blob-code-inner js-file-line"><span class="pl-s">    store[id].menu = document.getElementById('menu-' + id).value</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L73" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="73"></td>
          <td id="file-postman-restaurant-visualizer-js-LC73" class="blob-code blob-code-inner js-file-line"><span class="pl-s"></span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L74" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="74"></td>
          <td id="file-postman-restaurant-visualizer-js-LC74" class="blob-code blob-code-inner js-file-line"><span class="pl-s">    // Update the central store</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L75" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="75"></td>
          <td id="file-postman-restaurant-visualizer-js-LC75" class="blob-code blob-code-inner js-file-line"><span class="pl-s">    document.getElementById('store').value = JSON.stringify(store);</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L76" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="76"></td>
          <td id="file-postman-restaurant-visualizer-js-LC76" class="blob-code blob-code-inner js-file-line"><span class="pl-s"> } </span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L77" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="77"></td>
          <td id="file-postman-restaurant-visualizer-js-LC77" class="blob-code blob-code-inner js-file-line"><span class="pl-s">&lt;/script&gt;</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L78" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="78"></td>
          <td id="file-postman-restaurant-visualizer-js-LC78" class="blob-code blob-code-inner js-file-line"><span class="pl-s">`</span><span class="pl-kos">;</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L79" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="79"></td>
          <td id="file-postman-restaurant-visualizer-js-LC79" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L80" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="80"></td>
          <td id="file-postman-restaurant-visualizer-js-LC80" class="blob-code blob-code-inner js-file-line"><span class="pl-c">// Continue building string with HTML to render</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L81" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="81"></td>
          <td id="file-postman-restaurant-visualizer-js-LC81" class="blob-code blob-code-inner js-file-line"><span class="pl-s1">v</span> <span class="pl-c1">+=</span> <span class="pl-s">'&lt;h1&gt;Restaurants&lt;/h1&gt;'</span><span class="pl-kos">;</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L82" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="82"></td>
          <td id="file-postman-restaurant-visualizer-js-LC82" class="blob-code blob-code-inner js-file-line"><span class="pl-s1">v</span> <span class="pl-c1">+=</span> <span class="pl-s">'&lt;p&gt;This is an editor for my mock restaurant data, pulling a list of restaurants I have stored in a Postman collection, renders to the screen as HTML using visualizer, but then allows me to edit two of the fields. Once done editing I can click the save button and it will save the data back to the example in the Postman collection, essentially using Postman collections as a data store.&lt;/p&gt;'</span><span class="pl-kos">;</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L83" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="83"></td>
          <td id="file-postman-restaurant-visualizer-js-LC83" class="blob-code blob-code-inner js-file-line"><span class="pl-s1">v</span> <span class="pl-c1">+=</span> <span class="pl-s">'&lt;table width="100%" border="0"&gt;'</span><span class="pl-kos">;</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L84" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="84"></td>
          <td id="file-postman-restaurant-visualizer-js-LC84" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L85" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="85"></td>
          <td id="file-postman-restaurant-visualizer-js-LC85" class="blob-code blob-code-inner js-file-line"><span class="pl-c">// Loop through each entry in the response.</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L86" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="86"></td>
          <td id="file-postman-restaurant-visualizer-js-LC86" class="blob-code blob-code-inner js-file-line"><span class="pl-k">for</span> <span class="pl-kos">(</span><span class="pl-s1">i</span> <span class="pl-c1">=</span> <span class="pl-c1">0</span><span class="pl-kos">;</span> <span class="pl-s1">i</span> <span class="pl-c1">&lt;</span> <span class="pl-s1">jsonData</span><span class="pl-kos">.</span><span class="pl-c1">length</span><span class="pl-kos">;</span> <span class="pl-s1">i</span><span class="pl-c1">++</span><span class="pl-kos">)</span> <span class="pl-kos">{</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L87" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="87"></td>
          <td id="file-postman-restaurant-visualizer-js-LC87" class="blob-code blob-code-inner js-file-line">  <span class="pl-s1">v</span> <span class="pl-c1">+=</span> <span class="pl-s">'&lt;tr&gt;'</span><span class="pl-kos">;</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L88" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="88"></td>
          <td id="file-postman-restaurant-visualizer-js-LC88" class="blob-code blob-code-inner js-file-line">  <span class="pl-s1">v</span> <span class="pl-c1">+=</span> <span class="pl-s">'&lt;td width="30%" style="border:0px;"&gt;&lt;input ty[e="text" onchange="updateData('</span> <span class="pl-c1">+</span> <span class="pl-s1">i</span> <span class="pl-c1">+</span> <span class="pl-s">');" id="servesCuisine-'</span> <span class="pl-c1">+</span> <span class="pl-s1">i</span> <span class="pl-c1">+</span> <span class="pl-s">'" name="menu" value="'</span> <span class="pl-c1">+</span> <span class="pl-s1">jsonData</span><span class="pl-kos">[</span><span class="pl-s1">i</span><span class="pl-kos">]</span><span class="pl-kos">.</span><span class="pl-c1">servesCuisine</span> <span class="pl-c1">+</span> <span class="pl-s">'" style="width: 100%; border: 1px solid #000; padding: 5px;"&gt;&lt;/td&gt;'</span><span class="pl-kos">;</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L89" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="89"></td>
          <td id="file-postman-restaurant-visualizer-js-LC89" class="blob-code blob-code-inner js-file-line">  <span class="pl-s1">v</span> <span class="pl-c1">+=</span> <span class="pl-s">'&lt;td width="70%" style="border:0px;"&gt;&lt;input ty[e="text" onchange="updateData('</span> <span class="pl-c1">+</span> <span class="pl-s1">i</span> <span class="pl-c1">+</span> <span class="pl-s">');" id="menu-'</span> <span class="pl-c1">+</span> <span class="pl-s1">i</span> <span class="pl-c1">+</span> <span class="pl-s">'" name="menu" value="'</span> <span class="pl-c1">+</span> <span class="pl-s1">jsonData</span><span class="pl-kos">[</span><span class="pl-s1">i</span><span class="pl-kos">]</span><span class="pl-kos">.</span><span class="pl-c1">menu</span> <span class="pl-c1">+</span> <span class="pl-s">'" style="width: 100%; border: 1px solid #000; padding: 5px;"&gt;&lt;/td&gt;'</span><span class="pl-kos">;</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L90" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="90"></td>
          <td id="file-postman-restaurant-visualizer-js-LC90" class="blob-code blob-code-inner js-file-line">  <span class="pl-s1">v</span> <span class="pl-c1">+=</span> <span class="pl-s">'&lt;/tr&gt;'</span><span class="pl-kos">;</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L91" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="91"></td>
          <td id="file-postman-restaurant-visualizer-js-LC91" class="blob-code blob-code-inner js-file-line"><span class="pl-kos">}</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L92" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="92"></td>
          <td id="file-postman-restaurant-visualizer-js-LC92" class="blob-code blob-code-inner js-file-line"><span class="pl-s1">v</span> <span class="pl-c1">+=</span> <span class="pl-s">'&lt;/table&gt;'</span><span class="pl-kos">;</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L93" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="93"></td>
          <td id="file-postman-restaurant-visualizer-js-LC93" class="blob-code blob-code-inner js-file-line"><span class="pl-s1">v</span> <span class="pl-c1">+=</span> <span class="pl-s">'&lt;div id="alert" style="text-align: center; margin-bottom: 5px;"&gt;&lt;/div&gt;'</span><span class="pl-kos">;</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L94" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="94"></td>
          <td id="file-postman-restaurant-visualizer-js-LC94" class="blob-code blob-code-inner js-file-line"><span class="pl-s1">v</span> <span class="pl-c1">+=</span> <span class="pl-s">'&lt;textarea id="store" cols="100" rows="10" style="display: none;"&gt;'</span> <span class="pl-c1">+</span> <span class="pl-c1">JSON</span><span class="pl-kos">.</span><span class="pl-en">stringify</span><span class="pl-kos">(</span><span class="pl-s1">jsonData</span><span class="pl-kos">)</span> <span class="pl-c1">+</span> <span class="pl-s">'&lt;/textarea&gt;'</span><span class="pl-kos">;</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L95" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="95"></td>
          <td id="file-postman-restaurant-visualizer-js-LC95" class="blob-code blob-code-inner js-file-line"><span class="pl-s1">v</span> <span class="pl-c1">+=</span> <span class="pl-s">'&lt;center&gt;&lt;input type="button" name="save" value="Save Changes" onclick="saveData();"&gt;&lt;/center&gt;'</span><span class="pl-kos">;</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L96" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="96"></td>
          <td id="file-postman-restaurant-visualizer-js-LC96" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L97" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="97"></td>
          <td id="file-postman-restaurant-visualizer-js-LC97" class="blob-code blob-code-inner js-file-line"><span class="pl-c">// Visualize our list of data</span></td>
        </tr>
        <tr>
          <td id="file-postman-restaurant-visualizer-js-L98" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="98"></td>
          <td id="file-postman-restaurant-visualizer-js-LC98" class="blob-code blob-code-inner js-file-line"><span class="pl-s1">pm</span><span class="pl-kos">.</span><span class="pl-c1">visualizer</span><span class="pl-kos">.</span><span class="pl-en">set</span><span class="pl-kos">(</span><span class="pl-s1">v</span><span class="pl-kos">)</span><span class="pl-kos">;</span></td>
        </tr>
  </tbody></table>
</div>


    </div>

  </div>
</div>

      </div>
      <div class="gist-meta">
        <a href="https://gist.github.com/kinlane/a410511790a1fc308b9e386f7ffe749e/raw/760c0d467e632201894e7b0e2ca5b6f5386f7f29/postman-restaurant-visualizer.js" style="float: right;">view raw</a>
        <a href="https://gist.github.com/kinlane/a410511790a1fc308b9e386f7ffe749e#file-postman-restaurant-visualizer-js">
          postman-restaurant-visualizer.js
        </a>
        hosted with ❤ by <a href="https://github.com/">GitHub</a>
      </div>
    </div>
</div>


I can definitely improve this script in a lot of ways, allowing me to add rows, delete rows, and make it more generic so it will handle any time of JSON, not just my restaurant data. I will get around to all of this. I just wanted to build the basic proof of concept and show that I could pull data from a collection, render it using visualizer, update it, and save it back via the Postman API—-mission accomplished. This means that each of my collections I am using to store data can also have a little UI for editing that data. I am perfectly happy editing the data via JSON, but sometimes it is a pain in the ass. Plus this means non-developers can get in here and potentially manage data without feeling like they will mess up the JSON.


Next I will retrofit a few of my example data store collections with this editor and improve on my JavaScript. Then I am going to play around with actually pulling data from an API, rendering the results to the editor via visualizer, allow for editing, filtering, curating, etc. and then allow the desired results to be saved to the underlying example or examples within the collection. This means I can pull a list of news articles from an RSS feed, allow for curation, and saving to the underlying collection for making daa available via a static API for use in other applications. I could do the same for Twitter, Github, or any other types of results I want to pull from a 3rd party API, but then store data locally within the collection. I don’t see the Postman mock feature in the same way everyone else does. I see it as a static API data server, and collections are just a key/value store, allowing me to do whatever I want in an API-first way.