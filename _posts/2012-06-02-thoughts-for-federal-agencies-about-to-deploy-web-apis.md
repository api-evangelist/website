---
layout: post
title: "Thoughts For Federal Agencies About to Deploy Web APIs"
url: 'http://apievangelist.com/2012/06/02/thoughts-for-federal-agencies-about-to-deploy-web-apis/'
image: 'http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/blog/Building-a-21st-century-platform-to-better-serve-the-american-people-1.png'
---

[<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/api-evangelist/federal-government/Building-a-21st-century-platform-to-better-serve-the-american-people-1.png" alt="" width="250" align="right" />][1]

I wanted to publish some thoughts, on what Federal Agencies responding to the [Executive Order 13571][2] issued on April 27, 2011, and the White House CIO’s, "[Digital Government: Building a 21st Century Platform to Better Serve the American People][3]" strategy should be considering.

These thoughts are in the business and marketing aspects web API deployment, with light thoughts in the technical areas. My speciality is not with technical deployment of APIs, I recommend agency leaders visit [API-Craft][4], an industry forum with some seriously smart API industry leaders discussing the finer, technical points of web API deployment.

Where I would like to share some thoughts is in the business of deploying and managing Federal Agency APIs. Insights evolved over 20 years in the technology field, but exclusively spending the last 2 years studying the business of popular APIs like Twitter and Facebook, and larger API providers like Google and Amazon Web Services.

I’m sharing my thoughts, not to benefit any company, but because I strongly believe in the transformative powers of Web APIs. Web APIs have the power to change the way our Government operates both internally, and with the public. Barack Obama’s mandate, “requiring agencies to establish central online resources for outside developers and to adopt new standards for making applicable Government information open and machine-readable by default”, marks an important point in history.

We can’t screw this up!

While much of the discussion around this announcement on [Twitter][5], [Reddit][6] and [Hacker News][7] is positive, there is a lot of skepticism around whether the government can succeed. With this post, I wanted to share some thoughts on the essential building blocks we’ll need to make this work.

**Technical Building Blocks
**I will only speak lightly on essential technical building blocks that need go into Federal Agencies Web APIs, but there are a couple I consider essential:

  * **Access** \- Idenitying proper access levels for web APIs, leaving open when possible, requiring keys when needed and implementing oAuth when it makes sense give users control over which applications access their data
  * **REST** \- The dominant approach to deploying web APIs, building on top of the existing structure of the World Wide Web. REST has proven to robust enough for most any web API while keeping it simple and intuitive for access by a wide audience
  * **JSON** \- I’m not advocating for getting rid of XML, but JSON is the accepted standard for API communication. JSON needs to be adopted as the default for federal agency web APIs

There are plenty of other technical considerations, but I’ll leave that for other experts to deliver on.  Next lets get users, onboarded and using each agencies APis.

**User Onboarding
**There are a lot of challenges for the average web API developer faces when trying to integrate, initial onboarding has to be quick and painless. There are a couple of essential building blocks that assists in user onboarding:

  * **Landing Page** \- A single landing page for everyone to access federal agency APIs, providing single click access to everything you need to get up and running with the API
  * **Self-Service** \- API access needs to be self-service, enabling anyone to discover and integrate 24 / 7 without assistance from any agency staff
  * **Account Management -** Allow users to quickly register using common single sign-on using my Twitter, Facebook or Google accounts, and provide users with easy to understand account, key, application and API usage management tools

Next for a developer to successfully go from onboarding to, API integration, it will require an essential set of resource building blocks providing everything they need to understand the API interface, and begin using:

  * **Authentication** \- Give users a quick introduction to API access including which endpoints are open, keyed or require oAuth for usage. Also provide links to support technical information about authentication
  * **Documentation** \- Provide simple, complete and up to date documentation for every Web API endpoint.  Also consider deploying interactive, smart documention using a technology like Swagger
  * **Code Samples** \- Provide sample code for each API endpoint in all the common languages including PHP, Python, Ruby, .NET, Perl, Java, Objective-C, all provided as Github repositories
  * **Starter Kits -** Provide as many ready to code sample applications and starter kits to show developers what is possible, all provided as Github repositories
  * **Mobile** \- Provide mobile specific code samples, SDKs and other resources supporting mobile specific development

After you’ve provided the essential technical, onboarding and resource building blocks, you need to make sure your your agencies API area has the necessary communication building blocks, allowing you to effectively communicate with users about your API, but also give your users a voice in API operations:

  * **Blog** \- A blog is an essential communication tool in API ecosystems. Make sure the blog is active, and provides an RSS feed
  * **Forum** \- A forum will provide a platform for you to communicate back and forth with API users, providing a rich knowledge for future users, and also opening up the possibility of users helping other users
  * **FAQ** \- Provide a simple, realistic and complete list of the most frequently asked questions. Also keep it a living list, truly reflecting which questions get asked every month
  * **Contact** \- Establish some way users can directly contact the agency for support
  * **Twitter** \- An active Twitter account is a required communication tool
  * **LinkedIn** \- A presence on the top business social network is important
  * **Facebook** \- An active page on Facebook helps with communication
  * **Google ** \- Google's social network can help with developer interaction

With proper communication building blocks in place, next make sure and address the legal considerations around the web API:

  * **Terms of Use** \- Clearly let users know what is expected when they access the agencies web APIs
  * **Privacy** \- Establish clear privacy policies for all people and companies involved
  * **Licensing** \- Provide data, API interface and code licensing for everyone to see

With legal expectations set, make sure and think about branding for the agency. While these web APIs are the federal government, for them to be successful, the word needs to get out that our government does such a find job making data available. There are some common API branding building blocks emerging to accomplish this:

  * **Branding Requirements** \- Establish a base understanding of how to properly attribute the agency in compliance with overall usage requirements
  * **Logo** \- Provide a single place to find a selection of approved graphical logos and HTML or JavaScript code snippets users can use when adhering to branding requirements

After baking in some user implemented marketing for the agency, with API branding, make sure and provide some operational building blocks that help API users understand what is going on with the agencies APIs and where they are going:

  * **Roadmap** \- Give users a clear roadmap of where the agency is going with it’s digital strategy, providing insight as far in the future as possible
  * **Changelog** \- Provide a real-time list of changes made to the API and its supporting building blocks

Providing real-time communication on your API operations is important to establishing trust with developers. If you just make it part of your daily operations, it isn't that much more work.

**Non-Developers**
While planning the digital strategy for your agencies web API make sure and consider non-developers. One reason for the success of web APIs is that it uses REST, which uses the technology driving the existing World Wide Web, making RESTful APIs potentially familiar to non-developers. With the right building blocks, web APIs become accessible to a wide variety of users:

  * **Embeddable** \- Buttons, widgets and badges that are provided on top of a web API provide a copy and paste method for non-developers to quicky make use of the data and information available via an API
  * **Media** \- Provide a section dedicated to media, helping media on two fronts 1) to understand what an API does in plain english 2) to put a web API to potential use in their data journalism efforts
  * **Educational** \- Provide information and resources that facilitates API usage by any level of academic research and projects
  * **Platforms ** \- With introduction of Google Docs, Google Big Query and other big data processing solutions, the opportunity for API integration on these platforms is growing. Provide templates for using agency APIs within these platforms

Everything suggested up until now, truly supports a digital approach, to each agencies digital strategy, but in these environments, the need for face to face and human interaction can be critical to building understanding, awareness and ultimatley a community around a web API.

**Events**
Events are a great way to build awareness around an API, there are several common event building blocks that are used in the industry:

  * **Annual Conference** \- Establish an annual event where each API stake holder and any user can rub elbows and share their thoughts about web APIs
  * **Road Show -** Develop a road show that goes from city-to-city, providing a town hall format for understanding each agencies digital strategy
  * **Meetups** \- Attend existing developer meetups and gathers that are already occuring in cities around the country
  * **Hackathons** \- Sponsors, attend and put on hackathons that encourage hacking around federal agency APIs

I think that represents my thoughts on the essential API building blocks federal agencies should consider while formulating their digital strategy. The only other area I would offer more details on, is around API evangelism and developer advocacy. Who will be in charge of getting the word out about an API? Will this be a single person or shared responsibility? An API Evanglism strategy is critical to the success of an API, but I think I will cover that in another post.

Scrolling back up the page, this seems like a lot, and potentially counter to my wishes that we start simple and make sure this is a success. My goal with these thoughts is to provide a potential business framework that could be adopted across all agency deployments.

These building blocks are derived from reviewing the API operations of hundreds of existing public APIs, including industry heavyweights like Google and Amazon. While some APIs like Twitter deal with API management at massive scale, Google and Amazon provide models for managing large numbers of web APIs.

Make sure and spend some time and look at how Google or Amazon is organizing their developer community.  If any developer could go to any of the over 100 agencies, or the over 1000 domains, and find a consistent experience shared across **ALL** agency web API areas, like they do at Google or Amazon APIs, the chances for success of this iniative is much greater.

I hope someone in one of the agencies reads this, and understands the importance of this moment, and that an API is more than just a CSV or XML dump at a web address. That, with the right business approach to deploying and managing we can truly transform how government interacts both internally, inter-agency and with the public. Opening up the federal government to a whole new era of democratic participation, government transparency and interoperability.

   [1]: http://www.whitehouse.gov/sites/default/files/omb/egov/digital-government/digital-government-strategy.pdf
   [2]: http://www.gpo.gov/fdsys/pkg/FR-2011-05-02/pdf/2011-10732.pdf
   [3]: http://www.whitehouse.gov/sites/default/files/omb/egov/digital-government/digital-government-strategy.pdf (Digital Government: Building a 21st Century Platform to Better Serve the American People)
   [4]: https://groups.google.com/forum/?fromgroups#!forum/api-craft (API-Craft)
   [5]: https://twitter.com/search?q=http://blog.apievangelist.com/2012/06/01/barak-obama-directs-all-federal-agencies-to-have-an-api/ (Twitter)
   [6]: http://www.reddit.com/r/programming/comments/ughx0/barack_obama_directs_all_federal_agencies_to_have/ (Reddit)
   [7]: http://news.ycombinator.com/item?id=4056310 (Hacker News)
