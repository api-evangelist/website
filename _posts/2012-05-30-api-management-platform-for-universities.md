---
layout: post
title: "API Management Platform for Universities"
url: 'http://apievangelist.com/2012/05/30/api-management-platform-for-universiteis/'
image: 'http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/blog/UW-Web-Service-Registry.png'
---

[<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/api-evangelist/universities/UW-Web-Service-Registry.png" alt="" width="275" align="right" />][1]

I recently stumbled across the [University of Washington’s Web Services area][2], where they are working to create a single place to learn about, discover and connect with various APIs that are available at the University.

As the home page says:

> _Web Services at the University of Washington is a method of getting important institutional data from and/or into your applications. Web Services are a way for applications or systems to talk to one another and does not usually involve human interaction._

I’m always trying to understand where the next wave of API growth might come from, and while the enterprise is definintely sitting on a treasure chest of information and resources, just waiting to be exposed via APIs--I think Universities might be in the same position.

As soon as Universities start realizing how many APIs they have laying around already, and understand the potential of launching new ones, they are going to have a massive API management problem.

I stumbled across UW APIs via a [ProgrammableWeb][3] update of 7 web services from the University. I started looking around further, and discovered there were 29 total APIs available at UW Web Services. I’m not sure why only 7 are listed at PW, but right there you start seeing slippage in the current API directory model.

Quickly invdividual schools are going to face the same [problems Google has faced with its almost 100 APIs][4] and need to standardize their management platform with:

  * **Access** \- Usage of a healthy balance of keys and OAuth for accessing school and student data 
  * **Discovery** \- Establish some sort of WADL or other discovery service that can feed not just a human directory but IDEs and other programmatic discovery. 
  * **Explorer** \- Provide an API explorer so developers and even non-programmers can make calls against any API without writing code 
  * **Billing** \- Establish some sort of billing layer, if only for making high volume users pay for access and pay for infrastructure--but also possibly opening up new revenue streams for universities

<img class="c2" src="http://kinlane-productions.s3.amazonaws.com/api-evangelist/universities/univeristy-info-systems.jpg" alt="" width="250" align="right" />

In addition to these areas, Universities will have to establish a common set of API building blocks that they will use across all departments, creating a consistent API area for developers to use while learning about and integrating with University Web Services.

With some proper planning and a little work, each University could setup a highly functional API strateg and management framework allowing them to efficiently manage not just dozens of APIs, but thousands across all areas of the University.

Think of the opportunities for students to build out much needed mobile and web applications around school information as part of class projects. The benefits of having self-service interfaces that individual departments can use to get the information they need, as well as for 3rd party vendors who need access to vital school data.

Next, would be to create a state and federal discovery layer on top of each University, allowing better oversight and interaction between government and Universities--but that will have to come later, we have a lot of work to do at each University before we get there.

   [1]: http://webservices.washington.edu/ (University of Washington)
   [2]: http://www.apievangelist.com/2012/05/29/university-information-access-with-apis/ (University of Washingtons Web Services Area)
   [3]: http://www.programmableweb.com (ProgrammableWeb)
   [4]: http://www.apievangelist.com/2011/12/21/business-of-google-apis-2011/ (problems Google has faced with its almost 100 APIs)
