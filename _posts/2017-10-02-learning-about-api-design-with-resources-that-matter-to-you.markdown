---
published: true
layout: post
title: Learning About API Design With Resources That Matter To You
date: 2017-10-02T11:00:00.000Z
tags:
  - API Evangelist
  - Design
  - Schema
  - Definitions
  - Github
  - Education
image: >-
  https://s3.amazonaws.com/kinlane-productions/hack-education/hack-education-data.png
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/hack-education/hack-education-data.png" align="right" width="35%" style="padding: 15px;" /></p>I have been helping my partner in crime Audrey Watters ([@audreywatters](https://twitter.com/audreywatters)) evolve her data work as part of her Columbia Spencer Education Journalism Fellowship, where she is publishing [a wealth of ed-tech funding data to Github](https://github.com/hack-education-data/). I worked with her to evolve the schema she is using across the Google Sheet, and YAML data stores she is using. Something that will autogenerate APIs (well dynamic JSON) based upon the filename, and the fields she chooses as part of her data stores. I just planted the seeds, and she has been cranking away creating repos, and building data stores since this last summer.

She mentioned to me recently that she thought she had been being consistent in her naming conventions across her work, but had recently noticed some inconsistencies--realizing the importance of a consistent design and schema across the projects, something that really could become problematic at scale if she hadn't caught. Luckily she was able to fix with some work, and was back on track. She isn't as automated in the replication of data across her projects, but that is a good thing. It is forcing her to think more deeply about the naming and overall design of her static data APIs, which she uses across many repos, and displayed in a variety of lists, outlines, and stories she is telling around her work.

Audrey has spent seven years listening to me talk about API design blah blah blah, but until she was working with her own data, that she cared about, she didn't fully grasp some of the API design and implications of working with the access, reusability, and maintenance of data at scale. I've offered to automate more of the maintenance, replication, and standardization of data across her repos, but she's declined. She said she finds it valuable to work with the design, and naming of her data stores, for us in different projects. She likes keeping here YAML data stores in separate repos, and then working with them individually in specific uses cases. As part of her work, she has a master ed-tech investor data store, and API of investors behind each ed-tech company, but then when she aggregates for her wider ed-tech funding, she replicates and names (or renames) it to fit that project.

The work that she is doing is what I consider static API design, where the data is YAML or JSON on Github, but then each project dynamically generates JSON, XML, CSV, or RSS using Liquid, and then also generates HTML UI elements using Liquid as well. It's not full blown API design, and deployment, but the same API definition, schema, and design concerns come into plays, because if she isn't thoughtful, and consistent, she will feel the pain at some point at the client level (Liquid/Jekyll). Also, since she is doing this across so many repos, at some point she will begin feeling the pain at a pretty significant scale. However, since she actually cares about the data she is managing, it is important for her to take the time to do it right, and not always opt for automation, so that she can make sure she gets the design and schema details right. Something I wish more API data stewards would realize.
