---
published: true
layout: post
title: 'The Dimensions of the API Lifecycle'
image: https://kinlane-productions2.s3.amazonaws.com/algorotoscope-master/bf-skinner-hallway-mirrors-hotel.jpg
tags:
 - Lifecycle
 - OpenAPI
---
Ok, I’ve gotten my recent immersion in thinking about the API lifecycle to a place where I think I want to put it to work on an actual API. [I spent some on a draft OpenAPI extension to help guide my API lifecycle](https://apievangelist.com/2021/08/03/an-openapi-lifecycle-extension/). Then I went through [thirteen separate API lifecycle definitions that were shared with me](https://apievangelist.com/2021/03/11/what-is-your-api-lifecycle/) in an earlier blog post and [connected each stop along each API lifecycle to some element of the Postman API platform](https://apievangelist.com/2021/08/05/enabling-an-openapi-lifecycle/). This resulted in me further fleshing out my OpenAPI API lifecycle extension to a point that I feel it is wroth to use when guiding, demonstrating, managing, and governing one of my APIs. I don’t expect anyone to implement the full version of this, but I am hoping it is flexible enough that it can accommodate many different versions of the API lifecycle. This is why I tested it against those thirteen API lifecycle, because I wanted to see how it would hold up in theory to many different people’s versions. Here are some simple, basic, intermediate, and complete examples of what I am thinking this extension could be applied.

### Simple API Lifecycle
Based upon what I’ve come across in issues in the OpenAPI spec repo, and what I’ve wanted when it comes to defining the API lifecycle, I wanted the API lifecycle extension to expand upon the versioning capabilities of the OpenAPI spec by allowing me to navigate between versions of the API, allowing me to walk backwards, forwards, and jump to the latest version. I also wanted it to provide me access to API environments, as well as the maturity and visibility of the API. I feel like these dimensions are pretty critical to exactly what the API lifecycle might mean on the ground within API Operations.

<div id="gist111102848" class="gist">
    <div class="gist-file" translate="no">
      <div class="gist-data">
        <div class="js-gist-file-update-container js-task-list-container file-box">
  <div id="file-openapi-lifecycle-extension-v0-2-0-simple-yaml" class="file my-2">
    
    <div itemprop="text" class="Box-body p-0 blob-wrapper data type-yaml  ">

        
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

  <table data-hpc="" class="highlight tab-size js-file-line-container js-code-nav-container js-tagsearch-file" data-tab-size="8" data-paste-markdown-skip="" data-tagsearch-lang="YAML" data-tagsearch-path="openapi-lifecycle-extension-v0.2.0.-simple.yaml">
        <tbody><tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-simple-yaml-L1" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="1"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-simple-yaml-LC1" class="blob-code blob-code-inner js-file-line"><span class="pl-c"><span class="pl-c">#</span> An extension for OpenAPI</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-simple-yaml-L2" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="2"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-simple-yaml-LC2" class="blob-code blob-code-inner js-file-line"><span class="pl-ent">x-lifecycle</span>:</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-simple-yaml-L3" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="3"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-simple-yaml-LC3" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-simple-yaml-L4" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="4"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-simple-yaml-LC4" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Navigating Change</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-simple-yaml-L5" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="5"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-simple-yaml-LC5" class="blob-code blob-code-inner js-file-line">  <span class="pl-ent">version</span>:</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-simple-yaml-L6" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="6"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-simple-yaml-LC6" class="blob-code blob-code-inner js-file-line">      <span class="pl-ent">current</span>: <span class="pl-s"><span class="pl-pds">'</span>http://example.com/next<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-simple-yaml-L7" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="7"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-simple-yaml-LC7" class="blob-code blob-code-inner js-file-line">      <span class="pl-ent">next</span>: <span class="pl-s"><span class="pl-pds">'</span>http://example.com/next<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-simple-yaml-L8" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="8"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-simple-yaml-LC8" class="blob-code blob-code-inner js-file-line">      <span class="pl-ent">previous</span>: <span class="pl-s"><span class="pl-pds">'</span>http://example.com/next<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-simple-yaml-L9" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="9"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-simple-yaml-LC9" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-simple-yaml-L10" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="10"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-simple-yaml-LC10" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Development</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-simple-yaml-L11" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="11"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-simple-yaml-LC11" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Staging</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-simple-yaml-L12" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="12"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-simple-yaml-LC12" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Production</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-simple-yaml-L13" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="13"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-simple-yaml-LC13" class="blob-code blob-code-inner js-file-line">  <span class="pl-ent">environments</span>: </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-simple-yaml-L14" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="14"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-simple-yaml-LC14" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-simple-yaml-L15" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="15"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-simple-yaml-LC15" class="blob-code blob-code-inner js-file-line">      <span class="pl-c"><span class="pl-c">#</span> Environment for production</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-simple-yaml-L16" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="16"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-simple-yaml-LC16" class="blob-code blob-code-inner js-file-line">      - <span class="pl-ent">name</span>: <span class="pl-s">Production</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-simple-yaml-L17" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="17"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-simple-yaml-LC17" class="blob-code blob-code-inner js-file-line">        <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://www.postman.com/environment<span class="pl-pds">'</span></span>  </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-simple-yaml-L18" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="18"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-simple-yaml-LC18" class="blob-code blob-code-inner js-file-line">        <span class="pl-ent">variables</span>:</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-simple-yaml-L19" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="19"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-simple-yaml-LC19" class="blob-code blob-code-inner js-file-line">            <span class="pl-ent">base_url</span>: <span class="pl-s"><span class="pl-pds">'</span>http://example.com/production<span class="pl-pds">'</span></span>       </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-simple-yaml-L20" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="20"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-simple-yaml-LC20" class="blob-code blob-code-inner js-file-line">            <span class="pl-ent">api_key</span>: <span class="pl-s"><span class="pl-pds">'</span>xe3847d3J78393jkdm1123<span class="pl-pds">'</span></span>                </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-simple-yaml-L21" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="21"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-simple-yaml-LC21" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-simple-yaml-L22" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="22"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-simple-yaml-LC22" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Design</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-simple-yaml-L23" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="23"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-simple-yaml-LC23" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Pre-Release    </span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-simple-yaml-L24" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="24"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-simple-yaml-LC24" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Active</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-simple-yaml-L25" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="25"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-simple-yaml-LC25" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Recommended</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-simple-yaml-L26" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="26"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-simple-yaml-LC26" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Retired</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-simple-yaml-L27" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="27"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-simple-yaml-LC27" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Deprecated</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-simple-yaml-L28" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="28"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-simple-yaml-LC28" class="blob-code blob-code-inner js-file-line">  <span class="pl-ent">maturity</span>: <span class="pl-s"><span class="pl-pds">'</span>Active<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-simple-yaml-L29" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="29"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-simple-yaml-LC29" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-simple-yaml-L30" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="30"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-simple-yaml-LC30" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Public</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-simple-yaml-L31" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="31"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-simple-yaml-LC31" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Internal</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-simple-yaml-L32" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="32"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-simple-yaml-LC32" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Group</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-simple-yaml-L33" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="33"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-simple-yaml-LC33" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Partner</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-simple-yaml-L34" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="34"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-simple-yaml-LC34" class="blob-code blob-code-inner js-file-line">  <span class="pl-ent">visibility</span>: <span class="pl-s"><span class="pl-pds">'</span>Public<span class="pl-pds">'</span></span></td>
        </tr>
  </tbody></table>
</div>


    </div>

  </div>
</div>

      </div>
      <div class="gist-meta">
        <a href="https://gist.github.com/kinlane/d56a21a220c4a1b7ed29757ce9c8873a/raw/c1f31679cfb590d512994bfa538d9c9c7ef98536/openapi-lifecycle-extension-v0.2.0.-simple.yaml" style="float: right;">view raw</a>
        <a href="https://gist.github.com/kinlane/d56a21a220c4a1b7ed29757ce9c8873a#file-openapi-lifecycle-extension-v0-2-0-simple-yaml">
          openapi-lifecycle-extension-v0.2.0.-simple.yaml
        </a>
        hosted with ❤ by <a href="https://github.com/">GitHub</a>
      </div>
    </div>
</div>


This OpenAPI API lifecycle extension adds a little bit of life and cycle each OpenAPI. It makes it so each versions aren’t orphans, and it let’s us know the state of maturity for an API, which is something that is heavily defined by the visibility of an API. These things lay the foundation for the API lifecycle. The number of stops, and the blast radius for changes to an API will vary significantly based upon these dimensions, and while the API lifecycle will still vary widely from API producer to API producer, it gets at some of the important dimensions of how people see the API lifecycle.

### Basic API Lifecycle
To step things up a bit I wanted to add in some other essential elements that are often attributed to the API lifecycle, while keeping the simple dimensions I included above. This OpenAPI lifecycle extension gets at what I feel should exist at a minimum for any API I produce. They should have documentation, a basic set of tests, and I should be monitoring the tests to make sure that I am not breaking anything I expected the API do when I first published.

<div id="gist111102771" class="gist">
    <div class="gist-file" translate="no">
      <div class="gist-data">
        <div class="js-gist-file-update-container js-task-list-container file-box">
  <div id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml" class="file my-2">
    
    <div itemprop="text" class="Box-body p-0 blob-wrapper data type-yaml  ">

        
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

  <table data-hpc="" class="highlight tab-size js-file-line-container js-code-nav-container js-tagsearch-file" data-tab-size="8" data-paste-markdown-skip="" data-tagsearch-lang="YAML" data-tagsearch-path="openapi-lifecycle-extension-v0.2.0.-basic.yaml">
        <tbody><tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L1" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="1"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC1" class="blob-code blob-code-inner js-file-line"><span class="pl-c"><span class="pl-c">#</span> An extension for OpenAPI</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L2" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="2"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC2" class="blob-code blob-code-inner js-file-line"><span class="pl-ent">x-lifecycle</span>:</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L3" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="3"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC3" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L4" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="4"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC4" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Navigating Change</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L5" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="5"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC5" class="blob-code blob-code-inner js-file-line">  <span class="pl-ent">version</span>:</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L6" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="6"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC6" class="blob-code blob-code-inner js-file-line">      <span class="pl-ent">current</span>: <span class="pl-s"><span class="pl-pds">'</span>http://example.com/next<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L7" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="7"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC7" class="blob-code blob-code-inner js-file-line">      <span class="pl-ent">next</span>: <span class="pl-s"><span class="pl-pds">'</span>http://example.com/next<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L8" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="8"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC8" class="blob-code blob-code-inner js-file-line">      <span class="pl-ent">previous</span>: <span class="pl-s"><span class="pl-pds">'</span>http://example.com/next<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L9" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="9"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC9" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L10" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="10"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC10" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Development</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L11" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="11"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC11" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Staging</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L12" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="12"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC12" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Production</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L13" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="13"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC13" class="blob-code blob-code-inner js-file-line">  <span class="pl-ent">environments</span>: </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L14" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="14"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC14" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L15" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="15"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC15" class="blob-code blob-code-inner js-file-line">      <span class="pl-c"><span class="pl-c">#</span> Environment for production</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L16" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="16"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC16" class="blob-code blob-code-inner js-file-line">      - <span class="pl-ent">name</span>: <span class="pl-s">Production</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L17" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="17"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC17" class="blob-code blob-code-inner js-file-line">        <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://www.postman.com/environment<span class="pl-pds">'</span></span>  </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L18" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="18"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC18" class="blob-code blob-code-inner js-file-line">        <span class="pl-ent">variables</span>:</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L19" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="19"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC19" class="blob-code blob-code-inner js-file-line">            <span class="pl-ent">base_url</span>: <span class="pl-s"><span class="pl-pds">'</span>http://example.com/production<span class="pl-pds">'</span></span>       </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L20" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="20"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC20" class="blob-code blob-code-inner js-file-line">            <span class="pl-ent">api_key</span>: <span class="pl-s"><span class="pl-pds">'</span>xe3847d3J78393jkdm1123<span class="pl-pds">'</span></span>                </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L21" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="21"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC21" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L22" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="22"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC22" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Design</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L23" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="23"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC23" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Pre-Release    </span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L24" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="24"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC24" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Active</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L25" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="25"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC25" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Recommended</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L26" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="26"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC26" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Retired</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L27" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="27"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC27" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Deprecated</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L28" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="28"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC28" class="blob-code blob-code-inner js-file-line">  <span class="pl-ent">maturity</span>: <span class="pl-s"><span class="pl-pds">'</span>Active<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L29" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="29"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC29" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L30" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="30"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC30" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Public</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L31" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="31"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC31" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Internal</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L32" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="32"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC32" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Group</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L33" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="33"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC33" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Partner</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L34" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="34"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC34" class="blob-code blob-code-inner js-file-line">  <span class="pl-ent">visibility</span>: <span class="pl-s"><span class="pl-pds">'</span>Public<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L35" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="35"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC35" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L36" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="36"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC36" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Elements of the API Lifecycle</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L37" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="37"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC37" class="blob-code blob-code-inner js-file-line">  <span class="pl-ent">elements</span>:       </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L38" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="38"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC38" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L39" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="39"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC39" class="blob-code blob-code-inner js-file-line">      <span class="pl-c"><span class="pl-c">#</span> Documentation</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L40" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="40"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC40" class="blob-code blob-code-inner js-file-line">      <span class="pl-ent">documentation</span>:</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L41" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="41"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC41" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L42" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="42"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC42" class="blob-code blob-code-inner js-file-line">          <span class="pl-ent">label</span>: <span class="pl-s">Docs</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L43" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="43"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC43" class="blob-code blob-code-inner js-file-line">          <span class="pl-ent">guidance</span>: <span class="pl-s">http://example.com/guidance</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L44" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="44"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC44" class="blob-code blob-code-inner js-file-line">          <span class="pl-ent">elements</span>:</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L45" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="45"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC45" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L46" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="46"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC46" class="blob-code blob-code-inner js-file-line">              <span class="pl-c"><span class="pl-c">#</span> Reference Documentation</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L47" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="47"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC47" class="blob-code blob-code-inner js-file-line">              - <span class="pl-ent">type</span>: <span class="pl-s">reference</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L48" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="48"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC48" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">title</span>: <span class="pl-s">Reference Documentation</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L49" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="49"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC49" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://example.com/documentation<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L50" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="50"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC50" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">collection</span>: <span class="pl-s"><span class="pl-pds">'</span>https://www.postman.com/collection<span class="pl-pds">'</span></span>                                             </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L51" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="51"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC51" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L52" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="52"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC52" class="blob-code blob-code-inner js-file-line">      <span class="pl-c"><span class="pl-c">#</span> All Tests</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L53" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="53"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC53" class="blob-code blob-code-inner js-file-line">      <span class="pl-ent">tests</span>:</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L54" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="54"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC54" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L55" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="55"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC55" class="blob-code blob-code-inner js-file-line">          <span class="pl-ent">label</span>: <span class="pl-s">Testing</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L56" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="56"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC56" class="blob-code blob-code-inner js-file-line">          <span class="pl-ent">guidance</span>: <span class="pl-s">http://example.com/guidance</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L57" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="57"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC57" class="blob-code blob-code-inner js-file-line">          <span class="pl-ent">elements</span>:              </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L58" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="58"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC58" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L59" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="59"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC59" class="blob-code blob-code-inner js-file-line">              - <span class="pl-ent">type</span>: <span class="pl-s">contract</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L60" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="60"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC60" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">title</span>: <span class="pl-s">Contract Testing</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L61" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="61"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC61" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://example.com/contract-testing<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L62" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="62"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC62" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">collection</span>: <span class="pl-s"><span class="pl-pds">'</span>https://www.postman.com/collection<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L63" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="63"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC63" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L64" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="64"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC64" class="blob-code blob-code-inner js-file-line">      <span class="pl-c"><span class="pl-c">#</span> All Monitors</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L65" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="65"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC65" class="blob-code blob-code-inner js-file-line">      <span class="pl-ent">monitors</span>:</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L66" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="66"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC66" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L67" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="67"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC67" class="blob-code blob-code-inner js-file-line">          <span class="pl-ent">label</span>: <span class="pl-s">Monitors</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L68" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="68"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC68" class="blob-code blob-code-inner js-file-line">          <span class="pl-ent">elements</span>:              </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L69" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="69"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC69" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L70" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="70"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC70" class="blob-code blob-code-inner js-file-line">              - <span class="pl-ent">type</span>: <span class="pl-s">contract</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L71" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="71"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC71" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">title</span>: <span class="pl-s">Contract Testing Monitor</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L72" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="72"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC72" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://example.com/monitor<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L73" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="73"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC73" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">collection</span>: <span class="pl-s"><span class="pl-pds">'</span>https://www.postman.com/collection<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-L74" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="74"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-basic-yaml-LC74" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">environment</span>: <span class="pl-s"><span class="pl-pds">'</span>https://www.postman.com/environment<span class="pl-pds">'</span></span> </td>
        </tr>
  </tbody></table>
</div>


    </div>

  </div>
</div>

      </div>
      <div class="gist-meta">
        <a href="https://gist.github.com/kinlane/ffa225271e3e59bace484b83382a94d9/raw/db049d6f9690a761268a5134cf413e48f7498996/openapi-lifecycle-extension-v0.2.0.-basic.yaml" style="float: right;">view raw</a>
        <a href="https://gist.github.com/kinlane/ffa225271e3e59bace484b83382a94d9#file-openapi-lifecycle-extension-v0-2-0-basic-yaml">
          openapi-lifecycle-extension-v0.2.0.-basic.yaml
        </a>
        hosted with ❤ by <a href="https://github.com/">GitHub</a>
      </div>
    </div>
</div>


This provides a nice baseline for what folks could strive for as they are looking to move APIs from just being active to something you’d actually recommend folks use. Because the tests are defined as a Postman collection, something that can be paired with each environment, so you can automate the monitoring and testing of the API. Which for me, is something I’d like to see exist with each stop along the API lifecycle. Really, the API lifecycle should be API-driven. Which in my opinion opens up entirely new opportunities for automating the API lifecycle using the Postman platform.

### Intermediate Lifecycle
Next, I’d like to step up the mocking, management, testing, monitoring, observability, and discovery of each API. I’d say that all of these, eluding maybe observability are stops you hear folks include as part of their definition of what the API lifecycle is. These are things that all contribute to the maturity of an API, and contribute to the potential velocity of an API, and how fast you might want to be versioning each API. The better defined your API lifecycle is, the more control you have over it, and this is what this OpenAPI API lifecycle extension all about defining and enabling.

<div id="gist111102800" class="gist">
    <div class="gist-file" translate="no">
      <div class="gist-data">
        <div class="js-gist-file-update-container js-task-list-container file-box">
  <div id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml" class="file my-2">
    
    <div itemprop="text" class="Box-body p-0 blob-wrapper data type-yaml  ">

        
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

  <table data-hpc="" class="highlight tab-size js-file-line-container js-code-nav-container js-tagsearch-file" data-tab-size="8" data-paste-markdown-skip="" data-tagsearch-lang="YAML" data-tagsearch-path="openapi-lifecycle-extension-v0.2.0.-moderate.yaml">
        <tbody><tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L1" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="1"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC1" class="blob-code blob-code-inner js-file-line"><span class="pl-c"><span class="pl-c">#</span> An extension for OpenAPI</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L2" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="2"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC2" class="blob-code blob-code-inner js-file-line"><span class="pl-ent">x-lifecycle</span>:</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L3" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="3"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC3" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L4" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="4"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC4" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Navigating Change</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L5" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="5"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC5" class="blob-code blob-code-inner js-file-line">  <span class="pl-ent">version</span>:</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L6" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="6"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC6" class="blob-code blob-code-inner js-file-line">      <span class="pl-ent">current</span>: <span class="pl-s"><span class="pl-pds">'</span>http://example.com/next<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L7" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="7"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC7" class="blob-code blob-code-inner js-file-line">      <span class="pl-ent">next</span>: <span class="pl-s"><span class="pl-pds">'</span>http://example.com/next<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L8" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="8"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC8" class="blob-code blob-code-inner js-file-line">      <span class="pl-ent">previous</span>: <span class="pl-s"><span class="pl-pds">'</span>http://example.com/next<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L9" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="9"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC9" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L10" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="10"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC10" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Development</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L11" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="11"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC11" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Staging</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L12" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="12"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC12" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Production</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L13" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="13"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC13" class="blob-code blob-code-inner js-file-line">  <span class="pl-ent">environments</span>: </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L14" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="14"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC14" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L15" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="15"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC15" class="blob-code blob-code-inner js-file-line">      <span class="pl-c"><span class="pl-c">#</span> Environment for development</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L16" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="16"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC16" class="blob-code blob-code-inner js-file-line">      - <span class="pl-ent">name</span>: <span class="pl-s">Development</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L17" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="17"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC17" class="blob-code blob-code-inner js-file-line">        <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://www.postman.com/environment<span class="pl-pds">'</span></span>  </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L18" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="18"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC18" class="blob-code blob-code-inner js-file-line">        <span class="pl-ent">variables</span>:</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L19" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="19"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC19" class="blob-code blob-code-inner js-file-line">            <span class="pl-ent">base_url</span>: <span class="pl-s"><span class="pl-pds">'</span>http://example.com/development<span class="pl-pds">'</span></span>       </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L20" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="20"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC20" class="blob-code blob-code-inner js-file-line">            <span class="pl-ent">api_key</span>: <span class="pl-s"><span class="pl-pds">'</span>xe3847d3J78393jkdm1123<span class="pl-pds">'</span></span>  </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L21" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="21"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC21" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L22" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="22"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC22" class="blob-code blob-code-inner js-file-line">      <span class="pl-c"><span class="pl-c">#</span> Environment for production</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L23" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="23"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC23" class="blob-code blob-code-inner js-file-line">      - <span class="pl-ent">name</span>: <span class="pl-s">Production</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L24" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="24"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC24" class="blob-code blob-code-inner js-file-line">        <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://www.postman.com/environment<span class="pl-pds">'</span></span>  </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L25" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="25"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC25" class="blob-code blob-code-inner js-file-line">        <span class="pl-ent">variables</span>:</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L26" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="26"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC26" class="blob-code blob-code-inner js-file-line">            <span class="pl-ent">base_url</span>: <span class="pl-s"><span class="pl-pds">'</span>http://example.com/production<span class="pl-pds">'</span></span>       </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L27" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="27"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC27" class="blob-code blob-code-inner js-file-line">            <span class="pl-ent">api_key</span>: <span class="pl-s"><span class="pl-pds">'</span>xe3847d3J78393jkdm1123<span class="pl-pds">'</span></span>                </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L28" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="28"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC28" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L29" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="29"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC29" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Design</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L30" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="30"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC30" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Pre-Release    </span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L31" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="31"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC31" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Active</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L32" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="32"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC32" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Recommended</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L33" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="33"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC33" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Retired</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L34" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="34"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC34" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Deprecated</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L35" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="35"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC35" class="blob-code blob-code-inner js-file-line">  <span class="pl-ent">maturity</span>: <span class="pl-s"><span class="pl-pds">'</span>Active<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L36" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="36"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC36" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L37" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="37"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC37" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Public</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L38" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="38"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC38" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Internal</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L39" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="39"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC39" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Group</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L40" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="40"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC40" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Partner</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L41" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="41"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC41" class="blob-code blob-code-inner js-file-line">  <span class="pl-ent">visibility</span>: <span class="pl-s"><span class="pl-pds">'</span>Public<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L42" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="42"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC42" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L43" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="43"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC43" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Elements of the API Lifecycle</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L44" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="44"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC44" class="blob-code blob-code-inner js-file-line">  <span class="pl-ent">elements</span>:</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L45" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="45"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC45" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L46" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="46"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC46" class="blob-code blob-code-inner js-file-line">      <span class="pl-c"><span class="pl-c">#</span> All Mocks</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L47" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="47"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC47" class="blob-code blob-code-inner js-file-line">      <span class="pl-ent">mocks</span>:</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L48" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="48"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC48" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L49" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="49"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC49" class="blob-code blob-code-inner js-file-line">          <span class="pl-ent">label</span>: <span class="pl-s">Mocking</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L50" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="50"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC50" class="blob-code blob-code-inner js-file-line">          <span class="pl-ent">elements</span>:              </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L51" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="51"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC51" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L52" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="52"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC52" class="blob-code blob-code-inner js-file-line">              - <span class="pl-ent">type</span>: <span class="pl-s">sandbox</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L53" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="53"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC53" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">title</span>: <span class="pl-s">Mock Server</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L54" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="54"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC54" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://example.com/mock<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L55" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="55"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC55" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">collection</span>: <span class="pl-s"><span class="pl-pds">'</span>https://www.postman.com/collection<span class="pl-pds">'</span></span>        </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L56" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="56"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC56" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L57" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="57"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC57" class="blob-code blob-code-inner js-file-line">      <span class="pl-c"><span class="pl-c">#</span> Documentation</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L58" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="58"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC58" class="blob-code blob-code-inner js-file-line">      <span class="pl-ent">documentation</span>:</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L59" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="59"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC59" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L60" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="60"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC60" class="blob-code blob-code-inner js-file-line">          <span class="pl-ent">label</span>: <span class="pl-s">Docs</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L61" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="61"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC61" class="blob-code blob-code-inner js-file-line">          <span class="pl-ent">guidance</span>: <span class="pl-s">http://example.com/guidance</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L62" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="62"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC62" class="blob-code blob-code-inner js-file-line">          <span class="pl-ent">elements</span>:</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L63" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="63"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC63" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L64" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="64"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC64" class="blob-code blob-code-inner js-file-line">              <span class="pl-c"><span class="pl-c">#</span> Reference Documentation</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L65" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="65"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC65" class="blob-code blob-code-inner js-file-line">              - <span class="pl-ent">type</span>: <span class="pl-s">reference</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L66" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="66"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC66" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">title</span>: <span class="pl-s">Reference Documentation</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L67" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="67"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC67" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://example.com/documentation<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L68" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="68"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC68" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">collection</span>: <span class="pl-s"><span class="pl-pds">'</span>https://www.postman.com/collection<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L69" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="69"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC69" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L70" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="70"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC70" class="blob-code blob-code-inner js-file-line">      <span class="pl-c"><span class="pl-c">#</span> Management</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L71" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="71"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC71" class="blob-code blob-code-inner js-file-line">      <span class="pl-ent">management</span>:</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L72" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="72"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC72" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L73" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="73"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC73" class="blob-code blob-code-inner js-file-line">          <span class="pl-ent">label</span>: <span class="pl-s">Manage</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L74" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="74"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC74" class="blob-code blob-code-inner js-file-line">          <span class="pl-ent">guidance</span>: <span class="pl-s">http://example.com/guidance</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L75" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="75"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC75" class="blob-code blob-code-inner js-file-line">          <span class="pl-ent">elements</span>:     </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L76" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="76"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC76" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L77" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="77"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC77" class="blob-code blob-code-inner js-file-line">              <span class="pl-c"><span class="pl-c">#</span> Onboarding</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L78" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="78"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC78" class="blob-code blob-code-inner js-file-line">              - <span class="pl-ent">type</span>: <span class="pl-s">onboarding</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L79" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="79"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC79" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">title</span>: <span class="pl-s">Login / Registration</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L80" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="80"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC80" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://example.com/login<span class="pl-pds">'</span></span>                           </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L81" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="81"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC81" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L82" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="82"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC82" class="blob-code blob-code-inner js-file-line">              <span class="pl-c"><span class="pl-c">#</span> Plan</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L83" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="83"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC83" class="blob-code blob-code-inner js-file-line">              - <span class="pl-ent">type</span>: <span class="pl-s">aws-api-gateway-plan</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L84" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="84"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC84" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">title</span>: <span class="pl-s">Plan</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L85" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="85"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC85" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://console.aws.amazon.com/apigateway/home?#/usage-plans/859pid<span class="pl-pds">'</span></span>                              </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L86" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="86"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC86" class="blob-code blob-code-inner js-file-line">                </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L87" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="87"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC87" class="blob-code blob-code-inner js-file-line">      <span class="pl-c"><span class="pl-c">#</span> All Tests</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L88" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="88"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC88" class="blob-code blob-code-inner js-file-line">      <span class="pl-ent">tests</span>:</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L89" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="89"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC89" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L90" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="90"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC90" class="blob-code blob-code-inner js-file-line">          <span class="pl-ent">label</span>: <span class="pl-s">Testing</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L91" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="91"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC91" class="blob-code blob-code-inner js-file-line">          <span class="pl-ent">guidance</span>: <span class="pl-s">http://example.com/guidance</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L92" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="92"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC92" class="blob-code blob-code-inner js-file-line">          <span class="pl-ent">elements</span>:              </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L93" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="93"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC93" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L94" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="94"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC94" class="blob-code blob-code-inner js-file-line">              - <span class="pl-ent">type</span>: <span class="pl-s">contract</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L95" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="95"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC95" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">title</span>: <span class="pl-s">Contract Testing</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L96" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="96"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC96" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://example.com/contract-testing<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L97" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="97"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC97" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">collection</span>: <span class="pl-s"><span class="pl-pds">'</span>https://www.postman.com/collection<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L98" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="98"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC98" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L99" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="99"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC99" class="blob-code blob-code-inner js-file-line">              - <span class="pl-ent">type</span>: <span class="pl-s">performance</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L100" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="100"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC100" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">title</span>: <span class="pl-s">Performance Testing</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L101" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="101"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC101" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://example.com/performance-testing<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L102" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="102"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC102" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">collection</span>: <span class="pl-s"><span class="pl-pds">'</span>https://www.postman.com/collection<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L103" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="103"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC103" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L104" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="104"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC104" class="blob-code blob-code-inner js-file-line">              - <span class="pl-ent">type</span>: <span class="pl-s">security</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L105" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="105"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC105" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">title</span>: <span class="pl-s">OWASP Top 10</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L106" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="106"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC106" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://example.com/owasp-security-testing<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L107" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="107"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC107" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">collection</span>: <span class="pl-s"><span class="pl-pds">'</span>https://www.postman.com/collection<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L108" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="108"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC108" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L109" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="109"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC109" class="blob-code blob-code-inner js-file-line">      <span class="pl-c"><span class="pl-c">#</span> All Monitors</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L110" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="110"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC110" class="blob-code blob-code-inner js-file-line">      <span class="pl-ent">monitors</span>:</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L111" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="111"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC111" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L112" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="112"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC112" class="blob-code blob-code-inner js-file-line">          <span class="pl-ent">label</span>: <span class="pl-s">Monitors</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L113" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="113"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC113" class="blob-code blob-code-inner js-file-line">          <span class="pl-ent">elements</span>:              </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L114" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="114"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC114" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L115" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="115"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC115" class="blob-code blob-code-inner js-file-line">              - <span class="pl-ent">type</span>: <span class="pl-s">uptime</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L116" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="116"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC116" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">title</span>: <span class="pl-s">Uptime Monitor</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L117" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="117"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC117" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://example.com/monitor<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L118" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="118"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC118" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">collection</span>: <span class="pl-s"><span class="pl-pds">'</span>https://www.postman.com/collection<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L119" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="119"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC119" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">environment</span>: <span class="pl-s"><span class="pl-pds">'</span>https://www.postman.com/environment<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L120" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="120"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC120" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L121" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="121"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC121" class="blob-code blob-code-inner js-file-line">              - <span class="pl-ent">type</span>: <span class="pl-s">security</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L122" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="122"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC122" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">title</span>: <span class="pl-s">Recurring Security Testing Monitor</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L123" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="123"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC123" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://example.com/monitor<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L124" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="124"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC124" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">collection</span>: <span class="pl-s"><span class="pl-pds">'</span>https://www.postman.com/collection<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L125" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="125"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC125" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">environment</span>: <span class="pl-s"><span class="pl-pds">'</span>https://www.postman.com/environment<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L126" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="126"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC126" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L127" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="127"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC127" class="blob-code blob-code-inner js-file-line">              - <span class="pl-ent">type</span>: <span class="pl-s">contract</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L128" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="128"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC128" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">title</span>: <span class="pl-s">Contract Testing Monitor</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L129" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="129"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC129" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://example.com/monitor<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L130" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="130"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC130" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">collection</span>: <span class="pl-s"><span class="pl-pds">'</span>https://www.postman.com/collection<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L131" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="131"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC131" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">environment</span>: <span class="pl-s"><span class="pl-pds">'</span>https://www.postman.com/environment<span class="pl-pds">'</span></span>                                    </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L132" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="132"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC132" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L133" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="133"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC133" class="blob-code blob-code-inner js-file-line">              - <span class="pl-ent">type</span>: <span class="pl-s">performance</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L134" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="134"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC134" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">title</span>: <span class="pl-s">US East Regional Performance Testing Monitor</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L135" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="135"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC135" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://example.com/monitor<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L136" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="136"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC136" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">collection</span>: <span class="pl-s"><span class="pl-pds">'</span>https://www.postman.com/collection<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L137" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="137"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC137" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">environment</span>: <span class="pl-s"><span class="pl-pds">'</span>https://www.postman.com/environment<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L138" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="138"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC138" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L139" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="139"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC139" class="blob-code blob-code-inner js-file-line">              - <span class="pl-ent">type</span>: <span class="pl-s">performance</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L140" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="140"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC140" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">title</span>: <span class="pl-s">US West Regional Performance Testing Monitor</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L141" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="141"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC141" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://example.com/monitor<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L142" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="142"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC142" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">collection</span>: <span class="pl-s"><span class="pl-pds">'</span>https://www.postman.com/collection<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L143" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="143"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC143" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">environment</span>: <span class="pl-s"><span class="pl-pds">'</span>https://www.postman.com/environment<span class="pl-pds">'</span></span>                  </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L144" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="144"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC144" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L145" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="145"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC145" class="blob-code blob-code-inner js-file-line">      <span class="pl-c"><span class="pl-c">#</span> Observability</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L146" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="146"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC146" class="blob-code blob-code-inner js-file-line">      <span class="pl-ent">observability</span>:</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L147" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="147"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC147" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L148" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="148"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC148" class="blob-code blob-code-inner js-file-line">          <span class="pl-ent">label</span>: <span class="pl-s">Observability</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L149" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="149"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC149" class="blob-code blob-code-inner js-file-line">          <span class="pl-ent">elements</span>:              </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L150" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="150"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC150" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L151" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="151"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC151" class="blob-code blob-code-inner js-file-line">              - <span class="pl-ent">type</span>: <span class="pl-s">reports</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L152" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="152"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC152" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">title</span>: <span class="pl-s">Report Dashboard</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L153" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="153"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC153" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://example.com/reports<span class="pl-pds">'</span></span> </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L154" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="154"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC154" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L155" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="155"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC155" class="blob-code blob-code-inner js-file-line">              - <span class="pl-ent">type</span>: <span class="pl-s">change-log</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L156" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="156"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC156" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">title</span>: <span class="pl-s">Change Log</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L157" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="157"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC157" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://example.com/change-log<span class="pl-pds">'</span></span>      </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L158" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="158"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC158" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L159" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="159"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC159" class="blob-code blob-code-inner js-file-line">              - <span class="pl-ent">type</span>: <span class="pl-s">activity</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L160" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="160"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC160" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">title</span>: <span class="pl-s">Activity</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L161" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="161"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC161" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://example.com/activity<span class="pl-pds">'</span></span>                                                                   </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L162" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="162"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC162" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L163" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="163"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC163" class="blob-code blob-code-inner js-file-line">      <span class="pl-c"><span class="pl-c">#</span> Discovery</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L164" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="164"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC164" class="blob-code blob-code-inner js-file-line">      <span class="pl-ent">discovery</span>:</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L165" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="165"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC165" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L166" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="166"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC166" class="blob-code blob-code-inner js-file-line">          <span class="pl-ent">label</span>: <span class="pl-s">Discovery</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L167" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="167"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC167" class="blob-code blob-code-inner js-file-line">          <span class="pl-ent">elements</span>:              </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L168" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="168"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC168" class="blob-code blob-code-inner js-file-line">    </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L169" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="169"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC169" class="blob-code blob-code-inner js-file-line">              - <span class="pl-ent">type</span>: <span class="pl-s">network</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L170" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="170"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC170" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">title</span>: <span class="pl-s">Public Network</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L171" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="171"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC171" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://example.com/public-network<span class="pl-pds">'</span></span>                                  </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L172" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="172"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC172" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L173" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="173"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC173" class="blob-code blob-code-inner js-file-line">              - <span class="pl-ent">type</span>: <span class="pl-s">workspace</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L174" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="174"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC174" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">title</span>: <span class="pl-s">Public Workspace</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L175" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="175"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC175" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://example.com/public-workspace<span class="pl-pds">'</span></span>                                                                </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L176" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="176"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC176" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L177" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="177"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC177" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Milestones for the API (Achieved and Target)</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L178" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="178"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC178" class="blob-code blob-code-inner js-file-line">  <span class="pl-ent">milestones</span>:</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L179" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="179"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC179" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L180" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="180"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC180" class="blob-code blob-code-inner js-file-line">      <span class="pl-c"><span class="pl-c">#</span> Design Review</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L181" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="181"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC181" class="blob-code blob-code-inner js-file-line">      - <span class="pl-ent">type</span>: <span class="pl-s">design-review</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L182" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="182"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC182" class="blob-code blob-code-inner js-file-line">        <span class="pl-ent">description</span>: <span class="pl-s"><span class="pl-pds">'</span>Went through design review.<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L183" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="183"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC183" class="blob-code blob-code-inner js-file-line">        <span class="pl-ent">date</span>: <span class="pl-s"><span class="pl-pds">'</span>2021-06-01<span class="pl-pds">'</span></span>          </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L184" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="184"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC184" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L185" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="185"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC185" class="blob-code blob-code-inner js-file-line">      <span class="pl-c"><span class="pl-c">#</span> Staging</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L186" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="186"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC186" class="blob-code blob-code-inner js-file-line">      - <span class="pl-ent">type</span>: <span class="pl-s">staging</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L187" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="187"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC187" class="blob-code blob-code-inner js-file-line">        <span class="pl-ent">description</span>: <span class="pl-s"><span class="pl-pds">'</span>Left staging phase of development.<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L188" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="188"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC188" class="blob-code blob-code-inner js-file-line">        <span class="pl-ent">date</span>: <span class="pl-s"><span class="pl-pds">'</span>2021-07-01<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L189" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="189"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC189" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L190" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="190"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC190" class="blob-code blob-code-inner js-file-line">      <span class="pl-c"><span class="pl-c">#</span> Security Review</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L191" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="191"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC191" class="blob-code blob-code-inner js-file-line">      - <span class="pl-ent">type</span>: <span class="pl-s">security-review</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L192" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="192"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC192" class="blob-code blob-code-inner js-file-line">        <span class="pl-ent">description</span>: <span class="pl-s"><span class="pl-pds">'</span>Went through security review.<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L193" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="193"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC193" class="blob-code blob-code-inner js-file-line">        <span class="pl-ent">date</span>: <span class="pl-s"><span class="pl-pds">'</span>2021-06-01<span class="pl-pds">'</span></span>           </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L194" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="194"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC194" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L195" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="195"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC195" class="blob-code blob-code-inner js-file-line">      <span class="pl-c"><span class="pl-c">#</span> Active</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L196" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="196"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC196" class="blob-code blob-code-inner js-file-line">      - <span class="pl-ent">type</span>: <span class="pl-s">active</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L197" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="197"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC197" class="blob-code blob-code-inner js-file-line">        <span class="pl-ent">description</span>: <span class="pl-s"><span class="pl-pds">'</span>Put into production as active API.<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-L198" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="198"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-moderate-yaml-LC198" class="blob-code blob-code-inner js-file-line">        <span class="pl-ent">date</span>: <span class="pl-s"><span class="pl-pds">'</span>2021-07-15<span class="pl-pds">'</span></span>   </td>
        </tr>
  </tbody></table>
</div>


    </div>

  </div>
</div>

      </div>
      <div class="gist-meta">
        <a href="https://gist.github.com/kinlane/5f98c13685ed7e4422f989ce819fc47a/raw/63e25cbc55963907452835fc6d63184b9489ae55/openapi-lifecycle-extension-v0.2.0.-moderate.yaml" style="float: right;">view raw</a>
        <a href="https://gist.github.com/kinlane/5f98c13685ed7e4422f989ce819fc47a#file-openapi-lifecycle-extension-v0-2-0-moderate-yaml">
          openapi-lifecycle-extension-v0.2.0.-moderate.yaml
        </a>
        hosted with ❤ by <a href="https://github.com/">GitHub</a>
      </div>
    </div>
</div>


I feel like this extension will have multiple uses and benefits, but I feel like it has the potential to help define, guide, and stabilize how people approach the API lifecycle. I’ve been studying the API lifecycle for over a decade and I still find myself struggling with being able to "see it". Without an ability to see the API lifecycle we are unable to effectively implement APIs across teams and operations in consistent ways. I am hoping this definition can help ground how I deliver across the API lifecycle, but also talk about and tell stories about the API lifecycle.

### Robust API Lifecycle
Lastly, I wanted to just publish the most recent copy my OpenAPI API lifecycle extension. This is what I am going to use to move forward one of my demo APIs forward and further flesh out my definition of the API lifecycle. I am going to apply it to an existing API that I just want to move forward and iterate upon, as well as an entirely brand new API. I am looking to further flesh this extension, but ultimately get to a place where I can set the stage for applying governance in a more API lifecycle centered way.

<div id="gist111102375" class="gist">
    <div class="gist-file" translate="no">
      <div class="gist-data">
        <div class="js-gist-file-update-container js-task-list-container file-box">
  <div id="file-openapi-lifecycle-extension-v0-2-0-yaml" class="file my-2">
    
    <div itemprop="text" class="Box-body p-0 blob-wrapper data type-yaml  ">

        
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

  <table data-hpc="" class="highlight tab-size js-file-line-container js-code-nav-container js-tagsearch-file" data-tab-size="8" data-paste-markdown-skip="" data-tagsearch-lang="YAML" data-tagsearch-path="openapi-lifecycle-extension-v0.2.0.yaml">
        <tbody><tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L1" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="1"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC1" class="blob-code blob-code-inner js-file-line"><span class="pl-c"><span class="pl-c">#</span> An extension for OpenAPI</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L2" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="2"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC2" class="blob-code blob-code-inner js-file-line"><span class="pl-ent">x-lifecycle</span>:</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L3" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="3"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC3" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L4" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="4"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC4" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Navigating Change</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L5" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="5"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC5" class="blob-code blob-code-inner js-file-line">  <span class="pl-ent">version</span>:</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L6" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="6"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC6" class="blob-code blob-code-inner js-file-line">      <span class="pl-ent">current</span>: <span class="pl-s"><span class="pl-pds">'</span>http://example.com/next<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L7" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="7"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC7" class="blob-code blob-code-inner js-file-line">      <span class="pl-ent">next</span>: <span class="pl-s"><span class="pl-pds">'</span>http://example.com/next<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L8" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="8"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC8" class="blob-code blob-code-inner js-file-line">      <span class="pl-ent">previous</span>: <span class="pl-s"><span class="pl-pds">'</span>http://example.com/next<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L9" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="9"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC9" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L10" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="10"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC10" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Development</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L11" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="11"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC11" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Staging</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L12" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="12"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC12" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Production</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L13" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="13"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC13" class="blob-code blob-code-inner js-file-line">  <span class="pl-ent">environments</span>: </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L14" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="14"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC14" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L15" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="15"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC15" class="blob-code blob-code-inner js-file-line">      <span class="pl-c"><span class="pl-c">#</span> Environment for development</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L16" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="16"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC16" class="blob-code blob-code-inner js-file-line">      - <span class="pl-ent">name</span>: <span class="pl-s">Development</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L17" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="17"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC17" class="blob-code blob-code-inner js-file-line">        <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://www.postman.com/environment<span class="pl-pds">'</span></span>  </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L18" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="18"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC18" class="blob-code blob-code-inner js-file-line">        <span class="pl-ent">variables</span>:</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L19" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="19"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC19" class="blob-code blob-code-inner js-file-line">            <span class="pl-ent">base_url</span>: <span class="pl-s"><span class="pl-pds">'</span>http://example.com/development<span class="pl-pds">'</span></span>       </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L20" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="20"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC20" class="blob-code blob-code-inner js-file-line">            <span class="pl-ent">api_key</span>: <span class="pl-s"><span class="pl-pds">'</span>xe3847d3J78393jkdm1123<span class="pl-pds">'</span></span>  </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L21" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="21"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC21" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L22" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="22"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC22" class="blob-code blob-code-inner js-file-line">      <span class="pl-c"><span class="pl-c">#</span> Environment for production</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L23" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="23"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC23" class="blob-code blob-code-inner js-file-line">      - <span class="pl-ent">name</span>: <span class="pl-s">Production</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L24" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="24"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC24" class="blob-code blob-code-inner js-file-line">        <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://www.postman.com/environment<span class="pl-pds">'</span></span>  </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L25" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="25"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC25" class="blob-code blob-code-inner js-file-line">        <span class="pl-ent">variables</span>:</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L26" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="26"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC26" class="blob-code blob-code-inner js-file-line">            <span class="pl-ent">base_url</span>: <span class="pl-s"><span class="pl-pds">'</span>http://example.com/production<span class="pl-pds">'</span></span>       </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L27" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="27"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC27" class="blob-code blob-code-inner js-file-line">            <span class="pl-ent">api_key</span>: <span class="pl-s"><span class="pl-pds">'</span>xe3847d3J78393jkdm1123<span class="pl-pds">'</span></span>                </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L28" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="28"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC28" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L29" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="29"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC29" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Design</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L30" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="30"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC30" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Pre-Release    </span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L31" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="31"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC31" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Active</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L32" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="32"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC32" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Recommended</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L33" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="33"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC33" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Retired</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L34" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="34"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC34" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Deprecated</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L35" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="35"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC35" class="blob-code blob-code-inner js-file-line">  <span class="pl-ent">maturity</span>: <span class="pl-s"><span class="pl-pds">'</span>Active<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L36" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="36"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC36" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L37" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="37"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC37" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Public</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L38" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="38"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC38" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Internal</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L39" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="39"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC39" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Group</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L40" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="40"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC40" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Partner</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L41" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="41"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC41" class="blob-code blob-code-inner js-file-line">  <span class="pl-ent">visibility</span>: <span class="pl-s"><span class="pl-pds">'</span>Public<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L42" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="42"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC42" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L43" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="43"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC43" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Elements of the API Lifecycle</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L44" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="44"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC44" class="blob-code blob-code-inner js-file-line">  <span class="pl-ent">elements</span>:</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L45" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="45"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC45" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L46" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="46"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC46" class="blob-code blob-code-inner js-file-line">      <span class="pl-c"><span class="pl-c">#</span> All Mocks</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L47" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="47"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC47" class="blob-code blob-code-inner js-file-line">      <span class="pl-ent">mocks</span>:</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L48" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="48"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC48" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L49" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="49"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC49" class="blob-code blob-code-inner js-file-line">          <span class="pl-ent">label</span>: <span class="pl-s">Mocking</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L50" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="50"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC50" class="blob-code blob-code-inner js-file-line">          <span class="pl-ent">elements</span>:              </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L51" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="51"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC51" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L52" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="52"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC52" class="blob-code blob-code-inner js-file-line">              - <span class="pl-ent">type</span>: <span class="pl-s">sandbox</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L53" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="53"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC53" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">title</span>: <span class="pl-s">Mock Server</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L54" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="54"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC54" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://example.com/mock<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L55" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="55"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC55" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">collection</span>: <span class="pl-s"><span class="pl-pds">'</span>https://www.postman.com/collection<span class="pl-pds">'</span></span>        </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L56" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="56"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC56" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L57" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="57"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC57" class="blob-code blob-code-inner js-file-line">      <span class="pl-c"><span class="pl-c">#</span> Documentation</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L58" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="58"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC58" class="blob-code blob-code-inner js-file-line">      <span class="pl-ent">documentation</span>:</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L59" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="59"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC59" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L60" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="60"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC60" class="blob-code blob-code-inner js-file-line">          <span class="pl-ent">label</span>: <span class="pl-s">Docs</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L61" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="61"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC61" class="blob-code blob-code-inner js-file-line">          <span class="pl-ent">guidance</span>: <span class="pl-s">http://example.com/guidance</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L62" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="62"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC62" class="blob-code blob-code-inner js-file-line">          <span class="pl-ent">elements</span>:</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L63" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="63"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC63" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L64" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="64"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC64" class="blob-code blob-code-inner js-file-line">              <span class="pl-c"><span class="pl-c">#</span> Reference Documentation</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L65" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="65"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC65" class="blob-code blob-code-inner js-file-line">              - <span class="pl-ent">type</span>: <span class="pl-s">reference</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L66" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="66"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC66" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">title</span>: <span class="pl-s">Reference Documentation</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L67" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="67"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC67" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://example.com/documentation<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L68" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="68"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC68" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">collection</span>: <span class="pl-s"><span class="pl-pds">'</span>https://www.postman.com/collection<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L69" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="69"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC69" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L70" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="70"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC70" class="blob-code blob-code-inner js-file-line">              <span class="pl-c"><span class="pl-c">#</span> Onboarding Documentation</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L71" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="71"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC71" class="blob-code blob-code-inner js-file-line">              - <span class="pl-ent">type</span>: <span class="pl-s">onboarding</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L72" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="72"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC72" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">title</span>: <span class="pl-s">Onboarding Documentation</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L73" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="73"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC73" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://example.com/documentation<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L74" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="74"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC74" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">collection</span>: <span class="pl-s"><span class="pl-pds">'</span>https://www.postman.com/collection<span class="pl-pds">'</span></span>                  </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L75" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="75"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC75" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L76" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="76"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC76" class="blob-code blob-code-inner js-file-line">              <span class="pl-c"><span class="pl-c">#</span> Workflow Documentation</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L77" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="77"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC77" class="blob-code blob-code-inner js-file-line">              - <span class="pl-ent">type</span>: <span class="pl-s">workflow</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L78" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="78"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC78" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">title</span>: <span class="pl-s">Business Workflow Documentation</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L79" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="79"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC79" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://example.com/documentation<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L80" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="80"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC80" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">collection</span>: <span class="pl-s"><span class="pl-pds">'</span>https://www.postman.com/collection<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L81" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="81"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC81" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L82" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="82"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC82" class="blob-code blob-code-inner js-file-line">      <span class="pl-c"><span class="pl-c">#</span> Deployment</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L83" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="83"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC83" class="blob-code blob-code-inner js-file-line">      <span class="pl-ent">deployment</span>:</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L84" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="84"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC84" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L85" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="85"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC85" class="blob-code blob-code-inner js-file-line">          <span class="pl-ent">label</span>: <span class="pl-s">Publishing</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L86" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="86"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC86" class="blob-code blob-code-inner js-file-line">          <span class="pl-ent">guidance</span>: <span class="pl-s">http://example.com/guidance</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L87" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="87"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC87" class="blob-code blob-code-inner js-file-line">          <span class="pl-ent">elements</span>:            </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L88" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="88"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC88" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L89" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="89"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC89" class="blob-code blob-code-inner js-file-line">              <span class="pl-c"><span class="pl-c">#</span> GitHub Repository</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L90" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="90"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC90" class="blob-code blob-code-inner js-file-line">              - <span class="pl-ent">type</span>: <span class="pl-s">github</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L91" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="91"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC91" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">title</span>: <span class="pl-s">Github Repository</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L92" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="92"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC92" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://github.com/org/repo<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L93" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="93"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC93" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">sync</span>: <span class="pl-c1">true</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L94" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="94"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC94" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L95" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="95"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC95" class="blob-code blob-code-inner js-file-line">              <span class="pl-c"><span class="pl-c">#</span> Pipeline</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L96" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="96"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC96" class="blob-code blob-code-inner js-file-line">              - <span class="pl-ent">type</span>: <span class="pl-s">github-action</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L97" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="97"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC97" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">title</span>: <span class="pl-s">Github Action</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L98" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="98"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC98" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://github.com/org/repo/actions<span class="pl-pds">'</span></span>       </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L99" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="99"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC99" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L100" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="100"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC100" class="blob-code blob-code-inner js-file-line">              <span class="pl-c"><span class="pl-c">#</span> Gateway</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L101" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="101"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC101" class="blob-code blob-code-inner js-file-line">              - <span class="pl-ent">type</span>: <span class="pl-s">aws-api-gateway</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L102" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="102"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC102" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">title</span>: <span class="pl-s">AWS API Gateway</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L103" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="103"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC103" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span> https://uab3sjk0mna.execute-api.us-east-1.amazonaws.com<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L104" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="104"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC104" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">collection</span>: <span class="pl-s"><span class="pl-pds">'</span>https://www.postman.com/collection<span class="pl-pds">'</span></span>              </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L105" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="105"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC105" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">sync</span>: <span class="pl-c1">true</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L106" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="106"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC106" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L107" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="107"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC107" class="blob-code blob-code-inner js-file-line">      <span class="pl-c"><span class="pl-c">#</span> Management</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L108" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="108"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC108" class="blob-code blob-code-inner js-file-line">      <span class="pl-ent">management</span>:</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L109" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="109"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC109" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L110" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="110"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC110" class="blob-code blob-code-inner js-file-line">          <span class="pl-ent">label</span>: <span class="pl-s">Manage</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L111" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="111"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC111" class="blob-code blob-code-inner js-file-line">          <span class="pl-ent">guidance</span>: <span class="pl-s">http://example.com/guidance</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L112" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="112"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC112" class="blob-code blob-code-inner js-file-line">          <span class="pl-ent">elements</span>:     </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L113" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="113"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC113" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L114" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="114"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC114" class="blob-code blob-code-inner js-file-line">              <span class="pl-c"><span class="pl-c">#</span> Onboarding</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L115" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="115"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC115" class="blob-code blob-code-inner js-file-line">              - <span class="pl-ent">type</span>: <span class="pl-s">onboarding</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L116" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="116"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC116" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">title</span>: <span class="pl-s">Login / Registration</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L117" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="117"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC117" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://example.com/login<span class="pl-pds">'</span></span>                           </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L118" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="118"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC118" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L119" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="119"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC119" class="blob-code blob-code-inner js-file-line">              <span class="pl-c"><span class="pl-c">#</span> Plan</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L120" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="120"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC120" class="blob-code blob-code-inner js-file-line">              - <span class="pl-ent">type</span>: <span class="pl-s">aws-api-gateway-plan</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L121" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="121"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC121" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">title</span>: <span class="pl-s">Plan</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L122" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="122"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC122" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://console.aws.amazon.com/apigateway/home?#/usage-plans/859pid<span class="pl-pds">'</span></span>                              </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L123" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="123"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC123" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L124" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="124"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC124" class="blob-code blob-code-inner js-file-line">      <span class="pl-c"><span class="pl-c">#</span> SDKs</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L125" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="125"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC125" class="blob-code blob-code-inner js-file-line">      <span class="pl-ent">sdks</span>:</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L126" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="126"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC126" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L127" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="127"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC127" class="blob-code blob-code-inner js-file-line">          <span class="pl-ent">label</span>: <span class="pl-s">SDKs</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L128" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="128"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC128" class="blob-code blob-code-inner js-file-line">          <span class="pl-ent">guidance</span>: <span class="pl-s">http://example.com/guidance</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L129" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="129"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC129" class="blob-code blob-code-inner js-file-line">          <span class="pl-ent">elements</span>:     </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L130" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="130"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC130" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L131" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="131"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC131" class="blob-code blob-code-inner js-file-line">              <span class="pl-c"><span class="pl-c">#</span> Python</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L132" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="132"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC132" class="blob-code blob-code-inner js-file-line">              - <span class="pl-ent">type</span>: <span class="pl-s">python</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L133" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="133"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC133" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">title</span>: <span class="pl-s">Python Library</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L134" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="134"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC134" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://github.com/sdks/python<span class="pl-pds">'</span></span>                           </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L135" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="135"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC135" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L136" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="136"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC136" class="blob-code blob-code-inner js-file-line">              <span class="pl-c"><span class="pl-c">#</span> Node.js</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L137" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="137"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC137" class="blob-code blob-code-inner js-file-line">              - <span class="pl-ent">type</span>: <span class="pl-s">node.js</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L138" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="138"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC138" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">title</span>: <span class="pl-s">Node.js Library</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L139" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="139"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC139" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://github.com/sdks/nodejs<span class="pl-pds">'</span></span>   </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L140" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="140"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC140" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L141" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="141"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC141" class="blob-code blob-code-inner js-file-line">              <span class="pl-c"><span class="pl-c">#</span> Go</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L142" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="142"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC142" class="blob-code blob-code-inner js-file-line">              - <span class="pl-ent">type</span>: <span class="pl-s">go</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L143" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="143"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC143" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">title</span>: <span class="pl-s">Go Library</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L144" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="144"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC144" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://github.com/sdks/go<span class="pl-pds">'</span></span>                        </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L145" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="145"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC145" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L146" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="146"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC146" class="blob-code blob-code-inner js-file-line">      <span class="pl-c"><span class="pl-c">#</span> All Tests</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L147" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="147"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC147" class="blob-code blob-code-inner js-file-line">      <span class="pl-ent">tests</span>:</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L148" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="148"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC148" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L149" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="149"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC149" class="blob-code blob-code-inner js-file-line">          <span class="pl-ent">label</span>: <span class="pl-s">Testing</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L150" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="150"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC150" class="blob-code blob-code-inner js-file-line">          <span class="pl-ent">guidance</span>: <span class="pl-s">http://example.com/guidance</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L151" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="151"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC151" class="blob-code blob-code-inner js-file-line">          <span class="pl-ent">elements</span>:              </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L152" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="152"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC152" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L153" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="153"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC153" class="blob-code blob-code-inner js-file-line">              - <span class="pl-ent">type</span>: <span class="pl-s">contract</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L154" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="154"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC154" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">title</span>: <span class="pl-s">Contract Testing</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L155" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="155"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC155" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://example.com/contract-testing<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L156" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="156"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC156" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">collection</span>: <span class="pl-s"><span class="pl-pds">'</span>https://www.postman.com/collection<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L157" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="157"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC157" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L158" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="158"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC158" class="blob-code blob-code-inner js-file-line">              - <span class="pl-ent">type</span>: <span class="pl-s">performance</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L159" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="159"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC159" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">title</span>: <span class="pl-s">Performance Testing</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L160" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="160"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC160" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://example.com/performance-testing<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L161" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="161"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC161" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">collection</span>: <span class="pl-s"><span class="pl-pds">'</span>https://www.postman.com/collection<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L162" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="162"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC162" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L163" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="163"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC163" class="blob-code blob-code-inner js-file-line">              - <span class="pl-ent">type</span>: <span class="pl-s">security</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L164" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="164"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC164" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">title</span>: <span class="pl-s">OWASP Top 10</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L165" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="165"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC165" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://example.com/owasp-security-testing<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L166" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="166"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC166" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">collection</span>: <span class="pl-s"><span class="pl-pds">'</span>https://www.postman.com/collection<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L167" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="167"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC167" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L168" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="168"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC168" class="blob-code blob-code-inner js-file-line">      <span class="pl-c"><span class="pl-c">#</span> All Monitors</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L169" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="169"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC169" class="blob-code blob-code-inner js-file-line">      <span class="pl-ent">monitors</span>:</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L170" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="170"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC170" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L171" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="171"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC171" class="blob-code blob-code-inner js-file-line">          <span class="pl-ent">label</span>: <span class="pl-s">Monitors</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L172" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="172"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC172" class="blob-code blob-code-inner js-file-line">          <span class="pl-ent">elements</span>:              </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L173" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="173"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC173" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L174" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="174"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC174" class="blob-code blob-code-inner js-file-line">              - <span class="pl-ent">type</span>: <span class="pl-s">uptime</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L175" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="175"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC175" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">title</span>: <span class="pl-s">Uptime Monitor</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L176" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="176"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC176" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://example.com/monitor<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L177" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="177"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC177" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">collection</span>: <span class="pl-s"><span class="pl-pds">'</span>https://www.postman.com/collection<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L178" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="178"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC178" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">environment</span>: <span class="pl-s"><span class="pl-pds">'</span>https://www.postman.com/environment<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L179" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="179"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC179" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L180" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="180"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC180" class="blob-code blob-code-inner js-file-line">              - <span class="pl-ent">type</span>: <span class="pl-s">security</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L181" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="181"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC181" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">title</span>: <span class="pl-s">Recurring Security Testing Monitor</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L182" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="182"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC182" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://example.com/monitor<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L183" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="183"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC183" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">collection</span>: <span class="pl-s"><span class="pl-pds">'</span>https://www.postman.com/collection<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L184" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="184"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC184" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">environment</span>: <span class="pl-s"><span class="pl-pds">'</span>https://www.postman.com/environment<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L185" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="185"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC185" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L186" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="186"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC186" class="blob-code blob-code-inner js-file-line">              - <span class="pl-ent">type</span>: <span class="pl-s">contract</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L187" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="187"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC187" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">title</span>: <span class="pl-s">Contract Testing Monitor</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L188" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="188"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC188" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://example.com/monitor<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L189" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="189"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC189" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">collection</span>: <span class="pl-s"><span class="pl-pds">'</span>https://www.postman.com/collection<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L190" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="190"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC190" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">environment</span>: <span class="pl-s"><span class="pl-pds">'</span>https://www.postman.com/environment<span class="pl-pds">'</span></span>                                    </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L191" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="191"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC191" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L192" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="192"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC192" class="blob-code blob-code-inner js-file-line">              - <span class="pl-ent">type</span>: <span class="pl-s">performance</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L193" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="193"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC193" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">title</span>: <span class="pl-s">US East Regional Performance Testing Monitor</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L194" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="194"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC194" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://example.com/monitor<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L195" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="195"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC195" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">collection</span>: <span class="pl-s"><span class="pl-pds">'</span>https://www.postman.com/collection<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L196" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="196"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC196" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">environment</span>: <span class="pl-s"><span class="pl-pds">'</span>https://www.postman.com/environment<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L197" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="197"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC197" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L198" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="198"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC198" class="blob-code blob-code-inner js-file-line">              - <span class="pl-ent">type</span>: <span class="pl-s">performance</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L199" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="199"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC199" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">title</span>: <span class="pl-s">US West Regional Performance Testing Monitor</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L200" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="200"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC200" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://example.com/monitor<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L201" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="201"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC201" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">collection</span>: <span class="pl-s"><span class="pl-pds">'</span>https://www.postman.com/collection<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L202" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="202"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC202" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">environment</span>: <span class="pl-s"><span class="pl-pds">'</span>https://www.postman.com/environment<span class="pl-pds">'</span></span>                  </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L203" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="203"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC203" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L204" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="204"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC204" class="blob-code blob-code-inner js-file-line">      <span class="pl-c"><span class="pl-c">#</span> Observability</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L205" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="205"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC205" class="blob-code blob-code-inner js-file-line">      <span class="pl-ent">observability</span>:</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L206" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="206"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC206" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L207" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="207"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC207" class="blob-code blob-code-inner js-file-line">          <span class="pl-ent">label</span>: <span class="pl-s">Observability</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L208" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="208"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC208" class="blob-code blob-code-inner js-file-line">          <span class="pl-ent">elements</span>:              </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L209" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="209"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC209" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L210" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="210"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC210" class="blob-code blob-code-inner js-file-line">              - <span class="pl-ent">type</span>: <span class="pl-s">reports</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L211" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="211"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC211" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">title</span>: <span class="pl-s">Report Dashboard</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L212" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="212"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC212" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://example.com/reports<span class="pl-pds">'</span></span> </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L213" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="213"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC213" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L214" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="214"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC214" class="blob-code blob-code-inner js-file-line">              - <span class="pl-ent">type</span>: <span class="pl-s">change-log</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L215" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="215"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC215" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">title</span>: <span class="pl-s">Change Log</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L216" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="216"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC216" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://example.com/change-log<span class="pl-pds">'</span></span>      </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L217" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="217"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC217" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L218" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="218"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC218" class="blob-code blob-code-inner js-file-line">              - <span class="pl-ent">type</span>: <span class="pl-s">activity</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L219" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="219"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC219" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">title</span>: <span class="pl-s">Activity</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L220" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="220"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC220" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://example.com/activity<span class="pl-pds">'</span></span>     </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L221" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="221"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC221" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L222" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="222"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC222" class="blob-code blob-code-inner js-file-line">              - <span class="pl-ent">type</span>: <span class="pl-s">apm</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L223" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="223"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC223" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">title</span>: <span class="pl-s">Datadog</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L224" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="224"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC224" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://datadog.com/dashboard<span class="pl-pds">'</span></span>   </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L225" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="225"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC225" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">sync</span>: <span class="pl-c1">true</span>   </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L226" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="226"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC226" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L227" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="227"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC227" class="blob-code blob-code-inner js-file-line">              - <span class="pl-ent">type</span>: <span class="pl-s">aws-api-gateway</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L228" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="228"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC228" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">title</span>: <span class="pl-s">Gateway Usage Report</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L229" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="229"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC229" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">url</span>: <span class="pl-s">url: ' https://uab3sjk0mna.execute-api.us-east-1.amazonaws.com/usage'  </span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L230" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="230"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC230" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">sync</span>: <span class="pl-c1">true</span>                    </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L231" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="231"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC231" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L232" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="232"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC232" class="blob-code blob-code-inner js-file-line">              - <span class="pl-ent">type</span>: <span class="pl-s">uptime</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L233" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="233"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC233" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">title</span>: <span class="pl-s">Uptime Monitor Results</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L234" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="234"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC234" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://example.com/monitor/results<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L235" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="235"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC235" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L236" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="236"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC236" class="blob-code blob-code-inner js-file-line">              - <span class="pl-ent">type</span>: <span class="pl-s">security</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L237" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="237"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC237" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">title</span>: <span class="pl-s">Recurring Security Testing Monitor Results</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L238" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="238"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC238" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://example.com/monitor/results<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L239" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="239"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC239" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L240" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="240"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC240" class="blob-code blob-code-inner js-file-line">              - <span class="pl-ent">type</span>: <span class="pl-s">contract</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L241" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="241"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC241" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">title</span>: <span class="pl-s">Contract Testing Monitor Results</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L242" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="242"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC242" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://example.com/monitor/results<span class="pl-pds">'</span></span>                                   </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L243" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="243"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC243" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L244" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="244"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC244" class="blob-code blob-code-inner js-file-line">              - <span class="pl-ent">type</span>: <span class="pl-s">performance</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L245" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="245"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC245" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">title</span>: <span class="pl-s">US East Regional Performance Testing Monitor Results</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L246" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="246"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC246" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://example.com/monitor/results<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L247" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="247"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC247" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L248" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="248"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC248" class="blob-code blob-code-inner js-file-line">              - <span class="pl-ent">type</span>: <span class="pl-s">performance</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L249" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="249"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC249" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">title</span>: <span class="pl-s">US West Regional Performance Testing Monitor Results</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L250" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="250"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC250" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://example.com/monitor/results<span class="pl-pds">'</span></span>                                                </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L251" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="251"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC251" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L252" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="252"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC252" class="blob-code blob-code-inner js-file-line">      <span class="pl-c"><span class="pl-c">#</span> Discovery</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L253" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="253"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC253" class="blob-code blob-code-inner js-file-line">      <span class="pl-ent">discovery</span>:</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L254" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="254"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC254" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L255" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="255"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC255" class="blob-code blob-code-inner js-file-line">          <span class="pl-ent">label</span>: <span class="pl-s">Discovery</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L256" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="256"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC256" class="blob-code blob-code-inner js-file-line">          <span class="pl-ent">elements</span>:              </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L257" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="257"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC257" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L258" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="258"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC258" class="blob-code blob-code-inner js-file-line">              - <span class="pl-ent">type</span>: <span class="pl-s">network</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L259" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="259"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC259" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">title</span>: <span class="pl-s">Private Network</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L260" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="260"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC260" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://example.com/private-network<span class="pl-pds">'</span></span>    </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L261" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="261"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC261" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L262" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="262"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC262" class="blob-code blob-code-inner js-file-line">              - <span class="pl-ent">type</span>: <span class="pl-s">network</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L263" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="263"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC263" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">title</span>: <span class="pl-s">Public Network</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L264" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="264"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC264" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://example.com/public-network<span class="pl-pds">'</span></span>                                  </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L265" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="265"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC265" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L266" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="266"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC266" class="blob-code blob-code-inner js-file-line">              - <span class="pl-ent">type</span>: <span class="pl-s">workspace</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L267" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="267"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC267" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">title</span>: <span class="pl-s">Private Workspace</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L268" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="268"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC268" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://example.com/private-workspace<span class="pl-pds">'</span></span>                  </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L269" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="269"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC269" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L270" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="270"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC270" class="blob-code blob-code-inner js-file-line">              - <span class="pl-ent">type</span>: <span class="pl-s">workspace</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L271" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="271"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC271" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">title</span>: <span class="pl-s">Public Workspace</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L272" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="272"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC272" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://example.com/public-workspace<span class="pl-pds">'</span></span>                 </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L273" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="273"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC273" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L274" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="274"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC274" class="blob-code blob-code-inner js-file-line">      <span class="pl-c"><span class="pl-c">#</span> Governance</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L275" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="275"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC275" class="blob-code blob-code-inner js-file-line">      <span class="pl-ent">governance</span>:</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L276" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="276"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC276" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L277" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="277"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC277" class="blob-code blob-code-inner js-file-line">          <span class="pl-ent">label</span>: <span class="pl-s">Governance</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L278" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="278"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC278" class="blob-code blob-code-inner js-file-line">          <span class="pl-ent">rules</span>:              </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L279" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="279"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC279" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L280" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="280"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC280" class="blob-code blob-code-inner js-file-line">              - <span class="pl-ent">type</span>: <span class="pl-s">design-rules</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L281" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="281"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC281" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">title</span>: <span class="pl-s">Design Rules</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L282" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="282"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC282" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://example.com/design-rules<span class="pl-pds">'</span></span>    </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L283" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="283"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC283" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L284" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="284"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC284" class="blob-code blob-code-inner js-file-line">              - <span class="pl-ent">type</span>: <span class="pl-s">management-rules</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L285" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="285"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC285" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">title</span>: <span class="pl-s">Management Rules</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L286" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="286"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC286" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://example.com/management-rules<span class="pl-pds">'</span></span>                       </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L287" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="287"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC287" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L288" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="288"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC288" class="blob-code blob-code-inner js-file-line">              - <span class="pl-ent">type</span>: <span class="pl-s">documentation-rules</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L289" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="289"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC289" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">title</span>: <span class="pl-s">Documentation Rules</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L290" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="290"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC290" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://example.com/documentation-rules<span class="pl-pds">'</span></span>   </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L291" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="291"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC291" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L292" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="292"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC292" class="blob-code blob-code-inner js-file-line">              - <span class="pl-ent">type</span>: <span class="pl-s">testing-rules</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L293" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="293"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC293" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">title</span>: <span class="pl-s">Testing Rules</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L294" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="294"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC294" class="blob-code blob-code-inner js-file-line">                <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://example.com/testing-rules<span class="pl-pds">'</span></span>                                                    </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L295" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="295"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC295" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L296" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="296"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC296" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Milestones for the API (Achieved and Target)</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L297" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="297"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC297" class="blob-code blob-code-inner js-file-line">  <span class="pl-ent">milestones</span>:</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L298" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="298"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC298" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L299" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="299"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC299" class="blob-code blob-code-inner js-file-line">      <span class="pl-c"><span class="pl-c">#</span> Design</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L300" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="300"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC300" class="blob-code blob-code-inner js-file-line">      - <span class="pl-ent">type</span>: <span class="pl-s">design</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L301" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="301"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC301" class="blob-code blob-code-inner js-file-line">        <span class="pl-ent">description</span>: <span class="pl-s"><span class="pl-pds">'</span>Design agreed upon by stakeholders.<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L302" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="302"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC302" class="blob-code blob-code-inner js-file-line">        <span class="pl-ent">date</span>: <span class="pl-s"><span class="pl-pds">'</span>2021-05-01<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L303" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="303"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC303" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L304" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="304"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC304" class="blob-code blob-code-inner js-file-line">      <span class="pl-c"><span class="pl-c">#</span> Design Review</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L305" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="305"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC305" class="blob-code blob-code-inner js-file-line">      - <span class="pl-ent">type</span>: <span class="pl-s">design-review</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L306" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="306"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC306" class="blob-code blob-code-inner js-file-line">        <span class="pl-ent">description</span>: <span class="pl-s"><span class="pl-pds">'</span>Went through design review.<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L307" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="307"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC307" class="blob-code blob-code-inner js-file-line">        <span class="pl-ent">date</span>: <span class="pl-s"><span class="pl-pds">'</span>2021-06-01<span class="pl-pds">'</span></span>          </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L308" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="308"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC308" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L309" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="309"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC309" class="blob-code blob-code-inner js-file-line">      <span class="pl-c"><span class="pl-c">#</span> Staging</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L310" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="310"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC310" class="blob-code blob-code-inner js-file-line">      - <span class="pl-ent">type</span>: <span class="pl-s">staging</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L311" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="311"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC311" class="blob-code blob-code-inner js-file-line">        <span class="pl-ent">description</span>: <span class="pl-s"><span class="pl-pds">'</span>Left staging phase of development.<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L312" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="312"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC312" class="blob-code blob-code-inner js-file-line">        <span class="pl-ent">date</span>: <span class="pl-s"><span class="pl-pds">'</span>2021-07-01<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L313" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="313"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC313" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L314" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="314"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC314" class="blob-code blob-code-inner js-file-line">      <span class="pl-c"><span class="pl-c">#</span> Security Review</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L315" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="315"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC315" class="blob-code blob-code-inner js-file-line">      - <span class="pl-ent">type</span>: <span class="pl-s">security-review</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L316" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="316"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC316" class="blob-code blob-code-inner js-file-line">        <span class="pl-ent">description</span>: <span class="pl-s"><span class="pl-pds">'</span>Went through security review.<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L317" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="317"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC317" class="blob-code blob-code-inner js-file-line">        <span class="pl-ent">date</span>: <span class="pl-s"><span class="pl-pds">'</span>2021-06-01<span class="pl-pds">'</span></span>           </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L318" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="318"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC318" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L319" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="319"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC319" class="blob-code blob-code-inner js-file-line">      <span class="pl-c"><span class="pl-c">#</span> Active</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L320" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="320"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC320" class="blob-code blob-code-inner js-file-line">      - <span class="pl-ent">type</span>: <span class="pl-s">active</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L321" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="321"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC321" class="blob-code blob-code-inner js-file-line">        <span class="pl-ent">description</span>: <span class="pl-s"><span class="pl-pds">'</span>Put into production as active API.<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L322" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="322"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC322" class="blob-code blob-code-inner js-file-line">        <span class="pl-ent">date</span>: <span class="pl-s"><span class="pl-pds">'</span>2021-07-15<span class="pl-pds">'</span></span>   </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L323" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="323"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC323" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L324" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="324"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC324" class="blob-code blob-code-inner js-file-line">      <span class="pl-c"><span class="pl-c">#</span> Retire</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L325" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="325"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC325" class="blob-code blob-code-inner js-file-line">      - <span class="pl-ent">type</span>: <span class="pl-s">retire</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L326" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="326"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC326" class="blob-code blob-code-inner js-file-line">        <span class="pl-ent">description</span>: <span class="pl-s"><span class="pl-pds">'</span>Planned retirement date.<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L327" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="327"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC327" class="blob-code blob-code-inner js-file-line">        <span class="pl-ent">date</span>: <span class="pl-s"><span class="pl-pds">'</span>2025-07-15<span class="pl-pds">'</span></span>                            </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L328" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="328"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC328" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L329" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="329"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC329" class="blob-code blob-code-inner js-file-line">      <span class="pl-c"><span class="pl-c">#</span> Deprecation</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L330" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="330"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC330" class="blob-code blob-code-inner js-file-line">      - <span class="pl-ent">type</span>: <span class="pl-s">deprecation</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L331" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="331"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC331" class="blob-code blob-code-inner js-file-line">        <span class="pl-ent">description</span>: <span class="pl-s"><span class="pl-pds">'</span>Planned deprecation date.<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-L332" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="332"></td>
          <td id="file-openapi-lifecycle-extension-v0-2-0-yaml-LC332" class="blob-code blob-code-inner js-file-line">        <span class="pl-ent">date</span>: <span class="pl-s"><span class="pl-pds">'</span>2025-12-15<span class="pl-pds">'</span></span> </td>
        </tr>
  </tbody></table>
</div>


    </div>

  </div>
</div>

      </div>
      <div class="gist-meta">
        <a href="https://gist.github.com/kinlane/6873d23edd662f730f7fa72630bb5b42/raw/31d52889325758950bf3ec23d6d5d4495516a415/openapi-lifecycle-extension-v0.2.0.yaml" style="float: right;">view raw</a>
        <a href="https://gist.github.com/kinlane/6873d23edd662f730f7fa72630bb5b42#file-openapi-lifecycle-extension-v0-2-0-yaml">
          openapi-lifecycle-extension-v0.2.0.yaml
        </a>
        hosted with ❤ by <a href="https://github.com/">GitHub</a>
      </div>
    </div>
</div>


The elements of my proposed OpenAPI API lifecycle extension are meant to be extensible, so that it can work for the different ways teams move through the API lifecycle. It is meant to expand and contract to work seamlessly across multiple platforms, allowing for use with any gateway, APM, or CI/CD solution. Wrapping common stops along the API lifecycle around API infrastructure across any cloud provider, or on-premise solution. This represents another level of flexibility I am looking for when it comes to defining the API lifecycle, accommodating everyone’s definition of what the API lifecycle, as well as how it functions underneath the hood.

### What It Is Used For?
OK, so what is this extension going to be used for? Honestly I am not entirely sure at this time. Ultimately I envision this extension guiding any service or tooling that is used to move an API forward. I am looking for this extension to help visualize the API lifecycle and make it more real for people. To help me keep fleshing out this extension, I wanted to think about the different potential uses of this extension in context of reducing friction across the API lifecycle.

    
- **Use to Guide** - Help teams move APIs forward confidently.
    
- **Use to Educate**  - Introduce teams to concepts along the way.
    
- **Use to Demonstrate** - Show how to implement stops along the lifecycle.
    
- **Use to Manage** - Provide ways to manage the full API lifecycle. 
    
- **Use to Automate** - Allow for the automation of the API lifecycle.
    
- **Use to Govern** - Provide scaffolding for applying API governance.


I am looking to use this extension to articulate what the API lifecycle can be, what it is, and where each API fits into said API lifecycle. I don’t think that these API lifecycle definitions should be an OpenAPI extension. Ultimately I think they should be standalone files that are referenced as part of a central [APIs.json](http://apisjson.org/)a&gt;, or at the very least referenced from within an OpenAPI, and eventually AsyncAPI. I think each API lifecycle definition should reference and emulate a central API lifecycle strategy, and be used to standardize APIs across an organization. We will see how it goes. I have a lot more work to even prove that this thing will be useful at all, and allow me to coherently articulate what the API lifecycle is to folks, while convincing them that they can customize and bend it to their own definition of what the API lifecycle is. Lot’s to do, but regardless, I am learning tons. As usual.