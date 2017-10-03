---
published: true
layout: post
title: 'Database To Database Then API, Instead Of Directly To API'
date: 2017-10-03T09:00:00.000Z
tags:
  - API Evangelist
  - Database
  - Deployment
image: >-
  https://s3.amazonaws.com/kinlane-productions/amazon/database-to-database-api.png
---
<p><img src="https://s3.amazonaws.com/kinlane-productions/amazon/database-to-database-api.png" align="right" width="40%" style="padding: 15px;" /></p>I am working with a team to expose a database as an API. With projects like this there can be a lot of anxiety in exposing a database directly as an API. Security is the first one, but in my experience, most of the time security is just cover for anxiety about a messy backend. The group I'm working with has been managing the same database for over a decade, adding on clients, and making the magic happen via a whole bunch of databases and table kung fu. Keeping this monster up and running has been priority number one, and evolving, decentralizing, or decoupling has never quite been a priority.

The database team has learned the hard way, and they have the resources to keep things up and running, but never seem to have them when it comes to refactoring it and thinking differently, let alone tackling the delivery of a web API on top of things. There will need to be a significant amount of education and training around REST, and doing APIs properly before we can move forward, something there really isn't a lot of time or interest in doing. To help bridge the gap I am suggesting that we do an entirely new API, with it's own database, and we focus on database to database communication, since that is what the team knows. We can launch an Amazon RDS instance, with an EC2 instance running the API, and the database team can work directly with RDS (MySQL) which they are already familiar with.

We can have a dedicated API team handle the new API and database, and the existing team can handle the syncing from database to database. This also keeps the messy, aggregate, overworked database out of reach of the new API. We get an API. The database team anxiety levels are lowered. It balances things out a little. Sure there will still be some work between databases, but the API can be a fresh start, and it won't be burdened by the legacy. The database to database connection can carry this load. Maybe once this pilot is done, the database team will feel a little better about doing APIs, and be a little more involved with the next one.

I am going to pitch this approach in coming weeks. I'm not sure if it will be well received, but I'm hoping it will help bridge the new to the old a little bit. I know the database team likes to keep things centralized, which is one reason they have this legacy beast, so there might be some more selling to occur on that front. Doing APIs isn't always about the technical. It is often about the politics of how things get done on the ground. Many organizations have messy databases, which they worry will make them look bad when any of it is exposed as an API. I get it, we are all self-conscious about the way our backends look. However, sometimes we still need to find ways to move things forward, and find compromise. I hope this database to database, then to API does the trick.
