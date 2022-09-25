---
published: true
layout: post
title: 'API Life Cycle Basics: Database'
date: 2018-01-03T15:00:00.000Z
tags:
  - API Evangelist
  - Database
image: 'https://s3.amazonaws.com/kinlane-productions/bw-icons/bw-database-new.png'
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/bw-icons/bw-database-new.png" align="right" width="25%" style="padding: 15px" /></p>

_This is a series of stories I'm doing as part of [my API Transit work](http://basics.apievangelist.com/), trying to map out a simple journey that some of my clients can take to rethink some of the basics of their API strategy. I'm using a subway map visual, and experience to help map out the journey, which I'm calling [API transit](http://basics.apievangelist.com/)--leveraging the verb form of transit, to describe what every API should go through._

Deploying an API from a database is the most common approach to delivering APIs today. Most of the data resources we are making available to partners and 3rd party developers via APIs lives in a database behind our firewall(s). While we have seen database platform providers begin to take notice of the need to make data available using the web, most APIs get deployed through custom frameworks, as well as gateways that expose backend systems as web APIs.

If you are deploying APIs from a centralized legacy database, there will be significantly more security, performance, and other operational concerns than if your database is dedicated to providing a backend to your API. There are a growing number of open source tools for helping broker the relationship between your API and the database, as well as evolving services, and entire database platforms that are API-centric. Here are just a handful of what I'm seeing out there to support the database stop along an API journey.

- [DataBeam](https://github.com/GSA/DataBeam) - Generic RESTful Interface for databases.
- [Arrest-MySQL](https://github.com/alixaxel/ArrestDB/) - A plug-n-play RESTful API for your MySQL database.
- [Postgrest](https://github.com/begriffs/postgrest/) - REST API for any Postgres database.
- [Restheart](https://github.com/SoftInstigate/restheart) - RESTHeart, the automatic REST API Server for MongoDB.
- [NodeAPI](https://github.com/ealeksandrov/NodeAPI) - Simple RESTful API implementation on Node.js + MongoDB.
- [PHP CRUID API](https://github.com/mevdschee/php-crud-api) - Single file PHP script that adds a REST API to a SQL database
- [Google Cloud Spanner](https://cloud.google.com/spanner/) - loud Spanner is the first and only relational database service that is both strongly consistent and horizontally scalable.

There are many database to API tools and services available out there. There are also many cloud-native solutions available to help you generate APIs from your preferred cloud provider. Amazon, Azure, and Google all provide API deployment, and management solutions directly from their database solutions. The most difficult part about helping folks thinking about this stop along the API journey, is the many different scenarios for how data is stored, and the limitations on how that data can be made available via APIs.

Ideally you are starting from scratch with your API, and you can deploy a new database, with a brand new API layer exposing your data store within. If you are deploying from a legacy database which serves other systems and applications, I recommend thinking about replicating the database and creating read only instances for accessing via the API, or if if you need read / write capabilities, then take a look at many of the gateway solutions available today. Beyond that, if you have the skills to securely connect directly to your database, there are many more options on the table to help you get the job done in todays web-centric, data-driven world.
