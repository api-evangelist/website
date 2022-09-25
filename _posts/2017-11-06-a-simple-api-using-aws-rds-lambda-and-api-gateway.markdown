---
published: true
layout: post
title: 'A Simple API Using AWS RDS, Lambda, and API Gateway'
date: 2017-11-06T13:00:00.000Z
tags:
  - API Evangelist
image: >-
  https://s3.amazonaws.com/kinlane-productions/amazon/api-gateway/aws-rds-lambda-api-gateway.jpg
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/amazon/api-gateway/aws-rds-lambda-api-gateway.jpg" align="right" width="45%" style="padding: 15px;" /></p>[I wrote about a simple API with AWS DynamoDB, Lambda, and API Gateway last week](http://apievangelist.com/2017/10/23/a-simple-api-with-aws-dynamodb-lambda-and-api-gateway/). I like this approach because of the simple nature of AWS DynamoDB. One benefit of going this route is that you can even bypass Lambda, as the AWS API Gateway can work directly with AWS DynamoDB API. I'm just playing around with different configurations and pushing forward my understanding of what is possible, and this week I switched out the database in this with AWS RDS, which opens up the ability to use MySQL or Postgres as the backend for any API.

For this example, I'm using a simple items database, which you can build with this SQL script after you fire up an RDS instance (I'm using MySQL):

<script src="https://gist.github.com/kinlane/f428a30c1a6a59718657cafd8e52f615.js"></script>

Next I wanted to have the basic CRUD operations for my API. I opted to use Node.js running in Lambda for the code layer of this API, starting with the ability to get all records from the database:

<script src="https://gist.github.com/kinlane/4afdde612d31d50b0fed2658ba73df29.js"></script>

After that I want to be able to insert new records:

<script src="https://gist.github.com/kinlane/36eb527dbd5e843f9f3a3c954302245c.js"></script>

Then of course be able to get a single record:

<script src="https://gist.github.com/kinlane/f1fc319aefa7dbde63b2f914f998d7e6.js"></script>

Then be able to update a single record:

<script src="https://gist.github.com/kinlane/17dd4cfb0c1bef1fefc132a5b4d20c7d.js"></script>

And of course I want to be able to delete records:

<script src="https://gist.github.com/kinlane/80b6d50b16097be5b5ae91b183c041b7.js"></script>

Now that I have the business logic setup in AWS Lambda for reading, and writing data to my relational database I want an API front-end for this backend setup. I am using AWS API Gateway as the API layer, and to setup I'm just importing an OpenAPI definition to jumpstart things:

<script src="https://gist.github.com/kinlane/73bda5467abe7428e9de93e47e774849.js"></script>

This gives me the skeleton framework for my API, with the paths and methods I need to accomplish the basics of reading and writing data. Now, I just need to wire up each API method to its accompanying Lambda function, something API Gateway makes easy.

<p><img src="https://s3.amazonaws.com/kinlane-productions/amazon/api-gateway/aws-api-gateway-lambda.png" /></p>

Now I have an API for my basic backend. There is one thing you have to do to make each method work properly with the Lambda function. You have to setup a body mapping to the item_id when passed in the path for the PUT, GET, and DELETE functions. If you don't the item_id won't be passed on to the Lambda function--it took me a while to get this one. There are other things you have to do, like setting up a usage plan, turning on API key access for each API, and setting up custom domain if you want, but hopefully this simple gets the point across. I will work on other parts in future posts. Hopefully it provides a basic example of an API using RDS, Lambda, and API Gateway, which is something I have wanted to have in my toolbox for some time.

The process has opened my eyes up wider to the serverless world, as well as playing more with Node.js--which has been on my list for some time now. It provides a pretty solid, scalable, manageable way to deploy an API using AWS. I have all the code on Github, and will be evolving as I push it forward. If you apply the Lambda scripts, make sure you upload individually as zipped files, so that the mysql dependencies are there, otherwise the script won't connect to the database. It should provide a base template you can use to seed any basic data API. This is why I've added it to my API Evangelist toolbox, giving me a simple, forkable set of scripts I can use as a seed for any new API. I will add more scripts and templates to it over time, rounding off the functionality as I evolve in my understanding of deploying API using AWS RDS, Lambda, and API Gateway.
