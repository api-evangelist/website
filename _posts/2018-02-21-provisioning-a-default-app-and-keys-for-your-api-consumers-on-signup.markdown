---
published: true
layout: post
title: Provisioning A Default App And Keys For Your API Consumers On Signup
date: 2018-02-21T12:00:00.000Z
tags:
  - API Evangelist
  - On-boarding
  - Management
  - Registration
image: >-
  https://s3.amazonaws.com/kinlane-productions/sabre/sabre-travel-signup-keys.png
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/sabre/sabre-travel-signup-keys.png" align="right" width="45%" style="padding: 15px;" /></p>I sign up for a lot of APIs. I love anything that reduces friction when on-boarding, and allows me to begin making an API call in 1-3 clicks. I'm a big fan of API providers that allow me to signup using my Github OAuth, preventing me from having to sign up for yet another account. I'm also a big fan of providers who automatically provision an application for me as part of the signup, and have my API keys waiting for me as soon as I've registered.

[While signing up for the Sabre travel API I saw that they provisioned my application as part of the API sign up process in a way that was worth showcasing](https://developer.sabre.com/member/register). Saving me the time and hassle of having to add a new application after I've signed up. Stuff like this might seem like a pretty small detail when developing an API on-boarding process, but when you are signing up for many different APIs, and trying to manage your time--these little details add up to be a significant time saver.

Ideally, API providers would auto-provision a default application along with the signup, but I like the idea of also giving me the option to name my application while registering. When crafting your API registration flow, make sure you spend time signing up multiple times, and try to put yourself in your API consumers shoes. I even recommend signing up for an account each week, repeatedly experiencing what your consumers will be exposed to. I also recommend spending time signing up for other APIs on a regular basis, to experience what they offer--you will always surprised by what I find.
