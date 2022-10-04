---
published: true
layout: post
title: 'Some Thoughts on API Governance'
image: https://s3.amazonaws.com/kinlane-productions2/algo-rotoscope/stories/supreme-court-judgement.jpg
tags:
- Governance
- Design
- Testing
---
API governance is a massive subject that takes regular work to make sense of and to be able to successfully articulate to others. With the growing number of APIs and microsservices in use across enterprise organizations, API governance is quickly becoming one of the most important areas of discussion for me. To help organize all of the moving parts of API governance into some (hopefully) more actionable guidance, I wanted to share some thoughts on API governance as I see it today.

### What is API Governance?
API governance is ensuring that the complex systems powering the enterprise are as defined, discoverable, and observable as possible so that you can understand the state of the system, and then incrementally evolve the state of the system as a whole, in the right direction. Quantifying the system, but then allowing us to improve upon, standardize, and move the enterprise into a specific direction as defined by the business domains we operate within.

### Why Do You Need API Governance?
Without API governance you will never achieve any level of consistency in the design, delivery, and operation of APIs across teams. Without a consistent approach to doing APIs, you will never fully understand or be able to influence the quality of APIs, and teams will always struggle to achieve desired levels of productivity in their work--something that will make the velocity of an organization perpetually uncontrollable and unpredictable.

### How do you do API governance?
It takes a significant amount of planning, investment, and iteration to do API governance across a large enterprise organization. API governance involves defining all of your APIs as machine-readable artifacts, organizing, managing, and evolving them via a single API platform, tapping into the outputs of that platform to achieve the levels of observability needed to understand the state of the system. Then enabling teams to change behavior in how they design, develop, deploy, and manage APIs across a well-known API lifecycle, measuring, reporting, and communicating around where progress is being made, and where it is not.  Establishing a centrally defined, but federated approach to governing how teams operate, and APIs are being delivered, bringing increased productivity, quality, and velocity at scale across the enterprise.

### 101 - Design Governance
The most common form of API governance in existence today is design governance, which governs the surface area of APIs being delivered across teams. Design governance is top of mind because inconsistent APIs across teams introduce friction downstream across almost every stop along the API lifecycle. Making documentation, testing, and integration a challenge, while also delivering an API that is difficult to evolve and add capabilities to. There are a handful of common building blocks involved with realizing, applying, and evolving API design governance across teams.


- **Guidance** - Establishing a human-readable set of guidance that outlines how APIs should be designed.
- **Rules** - A machine-readable set of rules that can be used to ensure API artifacts are following guidance.
- **Scripts** - Executable scripts that can be used to understand if artifacts are following guidance.
- **Design** - Applying API design governance when an API artifact is being designed as part of development.
- **Develop** - Applying API design governance while an API is being developed using a code-first approach.
- **Build** - Enforcing API design governance as part of the CI/CD pipeline, ensuring APIs follow guidance.


Ideally API governance guidance, rules, and scripts are developed centrally as part of organizational-wide governance, but then applied at both design, develop, and build time as part of a federated approach by teams. With guidance, rules, and scripts being used by teams, but then also iterated upon and evolved by teams, helping evolve the API governance strategy based upon the reality on the ground delivering APIs by teams. Giving teams the agency to know best when to apply API governance, but then also giving them a voice in what API governance is, and how it is applied as part of regular operations.

### 201 - Foundational Governance
As teams mature in their approach to API design governance they should also be investing in more foundational API governance, which helps lay a more solid foundation for design governance while helping enable teams to better contribute to API governance observability through automation and reporting. Foundational API governance goes beyond the design of each individual API and ensures that APIs all have a solid foundation for documenting, testing, securing, and monitoring APIs, which puts individual APIs on more solid footing but also acts as the vehicle for continuing to realize API governance across an organization.


- **Guidance** - Establishing a human-readable set of guidance that outlines how APIs should be operated.
- **Documentation** - Ensuring that every API possesses up to date and accurate documentation for consumers.
- **Testing** - Making sure that all APIs possess contract, performance, and any other type of tests required.
- **Security** - Making sure that all APIs possess the same levels of security testing across all teams.
- **Monitoring** - Require that the contract, performance, and security tests for APIs are actively monitored.


Foundational API governance is the next logical dimension of API governance after the design of an API because it doesn’t matter how consistently designed APIs are if there is no documentation available, the quality of APIs is low, and APIs are lacking security. Foundational API governance helps establish guidelines for how teams should be operating, providing a consistent way to document, test, secure, and monitor their APIs, influencing the behavior across teams, but then also monitoring and reporting upon how well teams are doing when it comes to being compliant with wider API governance.

### 301 - Lifecycle Governance
Once the design of APIs becomes more consistent across teams, and the foundation is strengthened through consistent documentation, testing, security, and monitoring, teams can shift to governing other essential stops along the API lifecycle. Making sure teams are deploying their APIs inconsistent ways that help support design and foundational API governance, but then also possess the necessary feedback loop to effectively move APIs forward. Ensuring teams can effectively iterate upon the resources and capabilities they APIs are providing access to while making sure that APIs are meeting consumer demand with the right amount of velocity to support their applications and integrations.


- **Guidance** - Establishing a human-readable set of guidance that outlines how APIs should be deployed.
- **CI/CD** - Defining how CI/CD pipelines are used to test, secure, automate, and deploy as part of the lifecycle.
- **Gateway** - Defining how API gateways are used for deployment, and policies are managed across APIs.
- **Feedback** - Ensuring that issues, comments, and other feedback loops exist, are active, and being applied.


This dimension of API governance is how we govern the velocity and forward motion of API operations, ensuring that teams are consistent in how they deploy APIs while making sure the design and operational governance is applied across all teams.  All three of these areas of API governance can be invested in separately, but ultimately they all support each other, and to realize API governance across all teams you will need to properly invest across design, foundational, and lifecycle governance. Otherwise, there is really no way of knowing whether API governance is working across an organization, and there will be no reporting and feedback loop in place across teams to iterate and evolve API governance forward.

### Artifacts
None of this API governance is possible without machine-readable artifacts that shape APIs and the operations around them, but also provide the measurable outputs needed to understand if the behavior is being changed across teams. These artifacts perpetually define each individual and the change that occurs to them, but also allow us to observe the overall state of the enterprise system. All because there are artifacts produced, evolved, and monitored across all APIs throughout the lifecycle that moves each of them forward as part of each business domain.


- **OpenAPI** - The OpenAPI specification provides the contract for each API, and is used to govern the design of each API in production.
- **Collection** - Postman collections provide the executable unit of governance that ensures the entire API lifecycle is well understood.
- **API Outputs** - The response from any API used across the API lifecycle provides an artifact that can be used to understand the state.


OpenAPI is essential to API design governance, and collections are essential for foundational and lifecycle governance but is actually the fundamental ingredient that makes governance something that is both observable and executable. But, it is ultimately APIs that will provide us with the artifacts we need to make sense of each API, as well as across many different APIs being delivered by many different teams, helping understand when APIs are deployed, what policies are applied at the management layer, and anything else we want to understand, measure, monitor, and evolve as part of our organizational-wide API governance.

### Discovery
You cannot govern what you cannot find. Leaving discovery another essential ingredient in API governance. Discovery in service of API governance isn’t just about being able to find the APIs or the OpenAPIs for each API. Discovery has to be the default across all parts of operations, and the lifecycle that moves each API forward. For API governance to happen at scale, the discovery across teams, workspaces, APIs, and all the elements that support them have to be discoverable by default, ensuring that there isn’t too much additional work needed for teams to make their work visible internally, with partners, or when it make sense, to the public.


- **Teams** - Being able to search and browse for team members who are working on different APIs across any business domain.
- **Workspaces** - Ensuring that the workspaces and repositories where work on APIs is happening is searchable and browsable.
- **APIs** - Making sure that the OpenAPI and Postman collections for all APIs are indexed and able to be browsed and searched.
- **Environments** - Having the individual environments for mock, development, staging, and production are all discoverable.
- **Tests** - Making sure that the tests for each API is properly named, documented, and discoverable via search and browsing.
- **Monitors** - Allowing the scheduled monitors for testing, security, and governance are all searchable and browsable by default.


Teams will need to apply descriptive metadata to workspaces, APIs, and the supporting elements, but beyond naming, describing, and applying a little role-based access control, teams shouldn’t be required to do much work to ensure their APIs and the work behind them are discoverable by default. Relying on the platform beneath API operations to make everything discoverable, so that artifacts and activity are able to be monitored, measured, reported upon, and considered as part of steering an organization forward using API governance. Perpetually mapping API operations so that it can be properly governed, but also so it can also inform the future of API governance.

### Observability
Being able to understand the state of API operations using its existing outputs is essential to stay informed of what is happening across teams. API observability is about piping the results of the test, security, and other collection runs into existing application performance monitoring (APM) solutions. Ensuring that each API or lifecycle artifact we’ve defined and made discoverable is properly monitored, and the results are collected, aggregated, and made available via reporting and monitoring dashboards. Making observability the default across all APIs in production, helping us understand the state of operations because we’ve required every API to possess a consistent set of outputs across the entire API lifecycle.


- **Teams** - Understanding how teams are organized, as well as the activity that exists across teams as they deliver APIs.
- **Workspaces** - Tuning into the activity and history that is occurring within workspaces to make sense of working going on.
- **APIs** - Seeing the change occurring across APIs, and understanding how the design of APIs is being evolved over time.
- **Tests** - High or low level observability into the quality, execution, and coverage of testing that is in place across APIs.
- **Security** - Making security across all APIs observable by tapping into the manual, scheduled, and automated scans.
- **Monitoring** - Monitoring the monitoring of operations, making sure that 100% of operations is being piped into our APM.
- **Feedback** - Ensuring the feedback loop across APIs is active and healthy, and being used to evolve API operations.
- **Governance** - Making governance itself something that is observed, measured, reported upon and used to guide teams.


Observability isn’t just about the health of individual APIs, it is about the overall productivity, quality, and governance of API operations. Every part of the API lifecycle has an API, meaning every stop along the API lifecycle can have a Postman collection defined to monitor the stop for a specific API. Which then produces an output for that API at that point of the API lifecycle, which can then be collected, aggregated, and reported upon as part of overall API governance. Demonstrating how APIs ensure that the entire API lifecycle and governance being applied to it is defined, monitored, and made observable as part of a wider API governance strategy.

### Enablement
API governance is only governance to business leadership, and on the ground floor within the enterprise, it should just look like API enablement. A strong API governance strategy focuses on enabling teams to do the right thing throughout the API lifecycle. Enabling teams to deliver high-quality APIs at a greater velocity via a solid platform, making it easy to deliver an API that is designed in accordance with wider API design governance, complete with the documentation, testing, security, and monitoring needed to support foundational API governance, and begin to realize API governance across the entire API lifecycle. Spreading API governance out across the API lifecycle, meeting developers where they are, but also enabling us to effectively understand the state of our enterprise system, and incrementally change behavior across teams over time.


- **Platform** - This is just too big of a thing to do with a solid API platform that connects all our infrastructure and APIs together.
- **Guidance** - The guidance for API governance must be always up to date and reflect the current state of governance across an organization.
- **Collections** - Portable, shareable, executable, and documented collections are the gears of the API lifecycle, but also API governance.
- **Rules** - The rules of the API governance games should be defined as machine-readable rules that can help automate governance.
- **Scripts** - Simple scripts should be available to help teams apply, visualize, fix, and help realize API governance as part of their regular work.
- **Schema** - There should be a wealth of standardized and validated schema available to shape our digital resources, capabilities, and governance.
- **Examples** - Teams should always have simple examples of what healthy API practices should look like so they have positive examples to apply.
- **IDE** - API governance should be available in the integrated development environments (IDE) that teams are already using to deliver API infrastructure.
- **CLI** - API governance should be available at the command line interface (CLI), allowing for teams to apply and automated governance here.
- **Automation** - The automation of API governance during the design, development, deployment, and management phases is essential.
- **Reviews** - API design, foundational, and lifecycle governance reviews should be a regular part of working with teams to realize API governance.
- **Workspaces** - API governance should be a native part of the workspaces where teams are producing APIs, bringing governance to them.
- **Educate** - API governance education should be available via guidance, reviews, and workshops, but also inline as part of API governance automation.
- **Support** - Teams should never be left without support when it comes to API governance, providing a place where they can get the help they need.


If API governance does not look like enablement on the ground across teams, you will encounter stiff resistance. Of course, there will always be resistance to governance from teams, but the more informed and enabled they are, the more likely they will not just help apply API governance, but also participate in the evolution of what it means. API enablement across teams is just good governance. Teams aren’t setting out with the intention of creating APIs that are designed in different ways. They just don’t have what they need to properly design an API. The same applies to documentation, testing, and security. It isn’t that they don’t care about these areas, they just don’t have the right support to understand how important it all is, or that there is a standard way of moving their APIs forward across a shared API lifecycle.

### Reporting
The final critical dimension of API governance centers on the ability to report on what is happening across teams. Ensuring that everything we’ve discussed today is visible via reporting and existing APM infrastructure. Reporting is how leadership will be informed regarding the current state of enterprise API operations enough to be able to begin to change behavior across teams. Reporting makes everything we’ve talked about so far visible to not just teams, but also business leaders, allowing them to see things at a high level, but also drill down into the details of individual teams, APIs, and other aspects of how things are working or not across the enterprise.


- **State** - There needs to be a summary dashboard that provides the overall state of API operations, but also the governance being applied to it.
- **APIs** - Reporting should be available for all APIs, providing the current and historical details regarding the API, but also the operations around it.
- **Teams** - There should be reporting to understand what teams are working on, and their overall performance when it comes to APIs and governance.
- **APM** - Everything across API operations and the governance of APIs should be piped into APM solutions, so it is always made as observable as possible.


Without investment in reporting, the awareness required to change an organization's behavior in how they design, deploy, manage, and evolve API will always fall short. Postman collections are how we make it so that every individual API and stop along the API lifecycle can be seen via reports. Providing us with the data we need to see APIs and the operations around them. Turning these very abstract technical things into something anyone can pay attention to via reporting and dashboards. Turning API operations, the lifecycle, and governance, into something we can actually make sense of at scale over time.

### More Work to Do
This isn’t the highest level API governance narrative I’ve published, you can [see one I did for the Department of Veterans Affairs a few years back](https://department-of-veterans-affairs.github.io/ES-ASG/skylight_api_governance_research_report.html)), but it is the most comprehensive and potentially hands-on one I have ever published. Meaning, I can actually make all of this happen now, where the one I did for the VA was based upon lots of interviews and research, but this one I can actually apply using the Postman API platform.. This is why I started working at Postman, so I could begin to take more of my theories and put them into practice, applying governance across organizations, rather than just talking about it. There is still a lot more work to be done here to refine this approach and make something the organizations I am talking to can apply as part of their operations, but it gathers up all the moving parts of a hands-on governance approach for me and gets me to a place where I can start distilling down into demonstrable guidance.


With this round of API governance work I am looking to distill my guidance down into much smaller executable chunks. Helping folks who are just getting started with where they should be starting, but then also provide what teams need no matter where they are in their journey. I am really determined to make API governance more accessible for enterprise leadership, while also making it actionable on the ground floor. I have some large enterprises that are pretty far along in their API governance journey, but for the most part, everyone I am talking about is desperately in need of practical guidance for what they should be doing today. It is something that is only growing more critical with each, as the number of APIs and microservices increases, and the demand on teams to keep moving forward with increased velocity grows. I’ll keep working to polish this overview and the supporting guidance, and keep investing in making it available via Postman public workspaces so anyone can actually put it to work as part of their API governance efforts.