---
layout: post
title: "Providing API Developers with Github Login Using Singly"
url: 'http://apievangelist.com/2012/09/05/provide-api-developers-with-github-login-using-singly/'
image: 'http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/blog/singly-plus-github.png'
---

[<img class="c1" src="https://s3.amazonaws.com/kinlane-productions/singly/singly-plus-github.png" alt="" width="150" align="right" />][1]

I’m building a small API that I want to allow developers to register for. I don’t want to make it a complicated registration process, I just want them to provide some sort of credentials and I will issWue a key that they can use to make API calls.

To keep it simple I’m offering a login using a [Github][2] account. Every developer has a Github account right? Well if they don’t, they should. The easiest way there is to enable your API with a Github login is Singly.

Using [Singly][3], I sign in with my Github account (this is where I got this idea), then I [add a new application][4], giving it the root URL and callback URL of my API developer area.

[<img class="c2" src="https://s3.amazonaws.com/kinlane-productions/singly/Singly-Application-Github.png" alt="" width="500" />][4]

Next I need to link up my Github account to my Singly account, by [adding an application to my Github account][5]. I give it a name, URL and when adding the callback, I add a Singly specific callback--Singly will handle the rest.

<img class="c2" src="https://s3.amazonaws.com/kinlane-productions/singly/Github-App-Settings.png" alt="" width="500" />

Now I just add a login with Github button to my developer area with the following URL: 

  * _https://api.singly.com/v0/services/github?access_token=my_token_

When one of my API developers click on the Github login, it will route them to Github for OAuth, back to Singly and to my API callback URL where I can grab the authorization code for the user.

Now I can reference my API developer using their Github account, using their profile image, name as well as having some stats about the user like how many repositories they have, number of followers and who they follow--which provides me a pretty good baseline metric for distinguishing active developers vs. in-active developers.

[<img src="https://s3.amazonaws.com/kinlane-productions/kinlane-github.png" alt="" align="right" />][6]

Github login should be default for all API providers. It reduces developer on-boarding friction with an API, and uses the social network that makes the most sense for API developers.

   [1]: https://singly.com/docs/github
   [2]: http://www.github.com (Github)
   [3]: http://www.singly.com (Singly)
   [4]: https://singly.com/apps/new
   [5]: https://github.com/settings/applications
   [6]: https://github.com/kinlane
