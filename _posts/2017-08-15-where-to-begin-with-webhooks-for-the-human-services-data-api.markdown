---
published: true
layout: post
title: Where To Begin With Webhooks For The Human Services Data API
date: 2017-08-15T09:00:00.000Z
tags:
  - API Evangelist
  - Webhooks
  - HSDS
  - HSDA
image: 'https://s3.amazonaws.com/kinlane-productions/webhooks/RESTHooks.png'
---
<p><a href="https://www.slideshare.net/progrium/web-hooks-and-the-programmable-world-of-tomorrow-presentation/21-REST_Hooksrest_and_web_hooks"><img src="https://s3.amazonaws.com/kinlane-productions/webhooks/RESTHooks.png" align="right" width="40%" style="padding: 15px;" /></a></p>I am getting to work on a base set of webhook specification for [my human services data API work](http://org.open.referral.adopta.agency/), and I wanted to take a fresh drive through a handful of the leading APIs I'm tracking on. I'm needing to make some recommendations regarding how human services data APIs should be pushing information via APIs, as we as providing APIs. Webhooks are fascinating to me because they really are just APIs in reverse. Webhooks are just an API request, where the target URL is a variable, allowing an API call to be made from a platform, to any target URL, on an triggering events, or on a schedule as a job.

Here are six of the API providers I took a look at while doing this webhook research:

- [**Box**](https://developer.box.com/v2.0/docs/getting-started-with-webhooks-v2)
- [**Gumroad**]([https://gumroad.com/webhooks)
- [**Venmo**](https://developer.venmo.com/docs/webhooks)
- [**Github**](https://developer.github.com/webhooks/)
- [**Stripe**](https://stripe.com/docs/webhooks)
- [**Slack**](https://api.slack.com/incoming-webhooks)

All of these API providers offer webhooks, allowing developers to create an API call that will be fired off when a specific event occurs. These events are usually tied to a specific object. Box is documents. Github is a repository. Stripe is a payment. With human services it will be an organization, location, or service. There are a handful of key concepts at play when it comes to webhooks, making them an important part of the equation:

- **Object** - The object in which an event is occurring. For this project it is organizations, locations, services, contacts, and potentially other elements of API operations.
- **Events**  - This is a list of events that can occur against all the objects that will trigger the execution of a webhook.
- **Target** - The URL of the webhook. This is the variable of the outgoing API call, allowing them to be defined by API consumers, nd executed by the API provider.
- **Fat** - The webhook will carry a payload, submitting a predefined schema, usually of the associated object to the target.
- **Ping** - The webhook does not carry a payload, simply pinging the target of a webhook, letting API consumers know an even has occurred.
- **Status** - The ability to identify the status of a webhook.
- **Errors** - The errors that should be returned as part of webhook execution, and shared as it's status.
- **Retries** - Allowing for webhook execution to be replayed, executing a specific event that occurred in the past.
- **Signatures** - Allowing for the signature of each webhook request to be verified for security and integrity purposes.
- **Test** - Enable API cnosumers to test a webhook and see if it will work, sending over real or sample data.
- **History** - Providing a complete history of webhook execution for API consumers to search, browse, and review.

The external focus, and their event based nature are the most notable characteristics of a webhook, but it is the transactional nature of their supporting systems that seem to make them such a utility that can help alleviate the load on APIs. There are a number of other characteristics of webhooks, but this gets at the core of what they do, and provide me with what I need to move my human services API conversations forward. I'm looking to have a handful of examples of webhook implementations for well-known API platforms to share with folks, and begin setting the stage for an initial API design and definition for a human services webhook implementation, based upon common practices already in use.

I find webhooks interesting because are not a standard, and there really aren't much in the way of best practices. Just some common examples of how they are used by existing API providers. Webhooks are just APIs. It is just the target URL that is variable, and the objects and events that can be unique to each API platform. In human services implementations I don't just see webhooks as being about making API calls to other applications. I see webhooks as something that can satisfy pushing of data between many different API implementations, beginning to set the stage for interoperability between hundreds or even thousands of human service providers, pushing and pulling data as needed, and prescribed by each API provider. Allowing human service providers to speak a common language and seamlessly share information across a variety of partnerships. Getting closer to Greg Bloom's vision, the creator of [Open Referral](http://openreferral.org), and the person behind the Human Services Data Specification (HSDS), for how all of this should be working.

**Photo Credit: **[REST and webhooks are two sides of the same coin. In “Web Hooks and the Programmable World of Tomorrow“, Jeff Lindsay, October 2008](https://www.slideshare.net/progrium/web-hooks-and-the-programmable-world-of-tomorrow-presentation/21-REST_Hooksrest_and_web_hooks)
