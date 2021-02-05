---
published: true
layout: post
title: How Do You Ask Questions Of Data Using APIs?
date: 2017-12-01T11:00:00.000Z
tags:
  - API Evangelist
  - Data
  - Database
  - Machine Learning
  - Design
image: >-
  https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories-new/27_93_800_500_0_max_0_-5_-5.jpg
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/algo-rotoscope/stories-new/27_93_800_500_0_max_0_-5_-5.jpg" align="right" width="45%" style="padding: 15px;"></p>I'm preparing to publish a bunch of transit related data as APIs, for us across a number of applications from visualizations to conversation interfaces like bots and voice-enablement. As I'm learning about the data, publishing it as unsophisticated CRUD APIs, I'm thinking deeply about how I would enable others to ask questions of this data using web APIs. I'm thinking about the hard work of deriving visual meaning from specific questions, all the way to how would you respond to an Alexa query regarding transit data in less than a second. Going well beyond what CRUD gives us when we publish our APIs and taking things to the next level.

Knowing the technology sector, the first response I'll get is machine learning! You take all your data, and you train up some machine learning models, put some natural language process to work, and voila, you have your answer to how you provide answers. I think this is a sensible approach to many data sets, and for organizations who have the machine learning skills and resources at their disposal. There are also a growing number of SaaS solutions for helping put machine learning work to answer complex questions that might be asked of large databases. Machine learning is definitely part of the equation for me, but I'm not convinced it is the answer in all situations, and it might not always yield the correct answers we are always looking for.

After machine learning, and first on my list of solutions to this challenge is API design. How can I enable a domain expert to pull out the meaningful questions that will be asked of data, and expose as simple API paths, allowing consumers to easily get at the answers to questions. I'm a big fan of this approach because I feel like the chance we will get right answers to questions will be greater, and the APIs will help consumers understand what questions they might want to be asking, even when they are not domain experts. This approach might be more labor intensive than the magic of machine learning, but I feel like it will produce much higher quality results, and better serve the objectives I have for making data available for querying. Plus, this is a lower impact solution, allowing more people to implement, who might not have the machine learning skills or resources at their disposal. API design using low-cost web technology, makes for very accessible solutions.

Whether you go the machine learning or artisanal domain expert API design route, there has to be a feedback loop in place to help improve the questions being asked, as well as the answers being given. If there is no feedback loop, the process will never be improved. This is what APIs excel at when you do them properly. The savvy API platform providers have established feedback loops for API consumers, and their users to correct answers when they are wrong, learn how to ask new types of questions, and improve upon the entire question and answer life cycle. I don't care whether you are going the machine learning route, or the API design route, you have to have a feedback loop in place to make this work as expected. Otherwise it is a closed loop system, and unlikely to give the answers people are looking for.

For now, I'm leaning heavily on the API design route to allow for my consumers to ask questions of the data I'm publishing as APIs. I'm convinced of my ability to ask some sensible questions of the data, and expose as simple URLs that anyone can query, and then evolve forward and improve upon as time passes. I just don't have the time and resources to invest in the machine learning route at this point. As the leading machine learning platforms evolve, or as I generate more revenue to be able to invest in these solutions I may change my tune. However, for now I'll just keep publishing data as simple web APIs, and crafting meaningful paths that allow people to ask questions of some of the data I'm coming across locked up in zip files, spreadsheets, and databases.
