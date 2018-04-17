---
published: true
layout: post
title: >-
  My Response To The VA Microconsulting Work Statement On API Landscape Analysis
  and Near-term Roadmap
date: 2018-04-17T09:00:00.000Z
tags:
  - API Evangelist
  - Federal Government
  - Veterans
  - Road Map
  - Low Hanging Fruit
  - Adopta Agency
image: >-
  https://s3.amazonaws.com/kinlane-productions/federal-government/state-2017/kin-lane-presidential-innovation-fellow.png
---
<p><img src="{{ page.image }}" width="45%" align="right" style="padding: 15px;" /></p>The Department of Veterans Affairs (VA) is listening to my advice around how to execute their API strategy and adopting a micro-approach to not just delivering services, but also to the business of moving the platform forward at the federal agency. I've responded to [round one](http://apievangelist.com/2017/10/26/my-response-on-the-department-of-veterans-affairs-rfi-for-the-lighthouse-api-management-platform/), and [round two](http://apievangelist.com/2018/02/24/department-of-veterans-affairs-lighthouse-platform-rfi-round-two/) of the RFI's, and [now they have submitted a handful of work statements on Github](https://github.com/department-of-veterans-affairs/lighthouse), so I wanted to provide an official response, share my thoughts on each of the work statements, and actually bid for the work.

**First, Here is The VA Background**
The Lighthouse program is moving VA towards an Application Programming Interface (API) first driven digital enterprise, which will establish the next generation open management platform for Veterans and accelerate transformation in VA's core functions, such as Health, Benefits, Burial and Memorials. This platform will be a system for designing, developing, publishing, operating, monitoring, analyzing, iterating and optimizing VA’s API ecosystem.

**Next, What The VA Considers The Play**
As the VA Lighthouse Product Owner I have identified two repositories of APIs and publicly available datasets containing information with varying degrees of usefulness to the public. If there are other publicly facing datasets or APIs that would be useful they can be included. I need an evaluation performed to identify and roadmap the five best candidates for public facing APIs.

The two known sources of data are:

- Data.gov - https://catalog.data.gov/organization/va-gov and www.va.gov/data
- Vets.gov - https://github.com/department-of-veterans-affairs/vets-api

**Then, What The VA Considers The Deliverable**
Rubric/logical analysis for determining prioritization of APIs
Detail surrounding how the top five were prioritized based on the rubric/analysis (Not to exceed 2 pages unless approved by the Government)
Deliverables shall be submitted to VA's GitHub Repo.

**Here Is My Official Response To The Statement**
To describe my approach to this work statement, and describe what I've been already doing in this area for the last five years, I'm going to go with a more logical analysis, as opposed a rubric. There is already too much structured data in all of these efforts, and I'm a big fan of making the process more human. I've been working to identify the most valuable data, content, and other resoures across the VA, as well as other federal agencies since I worked in DC back in2013, something that has inspired my Knight Foundation funded work with [Adopta.Agency](http://adopta.agency/).

**Always Start With Low Hanging Fruit**
When it comes to where you should start with understanding what data and content should be turned into APIs, you always begin with the public website for a government agency. If the data and content is already published to the website, it means that there has been demand for accessing the information, and it has already been through a rigorous process to make publicly available. [My well developed low hanging fruit process](https://apievangelist.com/2016/04/13/formalizing-my-approach-to-identifying-the-low-hanging-api-fruit/) involves spidering of all VA web properties identifying any page containing links to XML, CSV, and other machine readable formats, as well as any page with a table containing over 25 rows, and any forms providing search, filtering, and access to data. The low hanging fruit portion of this will help identify potentially valuable sources of data beyond what is already available at va.gov/data, data.gov, and on Github. Expanding the catalog we should be considering when it comes to what API should be published.

**Tap Existing Government Metrics**
To help understand what data available at va.gov/data, data.gov, on Github, as well as across all VA web properties, you need to reach out to existing players who are working to track activity across the properties. [analytics.usa.gov](http://aalytics.usa.gov) is a great place to start to understand what people are looking at and searching for across the existing VA web properties. While talking with the folks at the GSA, I would also be talking to them about any available statistics for relevant data on data.gov, understanding what is being downloaded and access when it comes to VA data, but also any other related data from other agencies. Then I'd stop and look at the metrics available on Github for any data stored in with repositories, taking advantage of the metrics built into the social coding platform. Tapping into as many of the existing metrics being tracked on across the VA, as well as other federal agencies.

**Talk To Veterans And Their Supporters**
Next, I'd spend time on Twitter, Facebook, Github, and Linkedin talking to veterans, veteran service organizations (VSO), and people who advocate for veterans. This work would go a long way towards driving other platform outreach and evangelism described in the other statement of work I responded to. I'd spend a significant amount of time asking veterans and their supports what data, content, and other resources they most use, and would be most valuable if were made more available in web, mobile, and other applications. Social media would provide a great start to help understand what information should be made available as APIs, then you could also spend time reviewing the web and mobile properties of organizations that support veterans, taking note of what statistics, data, and other information they are publishing to help them achieve their mission, and better serve veterans.

**Start Doing The Work**
Lastly, I'd start doing the work. Based upon what I've learned from my [Adopta.Agency](http://adopta.agency/) work, each dataset I identified I'd publish my profiling to an individual Github repository. Publishing a README file describing the data, where it is located, and a quick snapshot of what is needed to turn the dataset into an API. No matter where the data ended up being in the list of priorities there would be a seed planted, which might attract its own audience, stewards, and interested parties that might want to move the conversation forward--internally, or externally to VA operations. EVERY public dataset at the VA should have its own Github repository seed, and then eventually it's corresponding API to help make sure the latest version of the data is available for integration in applications. There is no reason that the work to deploy APIs cannot be started as part of the identifying and prioritization of data across the VA. Let's plant the seed to ensure all data at the VA eventually becomes an API, no matter what it's priority level is this year.

**Some Closing Thoughts On This Project**
It is tough to understand where to begin with an API effort at any large institution. Trust me, I tried to do at the VA. I was the person who originally setup the VA Github organization, and began taking inventory of the data now available on data.gov, va.gov/data, and on Github. To get the job done you have to do a lot of legwork to identify where all the valuable data is. Then you have to do the hard work of talking to internal data stewards, as well as individuals and organizations across the public landscape who are serving veterans. This is a learning process unto itself, and will go a long way towards helping you understand which datasets truly matter, and should be a priority for API deployment, helping the VA better achieve its mission in serving veterans.
