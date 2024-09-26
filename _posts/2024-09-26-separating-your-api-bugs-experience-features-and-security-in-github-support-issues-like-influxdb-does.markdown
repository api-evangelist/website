---
published: true
layout: post
title: 'Separating Your API Bugs, Experience, Features, and Security in GitHub Support Issues Like InfluxDB Does'
tags:
  - Support
  - Feedback
  - Bugs
  - Experience
  - Security
image: https://kinlane-productions2.s3.amazonaws.com/influxdb-support-issues.png
---
I am a fan of using GitHub issues to manage the feedback loop for APIs. Mostly because it keeps the provenance of what is happening alongside the API contracts. [As I am profiling APIs for inclusion in APIs.io I enjoy writing stories about the unique approaches I see as part of API operations](https://apis.io/2024/09/25/profiling-influxdb-time-series/).  So when I find interesting uses of GitHub by API providers, I am always happy to showcase. This round is from [the InfluxDB Time Series APIs](https://github.com/influxdata/influxdb/issues/new/choose/), and the way they have broken out their support into the following GitHub issue templates.

- **Bug Report** - Create a report to help us improve
- **Developer Experience Problem** - Tell us about slow builds, tests, and code editing
- **Feature Request** - Opening a feature request kicks off a discussion
- **Report a Security Vulnerability** - Please review our security policy for more details.

I like this separation of concerns. I think feature requests and experience friction often gets caught up in bug reports. I think teams producing APIs are so puckered up about bugs, they shut down feedback loops on other topics. Similarly I think consumers feel like they shouldn’t speak up unless there is a real problem. I separate out bugs, questions, and feedback in my support channel approach using GitHub issues, but I like the focus on experience and security—something I may emulate. Using GitHub issues for feedback loop is simple to implement, and simple for your ecosystem to engage with, and I will augment my API guidance with a page from the InfluxDB Time Series API playbook.