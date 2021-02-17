---
published: true
layout: post
title: 'The Child Welfare Digital Services (CWDS) Certification, Approval, and'
image: https://s3.amazonaws.com/kinlane-productions2/child-welfare-digital-services-california/child-welfare-digital-services.png
---

<p><img src="https://s3.amazonaws.com/kinlane-productions2/child-welfare-digital-services-california/child-welfare-digital-services.png" align="right" width="45%" style="padding: 15px;" />
<p>My partner Chris Cairns(<a href="https://twitter.com/cscairns">@cscairns</a>) over at <a href="https://skylight.digital/">Skylight</a> sent me a link to <a href="https://github.com/ca-cwds">the Child Welfare Digital Services (CWDS) Certification, Approval, and Licensing Services (CALS) API on Github</a> the other day. The API isn’t your traditional public API, but shows what is possible when it comes to APIs at government agencies. The group behind the API has published their <a href="https://cwds.ca.gov/digital_service_design_standards">Digital Service Development Standards</a>, and is actively using <a href="https://github.com/ca-cwds/cals-api/wiki">a Github Wiki to layout the API strategy for the organization</a>.

<p>To give some backround, the Child Welfare Digital Services (CWDS) is for <em>“state and county workers who ensure that safe and quality licensed facilities and approved homes are available for the children and nonminor dependents who need them, the CALS Digital Service Team will facilitate activities related to ensuring that licensed facilities, approved homes and associated adults meet and maintain required standards.”</em> It makes me happy to see that they are investing so heavily in API, in support of such a worthy cause.

<p>Looking around their wiki I found a handful of APIs:

<ul>
  <li><a href="https://github.com/ca-cwds/cals-api/wiki/Facility-Resource"><strong>Facility</strong></a></li>
  <li><a href="https://github.com/ca-cwds/cals-api/wiki/Facility-Children-Resource-v1"><strong>Facility Children</strong></a></li>
  <li><a href="https://github.com/ca-cwds/cals-api/wiki/Facility-Complaints-Resource"><strong>Facility Complaint</strong></a></li>
  <li><a href="https://github.com/ca-cwds/cals-api/wiki/Facility-Inspections-Resource-v1"><strong>Facility Inspections</strong></a></li>
</ul>

<p>You can also find more about their development process, data model, and approach to security on the Github Wiki for the organization. After looking around more at their Github organization, I found a handful of other operational APIs:

<ul>
  <li><a href="https://github.com/ca-cwds/API"><strong>Modules API</strong></a></li>
  <li><a href="https://github.com/ca-cwds/intake_api"><strong>Intake API</strong></a></li>
  <li><a href="https://github.com/ca-cwds/case-management-api"><strong>Case Management API</strong></a></li>
  <li><a href="https://github.com/ca-cwds/dms-api"><strong>Document Management API</strong></a></li>
  <li><a href="https://github.com/ca-cwds/forms-api"><strong>Forms API</strong></a></li>
  <li><a href="https://github.com/ca-cwds/geo-services-api"><strong>Geo Services API</strong></a></li>
</ul>

<p>There was also a <a href="https://github.com/ca-cwds/api-core">Core API</a> which they use as a base across all API projects, standardizing how they do things. Smart! I also found their testing strategy worthy of noting, just so I can add to my research.

<ul>
  <li><strong>Integration Testing</strong> - To run Integration tests set property cals.api.url to point to environment host. Use gradle integrationTest task. In this case token will be generated for default test user, so it’s possible to test environment with Perry running in dev mode.</li>
  <li><strong>Smoke Testing</strong> - Smoke test suite is part of integration tests. Set cals.api.url, use gradle smokeTestSuite task. Smoke test endpoint is not protected by Perry.</li>
</ul>

<p>I like the style of the Child Welfare Digital Services (CWDS) team. They are investing heavily in APIs, and aren’t afraid of doing it out in the open. As it should be. It is important that ALL government agencies do this, so that other agencies can come along and build on their work, making government more efficient, and cost effective when getting business done. All of the APIs above can, and should be forked, and put to use across other child welfare organizations. I notice they are also using OpenAPI (fka Swagger), but haven’t published them as part of some of their projects. I will keep an eye on and update when they do–reuse of API definitions, is even more than reuse of code.

<p>If you know of any government agency who is this progressive, and publishing their API strategy, processes, definitions, and code on Github–please let me know! This type of behavior needs showcasing, and I like to have a wealth of references on my blog which I can cite as I’m traveling around speaking, and consulting with government agencies. This type of API efforts should be default across all city, county, state, and federal government agencies.


