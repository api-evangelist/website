---
title: Studying How Providers Are Supporting Batch API Requests
date: 2017-05-17 12:00:00 Z
tags:
- Batch
- Design
image: https://s3.amazonaws.com/kinlane-productions/bw-icons/bw-bulk-requests.png
---

<p><img style="padding: 15px;" src="https://s3.amazonaws.com/kinlane-productions/bw-icons/bw-bulk-requests.png" align="right" width="35%" /></p>

A recent addition to my API research is the concept of making batch API requests. I was reminded of this during [a webinar I did with Cloud Elements when they cited batch API requests as an area needing improvement in their State of API Integration report](http://resources.cloud-elements.com/presentations-2/the-state-of-api-integration-webinar-slides). I had also recently come across several batch APIs while profiling the Google API stack, so I already had the topic in my notebook, but Cloud Element pushed me to add the topic to my research.

Here are a handful of batch API implementations I am working through, to better understand how providers are approaching the problem:

[Facebook Graph API](https://developers.facebook.com/docs/graph-api/making-multiple-requests)
[Google Cloud Storage](https://cloud.google.com/storage/docs/json_api/v1/how-tos/batch
[Full Contact](https://www.fullcontact.com/developer/docs/batch/)
[Zendesk](https://developer.zendesk.com/blog/from-100-requests-to-1-introducing-our-new-bulk-and-batch-apis)
[SalesForce](https://developer.salesforce.com/docs/atlas.en-us.api_rest.meta/api_rest/requests_composite_batch.htm)
[Microsoft Office](https://dev.office.com/sharepoint/docs/sp-add-ins/make-batch-requests-with-the-rest-apis)
[Amazon](http://docs.aws.amazon.com/AWSECommerceService/latest/DG/BatchandMultipleOperationRequests.html)
[MailChimp](https://developer.mailchimp.com/documentation/mailchimp/guides/how-to-use-batch-operations/)
[Meetup](https://www.meetup.com/meetup_api/docs/batch/)

As I do, in my approach to API research, I will process the common patterns I come across in each of these implementations, then add as building blocks in my [API design research](http://design.apievangelist.com/), hopefully providing some details API providers can consider early on in the API lifecycle. I'm not looking to tell people how to deliver batch APIs--I am just looking to shine a light on how the successful APIs are already doing it.

I feel like batch APIs are a response to more APIs, and less direct database access or full data download availability. While modular, simple APIs that do one thing well works in many situations, sometimes you need to move large amounts of resources around and make API requests that do more than just update a single resource or database record. I'll file this research under [API design](http://design.apievangelist.com/), but I'll migrate make a mention of it at the [database](http://database.apievangelist.com/) and other levels, as I identify the variances in how bulk API requests are being made and the solutions they are providing.