---
layout: post
title: "AWS API Reference Architecture"
url: 'http://apievangelist.com/2013/02/13/aws-api-reference-architecture/'
image: 'http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/blog/aws-ecommerce-reference-architecture.png'
---

<img class="c1" src="https://s3.amazonaws.com/kinlane-productions/api-evangelist/aws/aws-ecommerce-reference-architecture.png" alt="" width="300" align="right" />

I was checking out the [updates to the AWS Reference Architecture][1], where they provide blueprints for how you can use AWS. In this version AWS provides an e-commerce architecture reference--providing a system overview, a detailed architectural diagram, and a list of the AWS services used in the architectural approach.

The AWS e-commerce architecture reference provides three separate areas:

  * **Web Frontend** \- This is a reference architecture for the web frontend of an e-commerce site. It makes use of Route 53, CloudFront, Elastic Beanstalk, S3, ElastiCache, DynamoDB and CloudSearch
  * **Checkout Pipeline** \- This is a reference architecture for a secure and highly available checkout pipeline service for an e-commerce site. It uses the Virtual Private Cloud, the Simple Workflow Service, Elastic Beanstalk, the Relational Database Service, and the Simple Email Service
  * **Marketing **

   [1]: http://aws.typepad.com/aws/2013/02/three-new-aws-reference-architectures-for-e-commerce.html
