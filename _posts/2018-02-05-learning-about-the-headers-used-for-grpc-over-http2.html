---
published: true
layout: post
title: 'Learning About The Headers Used for gRPC over HTTP/2'
image: https://s3.amazonaws.com/kinlane-productions2/bw-icons/bw-grpc.png
---

<p><img src="https://s3.amazonaws.com/kinlane-productions2/bw-icons/bw-grpc.png" align="right" width="45%" style="padding: 15px;" />
<p>I am learning more about gRPC and HTTP/2, as part of the recent expansion of my API toolbox. I’m not a huge fan of Protocol Buffers, however I do get the performance gain they introduce, but I am very interested in learning more about how HTTP/2 is being used as a transport. While I’ve been studying how websockets, Kafka, MQTT, and other protocols have left the boundaries of HTTP and are embracing the performance gains available in the pure TCP realm, I’m more intrigued by the next generation of HTTP as a transport.

<p>Part of my learning process is all about understanding the headers available to us in the HTTP/2 realm. I’ve been learning more about the next generation HTTP headers from the <a href="https://github.com/grpc/grpc/blob/master/doc/PROTOCOL-HTTP2.md">gRPC Github repository</a> which provides details on the request and response headers in play.

<p><strong>HTTP/2 API Request Headers</strong>

<ul>
  <li>Request-Headers → Call-Definition *Custom-Metadata</li>
  <li>Call-Definition → Method Scheme Path TE [Authority] [Timeout] Content-Type [Message-Type] [Message-Encoding] [Message-Accept-Encoding] [User-Agent]</li>
  <li>Method → “:method POST”</li>
  <li>Scheme → “:scheme “ (“http” / “https”)</li>
  <li>Path → “:path” “/” Service-Name “/” {method name} # But see note below.</li>
  <li>Service-Name → {IDL-specific service name}</li>
  <li>Authority → “:authority” {virtual host name of authority}</li>
  <li>TE → “te” “trailers” # Used to detect incompatible proxies</li>
  <li>Timeout → “grpc-timeout” TimeoutValue TimeoutUnit</li>
  <li>TimeoutValue → {positive integer as ASCII string of at most 8 digits}</li>
  <li>TimeoutUnit → Hour / Minute / Second / Millisecond / Microsecond / Nanosecond</li>
  <li>Hour → “H”</li>
  <li>Minute → “M”</li>
  <li>Second → “S”</li>
  <li>Millisecond → “m”</li>
  <li>Microsecond → “u”</li>
  <li>Nanosecond → “n”</li>
  <li>Content-Type → “content-type” “application/grpc” [(“+proto” / “+json” / {custom})]</li>
  <li>Content-Coding → “identity” / “gzip” / “deflate” / “snappy” / {custom}</li>
  <li>Message-Encoding → “grpc-encoding” Content-Coding</li>
  <li>Message-Accept-Encoding → “grpc-accept-encoding” Content-Coding *(“,” Content-Coding)</li>
  <li>User-Agent → “user-agent” {structured user-agent string}</li>
  <li>Message-Type → “grpc-message-type” {type name for message schema}</li>
  <li>Custom-Metadata → Binary-Header / ASCII-Header</li>
  <li>Binary-Header → {Header-Name “-bin” } {base64 encoded value}</li>
  <li>ASCII-Header → Header-Name ASCII-Value</li>
  <li>Header-Name → 1*( %x30-39 / %x61-7A / “_” / “-“ / “.”) ; 0-9 a-z _ - .</li>
  <li>ASCII-Value → 1*( %x20-%x7E ) ; space and printable ASCII</li>
</ul>

<p><strong>HTTP/2 API Response Headers</strong>

<ul>
  <li>Response → (Response-Headers *Length-Prefixed-Message Trailers) / Trailers-Only
Response-Headers → HTTP-Status [Message-Encoding] [Message-Accept-Encoding] Content-Type *Custom-Metadata</li>
  <li>Trailers-Only → HTTP-Status Content-Type Trailers</li>
  <li>Trailers → Status [Status-Message] *Custom-Metadata</li>
  <li>HTTP-Status → “:status 200”</li>
  <li>Status → “grpc-status” 1*DIGIT ; 0-9</li>
  <li>Status-Message → “grpc-message” Percent-Encoded</li>
  <li>Percent-Encoded → 1*(Percent-Byte-Unencoded / Percent-Byte-Encoded)</li>
  <li>Percent-Byte-Unencoded → 1*( %x20-%x24 / %x26-%x7E ) ; space and VCHAR, except %</li>
  <li>Percent-Byte-Encoded → “%” 2HEXDIGIT ; 0-9 A-F</li>
</ul>

<p>I’m enjoying getting down to the nitty gritty details of how HTTP/2 works. I’m intrigued by the multi-directionality of it. Being able to use just like HTTP/1.1 with simple requests and responses, but also being able to introduce bi-directional API calls, where you can make many different API calls as you want. I don’t think I will get any time to play with in the near future. I have way too much work. However, I do like learning about how it is being used, and I think Google is the most forward thinking when it comes to HTTP/2 adoption in the API sector–providing multi-speed APIs in JSON using HTTP/1.1, or Protocol Buffers using HTTP/2.

