---
title: Making Machine Learning Accessible To Spreadsheet Power Users
date: 2017-06-21 09:00:00 Z
tags:
- Machine Learning
image: https://s3.amazonaws.com/kinlane-productions/algorithmia/AlgorithmiaSpreadsheets.png
---

<p><a href="https://blog.algorithmia.com/google-sheets-algorithmia-machine-learning-spreadsheets/"><img src="https://s3.amazonaws.com/kinlane-productions/algorithmia/AlgorithmiaSpreadsheets.png" align="right" width="40%" style="padding: 15px;" /></a></p>My friends [over at Algorithmia](https://algorithmia.com) are up to some good things--[making their algorithms available within a spreadsheet](http://blog.algorithmia.com/google-sheets-algorithmia-machine-learning-spreadsheets/). Algorithmia has created a set of open source scripts and walkthrough to help you inject the algorithms from their marketplace into your Google Spreadsheets.

They have seven useful algorithms to inject into spreadsheets:

* [Linear Detrend](https://algorithmia.com/algorithms/timeseries/LinearDetrend) – removes increasing or decreasing trends in time series
* [Autocorrelate](https://algorithmia.com/algorithms/timeseries/AutoCorrelate) – used to analyze the seasonality of a time series
* [Outlier Detection](https://algorithmia.com/algorithms/timeseries/OutlierDetection) – flags unusual data points
* [Forecast](https://algorithmia.com/algorithms/timeseries/Forecast) – predict a given time series into the future
* [Summarizer](https://algorithmia.com/algorithms/nlp/Summarizer) – creates a text summary by extracting key topic sentences
* [Social Sentiment Analysis](https://algorithmia.com/algorithms/nlp/SocialSentimentAnalysis) – assigns sentiment ratings of “positive”, “negative” and “neutral”
* [Count Social Shares](https://algorithmia.com/algorithms/web/ShareCounts) – returns the number of times that URL has been shared on various social media sites

[The Google scripts are available on Github](https://github.com/kenburcham/algorithmia-google), thanks to the hard work of Ken Burcham. It provides yet another interesting example of how a spreadsheet can be used as an API client but it also provides an interesting example of how machine learning API providers can get their ML warez in front of the average business user. Developers building applications with your ML APIs is one thing but getting the average business spreadsheet power user to put your ML API to work in their everyday workflow is a whole other world of API integration opportunity.

[I have been preaching the spreadsheet to API connection for a while now](http://spreadsheets.apievangelist.com/). I know that many API developers want to do away with the spreadsheet, but I think they would be better off focusing on injecting their API solutions into spreadsheets like Algorithmia is doing. When you are designing your algorithmic-centric APIs, providing access to your machine learning models, make sure you keep your APIs simple and doing one thing well like Algorithmia does, then your ML APIs can be injected into the spreadsheets around the globe that are driving business each day.

