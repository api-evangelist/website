---
published: true
layout: post
title: 'API Ecosystem Building Blocks – SMTP, POP, HTTP, CSV, and Stripe'
image: https://s3.amazonaws.com/kinlane-productions2/algorotoscope-master/yellow-journalism-gargoyle-paris.jpg
author:
    name: kinlane
tags:
- POP
- SMTP
- Substack
- Fascism
- Migration
- CSV
- Stripe

---
<a href="https://2ndbreakfast.audreywatters.com/leaving-substack-again/">My wife recently moved off of Substack</a>. She was run off by their <a href="https://substack.com/@hamish/note/c-45811343?utm_source=notes-share-action&r=bgg2">support of fascism on their platform</a>, and was in real need of supporting her 1,300+ subscribers. I was impressed with her way of handling the research, planning, and ultimate migration of her newsletter operation, and found the pragmatic API story there to be one worth telling. While I think REST, GraphQL, gRPC, and other event-driven approaches to APIs will continue to dominate the enterprise API landscape, I can’t help but feel her pragmatic real world needs and solutions will continue to shape the consumer API experience. 

The decision my wife faced with Substack is one many individuals and businesses will have to make over and over while trying to get work done on a daily basis. My wife just needed a quality email newsletter solution to build her network of subscribers. She has accumulated a mix of 1300 free and paid subscribers, and has a serious newsletter-driven health and fitness technology network developing. She doesn’t need Substack’s politics and network filtering philosophy to get in the way of her business. I purposely didn’t choose Substack for my email newsletter solution because they didn’t have an API, but she didn’t let the absence of an API stop her from moving to another platform.
The OG APIs - SMTP & POP

Email has long been used as an API, and I must say that my wife’s migration has made me realize the business and political power of using email as a delivery platform for your applications. The fact that her primary delivery mechanism was via SMTP allowed her to retain control over her audience when she migrated. That is some powerful juju. It is easy to take email for granted, but she couldn’t switch her audience from Twitter or any other platform because they consumed her work via platform controlled applications. Email newsletters leverage a standardized messaging API to deliver content and data to consumers via the email client of their choosing, relying on the inbox to act as the application interface. The fact that my wife’s subscribers are engaged via email allows her to take them with her, leveraging SMTP to migrate her business from Substack to a new platform.
CSV Export and Import

Next, to migrate her subscribers out of Substack and into her new email newsletter platform, my wife exported CSV files out of Substack and imported them into the new platform. Once again leveraging a proven API (HTTP + CSV) to retain control over your valuable data—in this case it was an email newsletter subscriber list. Substack made a decision to not have an API, likely due to competitive reasons, but did feel compelled to provide users with a way to get their data out. Something their competitors still took advantage of, by offering a streamlined way to import Substack CSV exports easily. In my book, CSV downloads are an API. They are accessing a standardized machine-readable format via HTTP, utilizing common authentication and authorization methods. Like email, I think the pragmatic approach to utilizing CSV files for migrating systems is worthy of evaluating further.
Stripe Payments API

The remaining piece of the puzzle that would allow my wife to migrate her paid subscribers off Substack to her new email newsletter platform, was the fact that Substack uses Stripe. Because of common payment industry practices combined with the dominance of Stripe as a payment API provider, Substack doesn’t own the payment relationship my wife has with her paid subscribers—they just take a percentage of the action. All she has to do is sever this relationship, and either reroute to the new platform or maintain 100% of the subscriptions herself. While the role of the Stripe API is very different than the role that SMTP, POP and CSV played in this migration, I think it says a lot about the role that leading API providers can play in standardizing sectors of our economy, I guess letting the market truly work things out in ways that maybe the power players in the market didn’t anticipate. 
SMTP, CSV, and Stripe APIs

I am a big fan of simplicity. This is why I think REST APIs will continue to dominate. However I think that SMTP and CSV represent cornerstone API patterns that we ignore at our own peril. While most of us dislike our inboxes, email is an accepted aspect of mainstream life. CSV, while not as structured as JSON affords, gets the job done in 80% of the situations. The ease of use and market dominance of Stripe helps complete the migration and interoperability picture we need. While this approach to migration will not work in all application situations, for the email newsletter use case it is worth noting. Honestly I think that SMTP, POP, IMAP, HTTP, and CSV are like the essential building blocks of the API economy, with JSON as the runner up when it comes to meaningful protocols.

While I think my wife is a little more sophisticated in her business approach to IT, I think it represents a pretty pragmatic view of how things will play out when it comes to the business model and fascist fueled chaos that is regularly occurring across the web and will only continue to grow. While I’d like all API providers to have APIs with standardized authentication and authorization, I’ll take interoperability via existing cornerstone protocols and providers. I am thinking I will write up the approach my wife took as a blueprint, not just for others to follow when it comes to migrating from Substack, but one way to consider when it comes to migrating off any platform, as well as where government regulators should look when it comes to forthcoming regulations to help tame the chaos and exploitation across everything the web and APIs are touching today.