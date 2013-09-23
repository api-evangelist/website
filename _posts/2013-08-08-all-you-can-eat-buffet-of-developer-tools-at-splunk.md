---
layout: post
title: "All You Can Eat Buffet of Developer Tools at Splunk"
url: 'http://apievangelist.com/2013/08/08/all-you-can-eat-buffet-of-developer-tools-at-splunk/'
image: 'http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/blog/splunk-logo.gif'
---

[<img src="https://s3.amazonaws.com/kinlane-productions/api-evangelist/splunk/splunk-logo.gif" alt="" width="250" align="right" />][1]

During my monitoring of the API space this week, I came across an interesting blog post from data platform [Splunk][1], [showcasing the tools they provide for developers][2] who are putting their real-time data platform to use.

Splunk has an amazing smorgasbord of developer tools, but there are a handful that I feel need highlighting, so that other data API providers can consider as part of their own offerings:

  * **Command Line Interface (CLI) -** Monitor, configure and search Splunk via a terminal/shell interface or wrapping the commands in a shell script
  * **REST API -** Most of the functionality in Splunk exposed as a suite of REST endpoints Software Development Kits (SDK) - Development kits for accelerating integration with the Splunk API in six different languages: Python, Java, JavaScript, PHP, Ruby, C#
  * **Apps and Add-ons -** Packaging up of the various configurations, searches, knowledge objects, UI components and customizations, inputs, role definitions, field extractions etc. that you might typically create via Splunk on the web
  * Scripted inputs - Out of the box, Splunk has simple generic input options available for getting data from a file or receiving data over TCP/UDP
  * **Modular Inputs -** Modular Inputs build upon Scripted Inputs by elevating the creation of custom input add-ons to first class citizen status in Splunk
  * Custom search commands - Splunk’s Search language is incredibly powerful and extensive for deriving a wide range of analytical insights from your indexed data
  * **Custom alert scripts -** Splunk alerting channels provided by defaults are Email and RSS. But let’s say for example that you wanted to send alerts via SMS, to a Messaging Queue, as an SNMP or directly to a trouble ticket system
  * **Custom REST endpoints -** Splunk’s REST API is very thorough, but this can also be extended with your own custom REST endpoints that you could then integrate with programmatically

Obviously Splunk is a big data platform, so the idea of custom search and other building blocks, may not work for all API providers. Regardless this list provides some thought provoking implementations that other data API providers should look as part of their own roadmap.

Make sure and head over to the [blog post that sparked this story,][2] they have other goodies like App Frameworks, and specific connectors for Apache, Spring, Flurry and a long-tail of API integration building blocks.

   [1]: http://www.splunk.com/
   [2]: http://blogs.splunk.com/2013/08/06/a-developers-smorgasbord/
