---
published: true
layout: post
title: 'My Mastodon #FollowFriday Postman Collection'
image: https://kinlane-productions2.s3.amazonaws.com/follow-friday-mastodon/follow-friday-post.png
author:
name: kinlane
tags:
- Mastodon
- Postman
- Workspaces
- Collections
---
I have been making a number of [Postman collections to help automate and scale my new Mastodon universe](https://www.postman.com/api-evangelist/workspace/mastodon/overview), and when I share them I get one of two responses: 1) these are awesome and I’ll be putting them to use, and 2) these appear to be awesome but I have no idea what they are and how they work. Once again helping me realize that you are either in the know about APIs (and Postman), or you aren’t. Those of us in the know when it comes to APIs are regularly assuming that everyone knows what they are and how to put them to work. To counteract this reality, I wanted to attempt to craft a post that would onboard anyone, and I mean ANYONE, to use my [Mastodon #FollowFriday Postman Collection](https://www.postman.com/api-evangelist/workspace/mastodon/documentation/35240-70fa0959-3e1a-480b-88a0-a54d5db80cc6?entity=&branch=&version=). I know that I will miss things, but I find this exercise super illuminating, and I am hoping I will get better with time.

## What Is An API, or Application Programming Interface?
Let’s start with the basics. I don’t want to assume anyone knows what the acronym API standards for. API stands for Application Programming Interface, and is how almost all modern web, mobile, and device applications use to deliver the functionality you are using. Every one of those applications on your mobile phone use APIs. Every website you visit online uses an API. You are using APIs every day, but are not likely aware of it unless you are in the business of developing applications. APIs are like the banking system. You do not have to understand how they work at a technical level, but you should be aware of how they power your world, and be able to competently and securely use them to operate your world.

Like other applications Mastodon has an API. The mobile or web application you use to engage with the Mastodon universe uses the [Mastodon API](https://docs.joinmastodon.org/dev/routes/#api). Like all the other applications you use it can help to be aware that this is happening behind the scenes, and if you have the interest you can put the API to work for you. While it is common for you to need to write code in at least one programming language to use the API, there are no-code / low-code solutions out there that will help you do this without having to be a full blown programmer. Personally, I am not an engineer, I am a reverse engineer and I just learned to code by reading the code of others. What I am going to walk you through here is how you can use Postman, a low-code/no-code solution to use the Mastodon API, or more specifically use the Mastodon API to automate the pulling of followers and likes to generate a #FollowFriday post.

## What is Postman?
[Postman](https://www.postman.com/) is a startup that developers have grown to love over the last decade, and where I work as the Chief Evangelist. Of course I am biased and want you to use Postman, but if you ask most any developer, they will tell you that Postman is an indispensable tool in their toolbox and they can’t live without it. Think of Postman as a browser, instead of for the web, it is for APIs—which really are the same thing. The web is for humans, and APIs are for machines. Postman gives you all of the controls over the websites you visit, the applications you use, and the APIs these websites and applications put to work behind the scenes. You do not have to be a programmer to use Postman, and with it you will be pulling back the curtain on how the web works and obtaining more control over your data, and how the applications you depend on works.

![Postman](https://kinlane-productions2.s3.amazonaws.com/follow-friday-mastodon/postman-1.png)

Postman is free to use. Postman is what is called an API client, allowing you to make API calls without writing code. You can sign up for Postman by visiting [Postman.com](https://www.postman.com/) and creating a new account. You can choose to download Postman locally or use it on the web. There are advantages to both, but if you are just getting started I recommend using the web. Once you have signed up for Postman, you can visit [my Mastodon workspace](https://www.postman.com/api-evangelist/workspace/mastodon/documentation/35240-70fa0959-3e1a-480b-88a0-a54d5db80cc6?entity=&branch=&version=), fork any of the collections I am developing and begin using for yourself. However, there are several things you are going to need to understand to make all of this work, and I am hoping I will not miss any fundamental steps that help you be successful in this journey. Before we dive into the workspace full of Mastodon API collections I have built, let’s cover a few of the Postman fundamentals you will need to make this work.

## What is a Postman Workspace?
A Postman workspace is just what it says, a space where you can do work with APIs in a collaborative way. You can have personal, team, partner, or public workspaces. What I am sharing with you is a workspace I have set up to do all of my Mastodon API work, but it is made public so I can share as part of various stories I tell about my Mastodon work, but done in a way anyone can use.

![Postman](https://kinlane-productions2.s3.amazonaws.com/follow-friday-mastodon/mastodon-workspace-1.png)

A workspace provides a collaborative space for API work to occur publicly or privately. APIs are very hard to see and collaborate around, and workspaces make them much more tangible and easy to discover. [I have hundreds of API workspaces](https://www.postman.com/api-evangelist), and this one is just the one I have set up dedicated to my Mastodon API work. You will find similar workspaces I have for Twitter, LinkedIn, Facebook, Youtube, and the other APIs I use to automate my work.

## What is a Postman Collection?
To learn about [Postman collection](https://learning.postman.com/docs/getting-started/creating-the-first-collection/#:~:text=Postman%20Collections%20are%20a%20group,particular%20request%20in%20your%20history.) you can visit my Mastodon workspace where you will find a bunch of Mastodon collections. These are basically little portable folders containing one or more API requests. Postman allows you to define all of the elements you need to make an API request and then save them as a collection that you can share, execute, and evolve to meet your needs—-without writing code. Collections have all the inputs you need to work with the Mastodon API, and I have saved them as small modular collections to help make the Mastodon API easier to use and automate with.

![Postman](https://kinlane-productions2.s3.amazonaws.com/follow-friday-mastodon/postman-2.png)

Postman collections allow you to work with APIs without writing code. There are parts of manipulating, saving, and working with APIs that might require scripting within a collection, but for the most part you can call APIs and do things with a collection—no programming necessary. Each collection can be run using a runner or scheduled to run using a monitor, allowing you to create API collections for different purposes and run them as you need.

## What is a Postman Environment?
A [Postman environment](https://learning.postman.com/docs/sending-requests/managing-environments/) is another artifact like a collection, but it is where you store your tokens, secrets, and other things you will need across the APIs you are working with. When working with APIs you will often need what is called an API key or token to make sure you have the proper authorization to use an API. In a bit I will show you how to get your Mastodon API key from your instance, but you will apply to your own collection. Postman collections describe the API you will be working with, and your environment provides you the keys to use that API.

![Postman](https://kinlane-productions2.s3.amazonaws.com/follow-friday-mastodon/postman-3.png)

I have put the base URL for my own Mastodon instance, my token, and my account ID. These are the three unique identifiers I will need to use the Mastodon collections I create. All of the collections I have developed will apply this URL, token, and account ID to make things work. This abstracts away the unique parts of working with an API, and allows me to use the same Postman collection across all of the instances and accounts that I manage.

## What is the Mastodon API?
To use any of the collections I have built, you will need to use the Mastodon API for your instance. The [Mastodon API](https://docs.joinmastodon.org/dev/routes/#api) is the same for all Mastodon instances-—this is the magic of federated solutions like Mastodon. You can view the documentation for the Mastodon API, and to be able to use it you will need to create a token for your account and instance. To do this you need to visit the preferences area and click on development—then add a new application. 

![Postman](https://kinlane-productions2.s3.amazonaws.com/follow-friday-mastodon/mastodon-1.png)

Just give your application a name and any URL for your profile, and then create. You will be issued a client key, client secret, and access token. All we will need for our purposes is your access token. The key and secret is meant for other situations that are beyond the scope of this story. You will be putting the access token in your Postman environment, and applying to the #FollowFriday collection that we will be using below.

## What is the Mastodon FollowFriday Collection?
The [Mastodon #FollowFriday Collection](https://www.postman.com/api-evangelist/workspace/mastodon/documentation/35240-70fa0959-3e1a-480b-88a0-a54d5db80cc6?entity=&branch=&version=) I have created is a Postman Collection I have created and published to my public workspace for anyone to use. The collection has three separate API calls available, 1) Pulling your recent favorites, 2) Pulling your recent followers, and 3) Posting a status. This collection pulls your favorites and follows, and then randomly picks five from each, and assembles them into a #FollowFriday post that is then posted to your Mastodon account using the API.

![Postman](https://kinlane-productions2.s3.amazonaws.com/follow-friday-mastodon/follow-friday.png)

Make sure you explore the collection and play around. Don’t be afraid to look around. You won’t be actually able to run my collection in my workspace, so you can’t mess anything up. To actually be able to use the collection you will have to actually fork the collection to your own workspace. Collections work similar to code you see on GitHub, allowing you to reuse the work of others without actually messing up what they have built.

## How Do I Fork the Mastodon FollowFriday Collection?
Before you can actually use the Mastodon FollowFriday Collection you will have to fork it. This is done by clicking on the three little dots when you mouse over the name of the collection. Forking is simply just making a copy of the collection for your own use.

![Postman](https://kinlane-productions2.s3.amazonaws.com/follow-friday-mastodon/fork-collection-1.png)

Forking a collection is what makes all of this collaborative, and something anyone can reuse and put to work. You are now taking my collection, creating a copy in your own workspace so that you can run with your own keys against your own Mastodon instance.

![Postman](https://kinlane-productions2.s3.amazonaws.com/follow-friday-mastodon/fork-collection-2.png)

To continue, you just have to give your fork a label, and choose which workspace you will be working with the collection. Once you fork you will have your own copy, which will not impact my work at all. However, you will be able to see when I make updates to my and decide whether or not you want to bring in any updates.

## How Do I Apply Collection to My Mastodon Instance?
Even with the Mastodon #FollowFriday Collection forked you won’t be able to run it. Well if you do, you will just get an error. Go ahead and try-—you won’t break anything. Before you can run it successfully you will need to also fork the environment, and add your instance URL and token.

![Postman](https://kinlane-productions2.s3.amazonaws.com/follow-friday-mastodon/postman-4.png)

You will need to add the base URL for your Mastodon instance, as well as the token you obtained by adding an application under the development section of your preferences. Now there is a very important detail you need to consider. There are two columns in your environment: 1) Initial Value, and 2) Current Value. Both can be used to store your value, but your initial value will be available to anyone else who might use your workspace in a team or public environment. I recommend just using Current Value, which only you will ever be able to see.

## Test Your Collection By Running Favorites
Before we choose to run the entire FollowFriday Collection, let’s just run the favorites request all by itself to make sure things work. Click on the Favorites request in the collection, then before you click on the big blue send button, make sure right above it you have selected the environment you have forked from the dropdown. This will apply your base URL and token to the collection.

![Postman](https://kinlane-productions2.s3.amazonaws.com/follow-friday-mastodon/postman-5.png)

Once you hit send, you should see a list of things you have favorited in a JSON format. Don’t worry if you can’t read entirely, but you should see the user and content of the post you favorite amidst the brackets and commas that is JSON. You don’t have to do anything, and via the Test Script tab you will see a little script that has parsed the response and saved a list of accounts into your environment of usage by the other requests.

## Obtaining Your Account ID
Now, before you can run the followers request, you will need your account ID. Now I do not know how to advise you to do this via the interface. Maybe it is there, but I can’t find it. As an administrator I can look you up via interface, but the only way I know how to do it is to search for your user via the Mastodon API. So you will need to also fork the Mastodon Search collection I have created. Once you have forked, put your name in the “q” parameter of the collection, and hit send.

![Postman](https://kinlane-productions2.s3.amazonaws.com/follow-friday-mastodon/postman-6.png)

You should see your account id at the top of the response. Go ahead and copy and then go to your Postman environment and add it to the account ID variable, and click save. I wish that the followers API for Mastodon behaved the same as favorites and didn’t need an account ID, but this is something above your pay grade and mine. 

## Running the FollowFriday Collection
Once you have your account ID, go ahead and try running the followers request to make sure it works. If it works, then click on the top level name for the FollowFriday collection and you will see a Run button in the top of the collection view window—which will allow you to run all three requests at once.

![Postman](https://kinlane-productions2.s3.amazonaws.com/follow-friday-mastodon/postman-7.png)

What this runner will do is execute the entire collection, pulling the favorites, the followers, and then the script assembles and posts to your Mastodon account. Providing you with a simple way to publish a follow Friday post each week.

![Postman](https://kinlane-productions2.s3.amazonaws.com/follow-friday-mastodon/postman-8.png)

That is it, that is what this collection does. I know it takes a bit to onboard with the collection due to learning about APIs and Postman, but the collection itself is pretty straightforward to run. Hopefully you see the potential of it when it comes to giving you more control over your Mastodon presence.

## Mastodon FollowFriday Collection
I tried to make this walk through as complete as possible, but as I said it is really common for those in the know to leave out steps for those who are new. It is very easy for us to leave out important steps. I encounter this regularly in my work while learning from others and am guilty of it in my own work. If you get stuck I am happy to try and help, but I can’t always guarantee I will have the time, so make sure and re-read what is here before you reach out. But if you get stuck [you can ping me on Mastodon](https://mastodon.kinlane.com/web/@kin), or there is the ability to comment on the collection, and each individual requests using a hard to see icon on the right hand-side.

![Postman](https://kinlane-productions2.s3.amazonaws.com/follow-friday-mastodon/postman-9.png)

If you ask your question here, others who are reading this post can learn from my answers, where if you message me on Mastodon it is likely to get lost in the Indiana Jones warehouse of the Fediverse. I am sure I left some important steps out of this walk-through, but I tried to slow down and make as few assumptions about what you will already know as I possibly can. APIs can be very technical, but I believe that they can be accessible to everyone-—this is why I work at Postman. Please make sure you play around and experiment. You aren’t going to break anything, and spend time exploring these collections, as well as the other collections I have in my Mastodon workspace.

Please let me know if there are any mistakes or confusing aspects of this post. Once you have become more aware of APIs, and acquired more experience with Postman, most of the work involved in working with the Mastodon API using Postman will go away. This is why this workspace and collections are so interesting to people in the know, because they save you a lot of time having to program, and the modular reusable nature of them makes it easy to automate your presence on Mastodon. For me, as someone with multiple instances, these collections, combined with separate instance environments, make for a very powerful combination. I can easily program my way forward with all of this, but having everything defined as modular and reusable collections and environments helps save time and augment my day with API superpowers in the Fediverse.