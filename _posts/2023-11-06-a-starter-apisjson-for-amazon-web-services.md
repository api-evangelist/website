---
published: true
layout: post
title: 'A Starter APIs.json for Amazon Web Services'
image: https://s3.amazonaws.com/kinlane-productions2/algorotoscope-master/america-immigration_dumping-ground-seatlle-shipping-mountain.jpg
author:
    name: kinlane
tags:
- Cloud
- Storage
- Compute
- Amazon Web Services
- APIs.json
---
I need a master [APIs.json](https://apisjson.org/) for Amazon Web Services. I need an index of all the AWS APIs I depend on, and would like to have an index of the rest when I am ready to put to work. It is a daunting challenge to hand-craft an operational index of AWS, but I gotta start somewhere, so I headed over to the [APIs.json Builder](http://builder.apisyaml.org/) and added the name, description, and URL for the AWS developer portal.

Ok, what now? Where do you start mapping out the sprawling AWS API landscape? Well, you start where they started, with Amazon S3 and EC2. So I got to work adding names, descriptions, and tags for each of these APIs. There aren’t official OpenAPI for AWS, I’d have to generate them using [Smithy](https://smithy.io/2.0/index.html), but my friends over at APIs.guru do, so I just link over there for the OpenAPIs for S3 and EC2. Then I got to work adding a handful of common properties that apply across all of the APIs, resulting in the following APIs.json (YAML). 

```
# Metadata about API
name: Amazon Web Services
description: Amazon Web Services, Inc. is a subsidiary of Amazon that provides on-demand
  cloud computing platforms and APIs to individuals, companies, and governments, on
  a metered, pay-as-you-go basis. Clients will often use this in combination with
  autoscaling.

image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
url: https://aws.amazon.com/
created: 2023/11/6
modified: 2023/11/6
specificationVersion: '0.16'

tags:

- APIs
- Cloud

# All APIs in this Index
apis:

- name: Amazon S3
  description: Amazon Simple Storage Service (Amazon S3) is an object storage service
    offering industry-leading scalability, data availability, security, and performance.
    S3 is built to store and retrieve any amount of data from anywhere. Customers
    of all sizes and industries can store and protect any amount of data for virtually
    any use case, such as data lakes, cloud-native applications, and mobile applications.
  image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
  humanURL: https://aws.amazon.com/s3/?nc2=h_ql_prod_st_s3
  baseURL: https://s3.Region.amazonaws.com
  
  tags:

  - Storage

  properties:

  - type: Documentation
    url: https://docs.aws.amazon.com/AmazonS3/latest/API/Welcome.html
  - type: OpenAPI
    url: https://api.apis.guru/v2/specs/amazonaws.com/s3/2006-03-01/openapi.yaml
  
  contact:

  - FN: AWS Support
    url: https://aws.amazon.com/premiumsupport/?nc1=f_dr

- name: Amazon EC2
  description: This is the description of your API.
  image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
  humanURL: https://aws.amazon.com/ec2/?nc2=h_ql_prod_fs_ec2
  baseURL: https://ec2.region.amazonaws.com
  
  tags:

  - Compute
  
  properties:

  - type: Documentation
    url: https://docs.aws.amazon.com/AWSEC2/latest/APIReference/Welcome.html
  - type: OpenAPI
    url: https://api.apis.guru/v2/specs/amazonaws.com/ec2/2016-11-15/openapi.yaml
  contact:
  - FN: AWS Support
    url: https://aws.amazon.com/premiumsupport/?nc1=f_dr
    email: ''

# The common properties across APIs.
common:

- type: Getting Started
  url: https://aws.amazon.com/getting-started/?nc1=f_cc
- type: SDKs
  url: https://aws.amazon.com/developer/tools/?nc1=f_dr
- type: Blog
  url: https://aws.amazon.com/blogs/?nc1=f_cc
- type: Support
  url: https://aws.amazon.com/premiumsupport/?nc1=f_dr
- type: LinkedIn
  url: https://www.linkedin.com/company/amazon-web-services/
- type: Whats New
  url: https://aws.amazon.com/new/?nc1=f_cc
- type: SignUp
  url: https://portal.aws.amazon.com/billing/signup
- type: Login
  url: https://signin.aws.amazon.com/signin
- type: Terms of Service
  url: https://aws.amazon.com/serviceterms/
- type: Privacy Policy
  url: https://aws.amazon.com/privacy/

# Who Maintains This APIs.json
maintainers:

- FN: API Evangelist
  url: https://apievangelist.com
  email: info@apievangelist.com
```

I will try to add more APIs whenever I have time, and I will keep adding some of the other common properties they have. API pioneers like AWS help me push forward what some of the forward leaning API property types can be for APIs.json, so I like indexing these. My goal in doing this work is not just to create the resulting APIs.json, but is also about what I learn along the way about how API producers are managing their ecosystems. 

You submit a PR or issue on the [APIs.json repository where I am managing this work](https://github.com/apis-json/artisanal). I am probably going to move onto other APIs like Azure, Google, and the high profile ones who have a lot of APIs, before I get back to AWS to add more. My goal is to establish an APIs.json for many of the top APIs, then increase the number of APIs indexed for each provider. I learn more by looking at different providers than I do with the busy work of adding many APIs for each provider. I am looking to push forward APIs.json property types with this work, while also trying to establish a rich index of APIs, as a secondary objective.