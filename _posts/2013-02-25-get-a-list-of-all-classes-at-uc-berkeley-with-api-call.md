---
layout: post
title: 'Get A List Of All Classes At UC Berkeley With API Call'
url: http://apievangelist.com2013/02/25/get-a-list-of-all-classes-at-uc-berkeley-with-api-call/
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/blog/berkeley-api-central.png
---
{% include JB/setup %}
<p>
     <a href="https://developer.berkeley.edu/" target="_blank"><img src="https://s3.amazonaws.com/kinlane-productions/api-evangelist/university/uc-berkeley/berkeley-api-central.png"  width="200" align="right" /></a>
</p>
<p>
     I see a lot of dead simple, yet meaningful uses of APIs come across my desk (I don’t have a desk, why do I keep saying this?) each day. One I saw today is something every school, whether K-12, college or university should have.
</p>
<p>
     Using the UC Berkeley API, you can get a list of all departments:
</p>
<blockquote>
     <em>_curl -v -X GET "https://apis-dev.berkeley.edu/cxf/asws/department?departmentCode=a&amp;app_id=309fe68e&amp;app_key=51b9d67dc4f0501eed763822a641b17b"_</em>
</blockquote>
<p>
     Then with the proper department code you can pull a list of classes:
</p>
<blockquote>
     <em>_curl -v -X GET "https://apis-dev.berkeley.edu/cxf/asws/classoffering?departmentCode=ARCH&amp;app_id=your-id&amp;app_key=your-key"_</em>
</blockquote>
<p>
     With the proper keys, anyone can easily pull relevant UC Berkeley department and class data to use in website or app, or even populate a Google Spreadsheet for other purposes.
</p>
<p>
     <a href="https://developer.berkeley.edu/" target="_blank"><img src="https://s3.amazonaws.com/kinlane-productions/api-evangelist/university/uc-berkeley/uc-berkeley-get-classes.jpg"  width="325" align="right" /></a>
</p>
<p>
     The <a title="UC Berkeley API Management" href="https://developer.berkeley.edu/">UC Berkeley API Management Portal</a> is brand new, I’m still working on separate story regarding their approach, but I wanted to talk about how good it is to see such straightforward, valuable uses of an API at a leading university.
</p>
<p>
     This simple example is something you should be able to do by default at all schools across the country.
</p>
<p>
     The best part is that the API team is actively communicating these uses of the API on Google+, which is how I came across the story.
</p>
