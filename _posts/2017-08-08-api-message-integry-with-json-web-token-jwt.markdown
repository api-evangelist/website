---
published: true
layout: post
title: API Message Integrity with JSON Web Token (JWT)
date: 2017-08-08T11:00:00.000Z
tags:
  - API Evangelist
  - Authentication
  - Security
image: 'https://s3.amazonaws.com/kinlane-productions/json-web-token/json-web-token.png'
---
<p><a href="https://jwt.io"><img src="https://s3.amazonaws.com/kinlane-productions/json-web-token/json-web-token.png" align="right" width="30%" style="padding: 15px;" /></a></p>I don't have any production experience deploying [JSON Web Tokens (JWT)](https://jwt.io/introduction/), but it has been something I've been reading up on, and staying in tune with for some time. I often reference JWT as the leading edge for API authentication, but there is one aspect of JWT I think is worth me referencing more often--message integrity. JSON Web Token (JWT) is an open standard (RFC 7519) that defines a compact and self-contained way for securely transmitting information between parties as a JSON object.

JWT can not only be used for authentication of both message sender/receiver, it can ensure the message integrity as well, leveraging a digital signature hash value of the message body to ensure the message integrity during transmission. It adds another interesting dimension to the [API security](http://security.apievangelist.com) conversation, and while not be applicable in all APIs, I know many that it would make a lot of sense. Many of the networks we use today and applications we depend on today are proxied, creating an environment where message integrity should always come into question, and JWT gives us another tool in our toolbox to help us keep things secure.

I'm working my way through each layer of API operations, looking for aspects of API security that are often obscured, hidden, or just not discussed as they should be. I feel like JWT is definitely one track of API security that has evolved the conversation significantly over the last couple years, and is something that can make a significant impact on the space with just a little more storytelling and education. I'm going to make sure API request and response message integrity is a regular part of my API security storytelling, curriculum, and live talks that I develop.
