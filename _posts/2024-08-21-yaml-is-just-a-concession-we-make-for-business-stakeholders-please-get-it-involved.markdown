---
published: true
layout: post
title: 'YAML is a Concession We Make for Business Stakeholders — Please Get Involved'
tags:
  - YAML
  - Business
image: https://kinlane-productions2.s3.amazonaws.com/algorotoscope-master/eugenics-baggage-department.jpg
---
I hear a lot of complaints from developers about the usage of YAML when it comes to defining APIs. I have a pretty strong design and develop time YAML, and build and run time JSON philosophy in my work. I use YAML to define, configure, and validate EVERYTHING until it reaches a state where it is building, deploying, and operating as part of runtime—-then it is all JSON. I do this as a concession for business stakeholders, to help them get more involved in the design and development of APIs.

YAML and JSON are the same thing minus some brackets and quotes. Well, if you are a developer, you likely know that isn’t entirely true. There are some gotchas in there, but for the sake of discussion, and for 95% of the work people are going to do with OpenAPI and other schema used across the API lifecycle-—this holds true. YAML is just easier to read, edit, and play with than JSON, but in the end JSON is more precise. I tend to settle complaints from developers about JSON vs YAML with a gentle reminder about this being a concession for business stakeholders—-deal with it. If developers keep complaining, I mentioned we could go back to XML, it is actually more precise than JSON. ;-) 

I find that YAML hating is more about gate keeping and preventing business stakeholders from getting involved than it is ever about precision. So, please stop it developers. For business stakeholders, we are making this concession for you to help lower the bar and make it easier for you to get involved with defining the business and technical contract for the APIs you depend on to do business—-so please get involved. YAML is simply an outline, but something that can be validated according to an agreed upon structure using JSON Schema. I will be doing more writing about YAML and why it is just one part of the bridge between business and IT, and part of a larger effort to align the product with engineering when delivering high quality consistent APIs.