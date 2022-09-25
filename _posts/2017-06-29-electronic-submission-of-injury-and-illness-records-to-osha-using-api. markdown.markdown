---
published: true
layout: post
title: Electronic Submission of Injury and Illness Records to OSHA
date: 2017-06-29T13:00:00.000Z
tags:
  - API Evangelist
  - Regulation
  - Federal Government
  - Forms
image: 'https://s3.amazonaws.com/kinlane-productions/osha/osha-work-injury-form.jpg'
---
<p><a href="https://www.osha.gov/injuryreporting/"><img src="https://s3.amazonaws.com/kinlane-productions/osha/osha-work-injury-form.jpg" align="right" width="40%" style="padding: 15px;" /></a></p>
[I recently learned that Occupational Safety and Health Administration (OSHA) has issued guidance regarding the electronic submission of injury and illness records via an API, from an announcement that they has postponed the availability of electronic submissions for another six months](https://www.osha.gov/injuryreporting/). Regardless of the delay, it is good to see them migrating towards an API-focused approach to allowing businesses to be compliant with safety regulations and reporting guidelines.

Here are the details of the OSHA guidance, broken down into some interesting buckets of guidance:

* **Who**: Establishments with 250 or more employees that are currently required to keep OSHA injury and illness records, and establishments with 20-249 employees that are classified in certain industries with historically high rates of occupational injuries and illnesses.
* **What**: Covered establishments with 250 or more employees must electronically submit information from OSHA Forms 300 (Log of Work-Related Injuries and Illnesses), 300A (Summary of Work-Related Injuries and Illnesses), and 301 (Injury and Illness Incident Report). Covered establishments with 20-249 employees must electronically submit information from OSHA Form 300A.
* **When**: The requirement becomes effective on January 1, 2017. The new reporting requirements will be phased in over two years. In 2017, all covered establishments must submit information from their completed 2016 Form 300A by July 1, 2017. In 2018, covered establishments with 250 or more employees must submit information from all completed 2017 forms (300A, 300, and 301) by July 1, 2018, and covered establishments with 20-249 employees must submit information from their completed 2017 Form 300A by July 1, 2018. Beginning in 2019 and every year thereafter, covered establishments must submit the information by March 2.
* **How**: OSHA will provide a secure website that offers three options for data submission. First, users will be able to manually enter data into a web form. Second, users will be able to upload a CSV file to process single or multiple establishments at the same time. Last, users of automated record-keeping systems will have the ability to transmit data electronically via an API (application programming interface). We will provide status updates and related information here as it becomes available.

I think the three options available are interesting. Manual website, and a CSV file upload--which is kind of a gateway to API-land, but they will also be providing the real deal when it comes to submitting forms using an API. All government agencies should be migrating towards this approach to handling forms, and OSHA provides us with one more blueprint to point at when convincing government to be more machine readable when it comes to forms--if there is a web form, or PDF form, there should also be an API for submitting as well.

Now that the federal agency is on my radar I will be keeping an eye out for when their API is ready, and maybe even offer some help when it comes to the portal and presence for the API. I like this example because it is a good reference for APIs being used to deliver government forms, but also because it is a good example of API driven regulatory compliance, which I think we need more of. Not because regulations automatically equal good, but because we need regulations and business compliance to be as observable as we possibly can--APIs will be how we do this.
