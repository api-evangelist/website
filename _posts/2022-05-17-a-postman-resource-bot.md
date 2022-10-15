---
published: true
layout: post
title: 'A Postman Resource Bot'
image: https://kinlane-productions2.s3.amazonaws.com/postman-resource-bot.png
tags:
- Collection
- Bots
- Slack
- Postman
---
A rite of passage for most new Postman employees is creating their first collection. I asked my new collection developer Bello Gbadebo ([@gbahdeyboh](ttps://twitter.com/gbahdeyboh)), or “Debo”, to spend his first week on his first collection. Now that I am writing this, I realize the gravity of this situation, and very pleased that Debo rose to the occasion with a pretty kick ass first collection. Don’t get me wrong, I’ve seen some interesting first collections from new Postmanauts, but Debo really stepped up, hitting on all the right notes when it comes to demonstrating the power of a collection, with what he called his [Resource Bot](https://www.postman.com/postman/workspace/e7fc5730-6c18-4af9-af07-806edc6f49c0/documentation/20781379-8cd8625a-3e29-443d-a33b-895a436382d8). Most Postman’s will build a collection that integrates with a single API, but Debo made one that scrapes, integrates with multiple APIs, and uses webhooks, and other advanced capabilities of a Postman collection.

Here is the overview Debo provides for his Postman Resource Bot:

> <i>“This collection is a slack bot that can randomly suggest resources and blog posts for you to read anytime you need it to. It has a set of commands that can be sent to it and what it suggests depends on the command it receives. To read more about its usage and commands, please read this article or watch this video.”</i>

The Resource Bot collection pulls entries from the Postman learning center, the Postman blog, and Youtube, but it its use of both Slack and Postman Webhooks to leverage the collection as a Slack bot that really elevates his approach. Also, the Youtube pull is pretty straightforward, but the learning center and blog are scraping. The collection is immediately useful and educational, demonstrates the power of APIs and scraping, while showcasing the automation power of a Postman collection with webhooks. It is an implementation that is spawning a bunch more ideas for collections for me, and different ways to help educate the community around the world of APIs, the API Lifecycle, and the Postman API Platform.

I have to say, I am pretty excited about what Debo is going to be building. I setup [a Github repository to help manage the collection work Debo and team will be doing](https://github.com/postman-open-technologies/collections). Debo clearly gets what collections are all about, and be a willing partner in helping push the boundaries of what is possible with collections. I mean [look at his collection](https://www.postman.com/postman/workspace/e7fc5730-6c18-4af9-af07-806edc6f49c0/documentation/20781379-8cd8625a-3e29-443d-a33b-895a436382d8), it is all organized and well-documented!! Anyways, I am working away plotting and scheming with him to see what we can cook up with collections-—if you have any interesting ideas or have questions, feel free to submit an issue on the repo, or tweet at [@gbahdeyboh](https://twitter.com/gbahdeyboh) or [@kinlane](https://twitter.com/kinlane). We are going to have some fun!!