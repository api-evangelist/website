---
published: true
layout: post
title: 'Role of Provenance in Dealing with API Change'
tags:
 - Provenance
 - Change
image: https://kinlane-productions2.s3.amazonaws.com/algorotoscope-master/uncle-sam-gauge-holding.jpg
---
Change is the great enemy of a successful API. There are many ways that change can erode the quality, performance, velocity, and trust with the APIs we have powering desktop, web, mobile, and artificial intelligence applications. The versioning of APIs is just the tip of this iceberg, and there are other properties of our API operations that can positively or negatively impact API operations as APIs change, the operations around them change, consumers using an API change, or the industries we operate in change around everything.

APIs have change baked into their DNA if you know where to look, with versioning just being one possible signal and mechanism for communicating change. This is why we version—to communicate change between API producer and consumer.  To help my customers manage change I am focused on twelve separate policy areas for API contracts that contribute to the overall change management discussion.

- **Repository** -  Having a single source of truth for API contracts is essential to tracking the provenance of an API across all of these properties.
- **Contracts** -  One of the primary purposes of having an APIs.json manifest for any API contract is to gather all the details of change over time.
- **Design** -  The design of your API will literally help you manage change better, influencing how you make changes and how consumers deal with change.
- **Use-cases** -  Establishing the who, what, how, and why of your API consumption provides you with clear guard rails for how you address change.
- **Versioning** -  Utilizing Semantic or date-based versioning to manage the change of APIs and communicate that change with your API consumers.
- **Road map** -  Providing a road map of features being planned for an API, with dates, versions, and details about what consumers can expect.
Change log** -  Translating your road map into a change log as things occur, providing an accurate record of the change that has occurred with an API.
- **SDKs** -  Your API design and the quality of your SDKs help act as shock absorbers for your API consumers when it comes to handling API change.
- **Support** -  The way you handle support with API consumers will define how you are able to support them during change, and measure quality of change.
- **Feedback** -  Ensuring API consumers have a feedback loop as part of change management helps provide insight into how to best handle future change.
- **Communication** -  The way that you communicate change to your API consumers will dictate future changes you plan to make, and make without incident.
- **Policies** -  Business aligned policies automated and enforced with rules help provide an incremental and selective way for managing change at scale.

These policy areas, and policies themselves represent some serious knobs and levers you can adjust to help you govern the quality, performance, and velocity of change across API operations. An important aspect of managing change is represented tactically with each policy area, but also strategically when you implement these policies across many areas of operations, but more importantly, you get business and technical stakeholders involved in the defining, applying, enforcing, and evolving these policies that manage change. It is a lofty concept, and it takes involvement and true participation by everyone across the enterprise—not just IT. If the technical side of things is investing across these areas, but business stakeholders aren’t involved, or can introduce change outside of these policies, none of this works.

Many technical folks will dismiss the role of an API contract in a repository that is tracking on all of these policies. Many business folks will dismiss their role in defining, applying, evolving, and enforcing an API contract in a repository—it is a technical thing. Both are wrong. For API lifecycle and governance to work you need business and technical stakeholders involved across all these areas of the API contracts powering the enterprise. You also need awareness and involvement of leadership at the strategic and policy level for this to work. Without it you don’t have governance, and the weight of your enterprise will come crashing into your governance team as it works to standardize things at the front door. Managing change requires a balanced business and engineering approach that is in alignment with consumers, and possess the provenance of change from day one—providing us with the breadcrumbs of how we all got here and where we are headed.