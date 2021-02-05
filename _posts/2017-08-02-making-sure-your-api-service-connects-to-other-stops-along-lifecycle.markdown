---
published: true
layout: post
title: Making Sure Your API Service Connects To Other Stops Along The API Lifecycle
date: 2017-08-02T09:00:00.000Z
tags:
  - API Evangelist
  - iPaaS
  - Monitoring
image: >-
  https://s3.amazonaws.com/kinlane-productions/runscope/runscope-connected-services.png
---
<p><a href="https://www.runscope.com/docs/api-testing/integrations"><img src="https://s3.amazonaws.com/kinlane-productions/runscope/runscope-connected-services.png" align="right" width="40%" style="padding: 15px; "/></a></p>I am continuing [my integration platform as a service research](http://ipaas.apievangelist.com/), and spending a little bit of time trying to understand how API providers are offering up integrations with other APIs. Along the way, I also wanted to look at how API service providers are doing it as well, opening themselves up to other stops along n API lifecycle. To understand how API service providers are allowing their users to easily connect to other services I'm taking a look at how my partners are handling this, starting with [connected services at Runscope](https://www.runscope.com/docs/api-testing/integrations).

Runscope provides ready to go integration of their API monitoring and testing services with twenty other platforms, delivering a pretty interesting Venn diagram of services along the API lifecycle:

- Slack - Slack to receive notifications from Runscope API test results and Traffic Alerts.
- Datadog  - Datadog to create events and metrics from Runscope API test results.
- Splunk Cloud  - Splunk Cloud to create events for API test results.  
- PagerDuty  - A PagerDuty service to trigger and resolve incidents based on Runscope API test results or Traffic Alerts.
- Amazon Web Services   - Amazon Web Services to import tests from API Gateway definitions.
- Ghost Inspector  - Ghost Inspector to run UI tests from within your Runscope API tests.
- New Relic Insights - New Relic Insights to create events from Runscope API test results.
- Microsoft Teams  - Microsoft Teams to receive notifications from Runscope API test results.
- HipChat  - HipChat to receive notifications from Runscope API test results and Traffic Alerts.   
- StatusPage.io - StatusPage.io to create metrics from Runscope API test results.
- Big Panda - Big Panda to create alerts from Runscope API test results.   
- Keen IO - Keen IO to create events from Runscope API test results.
- VictorOps - A VictorOps service to trigger and resolve incidents based on Runscope API test results or Traffic Alerts.   
- Flowdock - Flowdock to receive notifications from Runscope API test results and Traffic Alerts.  
- AWS CodePipeline - Integrate your Runscope API tests into AWS CodePipeline.
- Jenkins  - Trigger a test run on every build with the Jenkins Runscope plugin.
- Zapier - integrate with 250+ services like HipChat, Asana, BitBucket, Jira, Trello and more.
- OpsGenie - OpsGenie to send alerts from Runscope API test results.
- Grove  - Grove to send messages to your IRC channels from Runscope API test results and Traffic Alerts.
- CircleCI  - Run your API tests after a completed CircleCI build.

Anyone can integrate [API monitoring and testing into operation using the Runscope API](https://www.runscope.com/docs/api), but these twenty services are available by default to any user, immediately opening up several important layers of our API operations. Immediately you see the messaging, notifications, chat, and other support layers. Then you see the continuous integration / deployment, code, and SDK layers. Then you come across Zapier, which opens up a whole other world of endless integration possibilities. I see [Runscope](https://www.runscope.com) owning the monitoring, testing, and performance stops along the API lifecycle, but their connected services puts other stops like deployment, management, logging, analysis, and many others also within reach.

I am working on a way to track the integrations between API providers, and API service providers. I'd like to be able to visualize the relationships between providers, helping me see the integrations that are most important to different groups of end users. I'm a big advocate for API providers to put iPaaS services like [Zapier](https://zapier.com/app/explore) and [DataFire](https://github.com/DataFire) to work, opening up a whole world of integrations to their developers and end users. I also encourage API service providers to work to understand how Zapier can open up other stops along the API lifecycle. Next, everyone should be thinking about deeper integrations like Runscope is doing with their connected services, and make sure you always publish a public page showcasing integrations, making it part of documentation, SDKs, and other aspects of your API service platform.
