---
layout: post
title: "Automated Documentation for REST APIs"
url: 'http://apievangelist.com/2012/03/08/automated-documentation-for-rest-apis/'
image: 'http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/blog/SDKBridge-logo.gif'
---

[<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/api-service-providers/sdk-bridge/SDKBridge-logo.gif" alt="" width="200" align="right" />][1]

_This post comes from the [SDK Bridge][1] newsletter.  I find so much value from what Peter and Jonathan do over at SDK Bridge, I always have to post their newsletter here and share with all of you._

People are constantly trying to come up with tools to make API documentation an easier task. If you are documenting an SDK built for C , C#, or Java, there are tools such as Doxygen, Sandcastle, and JavaDocs to take comments from the code and automatically generate documentation from them. Why aren't there tools like this for REST APIs?

The beauty of Web APIs is that they can be written in whatever language you like and in whatever manner you like. As long as when an HTTP request comes in, the proper HTTP response goes out, it doesn't matter how it actually happens on the server. But this very flexibility makes automated documentation nearly impossible, since there's no standard mapping between what an API request is and what the code is that generates its response.

Nonetheless, there are some solutions out there to this problem. I need to start by saying that there are in fact two approaches to automation that are used to document REST APIs. One is similar to the tools I mentioned above, where comments are taken from code to generate the documentation. The other involves having the documentation separate from the code, but in a data format (such as JSON) that can be parsed and used to generate the documentation.

I also should mention that documentation automation does not guarantee good documentation. Before choosing to to incorporate automation into your process, I recommend reading an excellent article by Dana Fujikawa: [What to Consider Before Considering Auto-Generated Documentation][2].

###  Automated Documentation from Code

There's no off-the-shelf tool that pulls documentation comments out of code that's going to work for all REST APIs. But there are two possible solutions:

  1. Use a framework that both generates the APIs and the documentation
  2. Create methods with a one-to-one mapping with API requests.

**Framework.** A good example of a REST API framework is [Enunciate][3]. Enunciate is an open-source Java-based Web API framework. It creates full HTML documentation of the services it generates, where the documentation is assembled from JavaDocs comments.

**Mapping.** Mapping requires some disciplined practices, but has the advantage that it can be used with any technology. In this case, you need to create public methods that map directly to API requests. So, for example, you might have an API request to get a brief user profile for a user with an ID of 23423 with a call like this:

`GET `

When this request comes in, you need to structure your code so that it calls a method by the name of something like:

`public get_users__id__profile(int id, string profile_type)`

Note that the `id` is surrounded by double underlines, indicating that it is not literally the text "id".

This method would then have comments that could be picked up by automated tool, such as JavaDoc, RDoc, or Sandcastle, and HTML documentation would be generated. Then you would need to run the HTML documentation through an automated process that would remove unnecessary information (such as class names), and convert the method names, replacing single underlines with slashes and double underlines with slashes and brackets so that

`public get_users__id__profile`

would become

`GET /users/{id}/profile`

The parameters table would also need some modification so that it's clear which parameters are part of the URL and which are query parameters.

It's not a simple process, but I have seen it done successfully using Ruby code and [RDoc][4].

###  Automated Documentation from Structured Data

The advantage of taking comments from code is that if there are changes in the code, the comments are more likely to be updated. However, a simpler and very flexible solution is to have the documentation in structured data (JSON or XML), and then have an automated process create the actual HTML documentation from it. There are a several tools that will do this, merging documentation with an ability to try out the REST calls, which is extremely handy. Here are some examples.

[Swagger][5]. Swagger is a tool created by Worknik that creates very nice looking API documentation with the ability to easily try any API request. You specify a resource discovery URL which returns JSON with information about the various REST resources, then for each resource, you specify the type of operation, the path, the potential errors, and the response. Although you are limited in how long your descriptions can be, it creates a very nice documentation system for straight-forward APIs.

[I/O Docs][6]. I/O Docs is a tool created by [Mashery][7] that is very similar to Swagger. The big difference is that it is open source. Written in JavaScript, the source is available on github, which means that you can taylor it to your own needs, as well as look-and-feel.

**Create your own**. If neither of these tools are flexible enough for your API, you can create your own. A beautiful implementation that I had the priviledge to work on was created by [Tendril][8]. Take a look at an example API request at [Cost and Consumption for a Single Device][9]. You can see how you can try it out on the first tab, but then other tabs list parameters, response, and notes. By creating their own system, they were able to document a fairly complex API call which would not have worked with an off-the-shelf system.

###  Conclusion

Automated REST API documentation can be used to:

  * Keep the documentation near the code so that it's easier to update.
  * Allow developers to try out of the API requests as part of the documentation.

Although it is impossible to have a tool that automatically generates REST API documentation from any code, there are a number of approaches that will let you autogenerate the documentation, including:

  * Using a framework that generates both the API code and its documentation.
  * Creating a mapping between methods and API requests and using standard documentation tools.
  * Writing documentation as structured data and generating HTML from it.

   [1]: http://sdkbridge.com/ (SDK Bridge)
   [2]: http://sdkbridge.createsend1.com/t/r/l/dyiukjk/hdhyyhjli/t/
   [3]: http://sdkbridge.createsend1.com/t/r/l/dyiukjk/hdhyyhjli/i/
   [4]: http://sdkbridge.createsend1.com/t/r/l/dyiukjk/hdhyyhjli/d/
   [5]: http://sdkbridge.createsend1.com/t/r/l/dyiukjk/hdhyyhjli/h/
   [6]: http://sdkbridge.createsend1.com/t/r/l/dyiukjk/hdhyyhjli/k/
   [7]: http://sdkbridge.createsend1.com/t/r/l/dyiukjk/hdhyyhjli/u/
   [8]: http://sdkbridge.createsend1.com/t/r/l/dyiukjk/hdhyyhjli/o/
   [9]: http://sdkbridge.createsend1.com/t/r/l/dyiukjk/hdhyyhjli/b/
