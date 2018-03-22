---
published: true
layout: post
title: Breaking Down Your Postman API Collections Into Meaningful Units Of Compute
date: 2018-03-20T09:00:00.000Z
tags:
  - API Evangelist
  - Definitions
  - Documentation
image: 'https://s3.amazonaws.com/kinlane-productions/postman/postman-icon.png'
---
<p><img src="{{ page.image }}" width="30%" align="right" style="padding: 15px;" /></p>I'm fascinated with the unit of compute as defined by a microservice, OpenAPI definition, Postman Collection, or other way of quantifying an API-driven resource. Asking the question, "[how big or how small is an API?](http://apievangelist.com/2018/02/15/how-big-or-small-is-an-api/)", and [working to define the small unit of compute needed at runtime](http://apievangelist.com/2018/03/09/defining-the-smallest-unit-possible-for-use-at-api-runtime/). I do not feel there is a perfect answer to any of these questions, but it doesn't mean we shouldn't be asking the questions, and packaging up our API definitions in a more meaningful way.

As I was profiling APIs, and creating Postman Collections, the Okta team tweeted at me, their own approach to delivering their APIs. They tactically place Run in Postman buttons throughout their API documentation, as well as [provide a complete listing of all the Postman Collections they have](https://developer.okta.com/docs/api/getting_started/api_test_client.html#collections-quick-reference). Showcasing that they have broken up their Postman Collections along what I'd consider to be service lines. Providing small, meaningful collections for each of [their user authentication and authorization APIs](https://developer.okta.com/docs/api/getting_started/api_test_client.html):

<table width="100%">
  <thead>
    <tr>
      <th style="text-align: left">Collections</th>
      <th style="text-align: left">Click to Run</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align: left">Authentication</td>
      <td style="text-align: left"><a href="https://app.getpostman.com/run-collection/f9684487e584101f25a3" target="_blank"><img src="https://run.pstmn.io/button.svg" alt="Run in Postman" /></a></td>
    </tr>
    <tr>
      <td style="text-align: left">API Access Management (OAuth 2.0)</td>
      <td style="text-align: left"><a href="https://app.getpostman.com/run-collection/e4d286b1af2294bb14a0" target="_blank"><img src="https://run.pstmn.io/button.svg" alt="Run in Postman" /></a></td>
    </tr>
    <tr>
      <td style="text-align: left">OpenID Connect</td>
      <td style="text-align: left"><a href="https://app.getpostman.com/run-collection/fd92d7c1ab0fbfdecab2" target="_blank"><img src="https://run.pstmn.io/button.svg" alt="Run in Postman" /></a></td>
    </tr>
    <tr>
      <td style="text-align: left">Client Registration</td>
      <td style="text-align: left"><a href="https://app.getpostman.com/run-collection/291ba43cde74844dd4a7" target="_blank"><img src="https://run.pstmn.io/button.svg" alt="Run in Postman" /></a></td>
    </tr>
    <tr>
      <td style="text-align: left">Sessions</td>
      <td style="text-align: left"><a href="https://app.getpostman.com/run-collection/b2e06a22c396bcc94530" target="_blank"><img src="https://run.pstmn.io/button.svg" alt="Run in Postman" /></a></td>
    </tr>
    <tr>
      <td style="text-align: left">Apps</td>
      <td style="text-align: left"><a href="https://app.getpostman.com/run-collection/4857222012c11cf5e8cd" target="_blank"><img src="https://run.pstmn.io/button.svg" alt="Run in Postman" /></a></td>
    </tr>
    <tr>
      <td style="text-align: left">Events</td>
      <td style="text-align: left"><a href="https://app.getpostman.com/run-collection/f990a71f061a7a16d0bf" target="_blank"><img src="https://run.pstmn.io/button.svg" alt="Run in Postman" /></a></td>
    </tr>
    <tr>
      <td style="text-align: left">Factors</td>
      <td style="text-align: left"><a href="https://app.getpostman.com/run-collection/9fdda657d134039fcaba" target="_blank"><img src="https://run.pstmn.io/button.svg" alt="Run in Postman" /></a></td>
    </tr>
    <tr>
      <td style="text-align: left">Groups</td>
      <td style="text-align: left"><a href="https://app.getpostman.com/run-collection/0bb414f9594ed93672a0" target="_blank"><img src="https://run.pstmn.io/button.svg" alt="Run in Postman" /></a></td>
    </tr>
    <tr>
      <td style="text-align: left">Identity Providers (IdP)</td>
      <td style="text-align: left"><a href="https://app.getpostman.com/run-collection/00a7a643fc0ab3bb54c8" target="_blank"><img src="https://run.pstmn.io/button.svg" alt="Run in Postman" /></a></td>
    </tr>
    <tr>
      <td style="text-align: left">Logs</td>
      <td style="text-align: left"><a href="https://app.getpostman.com/run-collection/9cfb0dd661a5432a77c6" target="_blank"><img src="https://run.pstmn.io/button.svg" alt="Run in Postman" /></a></td>
    </tr>
    <tr>
      <td style="text-align: left">Admin Roles</td>
      <td style="text-align: left"><a href="https://app.getpostman.com/run-collection/04f5ec85685ac6f2827e" target="_blank"><img src="https://run.pstmn.io/button.svg" alt="Run in Postman" /></a></td>
    </tr>
    <tr>
      <td style="text-align: left">Schemas</td>
      <td style="text-align: left"><a href="https://app.getpostman.com/run-collection/443242e60287fb4b8d6d" target="_blank"><img src="https://run.pstmn.io/button.svg" alt="Run in Postman" /></a></td>
    </tr>
    <tr>
      <td style="text-align: left">Users</td>
      <td style="text-align: left"><a href="https://app.getpostman.com/run-collection/1755573c5cf5fbf7968b" target="_blank"><img src="https://run.pstmn.io/button.svg" alt="Run in Postman" /></a></td>
    </tr>
    <tr>
      <td style="text-align: left">Custom SMS Templates</td>
      <td style="text-align: left"><a href="https://app.getpostman.com/run-collection/d71f7946d8d56ccdaa06" target="_blank"><img src="https://run.pstmn.io/button.svg" alt="Run in Postman" /></a></td>
    </tr>
  </tbody>
</table>

Okta's approach delivers a pretty coherent, microservices approach to crafting their Postman Collections, providing separate API runtimes for each service they bring to the table. Which I think gets at what I'm looking to understand when it comes to defining and presenting our APIs. It can be a lot more work to create your Postman Collections like this, rather than just creating one single collection, with all API paths, but I think from a API consumer standpoint, I'd rather have them broken down like this. I may not care about all APIs, and I'm just looking at getting my hands on a couple of services--why make me wade through everything?

I have imported the Postman Collections for the Okta API, and added to my API Stack research. I'm going to convert them into OpenAPI definitions so I can use beyond just Postman. I will end up merging them all back into a single OpenAPI definition, and Postman Collection for all the API paths. However, I will also be exploding them into individual OpenAPIs and Postman Collections for each individual API path, going well beyond what Okta has done. Further distilling down each unit of compute, allowing it to be profiled, executed, streamed, or other meaningful action in isolation, without the constraints of the other services surrounding it.

<script type="text/javascript">
  (function (p,o,s,t,m,a,n) {
    !p[s] && (p[s] = function () { (p[t] || (p[t] = [])).push(arguments); });
    !o.getElementById(s+t) && o.getElementsByTagName("head")[0].appendChild((
      (n = o.createElement("script")),
      (n.id = s+t), (n.async = 1), (n.src = m), n
    ));
  }(window, document, "_pm", "PostmanRunObject", "https://run.pstmn.io/button.js"));
</script>
