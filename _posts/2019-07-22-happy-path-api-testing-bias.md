---
published: true
layout: post
title: 'Happy Path API Testing Bias'
image: https://s3.amazonaws.com/kinlane-productions2/algorotoscope-master/aws-s3-stories-DSC-0084-dali-three.jpg
---

<p><img src="https://s3.amazonaws.com/kinlane-productions2/algorotoscope-master/aws-s3-stories-DSC-0084-dali-three.jpg" width="45%" align="right" style="padding: 15px;" />
I see a lot of happy path bias when it comes to the development of APIs, but specifically when it comes to crafting testing to ensure APIs are delivering as expected. Happy path is a term used in testing to describe the desired outputs a developer and product owner is looking for. Making the not so happy path being about testing for outcomes that a developer and product owner is not wanting to occur. When it comes to API development most developers and product owners are only interested in the happy path, and will almost always cut corners, minimize the investment in, or completely lack an imagination when it comes to less than happy path API testing.

<p>There are many reasons why someone will have a bias towards the happy path when developing an API. Every API provider is invested in achieving the happy path for delivering, providing, and consuming an API. This is what generates revenue. However, in this quest for revenue, we often become our own worst enemy. Shining a spotlight on the happy path, while being completely oblivious to what the not so happy paths will look like for end users. Why do we do this?

<ul>
  <li><strong>Greed</strong> - We are so interested in getting an API up and running, used in our applications, and generating behavioral surplus, we are more than willing to ignore all other possible scenarios if we can easily meet our revenue goals by ignoring the unhappy path and there are no consequences.</li>
  <li><strong>Tickets</strong> - Most development occurs using JIRA or other software development “tickets”, which tell developers what they are supposed to do to meet the requirements of their employment—tickets are written with the happy path in mind, and developers are rarely willing to do more.</li>
  <li><strong>Imagination</strong> - While many of us technologists think we are imaginative creatures, most of us are pretty stuck in a computational way of thinking, and elaborating, iterating, and exploring beyond the initial happy path design of our API just does not exist.</li>
  <li><strong>Use Software</strong> - Most of us developers do not actually use the platform we are developing, setting the stage for where we really don’t understand the problem being solve, further siloing us into seeing only the happy path that have been handed to us as part of initial product vision.</li>
  <li><strong>White Male</strong> - The majority of us API developers are white men, or developers who report to white men, leaving entire shadows regarding how our APIs will be used and abused—when you are privileged, the happy path is always easier to see and walk on.</li>
  <li><strong>Apathy</strong> - The majority of us are just doing our jobs, and we really do not have any excitement, passion, or interest in our jobs. We are just doing what we are told, and if our bosses do not specifically point out every single unhappy path, we don’t care.</li>
  <li><strong>Velocity</strong> - Things move fast at almost any company delivering APIs, and it is easy to not have time to be able to step back and sufficiently think about what the happy paths might be when we are delivering APIs that deliver some functionality amidst a fast pace environment.</li>
  <li><strong>Experience</strong> - Another reason for overlooking unhappy paths is we just do not have the experience to know about them. Startups and many technology focused companies like hiring young, low pay developers to get the job done, and they won’t always have the experience to see in the shadows.</li>
  <li><strong>By Design</strong> - The product owners do not want the less than happy or unhappy paths patched, as they are there by design, and support the overall business model, which is usually advertising. Encouraging abuse, and exploitation of APIs, or at least ensuring they are much lower priorities.</li>
</ul>

<p>There are few incentives to develop quality software these days. Revenue drives much of why we are delivering APIs, and incentivizing developers to think out of the box when it comes to API testing just doesn’t exist. Plus, it takes a lot of work to write first class tests alongside your code. Most developers are conditioned to see tests as secondary, and the thing you do only when you have the time. Making quality unhappy and less than happy path API testing always left on the cutting room floor, never making it into the final product.

<p>You can see this bias playing out in the APIs behind Facebook, Twitter, and other advertising driven platforms. The abuse of APIs are often overlooked if it generates clicks, traffic, and increases the eyeballs. Secondarily I’d say that the consequences for when unhappy paths are identified for APIs is almost non-existent. There is no accountability for poorly designed APIs, or APIs that allow for uses beyond their intended purpose. In this environment, most API providers will never prioritize API testing, and incentivize developers to properly explore how an API can be misused, abused, or just not deliver the functionality promised. Ensuring that much of API usage exists on the unhappy path by design.


