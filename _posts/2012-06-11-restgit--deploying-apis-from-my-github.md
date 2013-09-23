---
layout: post
title: "RESTGit - Deploying APIs from My Github"
url: 'http://apievangelist.com/2012/06/11/restgit-deploying-apis-from-my-github/'
image: 'http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/blog/github-logo.png'
---

<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/github/github-logo.png" alt="" width="175" align="right" />

I have a workflow for dealing with the steady stream of ideas that fly out of my arse on a daily basis. First, I write them all down in Evernote. If an idea sticks with me and keeps nagging on me in the back of my mind, I usually give it a place on the internal wiki that I use for managing my world. Then if an idea sits on the wiki for over a year and I haven’t finished building it, and successfully deployed or integrated into my platform--I set it free.

The one year expiration date has come for one of my ideas, and I want to publish here so maybe someone else will run with it.

  * **Project Idea:** RESTGit
  * **Summary:** A RESTful interface for any public or private Github repository.

I just want a quick way of throwing up a RESTful front, with or without authentication using [3Scale API management][1]. RESTGit would deploy any flavor of language I choose: PHP, Python, Ruby, Java or anything else.

This way I could take select code resources I possess, commit them to a Github repository--then point RESTGit at the repository, and it would generate a REST framework and allow me to customize and adjust as needed.

RESTGit would be open source of course. It could be deployed as an Amazon EC2 instance, letting me rapidly deliver APIs for any resources I posses and scale as needed using AWS.

I wish I had more time to invest in my side projects, but I’d rather see it implemented. Hopefully one of you readers will find the time to develop RESTGit and open source it for everyone to use.

   [1]: http://www.3scale.net (3Scale API management)
