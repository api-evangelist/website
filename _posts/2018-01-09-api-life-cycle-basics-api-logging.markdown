---
published: true
layout: post
title: 'API Life Cycle Basics: API Logging'
date: 2018-01-09T15:00:00.000Z
tags:
  - API Evangelist
  - Logging
image: 'https://s3.amazonaws.com/kinlane-productions/bw-icons/bw-logging-2.png'
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/bw-icons/bw-logging-2.png" align="right" width="45%" style="padding: 15px;" /></p>Logging has always been in the background of other stops along the API lifecycle, most notably the API management layer. However increasingly I am recommending pulling logging out of API management, and making it a first-class citizen, ensuring that the logging of all systems across the API lifecycle are aggregated, and accessible, allowing them to be accessed alongside other resources. Almost every stop in this basics of an API life cycle series will have its own logging layer, providing an opportunity to better understand each stop, but also side by side as part of the bigger picture.

There are some clear leaders when it comes to logging, searching, and analyzing large volumes of data generated across API operations. This is one area you should not be reinventing the wheel in, and you need to be leveraging the experience of the open source tooling providers, as well as the cloud providers who have emerged across the landscape. Here is a snapshot of a few providers who will help you make logging a first class citizen in your API life cycle.

[Elastic Stack](https://www.elastic.co/products) - Formerly known as the Elk Stack, the evolved approach to logging, search, and analysis out of Elastic. I recommend incorporating it into all aspects of operations, and deploying APIs to make them first class citizens.
[Logmatic](https://logmatic.io/) - Whatever the language or stack, staging or production, front or back, Logmatic.io centralizes all your logs and metrics right into your browser.
[Nagio](https://www.nagios.org/) - Nagios Log Server greatly simplifies the process of searching your log data. Set up alerts to notify you when potential threats arise, or simply query your log data to quickly audit any system.
[Google Stackdriver](https://cloud.google.com/stackdriver/) - Google Stackdriver provides powerful monitoring, logging, and diagnostics.
[AWS CloudWatch](https://aws.amazon.com/cloudwatch/) - Amazon CloudWatch is a monitoring service for AWS cloud resources and the applications you run on AWS.

I recommend cracking open logging from EVERY layer, and shipping them into a central system like Elastic for making them accessible. While each stop along the API lifecycle will come with its own logging and analysis solutions, depending on the services and tooling used, logs should also be shipped as part of a central system for analysis at the bigger picture level. Each stop along the API life cycle will have its own tooling and service, which will most likely come with its own logging and analysis services. Use these solutions. However, don't stop there, and consider the benefits from looking at log data side by side, and what the big picture might hold.

Logging will significantly overlap with the security stop along the API life cycle. The more logging you are doing, and the more accessible these logs are, the more comprehensive your API security will become. You'll find this becomes true at other stops along the API life cycle, and you will be able to better deliver o discovery, testing, define, and deliver in other ways, with a more comprehensive logging strategy. Remember, logging isn't just about providing a logging layer, it is also about having APIs for your logging, providing a programmatic layer to understand how things are working, or not.
