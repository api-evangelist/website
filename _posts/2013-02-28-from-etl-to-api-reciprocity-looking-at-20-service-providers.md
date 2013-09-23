---
layout: post
title: "From ETL to API Reciprocity, Looking at 20 Service Providers"
url: 'http://apievangelist.com/2013/02/28/from-etl-to-api-reciprocity,-looking-at-20-service-providers/'
image: 'http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/blog/reciprocity-trends.png'
---

[<img src="https://s3.amazonaws.com/kinlane-productions/api-evangelist/trends/reciprocity-trends.png" alt="" width="300" align="right" />][1]

I spent time this week looking at 20, of what I’m calling [API reciprocity providers][2], who are providing a new generation of what is historically known as ETL in the enterprise, to connect, transfer, transform and push data and content between the cloud services we are increasingly growing dependent on.

With more and more of our lives existing in the cloud and via mobile devices, the need to migrate data and content between services will only grow more urgent. While ETL has all the necessary tools to accomplish the job, the cloud democratized IT resources, and the same will occur to ETL, making these tools accessible by the masses.

There are quite a few ETL solutions, but I feel there are 3 solutions that are starting to make a migration towards an easier to understand and implement vision of ETL:

[<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/serviceproviders/cloveretl-logo.png" alt="" width="160" />][3]
[<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/serviceproviders/snaplogic-logo.png" alt="" width="160" />][4]

[<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/serviceproviders/talend-logo.png" alt="" width="160" />][5]
 

These providers are more robust, and provide much of the classic ETL tools the enterprise is used to, but also have the new emphasis on API driven services. But there are 10 new service providers I’m calling reciprocity platforms, that demonstrate the potential with offering very simple tasks, triggers and actions that can provide interaction between two or more API services:

[<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/serviceproviders/IFTTT-logo.jpeg" alt="" width="160" />][6]
[<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/serviceproviders/factor-io-logo.png" alt="" width="160" />][7]

[<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/serviceproviders/zapier-logo.png" alt="" width="160" />][8]
[<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/serviceproviders/Temboo-Logo.png" alt="" width="160" />][9]

[<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/serviceproviders/foxweave-logo.png" alt="" width="160" />][10]
[<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/serviceproviders/elasticio_logo.png" alt="" width="160" />][11]

[<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/serviceproviders/rules-io-logo.jpeg" alt="" width="200" />][12]
[<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/serviceproviders/itduzzit-logo.png" alt="" width="110" />][13]

[<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/serviceproviders/We-Wired-Web-Logo.png" alt="" width="200" />][14]
[<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/serviceproviders/Ritc-logo.png" alt="" width="120" />][15]

I consider reciprocity an evolution of ETL, because of three significant approaches:

  * **Simplicity** \- Simple, meaningful connections with transfer and tranformations that are meaningful to end users, not just a wide array of ETL building blocks an IT architect has to implement
  * **API** \- Reciprocity platforms expose meaningful connections users have the cloud services they depend on. While you can still migrate from databases or file locations as with classic ETL, reciprocity platforms focus on APIs, while maintaining the value for end-users as well as the originating or target platforms
  * **Value** \- Reciprocity focus on not just transmitting data and content, but identifying the value of the payload itself and the relationships, and emotions in play between users and the platforms they depend on

This new generation of ETL providers began the migration online with [Yahoo Pipes][16]. Which resonated with the alpha developers looking to harvest, migrate, merge, mashup and push data from RSS, XML, JSON and other popular API sources--except Yahoo lacked the simplicity necessary for wider audience appeal.

While I feel the 10 reciprocity providers isted above represent this new wave, there are six others incumbents trying to solve the same problem:

[<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/serviceproviders/automateit-logo.png" alt="" width="160" />][17]
[<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/serviceproviders/cloudwork-logo.png" alt="" width="160" />][18]

[<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/serviceproviders/mashablelogic-logo.jpeg" alt="" width="160" />][19]
[<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/serviceproviders/pentaho-logo.png" alt="" width="160" />][20]

[<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/serviceproviders/sortmybox-logo.png" alt="" width="160" />][21]
[<img class="c1" src="http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/serviceproviders/wappwolf-logo.png" alt="" width="160" />][22]

While studying the approach of these 20 reciprocity providers, it can be tough to identify a set of common identifiers to refer to the value created.  Each provider has their own approach and potentially identifying terminology. For my understanding, I wanted to try and establish a common way to describe how reciprocity providers are redefining ETL.  While imperfect, it will give me a common language to use, while also being a constant work in progress.

For most reciprocity providers, it starts with some ecompassing wrapper in the form of an assembly which describes the overall recipe, formula or wrapper that contains all the moving ETL parts.

Within this assembly, you can execute on workflows, usually in a single flow, but with some of the providers you can daisy chain together multiple (or endless) workflows to create a complex series of processes.

Each workflow has a defining trigger which determines the criteria that will start the workflow such as new RSS post or new tweet, and with each trigger comes a resulting action which is the target of the workflow, publishing the RSS post to a syndicated blog or adds the tweet to a Google Spreadsheet or Evernote, or any other combination of trigger and action a user desires.

Triggers and actions represent the emotional connections that are the underpinnings of ETL’s evolution into a more meaningful, reciprocation of value that is emerging in the clouds. These new providers are connecting to the classic lineup of ETL interfaces to get things done:

  * Databases
  * Files
  * Messaging
  * Web Service

While also providing the opportunity for development of open connectors to connect to any custom database, file, messages and web services. But these connectors are not described in boring IT terms, they are wrapped in the emotion and meaning derived from the cloud service--which could have different meanings for different users. This is where one part of the promise of reciprocity comes into play, by empowering average problem owners and every day users to define and execute against these types of API driven agreements.

All of these actions, tasks, formulas, jobs or other types of process require the ability to plan, execute and audit the processes, with providers offering:

  * Scheduling
  * History / Logging
  * Monitoring

With data being the lifeblood of much of these efforts, of course we will see “big data” specific tools as well:

  * Synchronization
  * Data Quality
  * Big Data
  * Analytics

While many reciprocity providers are offering interoperability between two specific services, moving data and resource from point a to b, others are bringing in classic ETL transformations:

  * Reformat
  * Aggregate
  * Sort
  * Dedupe
  * Filter
  * Partition
  * Merge
  * Join
  * Split
  * Convert

After the trigger and before the action, there is also an opportunity for other things to happen, with providers offering:

  * Push
  * Events

During trigger, action or transformation there are plenty of opportunities for custom scripting and transofrmations, with several approaches to custom programming:

  * Custom Scripts
  * JavaScript
  * Command Line
  * API

In some cases the reciprocity provider also provides a key value store allowing the storage of user specified data extracted from trigger or action connections or during the transformation process. Introducing a kind of memory store during the reciprocal cycle.

With the migration of critical resources, many of the leading providers are offering tools for testing the process before live execution:

  * Test
  * Debugger
  * Sandbox
  * Production

With any number of tasks or jobs in motion, users will need to understand whether the whole apparatus is working, with platforms offering tools for:

  * Performance
  * Monitoring
  * Optimization

While there are a couple providers offering completely open source solutions, there are also several providing OEM or white label solutions, which allow you to deploy a reciprocity platform for your partners, clients or other situations that would require it to branded in a custom way.

One area that will continue to push ETL into this new category of reciprocity providers is security. Connectors will often use OAuth, respecting a users already established relationship with platform either on the trigger or action sides, ensureing their existing relationship is upheld. Beyond this providers are offering SSL to provide secure transmissions, but in the near future we will see other layers emerge to keep agreements in tact, private and maintain the value of not just the payload but the relationships between platforms, users and reciprocity providers.

Even though reciprocity providers focus on the migration of resources in this new API driven, cloud-based world, several of them still offer dual solutions for deploying solutions in both environments:

  * Cloud
  * On-Premise

There is not one approach either in the cloud, or on premise that will work for everyone and all their needs. Some data will be perfectly find moving around the cloud, while others will require a more sensitive on-premise approach. It will be up to problem owners to decide.

Many of this new breed of providers are in beta and pricing  isn’t available. A handful have begun to apply cloud based pricing models, but most are still trying to understand the value of this new service and what market will bear. So far I’m seeing pricing based upon:

  * Seat
  * Assembly
  * Tasks
  * Connections
  * Extension
  * Sync
  * Support
  * Training

Much like IaaS, PaaS SaaS and now BaaS, reciprocity providers will have a lot of education and communication with end users before they’ll fully understand what they can charge for their services--forcing them to continue to define and differentiate themselves in 2013.

One of the most important evolutionary areas, I’m only seeing with one or two providers, is a marketplace where reciprocity platform users can browse and search for assemblies, connectors and tasks that are created by 3rd party providers for specific reciprocity approaches. A marketplace will prove to be how reciprocity platforms serve the long tail and niches that will exist within the next generation of ETL. Marketplaces will provide a way for developers to build solutions that meet specific needs, allowing them to monetize their skills and domain expertise, while also bringing in revenue to platform owners.

I understand this is all a lot of information. If you are still ready this, you most likely either already understand this space, or like me, feel it is an important area to understand and help educate people about. Just like with API service providers and BaaS, I will continue to write about my research here, while providing more refined materials as Github repos for each research area.

Let me know anything I'm missing or your opinions on the concept of API reciprocity.

   [1]: http://apievangelist.com/trends/reciprocity.php
   [2]: /trends/reciprocity.php
   [3]: /serviceproviders/cloveretl.php (CloverETL)
   [4]: /serviceproviders/snaplogic.php (SnapLogic)
   [5]: /serviceproviders/talend.php (Talend)
   [6]: /serviceproviders/if_this_then_that_(ifttt).php (If This Then That (IFTTT))
   [7]: /serviceproviders/factor.io.php (Factor.io)
   [8]: /serviceproviders/zapier.php (Zapier)
   [9]: /serviceproviders/temboo.php (Temboo)
   [10]: /serviceproviders/foxweave.php (Foxweave)
   [11]: /serviceproviders/elastic.io.php (Elastic.io)
   [12]: /serviceproviders/rules.io.php (Rules.io)
   [13]: /serviceproviders/itduzzit.php (itDuzzit)
   [14]: /serviceproviders/wewiredweb.php (WeWiredWeb)
   [15]: /serviceproviders/ritc.php (RITC)
   [16]: http://pipes.yahoo.com/ (Yahoo Pipes)
   [17]: /serviceproviders/automateit.php (AutomateIt)
   [18]: /serviceproviders/cloudwork.php (Cloudwork)
   [19]: /serviceproviders/mashablelogic.php (MashableLogic)
   [20]: /serviceproviders/pentaho_-_kettle.php (Pentaho - Kettle)
   [21]: /serviceproviders/sortmybox.php (SortMyBox)
   [22]: /serviceproviders/wappwolf.php (Wappwolf)
