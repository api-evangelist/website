---
published: true
layout: post
title: 'Making Sense of the Different Types of API Testing'
image: https://s3.amazonaws.com/kinlane-productions2/algorotoscope-master/america-immigration_dumping-ground-gauge-on-aircraft-carrier.jpg
---
<p><img style="padding: 15px;" src="https://s3.amazonaws.com/kinlane-productions2/algorotoscope-master/america-immigration_dumping-ground-gauge-on-aircraft-carrier.jpg" alt="" width="40%" align="right" /></p>
<p class="p1">I have to admit something. I don&rsquo;t fully grasp the entire landscape of API testing. I mean, I have a pretty decent awareness and experience in testing APIs, but I can&rsquo;t close my eyes and coherently break down each layer or type of testing, let alone competently navigate the many different types of services and tooling available on the market for API testing. Like most other dimensions of the API universe the content and guidance on the subject of API testing is all over the place. After a couple of hours Googling and making my way through my bookmarks, I uncovered a pretty expansive dictionary for what I&rsquo;d consider to be under the umbrella of API testing.</p>
<p class="p1">First off, I have to talk about API testing in the most general sense before I get into the more and less formal API testing approaches. It was a dimension of API testing I hadn&rsquo;t considered before I began working at Postman, but API testing meaning that I am just kicking the tires on a API, learning what it is all about, and how you use it. This is what the majority of Postman&rsquo;s 13 million users are doing when they say they are testing an API with the Postman platform. THis experimental and curious approach to API testing provides a great onramp to the world of API publishing and consumption, but does little to help us articulate what API testing is or isn&rsquo;t.</p>
<p class="p1">Beyond just &ldquo;testing out&rdquo; an API, from what I can gather across about 25 separate API testing articles, there are 25 different layers to the API testing onion:</p>
<ol>
<li class="li1"><strong>Validation Testing</strong> - I am guessing a general type of validation &mdash; seems pretty broad.</li>
<li class="li1"><strong>Functional Testing</strong> - Adopted as part of code testing practices, applied to unit of code.</li>
<li class="li1"><strong>Component Testing </strong>- Similar to functional, but testing based upon small unit of compute.</li>
<li class="li1"><strong>User Interface Testing</strong> - Testing of the API in the context of the end user interface.</li>
<li class="li1"><strong>Load Testing</strong> - Seeing how many requests each API is able to handle in a timeframe.</li>
<li class="li1"><strong>Performance Testing</strong> - Overlapping with load testing, but benchmarking the API performance.</li>
<li class="li1"><strong>Reliability Testing</strong> - Understanding the overall reliability of each individual API.</li>
<li class="li1"><strong>Runtime Error Detection </strong>- Focusing specifically on errors encountered at runtime.</li>
<img style="padding: 15px;" src="https://s3.amazonaws.com/kinlane-productions2/algorotoscope-master/america-immigration_dumping-ground-gears-pipes-plumbing.jpg" alt="" width="40%" align="right" />
<li class="li1"><strong>Security Testing</strong> - A broad umbrella for testing the layers of API security that is present.</li>
<li class="li1"><strong>Authorization Tests </strong>- Focused on testing the authentication for each individual API.</li>
<li class="li1"><strong>Penetration Testing </strong>- Seeing you can actually get into an API through alternate ways.</li>
<li class="li1"><strong>Fuzz Testing</strong> - Blasting an API with garbage, noise, and other junk to see what it does.</li>
<li class="li1"><strong>Interoperability Testing</strong> - Testing how well an API plays with other external APIs.</li>
<li class="li1"><strong>Integration Testing</strong> - Testing an API based upon its dependency on external APIs.</li>
<li class="li1"><strong>Discovery Testing </strong>- Understanding the discoverability of an API as part of operations.</li>
<li class="li1"><strong>Usability Testing </strong>- Testing an API from the perspective of how usable it is to consumers.</li>
<li class="li1"><strong>Behavioral Testing </strong>- Driving testing based upon external views of what is expected of the API.</li>
<li class="li1"><strong>Acceptance Tests -</strong> Tested defined by the consumer based upon what is meaningful to them.</li>
<li class="li1"><strong>End-to-End Testing</strong> - Testing the entire API stack from backend to front, and back again.</li>
<li class="li1"><strong>Contract Testing </strong>- Deriving specific business contracts for an API and testing them out.</li>
<li class="li1"><strong>Scenario Testing</strong> - Building tests that reflect specific business scenarios that are relied upon.</li>
<li class="li1"><strong>Workflow Testing</strong> - Another way to define a test for a series of API calls that reflect a business need.</li>
<li class="li1"><strong>Omni-Channel Tests </strong>- Testing out multiple channels of consumption like web, mobile, and devices.</li>
<li class="li1"><strong>Documentation Testing</strong> - Verifying that an API possess valid and up to date documentation.</li>
<li class="li1"><strong>Data-Driven Testing </strong>- Relying on data to define and drive the testing of each API.</li>
</ol>
<p class="p1">Don&rsquo;t count on any of these descriptions being accurate. They are more about be trying to make sense of each one. I will be doing more research into what each of these mean to services and tooling providers, but I wanted to try and at least get all of them on the table, and try to squint and see if I could find any interesting patterns across them. There are a mix of personas, intentions, and perceptions about where the value and pain lie in the API stack present in this API testing vocabulary. Seeing all of these types of API testing really doesn&rsquo;t help me understand much, or be able to better articulate it to my readers and Postman customers. It really is just a dizzying amount of activity going on across this slice of the API universe.</p>
<h3>Considering API Governance as Part of API Testing</h3>
<p class="p1">Everything I have covered so far is about testing API instances. Making sure each individual is doing what it should be.However, over the last decade a new dimension of testing has emerged that isn&rsquo;t about testing each individual API and it&rsquo;s requests and responses, but testing the surface area of the API, making sure it is consistent with the overall organizational strategy or industry standards. API governance tends to focus on the design of each API, making sure they are consistently designed across teams, but there are a mix of dimensions that API governance looks that overlap with areas above. Here are some of the types of things being tested when it comes to API governance.</p>
<ul class="ul1">
<li class="li1"><strong>Specification</strong> - Is the specification provided for each API a valid representation of the spec.</li>
<li class="li1"><strong>Information</strong> - The naming, description, and details of an API, making sure they are sufficient.</li>
<li class="li1"><strong>Versioning</strong> - Making sure that each API is using the same approach to managing change.</li>
<li class="li1"><strong>Paths</strong> - Considering the overall design of available API paths available across all APIs.</li>
<li class="li1"><strong>Requests</strong> - Ensuring that the structure of API requests are following a common set of patterns.</li>
<li class="li1"><strong>Responses</strong> - Ensuring the the structure of API response are following a common set of patterns.</li>
<li class="li1"><strong>Schema</strong> - Making sure the common schema are applied across requests and responses.</li>
</ul>
<p class="p1">I can get finer grain on requests, responses, and other aspects of governance, but this provides a general set of what I&rsquo;ve seen when it comes to tangible API governance testing. The discipline of manual or automated API governance testing isn&rsquo;t as mature as other areas of API testing, but this will prove as a nice base for considering API governance as part of the overall API testing suite. The big difference with these types of tests is that you aren&rsquo;t testing the results of each API instance, you are testing the surface area of the API and comparing it against all the other APIs, and an organizational, or industry wide set of specifications and standards.<span>&nbsp;</span></p>
<p><img style="padding: 15px;" src="https://s3.amazonaws.com/kinlane-productions2/algorotoscope-master/america-immigration_dumping-ground-fire-hydrant-water.jpg" alt="" width="40%" align="right" /></p>
<h3>Considering How we Test API Operations</h3>
<p class="p1">Now I want to continue pushing the notion of we are testing. I want to imagine where API testing needs to go to continue stabilizing how we deliver APIs across an organization or an industry. This is the dimension of API testing that isn&rsquo;t about any single API, or about the design of all APIs, and more about the entire API operations. The overall quality and reliability of APIs aren&rsquo;t just about the APIs themselves, and is often about how APIs are delivered across their overall lifecycle, as well as the resources available to operate and support each one. You can have an API that passes all of its instance testing and overall governance, but if other aspects of API operations are falling short, it doesn&rsquo;t matter--here is what I am imagining testing looking like at the operational level.</p>
<ul class="ul1">
<li class="li1"><strong>Documentation</strong> - This is a duplicate from above, but I feel like belongs here and not in the list above.</li>
<li class="li1"><strong>Testing</strong> - Actually testing what testing is in place for each API, making sure APIs are consistently tested.</li>
<li class="li1"><strong>Monitoring</strong> - Having consistent approach to scheduling or automating testing across API operations.</li>
<li class="li1"><strong>Workspaces</strong> - Making sure all APIs possess a known workspace where everything about them can be found.</li>
<li class="li1"><strong>Discovery</strong> - Another one from above that I think belongs in the overall operational view of testing.</li>
<li class="li1"><strong>Management</strong> - Applying consistent authentication, plans, rate limiting, and reporting across all APIs.<span>&nbsp;</span></li>
</ul>
<p class="p1">There are other dimensions of API operations I could advocate testing for, but this reflects the most important dimensions of what is happening across API operations today. You see two of these areas already reflected in the types of testing that I cam across studying API testing above. Each of these areas of operations possess infrastructure that have their own APIs, which also provide machine readable artifacts that can be tested. Either adding a 3rd layer to this API testing conversation, or as I see it, just another set of API tests that should be run, but can be categorized into separate buckets. Historically I have seen all of these things as different aspects of API Operations, but now I am beginning to see them as just a suite of different tests being run, that test each individual API instances, the surface area of all APIs, or testing using the infrastructure behind API Operations.</p>
<h3>Bringing a Little More Clarity to API Testing</h3>
<p class="p1">Obviously all of this is going to take a lot more work before I get it into a more coherent state. I am not confident in my understanding of all of the API testing types listed above, and I am sure that there are other ways that I want to be able to articulate governance and operational level API testing in better detail. I also want to think about the common patterns that exist across all of the existing types of testing before I move to far down the road. I see some like business value and who is testing, but I want more time to dive into each individual area and do more research, before I make any assumptions. Really I think the big revelation of this post for me is where the artifact we are testing originates, which is from one of these three locations:&nbsp;</p>
<ol class="ol1">
<li class="li1"><strong>API Instance</strong> - Testing the request and response of a specific API instance.</li>
<li class="li1"><strong>API Surface&nbsp; </strong>- Testing the design and surface area of each individual API.</li>
<li class="li1"><strong>API Operations -</strong> Testing the operations that exist around all APIs.</li>
</ol>
<p class="p1">I can envision different categories of tests existing across these three areas. I feel like next major dimensions of this conversation will be who is doing the testing, and the tangible business value associated with each test, or bundle of tests. I am also thinking that the delivery mechanisms for testing will heavily influence this conversation, providing a different set of realities if we are running tests manually, scheduling via a monitor or agent running in some cloud region, as part of a CI/CD pipeline, or some other event that gets triggered as part of API operations. I have a lot more research and thinking to do on this subject before I&rsquo;ll reach the levels of clarity I am looking for here, but this post really helped me get things rolling. Being able to see each of these dimensions of what we are testing has set in motion a whole other set of thoughts for me, depending on whether we are testing the API instance, surface, or operations.</p>

