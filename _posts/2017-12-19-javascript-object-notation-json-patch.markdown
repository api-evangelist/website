---
published: true
layout: post
title: JavaScript Object Notation (JSON) Patch
date: 2017-12-19T13:00:00.000Z
tags:
  - API Evangelist
  - Standards
  - Design
  - Definitions
image: >-
  https://s3.amazonaws.com/kinlane-productions/rfc/6902/javascript-object-notation-json-patch.png
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/rfc/6902/javascript-object-notation-json-patch.png" align="right" width="45%" style="padding: 15px;" /></p>I'm continuing my studying into what [my new partner in crime Streamdata.io does](http://streamdata.io), and part of this research is understanding the details of their technology stack. Today's work involves understanding their usage of [JavaScript Object Notation (JSON) Patch](https://tools.ietf.org/html/rfc6902). When you [proxy any existing web API using Streamdata.io](http://streamdata.io), the first thing you get back is a complete JSON representation of the response, but then with each change you just get back a JSON Patch response with only the details of what has changed. JSON Patch is used for expressing a sequence of operations to apply to a any JSON object or document and you'll find used with the HTTP PATCH method.

The introduction for [JSON Patch from RFC [RFC4627]](https://tools.ietf.org/html/rfc6902) describes it this way:

> JavaScript Object Notation (JSON) [RFC4627] is a common format for the exchange and storage of structured data.  HTTP PATCH [RFC5789] extends the Hypertext Transfer Protocol (HTTP) [RFC2616] with a method to perform partial modifications to resources.
> JSON Patch is a format (identified by the media type "application/json-patch+json") for expressing a sequence of operations to apply to a target JSON document; it is suitable for use with the HTTP PATCH method.
This format is also potentially useful in other cases in which it is necessary to make partial updates to a JSON document or to a data structure that has similar constraints (i.e., they can be serialized as an object or an array using the JSON grammar).

JSON Patch is an efficient way to only get the details from an API regarding only what has changed, instead of sending everything over the pipes each time. It makes sense that Streamdata.io has used it in conjunction with Server-Sent Events (SSE) to efficiently cache and stream data from existing web APIs. I have to admit I never put this together with the PATCH method for API responses. Most of the APIs I've seen that use PATCH, do not actually implement JSON PATCH, so this was a learning moment for me. Something I'm always thankful for, constantly reminding me just how much I do not know in the space, even with my experience studying APIs.

Next, I'm going to invest more time understanding how to write code that navigates and applies JSON Patch in real-world situations. I've got my handful of Streamdata.io enabled APIs streaming me data, but I don't have the experiencing applying the changes to a UI, or existing system integration as the data flows in. It all makes a lot more sense to me now, and provides me with a efficient model for managing changes that occur across APIs. It is also yet ANOTHER reminder for me of how important it is that I study up on RFCs, and be knowledgable regarding existing patterns like this that exist, so that I'm not reinventing the wheel when it comes to my API design.
