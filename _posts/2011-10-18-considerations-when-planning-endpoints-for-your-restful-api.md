---
layout: post
title: "Considerations When Planning Endpoints for your RESTful API"
url: 'http://apievangelist.com/2011/10/18/considerations-when-planning-endpoints-for-your-restful-api/'
image: 'http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/blog/Tag-Cloud-REST-URL.png'
---

<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/api-evangelist/Tag-Cloud-REST-URL.png" alt="" width="325" align="right" />

Someone asked me recently for some advice regarding what they should consider when constructing the URL and endpoints for their RESTful API.  I thought I’d share the advice I passed along.

I don't intend this to be a comprehensive guide to building URLs for a true REST API, just some things to consider for the newbie API product manager who may not have a hardcore REST developer on their team.

When planning your endpoints for a RESTful API, there are 3 things I tell people to consider:

  * **Domain** \- Put your API at a separate domain or sub-domain than your website.  It will make it easier to migrate and scale, and your IT team will thank you.  For example: 
    * 
  * **Versioning** \- Make sure and consider the versioning of your API in your URL structure.  How you version will depend on the preferences of your dev team, the most common patterns I see are a v preceding the version number of your API or using year and month of the version.  How often you release may impact your decision.  For example:
    * [https://api.yourdomain.com/v1/][1]
    * [https://api.yourdomain.com/2011/11/][2]
  * **Resources** \- The next part of your URL should be the resource of what you are offering.  Make it self-describing of the resource you are offering through the endpoint.  Make it reflect what a developer is looking to consume when using your API.  For example:
    * [https://api.yourdomain.com/v1/article/][3]
    * [https://api.yourdomain.com/v1/user/][4]

How you define your API resources is very important, its something you will have to live with forever.  Make your resource descriptions count, your developers will thank you.

The other thing I strong urge is to offer SSL for your API from day one.  Its not a huge problem down the road, but any change will come with issues, and many of your developers will request and even require SSL in some cases, before they integrate with your API.

That is all the general advice I have, how you describe your resources is up to you, and how RESTful you make the rest of your API is up to your dev team.  I don't get involved in the religious REST arguments, I leave that for the experts.  I just wanted share some of the common things you should consider when constructing your URL endpoints.

Let me know anything I'm missing you REST geeks!

   [1]: https://api.peoplebrowsr.com/v1/
   [2]: https://api.peoplebrowsr.com/2011/11/
   [3]: https://api.yourdomain.com/v1/articles/
   [4]: https://api.yourdomain.com/v1/users/
