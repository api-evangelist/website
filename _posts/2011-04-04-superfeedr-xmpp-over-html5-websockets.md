---
layout: post
title: "Superfeedr XMPP over HTML5 WebSockets"
url: 'http://apievangelist.com/2011/04/04/superfeedr-xmpp-over-html5-websockets/'
image: ''
---

[<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/api-evangelist/superfeedr-logo.png" alt="" width="250" align="right" />][1][Superfeedr][1] keeps showing what a pioneer they are when it comes to web, API and feed technology, with a [release of an Ejabber module that builds WebSockets into an XMPP server][2].

XMPP provides identity, authentication, presence, and notifications for APIs and other feeds, and with the growing adoption of HTML5, the [WebSockets API][3] is the perfect built-in browser client to interact with APIs and feeds in the browser.

The [Superfeedr Ejabber module][4] is written in Erlang and available over at [Github][5]. They recommend you use the module with [Strophejs][6], an XMPP library written in Javascript.

XMPP is growing in popularity as a protocol for providing real-time API and feed updates, while increasing the efficiency of API networks by minimizing polling of API endpoints.

   [1]: http://superfeedr.com (Superfeedr)
   [2]: http://blog.superfeedr.com/xmpp-over-websockets/ (release of an Ejabber module that builds Websocks into an XMPP server)
   [3]: http://dev.w3.org/html5/websockets/ (HTML5 WebSockets API)
   [4]: https://github.com/superfeedr/ejabberd-websockets (Superfeedr Ejabber Module)
   [5]: https://github.com/superfeedr/ejabberd-websockets (Github)
   [6]: https://github.com/metajack/strophejs (SropheJS)
