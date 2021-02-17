---
published: true
layout: post
title: 'The Ability To Deploy APIs In AWS, Google, or Microsoft Clouds'
image: http://kinlane-productions2.s3.amazonaws.com/api_evangelist_site/blog/bw_google_aws_microsoft.png
---

<p><img style="padding: 15px;" src="https://kinlane-productions2.s3.amazonaws.com/api_evangelist_site/blog/bw_google_aws_microsoft.png" alt="" width="40%" align="right" />
<p>I spent a day last week at the Google Community Summit, learning more about the Google Cloud road map, and one thing I kept hearing them focus on was the notion of being able to operate on any cloud platform--not just Google. It's a nice notion, but how real of a concept is it to think we could run seamlessly on any of the top cloud platforms--Google, AWS, and Microsoft.&nbsp;
<p>The concept is something I'll be exploring more with my <a href="https://openreferral.org/">Open Referral</a>, Human Services Data Specification (HSDS) work. It's an attractive concept, to think I could run the same API infrastructure in any of the leading cloud platforms. I see two significant hurdles in accomplishing this: 1) Getting the developer and IT staff (me) up to speed, and 2) Ensuring your databases and code all runs and scales seamlessly whichever platforms you operate in. I guess I'd have to add 3) Ensure your orchestration and continuous integration works seamlessly across all platforms you operate on.
<p>I am going to get to work deploying an HSDS compliant API on each of the platforms. My goal is to have just a simple yet complete API infrastructure running on Amazon, Google, and Microsoft. It is important to me that these solutions provide a complete stack helping me manage DNS, monitoring, and other important aspects. I'm also looking for there to be APIs for managing all aspects of my API operations--this is how I orchestrate and continuously integrate the APIs which I roll out.
<p>Along with each API that I publish, I will do a write up on what it took to stand up each one, including the cloud services I used, and their API definitions. I am pretty content (for now) on the AWS platform, leveraging Github Pages as the public facade for my projects, and each repositories acting as the platform gears of API code, and definitions. Even though I'm content where I am at, I want to ensure the widest possible options available to cities, and other organizations who are looking to deploy and manage their human service APIs.

