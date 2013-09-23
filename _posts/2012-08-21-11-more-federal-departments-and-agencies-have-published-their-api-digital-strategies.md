---
layout: post
title: "11 More Federal Departments and Agencies Have Published Their API Digital Strategies"
url: 'http://apievangelist.com/2012/08/21/11-more-federal-departments-and-agencies-have-published-their-api-digital-strategies/'
image: 'http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/blog/US_white_house_logo.png'
---

<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/api-evangelist/federal-government/US_white_house_logo.png" alt="" width="200" align="right" />

I’ve been running a monitoring script every night, so that I could tell when any of the federal department and agency have launched their digital strategy pages, per [Barack Obamas Presidential directive that every Federal Government agency should have an API][1], and the White House CIO's strategy, entitled "[Digital Government: Building a 21st Century Platform to Better Serve the American People][2]"

I noticed that many of the departments and agencies aren’t properly using HTTP response codes, and when I pulled pages, I often get 302 redirects to 404 pages, so I tended to treat 301, 302, 500 as 404’s. Today, I noticed that some of them actually were redirecting to their digital strategies, published at alternate locations, other than directed by the White House strategy, which was [domain]/digitalstrategy.

Recognizing this I put in some logic to handle redirects and check if it was a valid strategy page, and after re-running the script I found 11 more digital strategies published, bringing the total to 14 to date:

 

 
**Executive Departments or Agencies**
**Digital Strategy**

[<img src="http://kinlane-productions.s3.amazonaws.com/digital-strategy/logos/usda.png" alt="" width="100" />][3]
[Department of Agriculture (USDA)][3]

   [1]: http://blog.apievangelist.com/2012/06/01/barak-obama-directs-all-federal-agencies-to-have-an-api/ (Barack Obamas Presidential directive that every Federal Government agency should have an API)
   [2]: http://www.whitehouse.gov/sites/default/files/omb/egov/digital-government/digital-government-strategy.pdf
   [3]: http://www.usda.gov/
