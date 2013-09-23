---
layout: post
title: "Delivering Value For Developers Is First When It Comes To The Census Bureau APIs"
url: 'http://apievangelist.com/2013/08/22/delivering-value-for-developers-is-first-when-it-comes-to-the-census-bureau-apis/'
image: 'http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/blog/census.png'
---

[<img src="https://s3.amazonaws.com/kinlane-productions/digital-strategy/logos/census.png" alt="" align="right" />][1]

I wrote a piece about [providing a full download vs. API][2] last month, where I used the [Census Bureau API][3] as an example. The post got the attention of the folks at the Census, and they invited me out for a discussion yesterday about their API strategy.

The Census Bureau API team asked me what I thought of their [API developer area][3], and while I have lots of suggestions of where they could do, I first focused on what they have already delivered.

I don't know if you understand the size of the census, but it is a massive undertaking, resulting in data at a scope that we are only seeing matched in the last few years, with the Google's and Twitters of the world--the only difference is the census has been going on since 1790. it gives you an ideas of the serious big data potential behind the Census Bureau API.

Faced with data at this scope, I understand that delivering a simple, web API is not easy. I was impressed with the teams efforts before I came to D.C., but now I'm really impressed that such a simple, web API could be delivered out of such a large government entity. Many other agencies are still trying to even learn what an API is, and even if they do attempt at delivering APIs, the result is often the much more technical cousin of web APIs, SOAP web services.

I totally respect the simple start to the Census Bureau API. The current API landing gives you brief introduction to the API, shows you how to access the data via the URL endpoints, gives you example responses, error codes and addresses what you need to use the APIs in JavaScript. They also give you quick access to getting API keys, a developer forum, application gallery and of course you still get full access to Census downloads.

What a great start. So simple. Giving developers exactly what they need to get going.

Then before I gave my feedback on where they could go next with the APis, the Census team gave me a quick overview of the API road-map, to make sure I wasn't going to suggest anything they were already working on.

I was pleased to hear the Census Bureau API road-map centered around making sure all the public survey data at the Census was accessible via the API for developers. After that, the focus was on making it easier for developers to access, filter and work with all data via the APIs. One of the biggest challenges is that there are hundreds of thousands of fields developers can use when querying the API, and potentially millions of fields when all of it is made available. Opening up the question, how do you educate users that these fields exist, let alone put these fields to use.

I think the Census Bureau API road-map reflects the mission of the Census Bureau, with a focus on:

  * Complete Data Downloads
  * Simple API Interfaces
  * Access to All Public Data
  * Usability for Developers

This approach totally satisfies my number one requirement for all APIs--deliver value. If you focus on delivering value, the rest will work out. Developers will come, and build on that value. The Census team is on the right track with their road-map, dovetailing with any feedback I had brought with me to the meeting:

  * **Value** \- Keep focusing on providing value to developers. Make the data they desire available, make it as easy to access as possible.
  * **Simplicity** \- The key to success will be to keep building on the simple interfaces you've created. Complexity will slow API adoption for developers.
  * **Interactive** \- Look at Swagger, I/O Docs and API Blueprint for approaches to make learning about Census APIs interactive, exploratory and hands-on for developers.
  * **JavaScript** \- Keep up the good work on providing JavaScript resources for integrating with the developers, this will help encourage embeddable tools, single page apps and meaningful visualizations.
  * **Spreadsheets** \- Consider providing spreadsheet integration resources for using Census APIs in Excel and Google Spreadsheets, allowing spreadsheet packages complete with built in graphs, charts and other visualizations. This is a growing trend in the API space and will meet the needs of non-developer users, which will mean massive new adoption.
  * **Landing Page -** Keep the home page simple, but consider surfacing other valuable resources, making everything a developer needs to get started is one click away.

I do not want to overload the Census team with too many ideas, I want to keep my feedback as simple as their initial approach to their API. I had feedback loop on my list before arriving, but the team walked me through their existing feedback loop of partners, advisory groups, conferences, forums, list serves and Twitter. Add me coming by the office regularly, I think they have the feedback loop covered! :-)

In 2013, we are all excited about the potential of big data. I'm excited to see the OG Big Data provider, stepping up to the plate in such a meaningful way. There are some seriously smart people at the Census, and I'm really excited to see what they have coming down the pipeline, and I'm honored that they respect my opinions enough to have me out to the office.

   [1]: http://www.census.gov/
   [2]: http://apievangelist.com/2013/07/19/providing-full-data-download-vs-api/ (providing a full download vs. API)
   [3]: http://www.census.gov/developers/
