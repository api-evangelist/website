---
layout: post
title: "Widget Builder Environment for APIs"
url: 'http://apievangelist.com/2011/06/22/widget-builder-environment-for-apis/'
image: ''
---

[<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/api-evangelist/apigee-api-console.jpg" alt="" width="250" align="right" />][1]There are many tools out there for working with Web APIs, but the one I am seeing used more and more is an API explorer. API explorers allow users to make calls and explore REST APIs using a Web interface -- all without writing code.

These [API explorers][2] are making it a lot easier for developers to discover, learn, and integrate with Web APIs. I also think they have a lot more potential, beyond the developer community.

Non-developers can use an API explorer to make calls against an API, retrieve JSON, and then use tools like Google Spreadsheets to process responses, building visualizations, and so on.

There is a huge opportunity for API explorer providers to tap into the larger, non-developer community, and one of the easiest ways to do this may be by adding a widget layer to their applications.

An API widget builder would have similar features to the [Integrated Development Environment (IDE) for APIs][3] I proposed last week:

  * **API Discovery** \- Allowing users to discover and select pre-defined selection of RESTful APIs
  * **Authentication** \- Enable HTTP Basic and oAuth authentication with APIs
  * **Services** \- Render full list available services for selected API
  * **Request / Responses** \- Allow for building requests, manually sending, and seeing fresponses for selected API
  * **Github Integration** \- Allow adding and connecting to both private and public Github repositories
[<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/api-evangelist/wolfram-alpha/wolfram-alpha-widget-builder.png" alt="" width="250" align="right" />][4]Then I would add a new layer to the environment:

  * **Widget Builder** \- Provide tools for widget discovery, creation, connecting to APIs, configuration, sandbox, and copy / paste embeddable code for syndication.
  * **Export Tools** \- Ability to export any API responses to Google Spreadsheet, Microsoft Excel, Comma Separate or Tab Separated values.
With this type of environment, non-technical users could easily connect to APIs, mash-up responses and build widgets for embedding in their presentations, web sites, applications, and mobile devices.

There are a couple of widget building platforms out there like [Sprout Inc][5] or [Widgetbox][6], but I'm picturing something more like [WolframAlpha's widget builder][7]. Take [Apigee Console][1] and add a widget builder like WolframAlpha's, and I think you'd have something close to what I'm envisioning.

I hope some existing API service provider or IDE developer sees the opportunities within the API space and builds a developer IDE and widget builder for APIs.

######  Related articles

  * [Deploying Smarter API Documentation][8] (apievangelist.com)
  * [Integrated Development Environment (IDE) for APIs][9] (apievangelist.com)
  * [New Widgets and Graph-like API Expands LinkedIn's Reach][10] (programmableweb.com)
  * [LinkedIn API Platform and the Evolution of the API][11] (apievangelist.com)

   [1]: http://apigee.com/about/products_togo.html (Apigee Console)
   [2]: http://blog.apievangelist.com/2011/03/24/explorers-open-api-access-beyond-developers/ (API explorers)
   [3]: http://blog.apievangelist.com/2011/06/18/integrated-development-environment-ide-for-apis/ (Integrated Development Environment (IDE) for APIs)
   [4]: http://developer.wolframalpha.com/widgetbuilder/ (WolframAlphas widget builder)
   [5]: http://sproutinc.com/ (Sprout Inc)
   [6]: http://www.widgetbox.com/overview/ (Widgetbox)
   [7]: http://developer.wolframalpha.com/widgetbuilder/ (WolframAlphas Widget Builder)
   [8]: http://blog.apievangelist.com/2011/06/17/deploying-smarter-api-documentation/
   [9]: http://blog.apievangelist.com/2011/06/18/integrated-development-environment-ide-for-apis/
   [10]: http://blog.programmableweb.com/2011/04/15/new-widgets-and-graph-like-api-expands-linkedins-reach/
   [11]: http://blog.apievangelist.com/2011/04/13/linkedin-api-platform-and-the-evolution-of-the-api/
