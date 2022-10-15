---
published: true
layout: post
title: 'What Is HTTPBin and What Can You Do with the API?'
image: https://kinlane-productions2.s3.amazonaws.com/algorotoscope-master/gears_color-fire-hydrant-water.jpg
tags:
 - HTTPBin
 - HTTP
 - Open Source
---


I recently became the owner of [the request and response service HTTPBin](http://httpbin.org/#/). I am  in exploratory mode regarding what is needed when it comes to the operation of this very interesting API. As with all my work, it helps me to think through the narrative around an API, starting with the basics, then write it up here on the blog to help see the big picture. HTTPBin is an open source HTTP request and response service, which happens to exist as a simple API, that has a whole range of uses, and to help me load up all the details into my brain I wanted to write out the essentials of HTTPBin as derived from the OpenAPI definition that is published to Github.


    
- **HTTP Methods** - Tests different HTTP verbs.
    
- **Authentication** - Tests different authentication methods.
    
- **Status Codes** - Returns different status code.
    
- **Request Inspection** - Inspect the response data like caching and headers.
    
- **Response Formats** - Generates random and dynamic data.
    
- **Dynamic Data** - Generate random and dynamic data.
    
- **Cookies** - Creates, reads, and deletes cookies.
    
- **Images** - Returns different image formats.
    
- **Redirects** - Returns different redirect responses.
    
- **Anything** - Returns anything that is passed to request.
    
- **Form Post** - Allows you to post a form with fields.


When you are first introduced to HTTPBin it can be difficult to wrap your ahead around what is possible. First off, it is kind of a meta API that responds to data you send it, but it is also a reflection of many different aspects of the HTTP specification. It teaches you about the underlying base of APIs while providing an API that is customizable and flexible enough to do an unlimited number of interesting things with it. The HTTPBin API is an “open” API in the sense that you can make calls to it without having to authenticate, but since the API behind is open source, you are also able to fork the code behind the API and run the API anywhere you like. I have used the HTTPBin before, and have been getting more intimate with what is possible, and I know enough to know that my view of what is possible is just the tip of the iceberg, but here are a few:
&#10;
    
- **Education** - The number one value of this API is to teach you about the underlying HTTP dimension of our world.
    
- **Testing** - This API can be used in many different ways to evolve and harden your API testing practices and scripts.
    
- **Automation** - I regularly use HTTPBin to help me automate across APIs using Postman collections and environments.
    
- **Experimentation** - HTTPBin is such a meta API that you can really do interesting things other APIs won’t allow.


We are looking through the issues in the HTTPBin Github repo, evaluating what people have been asking for, and understanding more about how people are putting the API to work. We are just now getting our access to the repo and will be getting to work understanding what is going on, while also beginning to brainstorm what the road map might look like. If you have ideas, please let me know. It really is an interesting project, and I'd love to hear more about how you see things. One aspect of our work will be to share details about the API lifecycle around sustaining, but also evolving the HTTPBin API. For me, this is an excellent opportunity to be very public regarding how APIs can be designed, delivered, and operated, while also providing such an interesting and valuable public API resource for developers to use.