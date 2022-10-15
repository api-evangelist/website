---
published: true
layout: post
title: 'An OpenAPI Lifecycle Extension'
image: https://kinlane-productions2.s3.amazonaws.com/algorotoscope-master/uncle-sam-working-on-railroad-1.jpg
tags:
    - Lifecycle
    - OpenAPI
    - Extensions
---

Multiple API universes collided recently resulting in me spending some more time on defining what the API lifecycle is. A couple months back [](https://apievangelist.com/2021/03/11/what-is-your-api-lifecycle/)I asked a bunch of folks in my Twitter timeline what their API lifecycle was, then I sat down to take another look at how [I manage the API lifecycle using Postman](https://apievangelist.com/2020/08/02/managing-the-api-lifecycle-using-openapi-and-postman/), and created [a public workspace](https://www.postman.com/postman/workspace/postman-open-technologies-lifecycle/overview) to help me evolve my thoughts on this subject. As part of this work I went through any OpenAPI, AsyncAPI, or JSON Schema issues looking for anything that might speak to what folks are looking for when it comes to the API lifecycle. I have done a lot of thinking about the API lifecycle over the years, and you can see this work across API Evangelist, and as part my work on [APIs.json / APIs.yaml](http://apisjson.org/), but to help satisfy requests I am getting from within Postman, from our customers, and as part of my work within the OpenAPI, AsyncAPI, and JSON Schema communities, I wanted to spend some time thinking about the API lifecycle—-this time grounded in a potential extension for the OpenAPI specification.

### Proposed Extension for OAS
There is no better way to gather feedback from folks than just putting something out there and letting folks on the open web step up and tell me what is wrong with it. It is the beauty of how the open web, social media, and API space work. ;-) To release the hounds, here is a quick draft of an OpenAPI extension that for me speaks to the different dimensions of how I see the API lifecycle, providing one possible machine readable look at how we can communicate and automate around our APIs as they evolve, mature, and go away.

<div id="gist111063841" class="gist">
    <div class="gist-file" translate="no">
      <div class="gist-data">
        <div class="js-gist-file-update-container js-task-list-container file-box">
  <div id="file-openapi-lifecycle-extension-v0-1-0-yaml" class="file my-2">
    
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

  <table data-hpc="" class="highlight tab-size js-file-line-container js-code-nav-container js-tagsearch-file" data-tab-size="8" data-paste-markdown-skip="" data-tagsearch-lang="YAML" data-tagsearch-path="openapi-lifecycle-extension-v0.1.0.yaml">
        <tbody><tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L1" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="1"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC1" class="blob-code blob-code-inner js-file-line"><span class="pl-c"><span class="pl-c">#</span> An extension for OpenAPI</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L2" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="2"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC2" class="blob-code blob-code-inner js-file-line"><span class="pl-ent">x-lifecycle</span>:</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L3" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="3"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC3" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L4" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="4"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC4" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Navigating Change</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L5" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="5"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC5" class="blob-code blob-code-inner js-file-line">  <span class="pl-ent">version</span>:</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L6" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="6"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC6" class="blob-code blob-code-inner js-file-line">      <span class="pl-ent">current</span>: <span class="pl-s"><span class="pl-pds">'</span>http://example.com/next<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L7" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="7"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC7" class="blob-code blob-code-inner js-file-line">      <span class="pl-ent">next</span>: <span class="pl-s"><span class="pl-pds">'</span>http://example.com/next<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L8" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="8"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC8" class="blob-code blob-code-inner js-file-line">      <span class="pl-ent">previous</span>: <span class="pl-s"><span class="pl-pds">'</span>http://example.com/next<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L9" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="9"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC9" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L10" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="10"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC10" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Development</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L11" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="11"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC11" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Staging</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L12" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="12"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC12" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Production</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L13" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="13"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC13" class="blob-code blob-code-inner js-file-line">  <span class="pl-ent">environments</span>: </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L14" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="14"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC14" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L15" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="15"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC15" class="blob-code blob-code-inner js-file-line">      <span class="pl-c"><span class="pl-c">#</span> Environment for development</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L16" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="16"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC16" class="blob-code blob-code-inner js-file-line">      - <span class="pl-ent">name</span>: <span class="pl-s">Development</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L17" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="17"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC17" class="blob-code blob-code-inner js-file-line">        <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://www.postman.com/environment<span class="pl-pds">'</span></span>  </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L18" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="18"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC18" class="blob-code blob-code-inner js-file-line">        <span class="pl-ent">variables</span>:</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L19" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="19"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC19" class="blob-code blob-code-inner js-file-line">            <span class="pl-ent">base_url</span>: <span class="pl-s"><span class="pl-pds">'</span>http://example.com/development<span class="pl-pds">'</span></span>       </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L20" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="20"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC20" class="blob-code blob-code-inner js-file-line">            <span class="pl-ent">api_key</span>: <span class="pl-s"><span class="pl-pds">'</span>xe3847d3J78393jkdm1123<span class="pl-pds">'</span></span>  </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L21" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="21"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC21" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L22" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="22"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC22" class="blob-code blob-code-inner js-file-line">      <span class="pl-c"><span class="pl-c">#</span> Environment for production</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L23" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="23"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC23" class="blob-code blob-code-inner js-file-line">      - <span class="pl-ent">name</span>: <span class="pl-s">Production</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L24" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="24"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC24" class="blob-code blob-code-inner js-file-line">        <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://www.postman.com/environment<span class="pl-pds">'</span></span>  </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L25" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="25"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC25" class="blob-code blob-code-inner js-file-line">        <span class="pl-ent">variables</span>:</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L26" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="26"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC26" class="blob-code blob-code-inner js-file-line">            <span class="pl-ent">base_url</span>: <span class="pl-s"><span class="pl-pds">'</span>http://example.com/production<span class="pl-pds">'</span></span>       </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L27" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="27"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC27" class="blob-code blob-code-inner js-file-line">            <span class="pl-ent">api_key</span>: <span class="pl-s"><span class="pl-pds">'</span>xe3847d3J78393jkdm1123<span class="pl-pds">'</span></span>                </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L28" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="28"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC28" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L29" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="29"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC29" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Design</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L30" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="30"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC30" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Pre-Release    </span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L31" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="31"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC31" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Active</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L32" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="32"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC32" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Recommended</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L33" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="33"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC33" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Retired</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L34" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="34"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC34" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Deprecated</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L35" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="35"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC35" class="blob-code blob-code-inner js-file-line">  <span class="pl-ent">maturity</span>: <span class="pl-s"><span class="pl-pds">'</span>Active<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L36" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="36"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC36" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L37" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="37"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC37" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Public</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L38" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="38"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC38" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Internal</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L39" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="39"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC39" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Group</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L40" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="40"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC40" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Partner</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L41" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="41"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC41" class="blob-code blob-code-inner js-file-line">  <span class="pl-ent">visibility</span>: <span class="pl-s"><span class="pl-pds">'</span>Public<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L42" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="42"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC42" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L43" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="43"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC43" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Essential Building Blocks of the API Lifecycle</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L44" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="44"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC44" class="blob-code blob-code-inner js-file-line">  <span class="pl-ent">buildingBlocks</span>:</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L45" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="45"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC45" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L46" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="46"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC46" class="blob-code blob-code-inner js-file-line">      <span class="pl-c"><span class="pl-c">#</span> All Documentation</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L47" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="47"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC47" class="blob-code blob-code-inner js-file-line">      <span class="pl-ent">documentation</span>:</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L48" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="48"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC48" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L49" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="49"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC49" class="blob-code blob-code-inner js-file-line">          <span class="pl-c"><span class="pl-c">#</span> Reference Documentation</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L50" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="50"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC50" class="blob-code blob-code-inner js-file-line">          - <span class="pl-ent">type</span>: <span class="pl-s">reference</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L51" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="51"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC51" class="blob-code blob-code-inner js-file-line">            <span class="pl-ent">title</span>: <span class="pl-s">Reference Documentation</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L52" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="52"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC52" class="blob-code blob-code-inner js-file-line">            <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://example.com/documentation<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L53" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="53"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC53" class="blob-code blob-code-inner js-file-line">            <span class="pl-ent">collection</span>: <span class="pl-s"><span class="pl-pds">'</span>https://www.postman.com/collection<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L54" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="54"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC54" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L55" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="55"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC55" class="blob-code blob-code-inner js-file-line">          <span class="pl-c"><span class="pl-c">#</span> Workflow Documentation</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L56" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="56"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC56" class="blob-code blob-code-inner js-file-line">          - <span class="pl-ent">type</span>: <span class="pl-s">workflow</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L57" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="57"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC57" class="blob-code blob-code-inner js-file-line">            <span class="pl-ent">title</span>: <span class="pl-s">Workflow Documentation</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L58" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="58"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC58" class="blob-code blob-code-inner js-file-line">            <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://example.com/documentation<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L59" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="59"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC59" class="blob-code blob-code-inner js-file-line">            <span class="pl-ent">collection</span>: <span class="pl-s"><span class="pl-pds">'</span>https://www.postman.com/collection<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L60" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="60"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC60" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L61" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="61"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC61" class="blob-code blob-code-inner js-file-line">      <span class="pl-c"><span class="pl-c">#</span> All Tests</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L62" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="62"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC62" class="blob-code blob-code-inner js-file-line">      <span class="pl-ent">tests</span>:</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L63" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="63"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC63" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L64" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="64"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC64" class="blob-code blob-code-inner js-file-line">          - <span class="pl-ent">type</span>: <span class="pl-s">contract</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L65" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="65"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC65" class="blob-code blob-code-inner js-file-line">            <span class="pl-ent">title</span>: <span class="pl-s">Contract Testing</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L66" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="66"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC66" class="blob-code blob-code-inner js-file-line">            <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://example.com/contract-testing<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L67" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="67"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC67" class="blob-code blob-code-inner js-file-line">            <span class="pl-ent">collection</span>: <span class="pl-s"><span class="pl-pds">'</span>https://www.postman.com/collection<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L68" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="68"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC68" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L69" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="69"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC69" class="blob-code blob-code-inner js-file-line">          - <span class="pl-ent">type</span>: <span class="pl-s">performance</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L70" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="70"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC70" class="blob-code blob-code-inner js-file-line">            <span class="pl-ent">title</span>: <span class="pl-s">Performance Testing</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L71" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="71"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC71" class="blob-code blob-code-inner js-file-line">            <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://example.com/performance-testing<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L72" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="72"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC72" class="blob-code blob-code-inner js-file-line">            <span class="pl-ent">collection</span>: <span class="pl-s"><span class="pl-pds">'</span>https://www.postman.com/collection<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L73" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="73"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC73" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L74" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="74"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC74" class="blob-code blob-code-inner js-file-line">          - <span class="pl-ent">type</span>: <span class="pl-s">security</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L75" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="75"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC75" class="blob-code blob-code-inner js-file-line">            <span class="pl-ent">title</span>: <span class="pl-s">OWASP Top 10</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L76" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="76"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC76" class="blob-code blob-code-inner js-file-line">            <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://example.com/owasp-security-testing<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L77" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="77"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC77" class="blob-code blob-code-inner js-file-line">            <span class="pl-ent">collection</span>: <span class="pl-s"><span class="pl-pds">'</span>https://www.postman.com/collection<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L78" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="78"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC78" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L79" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="79"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC79" class="blob-code blob-code-inner js-file-line">      <span class="pl-c"><span class="pl-c">#</span> All Mocks</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L80" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="80"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC80" class="blob-code blob-code-inner js-file-line">      <span class="pl-ent">mocks</span>:</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L81" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="81"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC81" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L82" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="82"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC82" class="blob-code blob-code-inner js-file-line">          - <span class="pl-ent">type</span>: <span class="pl-s">sandbox</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L83" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="83"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC83" class="blob-code blob-code-inner js-file-line">            <span class="pl-ent">title</span>: <span class="pl-s">Mock Server</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L84" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="84"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC84" class="blob-code blob-code-inner js-file-line">            <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://example.com/mock<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L85" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="85"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC85" class="blob-code blob-code-inner js-file-line">            <span class="pl-ent">collection</span>: <span class="pl-s"><span class="pl-pds">'</span>https://www.postman.com/collection<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L86" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="86"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC86" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L87" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="87"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC87" class="blob-code blob-code-inner js-file-line">      <span class="pl-c"><span class="pl-c">#</span> All Monitors</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L88" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="88"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC88" class="blob-code blob-code-inner js-file-line">      <span class="pl-ent">monitors</span>:</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L89" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="89"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC89" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L90" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="90"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC90" class="blob-code blob-code-inner js-file-line">          - <span class="pl-ent">type</span>: <span class="pl-s">uptime</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L91" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="91"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC91" class="blob-code blob-code-inner js-file-line">            <span class="pl-ent">title</span>: <span class="pl-s">Uptime Monitor</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L92" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="92"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC92" class="blob-code blob-code-inner js-file-line">            <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://example.com/monitor<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L93" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="93"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC93" class="blob-code blob-code-inner js-file-line">            <span class="pl-ent">collection</span>: <span class="pl-s"><span class="pl-pds">'</span>https://www.postman.com/collection<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L94" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="94"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC94" class="blob-code blob-code-inner js-file-line">            <span class="pl-ent">environment</span>: <span class="pl-s"><span class="pl-pds">'</span>https://www.postman.com/environment<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L95" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="95"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC95" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L96" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="96"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC96" class="blob-code blob-code-inner js-file-line">          - <span class="pl-ent">type</span>: <span class="pl-s">performance</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L97" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="97"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC97" class="blob-code blob-code-inner js-file-line">            <span class="pl-ent">title</span>: <span class="pl-s">Regional Performance Monitor</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L98" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="98"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC98" class="blob-code blob-code-inner js-file-line">            <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://example.com/monitor<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L99" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="99"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC99" class="blob-code blob-code-inner js-file-line">            <span class="pl-ent">collection</span>: <span class="pl-s"><span class="pl-pds">'</span>https://www.postman.com/collection<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L100" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="100"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC100" class="blob-code blob-code-inner js-file-line">            <span class="pl-ent">environment</span>: <span class="pl-s"><span class="pl-pds">'</span>https://www.postman.com/environment<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L101" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="101"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC101" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L102" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="102"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC102" class="blob-code blob-code-inner js-file-line">      <span class="pl-c"><span class="pl-c">#</span> All Reports</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L103" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="103"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC103" class="blob-code blob-code-inner js-file-line">      <span class="pl-ent">reports</span>:</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L104" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="104"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC104" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L105" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="105"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC105" class="blob-code blob-code-inner js-file-line">          - <span class="pl-ent">type</span>: <span class="pl-s">overview</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L106" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="106"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC106" class="blob-code blob-code-inner js-file-line">            <span class="pl-ent">title</span>: <span class="pl-s">Dashboard</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L107" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="107"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC107" class="blob-code blob-code-inner js-file-line">            <span class="pl-ent">url</span>: <span class="pl-s"><span class="pl-pds">'</span>https://example.com/monitor<span class="pl-pds">'</span></span> </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L108" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="108"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC108" class="blob-code blob-code-inner js-file-line">            <span class="pl-ent">collection</span>: <span class="pl-s"><span class="pl-pds">'</span>https://www.postman.com/collection<span class="pl-pds">'</span></span>           </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L109" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="109"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC109" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L110" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="110"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC110" class="blob-code blob-code-inner js-file-line">  <span class="pl-c"><span class="pl-c">#</span> Milestones for the API</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L111" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="111"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC111" class="blob-code blob-code-inner js-file-line">  <span class="pl-ent">milestones</span>:</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L112" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="112"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC112" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L113" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="113"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC113" class="blob-code blob-code-inner js-file-line">      <span class="pl-c"><span class="pl-c">#</span> Design</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L114" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="114"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC114" class="blob-code blob-code-inner js-file-line">      - <span class="pl-ent">type</span>: <span class="pl-s">design</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L115" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="115"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC115" class="blob-code blob-code-inner js-file-line">        <span class="pl-ent">description</span>: <span class="pl-s"><span class="pl-pds">'</span>Design agreed upon by stakeholders.<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L116" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="116"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC116" class="blob-code blob-code-inner js-file-line">        <span class="pl-ent">date</span>: <span class="pl-s"><span class="pl-pds">'</span>2021-05-01<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L117" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="117"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC117" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L118" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="118"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC118" class="blob-code blob-code-inner js-file-line">      <span class="pl-c"><span class="pl-c">#</span> Review</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L119" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="119"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC119" class="blob-code blob-code-inner js-file-line">      - <span class="pl-ent">type</span>: <span class="pl-s">review</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L120" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="120"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC120" class="blob-code blob-code-inner js-file-line">        <span class="pl-ent">description</span>: <span class="pl-s"><span class="pl-pds">'</span>Wentn through architectural review.<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L121" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="121"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC121" class="blob-code blob-code-inner js-file-line">        <span class="pl-ent">date</span>: <span class="pl-s"><span class="pl-pds">'</span>2021-06-01<span class="pl-pds">'</span></span>          </td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L122" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="122"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC122" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L123" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="123"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC123" class="blob-code blob-code-inner js-file-line">      <span class="pl-c"><span class="pl-c">#</span> Staging</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L124" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="124"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC124" class="blob-code blob-code-inner js-file-line">      - <span class="pl-ent">type</span>: <span class="pl-s">staging</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L125" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="125"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC125" class="blob-code blob-code-inner js-file-line">        <span class="pl-ent">description</span>: <span class="pl-s"><span class="pl-pds">'</span>Left staging phase of development.<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L126" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="126"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC126" class="blob-code blob-code-inner js-file-line">        <span class="pl-ent">date</span>: <span class="pl-s"><span class="pl-pds">'</span>2021-07-01<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L127" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="127"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC127" class="blob-code blob-code-inner js-file-line">
</td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L128" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="128"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC128" class="blob-code blob-code-inner js-file-line">      <span class="pl-c"><span class="pl-c">#</span> Active</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L129" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="129"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC129" class="blob-code blob-code-inner js-file-line">      - <span class="pl-ent">type</span>: <span class="pl-s">active</span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L130" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="130"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC130" class="blob-code blob-code-inner js-file-line">        <span class="pl-ent">description</span>: <span class="pl-s"><span class="pl-pds">'</span>Put into production as active API.<span class="pl-pds">'</span></span></td>
        </tr>
        <tr>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-L131" class="blob-num js-line-number js-code-nav-line-number js-blob-rnum" data-line-number="131"></td>
          <td id="file-openapi-lifecycle-extension-v0-1-0-yaml-LC131" class="blob-code blob-code-inner js-file-line">        <span class="pl-ent">date</span>: <span class="pl-s"><span class="pl-pds">'</span>2021-07-15<span class="pl-pds">'</span></span>  </td>
        </tr>
  </tbody></table>
</div>


    </div>

  </div>
</div>

      </div>
      <div class="gist-meta">
        <a href="https://gist.github.com/kinlane/e156b91b1206b86e5f84e73c2225bcc0/raw/207d11e86c6b16bd26b248131538fb192abfd3c6/openapi-lifecycle-extension-v0.1.0.yaml" style="float: right;">view raw</a>
        <a href="https://gist.github.com/kinlane/e156b91b1206b86e5f84e73c2225bcc0#file-openapi-lifecycle-extension-v0-1-0-yaml">
          openapi-lifecycle-extension-v0.1.0.yaml
        </a>
        hosted with ❤ by <a href="https://github.com/">GitHub</a>
      </div>
    </div>
</div>


You can find this extension in [the public workspace I am using to define the API lifecycle](https://www.postman.com/postman/workspace/postman-open-technologies-lifecycle/api/471ec857-5d67-4a92-b3f9-14d62a33a277.). Feel free to highlight any part and leave inline comments within the workspace letting me know what you think about each property. Historically I do not believe that any of this should live within OAS, and I feel it should live within the APIs.json / APIs.yaml index for an API, but I know folks have a lot of apprehension about yet another specification, and there is a lot of attention place on the OpenAPI specification today. This is an exercise I will continue for event and message driven APIs using AsyncAPI, as well as pure schema using JSON Schema, but for this round it is all about doing for OpenAPI. Like most of my writing here on API Evangelist I am just looking to get something out there and gather feedback from other smart folks in the space, and once I wrap my head around the meaningful dimensions of the lifecycle for request and response APIs, I’ll focus some time on other specifications.

### Dimensions of the API Lifecycle
If you look at my earlier post where I ask folks what their API lifecycle is, you’ll see that ultimately there are many different dimensions to this conversation. Some are about the artifacts and versioning, others are more about the environments, where others are about the tangible building blocks that emerge across the API lifecycle. Ultimately I want to create an extension that is flexible enough to fit 90% of the ways folks see the API lifecycle, but it is such a sprawling world I have to start somewhere. In this first draft I am looking to build around a handful of dimensions using these properties:


- **Version** - This is about navigating between versions, and I am relying on the core OpenAPI version property to define the existing version.
- **Environments** - Each of the environments available for an API provide a lot of context that influence how people see the API lifecycle.
- **Maturity** - The overall maturity of an API is a verify significant factor in how people view what the API lifecycle should even be for an API.
- **Visibility** - The visibility of an API will very much influence the extent of the lifecycle for an API, as well as the scope of the audience.
- **Building Blocks**  - I struggled with the name for this dimension, but ultimately landed on what I consider to be the essential building blocks.
- **Milestones** - I feel that the lifecycle is very much defined by a handful of meaningful milestones that define how far along an API is.


This extension is way too verbose for my liking, but it gets at the critical dimensions of what I feel API lifecycle means to everyone. Next I will workshop this draft extension against all of the API lifecycle definitions folks provided to me and find ways of bending it to meet all of those expectations. Then I will take an existing demo or template API that I have an iterate upon it for a couple of versions, and see how my extension holds up in use across multiple OpenAPI definitions. Then I’ll see what other comments and feedback comes in via the workspace I setup, via Slack, and on the Twitterz. After that I will consider distilling down into maybe a suite of extensions, and think about what a minimum viable usage of it will be. Ultimately I know I want make everyone happy, but that isn’t my goal. I want to get something I can use to guide conversations, and use as guardrails to move this conversation forward even just a little bit. Success would be getting something in place for OpenAPI, AsyncAPI, and JSON Schema, and then get a handful of API service and tooling providers to put to work in some way.


I have spent way too much time over the last decade thinking about the API lifecycle, and I have seen way too little movement in providing meaningful vendor independent guidance for folks trying to get a handle on their API operations. It is one of those sprawling and highly opinionated conversations that seem to go nowhere, and can easily be shut down with some run of the mill criticism. Like with most of my work I’ll keep putting something out there and weather the criticism until I get something that speaks a meaningful cross section of the space. I want to get the feedback of the usual API echo chamber, but then I want to push to get out of the echo chamber and see what is needed for the average API product or engineering manager on the ground within the enterprise. APIs aren’t just a trend anymore, and are something that every company, organization, institution, and government agency is struggling with. We need some sort of guard rails to provide folks to help them move forward, evolve, and iterate in a standardize way. I am hoping this thinking can help continue to influence things, get the attention of the folks leading each of the API specifications, as well as API service and tooling providers, and begin laying a better foundation for the API lifecycle.
