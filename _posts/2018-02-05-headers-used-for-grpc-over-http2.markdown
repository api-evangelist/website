---
published: true
layout: post
title: Learning About The Headers Used for gRPC over HTTP/2
date: 2018-02-05T11:00:00.000Z
tags:
  - API Evangelist
  - gRPC
  - Protocols
  - Design
  - Headers
  - HTTP/2
image: 'https://s3.amazonaws.com/kinlane-productions/bw-icons/bw-grpc.png'
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/bw-icons/bw-grpc.png" align="right" width="45%" style="padding: 15px;" /></p>I am learning more about gRPC and HTTP/2, as part of the recent expansion of my API toolbox. I'm not a huge fan of Protocol Buffers, however I do get the performance gain they introduce, but I am very interested in learning more about how HTTP/2 is being used as a transport. While I've been studying how websockets, Kafka, MQTT, and other protocols have left the boundaries of HTTP and are embracing the performance gains available in the pure TCP realm, I'm more intrigued by the next generation of HTTP as a transport.

Part of my learning process is all about understanding the headers available to us in the HTTP/2 realm. I've been learning more about the next generation HTTP headers from the [gRPC Github repository](https://github.com/grpc/grpc/blob/master/doc/PROTOCOL-HTTP2.md) which provides details on the request and response headers in play.

**HTTP/2 API Request Headers**

- Request-Headers → Call-Definition *Custom-Metadata
- Call-Definition → Method Scheme Path TE [Authority] [Timeout] Content-Type [Message-Type] [Message-Encoding] [Message-Accept-Encoding] [User-Agent]
- Method → ":method POST"
- Scheme → ":scheme " ("http" / "https")
- Path → ":path" "/" Service-Name "/" {method name} # But see note below.
- Service-Name → {IDL-specific service name}
- Authority → ":authority" {virtual host name of authority}
- TE → "te" "trailers" # Used to detect incompatible proxies
- Timeout → "grpc-timeout" TimeoutValue TimeoutUnit
- TimeoutValue → {positive integer as ASCII string of at most 8 digits}
- TimeoutUnit → Hour / Minute / Second / Millisecond / Microsecond / Nanosecond
- Hour → "H"
- Minute → "M"
- Second → "S"
- Millisecond → "m"
- Microsecond → "u"
- Nanosecond → "n"
- Content-Type → "content-type" "application/grpc" [("+proto" / "+json" / {custom})]
- Content-Coding → "identity" / "gzip" / "deflate" / "snappy" / {custom}
- Message-Encoding → "grpc-encoding" Content-Coding
- Message-Accept-Encoding → "grpc-accept-encoding" Content-Coding *("," Content-Coding)
- User-Agent → "user-agent" {structured user-agent string}
- Message-Type → "grpc-message-type" {type name for message schema}
- Custom-Metadata → Binary-Header / ASCII-Header
- Binary-Header → {Header-Name "-bin" } {base64 encoded value}
- ASCII-Header → Header-Name ASCII-Value
- Header-Name → 1*( %x30-39 / %x61-7A / "_" / "-" / ".") ; 0-9 a-z _ - .
- ASCII-Value → 1*( %x20-%x7E ) ; space and printable ASCII

**HTTP/2 API Response Headers**

- Response → (Response-Headers *Length-Prefixed-Message Trailers) / Trailers-Only
Response-Headers → HTTP-Status [Message-Encoding] [Message-Accept-Encoding] Content-Type *Custom-Metadata
- Trailers-Only → HTTP-Status Content-Type Trailers
- Trailers → Status [Status-Message] *Custom-Metadata
- HTTP-Status → ":status 200"
- Status → "grpc-status" 1*DIGIT ; 0-9
- Status-Message → "grpc-message" Percent-Encoded
- Percent-Encoded → 1*(Percent-Byte-Unencoded / Percent-Byte-Encoded)
- Percent-Byte-Unencoded → 1*( %x20-%x24 / %x26-%x7E ) ; space and VCHAR, except %
- Percent-Byte-Encoded → "%" 2HEXDIGIT ; 0-9 A-F

I'm enjoying getting down to the nitty gritty details of how HTTP/2 works. I'm intrigued by the multi-directionality of it. Being able to use just like HTTP/1.1 with simple requests and responses, but also being able to introduce bi-directional API calls, where you can make many different API calls as you want. I don't think I will get any time to play with in the near future. I have way too much work. However, I do like learning about how it is being used, and I think Google is the most forward thinking when it comes to HTTP/2 adoption in the API sector--providing multi-speed APIs in JSON using HTTP/1.1, or Protocol Buffers using HTTP/2.
