---
published: true
layout: post
title: 'A Collection To Generate Static APIs Using Postman Mock Servers'
image: https://kinlane-productions2.s3.amazonaws.com/a-collection-to-generate-static-apis-using-postman-mock-servers-1.png
---


I have a lot of little datasets I am organizing for use across a variety of projects. Since Postman has replace Github as my place where I begin all of my API projects, I figured that it could also be used host all of my data projects as APIs. Postman collections often times resemble an OpenAPI definition in that it provides a reference of an API, but in practice collections go much further, allowing you to store example data so that it can be better used in documentation, mocks, testing, and other types of purposes. You can store examples in OpenAPI, but Postman really allows you to go the distance when it comes to actually bringing those examples to life as a documented static API using Postman collections and mock server.


An example of this in action can be found with [my Fortune 500 public workspace](https://api-evangelist.postman.co/workspace/Fortune-500~08e01ed9-6906-47a0-a81e-369948912ef4/overview). I needed a list of 2020 Fortune 500 companies so that I can use it a variety of data mining and automation projects. I can easily download the data and publish a proper API, but it is so easy for me to use Postman collection in conjunction with the mock feature to publish simple mock APIs for each of my datasets. Using Postman as a sort of poor mans API hosting, which I won’t be opening up for public use, but will be using across a number of my API Projects. However, just because I won’t be sharing the URLs of my static (mock) APIs, I will be sharing all the collections I have developed around this work, beginning with my collection for generating my static (mock) data API from a CSV.


[![](https://kinlane-productions2.s3.amazonaws.com/a-collection-to-generate-static-apis-using-postman-mock-servers-1.png)](https://api-evangelist.postman.co/workspace/Fortune-500~08e01ed9-6906-47a0-a81e-369948912ef4/documentation/35240-04f42a0a-be66-4351-9793-f6d057aebd4e)


This is just a first version of my collection for pulling any CSV, converting the CSV to JSON, creating a collection, adding the JSON as an example, and then publishing my collection to my public workspace. Next I will be adding an option for adding JSON converted from CSV to an existing collection, and also auto-generation of the mock server and environment with the URL published. It provides me with a quick way to pull any CSV file and quickly generate a collection that I can then share, export, mock, and make available for us in other workflows and orchestrations. The results provides me with a simple static API for all the Fortune 500 companies for both 2019 and 2020.


[![](https://kinlane-productions2.s3.amazonaws.com/a-collection-to-generate-static-apis-using-postman-mock-servers-2.png)](https://api-evangelist.postman.co/workspace/Fortune-500~08e01ed9-6906-47a0-a81e-369948912ef4/documentation/35240-c62c073c-fea0-40ee-9994-352d7c072302)


This isn’t a normal usage of Postman collections and mock servers, but it does provide a quick and dirty way to generate static APIs from common datasets, then reuse that data across a variety of workflows and orchestrations. It reflects how I have used Github for the last 8 years, as a static host for all of my data. Now that I have Postman workspaces for all my data and API storage, I am converting all my data stores to be static APIs in this way. With Postman monitors and pre-request and post-request scripts in Postman, I am able to go a lot further with using this data as part of meaningful business workflows, going much further than what I could do on Github.


I started this work by creating [a CSV to JSON file conversion collection](https://apievangelist.com/2021/03/29/a-csv-to-json-file-conversion-postman-collection/), which I evolved into being [my collection for generating static APIs using Postman collections and mock server](https://api-evangelist.postman.co/workspace/Fortune-500~08e01ed9-6906-47a0-a81e-369948912ef4/documentation/35240-04f42a0a-be66-4351-9793-f6d057aebd4e). My goal is to maintain a robust set of collections I can use to publish open data to public workspaces using Postman, but then also expose static (mock) APIs for all of this data, so that I can weave it into my daily work. Because all of my work is public by default I am sharing all of my data collections, as well as the collections I used to generate them in public workspaces. I am keen on sharing this approach with folks, because I realize that once people understand the different ways in which you can twist and use the Postman platform they are going to come up with more innovative approaches that I never thought of—which is what APIs are all about.