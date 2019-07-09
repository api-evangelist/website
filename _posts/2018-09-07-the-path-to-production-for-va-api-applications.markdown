---
published: true
layout: post
title: The Path To Production For Department of Veteran Affairs (VA) API Applications
date: 2018-09-07T09:00:00.000Z
tags:
  - API Evangelist
  - Getting Started
  - Management
  - On-boarding
  - Applications
  - Certification
image: >-
  https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories/los-angeles-downtow-freeway_blue_circuit_5.jpg
---
<p><img src="{{ page.image }}" width="45%" align="right" style="padding: 15px;" /></p>This post is part of my ongoing <a href="http://apievangelist.com/2018/08/28/reviewing-the-department-of-veterans-affairs-va-new-developer-portal/">review of the Department of Veteran Affairs (VA) developer portal and API presence</a>, moving on to where I take a closer look at their path to production process, and provide some feedback on how the agency can continue to refine the information they provide to their new developers. Helping map out the on-boarding process for any new developer, ensuring they are fully informed about what it will take to develop an application on top of VA APIs, and move those application(s) from a developer state to a production environment, and actually serving veterans.

Beginning with [the VA's base path to production template on GitHub](https://github.com/department-of-veterans-affairs/vets-api-clients/blob/master/Alpha-Path-to-Production.md), then pulling in some elements I found across the other APIs they have published to developer.va.gov, and finishing off with some ideas of my own, I shifted the outline for the path to production to look something like this:

- **Background** - Keeping the background of the VA API program.
- **[API Overview]** - Any information relevant to specific API(s).
- **Applications** - One right now, but eventually several applications, SDK, and samples.
- **Documentation** - The link, or embedded access to the API documentation, OpenAPI definition, and Postman Collection.
- **Authentication** - Overview of how to authenticate with VA APIs.
- **Development Access** - Provide an overview of signing up for development access.
- **Developer Review** - What is needed to become a developer.
	- **Individual** - Name, email, and phone.
	- **Business** - Name, URL.
	- **Location** - In country, city, and state.
- **Application Review** - What is needed to have an application(s).
	- **Terms of Service** - In alignment with platform TOS.
	- **Privacy Policy** - In alignment with platform TOS.
	- **Rate Limits** - Aware of the rate limits that are imposed.
- **Production Access** - What happens once you have production access.
- **Support & Engagement** - Using support, and expected levels of engagement.
- **Service Level Agreement** - Platform working to meet an SLA governing engagement.
- **Monthly Review** - Providing monthly reviews of access and usage on platform.
- **Annual Audits** - Annual audits of access, and usage, with developer and application reviews.

I wanted to keep much of the content that the VA already had up there, but I also wanted to reorganize things a little bit, and make some suggestions for what might be next. Resulting in a path production section that might look a little more like this.

<hr />

## Department of Veteran Affairs (VA) API Path To Production

### Background
The Lighthouse program is moving VA towards an Application Programming Interface (API) first driven digital enterprise, which will establish the next generation open management platform for Veterans and accelerate transformation in VA's core functions, such as Health, Benefits, Burial and Memorials. This platform will be a system for designing, developing, publishing, operating, monitoring, analyzing, iterating and optimizing VA’s API ecosystem. We are in the alpha stage of the project, wherein we provide one API that enables parties external to the VA to submit of VBA forms and supporting documentation via PDF on behalf of Veterans.

### [API Specific Overview]

### Applications
Take a look at the sample code and documentation we have on GitHub at https://github.com/department-of-veterans-affairs/vets-api-clients. We will be developing more starter applications, developing open source SDKs and code samples, while also showcasing the work of other API developers in the near future--check back often.

### Documentation
Spend some time with the documentation for the API(s) you are looking to use. Make sure the VA has the resources you will need to make your application work, before you sign up for a developer account, and submit your application for review.

### Authentication
VA uses token-based authentication. Clients must provide a token with each HTTP request as a header called apiKey. This token is issued by VA. To receive a developer token to access this API in a test environment, please request access.

### Development Access
All new developers must sign up for development access to the VA API platform, providing a minimal amount of information about yourself, business or organization you represent, where you operate in the United States, and the application you will be developing.

### Developer Review
You will provide the VA with details about yourself, the business you work for, and your location. Submitting the following information as a GitHub issue, or via email for more privacy:

- **Individual Information**
	- **Name** - Your name.
    - **Email** - You email address.
    - **Phone** - Your phone number.
- **Business Information**
	- **Name** - Your business or organizational name.
    - **Website** - Your business or organization website.
- **Location Information**
	- **City** - The city where you operate.
    - **State** - The state where you operation.
    - **Country** - Acknowledge that you operate within the US.

We will take a look at all your details, then verify you and your business or organization as quickly as possible. Once you hear back from us via email, you will either be declined, or we will send you a Client ID and Secret for access the VA API development environment. When you are ready, you can submit your application for review by the VA team.

### Application Review
You will provide us with details about the application you are developing, helping us understand the type of application you will be providing to veterans.  Submitting the following information as a GitHub issue, or via email for more privacy:

- **Name** - The name of your application.
- **Details** - Details about your application.
- **Terms of Service** - Your application is in alignment with ur terms of service.
- **Privacy Policy** - Your application is in alignment with our privacy policy
- **Rate Limits** - You are aware of the rate limits imposed on your application.
- **Working Demo** - A working demo of the application will be needed for the review.
- **Code Review** - A code review will be conducted when application goes to production.

We will take a look at all your details, and contact you about scheduling a code review. Once all questions about your applications are answered, and a code review has been conducted you will be notified letting you know if your application is accepted or not.

### Production Access
Once approved for production access, you will receive an email from the VA API team notifying you of your application's status. You will receive a new Client ID and Secret for your application for use in production, allowing use the base URL api.vets.gov instead of dev-api.vets.gov, and begin access live data.

### Support & Engagement
The VA will be providing support using GitHub issues, and via email. All developers will be required to engage through these channels to be able to actively engage with VA API operations, to be able to maintain access to VA APIs

### Service Level Agreement
The VA will be providing a service level agreement for each of the APIs we provide, committing to a certain quality of service, support, and communication around the APIs you will be integrating your applications with.

### Monthly Review
Each month developers will receive an email from the VA regarding your access and usage. Providing a summary of our engagement. A response is required to maintain an active status as a VA developer, and application. After 90 days of no response, all developer or production application keys will be revoked, until contact is made. Keeping all applications active, with a responsive administrator actively managing things.

### Annual Audits
Each year developers will receive an email from a VA API audit representative, reviewing your access, usage, and conducting a fresh developer review, as well as review application, access tokens, and end-usage. Ensuring that all applications operating in a production environment continually meet the expected security, privacy, support, and operational standards.

<hr />

**It Is Not Just A Path, But Journey**<br />
I'm trying to shift the narrative for the path to production into being a more complete picture of the journey. What is expected of the developers, their applications, as well as setting the table of what can be expected of the VA. I don't expect the VA to bite on all of these suggestions, but I can't help but put them in there when they are relevant, and I have the opportunity ;-)

**Decouple Developer And Application(s)**<br />
Some of the reasons I separated the developer review from the application review is so that a developer could sign up and immediately get a key to kick the tires and begin developing. When ready, which many will never be, they can submit an application for potential production access. Developers might end up having multiple applications, so if we can decouple them early on, and allow all developers to have a default application in the development environment, but also be able to have multiple applications in a production environment, I feel things will be more scalable.

**Not Forgetting The Path After Production**<br />
I wanted to make sure and put in some sort of process that would help ensure both the VA, and developers are investing in ongoing management of their engagement. Ensuring light monthly reviews of ALL applications using the APIs, and pushing for developers and the VA to stay engaged. While also making sure all developers and applications get annual reviews, preventing what happened with the Cambridge Analytica / Facebook situation, where a malicious application gets access to such a large amount of data, without any regular review. Making sure the VA isn't forgetting about applications once they are in a production state. Pushing this to be more than just about achieving production status with an application, and also continuing to ensure it is serving end-users, the veterans.

**Serving Veterans With Your Application**<br />
To close, I'd say that calling this a path to production doesn't do it justice. It should be guide to being able to serve a veteran with your application. Acknowledging that it will take a significant amount of development before your application will be ready, but also that the VA will work to review your developer account, and your application, and ensure that VA APIs, and the applications that depend on them will operate as expected, and always be in service of the veteran. Something that will require a certain level of rigor when it comes to the development, certification, and support of applications across the VA API ecosystem.
