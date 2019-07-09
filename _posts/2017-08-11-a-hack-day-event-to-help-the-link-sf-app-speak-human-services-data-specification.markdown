---
published: true
layout: post
title: >-
  A Hack Day Event To Help The Link-SF App Speak Human Services Data
  Specification (HSDS)
date: 2017-08-11T09:00:00.000Z
tags:
  - API Evangelist
  - HSDS
  - City Government
  - County Government
  - Hackathons
image: >-
  https://s3.amazonaws.com/kinlane-productions/open-referral/optimizely/optimizely-hackathon.JPG
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/open-referral/optimizely/optimizely-hackathon.JPG" align="right" width="40%" style="padding: 15px;" /></p>I went up to San Francisco on Wednesday to participate in a social good hack day at [Optimizely](https://www.optimizely.com/). They held their event at their downtown offices, where 20+ employees showed up to hack on some social good projects. Open Referral and our partner [Benetech](https://www.benetech.org/) had suggested Human Services Data Specification (HSDS) as a possible project, which resulted in us being one of the hack projects for the event.

The Open Referral Human Services Data Specification (HSDS) team consisted of five Optimizely developers.

- Derek Hammond - Software Engineer
- Michael Fields - Software Engineer
- Zachary Power - Software Engineering Intern
- Quinton Dang - Software Engineer
- Asa Schachar - Engineering Manager

The overall strength of the team leaned toward being front-end web and mobile developers, so we decided [to "forward engineer" the Link-SF application](https://github.com/zendesk/linksf), which provides a simple web or mobile application to help folks find a variety of human services in a handful of categories like food, housing, hygiene, medical, and technology. Link-SF is an ongoing collaboration between the [Tenderloin Technology Lab](http://www.tenderlointechnologylab.org/) and [Zendesk, Inc.](http://www.zendesk.com/), and we wanted to help contribute to their work, while also making the application potentially deployable by other cities and regions.

Once the team got to work on the project they identified that we could get at the data behind the SF application. The team decide they would forward engineer the dataset, the API, and the UI for the web and mobile application, making it all speak [Human Services Data Specification (HSDS)](https://github.com/openreferral/specification)--here is what they did:

- Took the Link-SF datasets and saved as a single JSON file.
- Converted the JSON schema to use HSDS -- the changes weren't significant.
- Made it so that the app reads [location data from a Github repository](https://raw.githubusercontent.com/optimizely/linksf/master/core/sf_location.json) (you can change this to your url)
- Updated the taxonomy fetch to use the new data
- Ensured the UI worked with the new data

[You can find the project in an Optimizely Github repository](https://github.com/optimizely/linksf), which they are going to invest some more time into cleaning up this week--so don't judge! ;-) If you want to run our app locally, [you can save a file as `config.js`and follow the instructions on the setup page](https://github.com/optimizely/linksf/blob/master/docs/SETUP.md). I am going to play with the application some more, and wait for them to clean up the page before we add the project to our official open source Human Services Data Specification (HSDS) solutions. Adding another HSDS compliant tool that any city, county, or other organization could deploy for their own purposes.

We didn't have much time for the hackathon. It went from 2:30 PM to 8:30 PM, and I was impressed what the team was able to get done. I like their hack which used Github as a backend, and the speed at which they were able to work together to fork the application and make working using HSDS. It provides an interesting open source blueprint that other cities could also fork, and implement with their own localized datasets. Their work shows what is possible when you decouple the backend API (or JSON file) from the front-end application, and utilize a common schema and API definition. It transforms the application from a single use application into a multi-use application that can be used over and over again.

Thank you to [Optimizely](https://www.optimizely.com/) for putting on the hackathon. Thank you to [Benetech](https://www.benetech.org/) for making the event happen. Thank you to the five developers who help moved the HSDS conversation forward. Once the Github repository gets cleaned up, I will spend some time playing with the application, and publish a follow-up story. I'd like to make the project push button deployable, so that organizations could launch a new instance of Link-[Any City] for low or no cost. We have another hackathon coming up in September on the east coast, and I learned a lot at this one about what I should have ready when it comes to help hackers be successful in the short time we have. It has been a while since I've attended a hackathon, and forgot how they can be a good vehicle for moving projects forward--at least the social good type of event. ;-)
