---
published: true
layout: post
title: HTTP as a Substrate
date: 2017-08-08T13:00:00.000Z
tags:
  - API Evangelist
  - HTTP
  - DNS
  - Protocols
image: 'https://s3.amazonaws.com/drone-recovery/babyfoot04.jpg'
---
<p><img src="https://s3.amazonaws.com/drone-recovery/babyfoot04.jpg" align="right" width="40%" style="padding: 15px;" /></p>I am spending a significant amount of time reading RFCs lately. I find the documents to be very cumbersome to read, but the more you read, the more tolerant you become. When I browse through RFCs I'm always reminded of how little I actually know about the web. In an effort to push forward my education, and maybe yours along the way, I'm going to be cherry picking specific sections of the interesting RFCs I'm digesting here on the blog. [Today's RFC is 3205, filed under Best Current Practice", and is on the use of HTTP as a Substrate](https://tools.ietf.org/html/rfc3205).

_Recently there has been widespread interest in using Hypertext Transfer Protocol (HTTP) [1] as a substrate for other applications- level protocols. Various reasons cited for this interest have included:

- familiarity and mindshare,
- compatibility with widely deployed browsers,
- ability to reuse existing servers and client libraries,
-  ease of prototyping servers using CGI scripts and similar extension mechanisms, authentication  and SSL or TLS,
- the ability of HTTP to traverse firewalls, and
- cases where a server often needs to support HTTP anyway.

The Internet community has a long tradition of protocol reuse, dating back to the use of Telnet as a substrate for FTP and SMTP.  However, the recent interest in layering new protocols over HTTP has raised a number of questions when such use is appropriate, and the proper way to use HTTP in contexts where it is appropriate. Specifically, for a given application that is layered on top of HTTP:

- Should the application use a different port than the HTTP default  of 80?
- Should the application use traditional HTTP methods (GET, POST,  etc.) or should it define new methods?
-  Should the application use http: URLs or define its own prefix?
- Should the application define its own MIME-types, or use something  that already exists (like registering a new type of MIME-directory structure)?

This memo recommends certain design decisions in answer to these  questions.

This memo is intended as advice and recommendation for protocol designers, working groups, implementors, and IESG, rather than as a strict set of rules which must be adhered to in all cases. Accordingly, the capitalized key words defined in RFC 2119, which are intended to indicate conformance to a specification, are not used in this memo._

I love the notion of [HTTP as a substrate](https://tools.ietf.org/html/rfc3205). The definition of substrate is "a substance or layer that underlies something, or on which some process occurs, in particular" or also, "the surface or material on or from which an organism lives, grows, or obtains its nourishment". I also love the notion of providing guidance for this line of thought. There are many things contained in this document I have learned from my time in the space, and included in my storytelling, without much thought regarding where it originated, or how accurate it was. I particularly like the notion of HTTP as a material in which an organism lives, but maybe more of a digital organism, or a bot. A reminder that everything that may take seed, flourish and grow in this environment, might not always be a good thing.
