---
published: true
layout: post
title: Thinking About API Status Codes For Destroying Entities Using DELETE
date: 2018-03-12T11:00:00.000Z
tags:
  - API Evangelist
  - Design
  - Status Codes
  - HTTP
image: >-
  https://s3.amazonaws.com/kinlane-productions/deliveroo/deliveroo-new-visual-branding-logo.jpg
---
<p><img src="{{ page.image }}" width="45%" align="right" style="padding: 15px;" /></p>I am pulling together some API design guidance for some projects I'm consulting on, so I'm spending time reviewing the API design guides the leading API providers who have published them publicly. Learning from what they are doing across their own companies, organizations, institutions, and government agencies when it comes to sensible API governance.

Today, I am learning from the British food delivery company, Deliveroo, and documenting [their guidance for which HTTP status codes should be returned for any API methods that use DELETE](https://deliveroo.engineering/guidelines/api-design/#external-facing):

If it exists, it should return status:

- 204 No Content if the entity was successfully destroyed,
- 404 Not Found if the entity does not exist
- 410 Gone if the entity is known to have existed but no longer does.

Additionally 4xx response codes may be used:

- 412 Precondition Failed
- 415 Unsupported if using versioning and the server doesn’t support the specified version.

I have to admit, I haven't been properly publishing status codes any DELETE methods I provide. I've just been returning a 200 if successful, and 404 if it didn't exist. I hadn't put any further thought into the proper way of handling it. I just haven't had the time, or the knowledge within reach to be able to handle properly.

I know that the RESTafarians enjoy debating these finer details of API design, and using HTTP, but for the rest of us, we just need some guidance from y'all. Which is why I spend time learning from existing API leaders who publish their API design guidance, and sharing as individual stories here on the blog, as well as including in my official project consulting guidance.
