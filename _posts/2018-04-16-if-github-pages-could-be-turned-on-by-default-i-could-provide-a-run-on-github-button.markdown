---
published: true
layout: post
title: If Github Pages Could Be Turned On By Default I Could Provide A Run On Github Button
date: 2018-04-16T09:00:00.000Z
tags:
  - API Evangelist
  - Github
  - Github Pages
  - Applications
image: 'https://s3.amazonaws.com/kinlane-productions/github/run-on-github-button.png'
---
<p><img src="{{ page.image }}" width="45%" align="right" style="padding: 15px;" /></p>My world runs on Gitub. 100% of my public website projects run on Github Pages, and about 75% of my public web applications run on Gitub Pages. The remaining 25% of it all is my API infrastructure. However, I'm increasingly pushing my data and content APIs to run entirely on Github with Github Pages as frontend, and the Github repo as the backend, with the Github API as the transport. I'd rather be serving up static JSON and YAML from repositories, and building JavaScript web applications that run using Jekyll, than dynamic server-side web applications.

It is pretty straightforward to engineer HTML, CSS, and JavaScript applications that run entirely on Github Pages, and leverage JSON and YAML stored in the underlying Github repo as the database backend, using the Github API as the API backend. Your Github OAuth token becomes your API key, and Github organization and user structure becomes the authentication and access management layer. These apps can run publicly, and when someone wants to write, as well as read data to the application, they just need to authenticate using Github--if they have permission, then they get access, and can write JSON or YAML data to the underlying repo via the API.

I'm a big fan of building portable micro applications using this approach. The only road block for me to make them easier to use by other users, is the ability to fork them into their own Github account with a single click. I have a Github OAuth token for any authenticated user, and with the right scopes I can easily fork a self-contained web application into their account or organization, giving them full control over their own version of the application. The problem is that each user has to enable Github Pages for the repository before they can view the application. It is a simple, but pretty significant hurdle for many users, and is something that prevents me from developing more applications that work like this.

If Github would allow for the enabling of Github Pages by default, or via the API, I could create a Run in Github button that would allow my micro apps to be forked and ran within each users own Github account. Maybe I'm missing something, but I haven't been able to make Github Pages be enabled by default for any repo, or via the API. It seems like a simple feature to add to the road map, which is something that would have profound implications on how we deploy applications, turning Github into a JavaScript serverless environment, where applications can be forked and operated at scale. It is an approach I will keep using, but I am afraid it won't catch on properly until users are able to deploy an application on Github with a single click. All I need is for Github to allow for me to create a new repository using the Github API, and allow me to turn on Github Pages by default when it is created--then my run in Github button will become a reality.
