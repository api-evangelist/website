---
title: Serverless Blueprints For Your API
date: 2017-06-16 11:00:00 Z
tags:
- Serverless
- API Evangelist
- Documents
- Storage
- Wholesale
image: https://s3.amazonaws.com/kinlane-productions/amazon/lambda_find_box_blue_1.png
---

<p><img src="https://s3.amazonaws.com/kinlane-productions/amazon/lambda_find_box_blue_1.png" width="40%" align="right" style="padding: 15px" /></p>[Serverless](http://serverless.apievangelist.com/) is spreading across the API sector, and is something that leading API providers are beginning to embrace as part of their operations. I saw an interesting example of this out of AWS and Box lately, with [the announcement of Lambda blueprints and code for integrating with the Box API via the AWS platform](https://aws.amazon.com/blogs/aws/box-platform-on-aws-marketplace-lambda-blueprints-sample-code/).

The Box serverless blueprints show you how to call the Box APIs and connect a Box webhook to a Lambda function via the Amazon API Gateway--providing some pretty interesting use cases for using Box via serverless functions:

* [Manage User Authentication with Box Platform using Amazon Cognito](https://medium.com/box-developer-blog/manage-user-authentication-with-box-platform-using-amazon-cognito-8828b5f1d1c9) – How to use Amazon Cognito to power a login page for application users. 
* [Add Deep Learning-based Image Recognition to your Box App with Amazon Rekognition](https://medium.com/box-developer-blog/add-deep-learning-based-image-recognition-to-your-box-app-with-amazon-rekognition-1878ab148b70) – How to build an image tagging application that is powered by Amazon Rekognition.

They are some pretty basic use cases, but it is the approach that opens up an entirely new door for API integration for me--Serverless Development Kits (SDK). Every API providers should have a whole catalog of open source serverless scripts that are deployable to Lambda, and other serverless platforms. [Of course, there are one-click buttons deploy each individual script to the cloud platform of your choice](http://apievangelist.com/2016/09/12/where-is-the-deploy-to-aws-and-google-button/). 

I'm diving into the other side of this story for me, where Box is embracing a tighter coupling with the AWS platform as part of their operations. [I am looking at how Box is providing a copy of the Box API for deployment on AWS](https://aws.amazon.com/marketplace/pp/B06XY1XHGV/?ref=_ptnr_awsblg). This all reflects how I see things working in the future, where you can deploy individual API integration scripts, as well as deploy APIs to a serverless environment like this--empowering anyone to become both API consumer and provider via the AWS, or any other cloud ecosystem.