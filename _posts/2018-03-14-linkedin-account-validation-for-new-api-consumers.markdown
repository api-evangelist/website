---
published: true
layout: post
title: LinkedIn Account Validation For New API Consumers
date: 2018-03-14T12:00:00.000Z
tags:
  - API Evangelist
  - On-boarding
  - Getting Started
  - Management
  - Authentication
image: >-
  https://s3.amazonaws.com/kinlane-productions/dawex/requiring-linkedin-validation.png
---
<p><img src="{{ page.image }}" width="45%" align="right" style="padding: 15px;" /></p>I was on-boarding with [the data marketplace Dawex](https://www.dawex.com/en/) the other day, and I thought their on-boarding process was interesting. It is pretty rigid, requiring users to validate themselves in multiple ways, but it provides some interesting approaches to knowing more about who your API developers are. Dawex has the basic level email and phone number validation, but they have added a 3rd dimension, validating who you are using your LinkedIn profile.

After signing up, I was required to validate my email account--pretty standard stuff. Then I was asked to enter a code sent to my cell phone via SMS--not as common, but increasingly a way that platforms are using to verify you. Then I was asked to OAuth and connect my LinkedIn account to my Dawex profile. I've seen sign up and login using LinkedIn, but never using it as a 3rd type of validating who you are, and that you are truly a legitimate business user. I haven't been verified yet, it says it will take up to 72 hour is what the notification at the top of my dashboard says, but it caught my attention.

Dawes also has a complete, [Know Your Customer (KYC)](https://en.wikipedia.org/wiki/Know_your_customer) process, which takes the validation to another level, and something I'll write about separately. I think the social profile validation provides an interesting look at how platforms validate who we are. In an environment where API developers will often sign up for multiple accounts, and do other shady things with anonymous accounts, I can get behind requiring consumers to prove who they are. I also think that providing robust, active, verifiable social media accounts using Github, Twitter, LinkedIn, and Facebook makes a lot of sense. I'd say that all four of these profiles represent who I am as a person, as well as a business.

I have talked about using Github to validate and rate API consumers before. I could see a world where I get validated upon signup using my social profile(s), and the amount of access to an API I am entitled to varies depending on how complete, robust, and verifiable my presence is. I'm not keen on giving up all my data to every API I sign up, but providing access to my profile so they can validate and rank who I am, and then get out of my way when it comes to using their resources, is something I can get behind. I could even envision where you throw Paypal into the mix, and my billing profile is further rounded off, allowing me to consume whatever I desire, and pay for what I used. 
