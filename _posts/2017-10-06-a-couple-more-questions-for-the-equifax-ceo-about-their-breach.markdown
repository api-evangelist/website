---
published: true
layout: post
title: A Couple More Questions For The Equifax CEO About Their Breach
date: 2017-10-06T09:00:00.000Z
tags:
  - API Evangelist
  - Politics of APIs
  - Security
  - Management
  - Monitoring
  - Regulation
image: >-
  https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories-new/digital-bits-capital-dc-flag-side-view.jpg
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories-new/digital-bits-capital-dc-flag-side-view.jpg" align="right" width="40%" style="padding: 15px;" /></p>[Speaking to the House Energy and Commerce Committee, former Equifax CEO Richard Smith pointed the finger at a single developer who failed to patch the Apache Struts vulnerability](https://www.theverge.com/2017/10/3/16410806/equifax-ceo-blame-breach-patch-congress-testimony). Saying that protocol was followed, and a single developer was responsible, shifting the blame away from leadership. It sounds like a good answer, but when you operate in the space you understand that this was a systemic failure, and you shouldn't be relying on a single individual, or even a single piece of scanning software to verify the patch was applied. You really should have many layers in place to help prevent breaches like we saw with Equifax.

If I was interviewing the CEO, I'd have a few other questions for him, getting at some of the other systemic and process failures based upon his lack of leadership, and awareness:

- **API Monitoring & Testing** - You say the scanner for the Apache Struts vulnerability failed, but what about other monitoring and testing. The plugin in questions was a REST plugin, that allowed for API communication with your systems. Due to the vulnerability, extra junk information was allowed to get through. Where were your added API request and response integrity testing and monitoring process? Sure you were scanning for the vulnerability, but are you keeping an eye on the details of the data being passed back and forth? API monitoring & testing has been around for many years, and service providers like [Runscope](http://apis.how/8nlsropidv) do this for a living. What other layers of monitoring and testing were in place?
- **API Management** - When you expose APIs like you did from Apache Struts, what does the standardized management approach look like? What sort of metering, logging, rate limiting, and analysis occurs on each endpoint, and verification occurs, ensuring that only required clients should have access? API management has been standard procedure for over a decade now for exposing APIs like this both internally and externally. Why didn't your API management process stop this sort of breach after only a couple hundred record went out? API management is about awareness regarding access to all your resources. You should have a dashboard, or at least some reports that you view as a CEO on this aspect of operations.

These are just two examples of systems and processes that should have been in place. You should not be depending on a single person, or a single tool to catch this type of security incident There should be many layers in place, with security triggers, and notifications in place. Your CTO should be in tune with all of these layers, and you as the CEO should be getting briefed on how they work, and have a hand in making sure they are in place. I'm guessing that your company is doing APIs, but is dramatically behind the times when it comes to commonplace API management practices. This is your fault as the CEO. This is not the fault of a single employee, or any group of employees. 

I am guessing that as a CEO you are more concerned with the selling of this data, than you are of securing it in storage, or transit. I'm guessing you are intimately aware of the layers that enable you to generate revenue, but you are barely investing in the technology and processes to do this securely, while respecting the privacy of your users. They are just livestock to you. They are just products on a shelf. It shows your lack of leadership to point the finger at a single person, or single piece of technology. There should have been many layers in place to catch this type of breach beyond a single vulnerability. It demonstrates your lack of knowledge regarding modern trends in how we secure and provide access to data, and you should never have been put in charge of such a large data brokerage company.
