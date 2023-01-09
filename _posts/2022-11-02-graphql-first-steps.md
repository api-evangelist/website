---
published: true
layout: post
title: 'GraphQL: First steps'
image: /images/posts/2022-11-04-graphql-first-steps.jpg
author:
  name: pascal
tags:
- Data
- Metadata
- APIs
- GraphQL
- Postgres
---

I know little about [GraphQL](https://graphql.org/), but based on what I've seen so far, it is a very promising technology for providing access to data and delivering over open APIs. Unlike other API specifications whose focus is on services, GraphQL is data centric and essentially provides a standard way to query datasets and deliver schema documentation in machine actionable formats. So I'm very hyped about this but need to understand the current state of affairs and how far this can go.

It happens that I have an ongoing research project using a PostgreSQL database which I need to front-end with APIs, so this presented a good opportunity to experiment with some of the available GraphQL platforms, particularly the ones designed to work hand in hand with PostgreSQL. The core tables I need to query also embeds JSON fields so was curious to see how this integrates.

For this exercise, I deployed the three following servers: [Hasura](https://hasura.io/), [StepZen](https://stepzen.com), and [Graphile](https://www.graphile.org/). Here are highlights of my experience and findings.

### Hasura

Hasura cloud was a breeze to setup and I was up and running within literally a few minutes. Basically opened a free cloud account, punched in the server connection string, picked the views I wanted to expose, and the database was ready to query. A secure public endpoint was automatically generated which allowed me connect from a Postman collection. Note that I did not explore the option to run Hasura locally using Docker or deploy my own instance, which are available options.

### StepZen

StepZen took a bit longer to setup as, while the dashboard is in the cloud, the endpoint configuration is done on your local machine using an npm package. Straightforward to install and trivial to run if you're familiar and already have [node.js](https://nodejs.org/), but this may be a barrier for some users. 
StepZen support SQL servers like Postgres, as well as other backends like NOSQL databases, REST APIs, SOAP/XML, GraphQL. 
For the records I also bumped into a couple of technical issues, but the support team was very responsive on Discord and my concerns were quickly addressed. One advantage of StepZen is that you can also run a localhost and directly edit the schema definitions in the local schema file.

### Graphile
Graphile is not a cloud based solution, which I actually like, and is very easy to get going, just like StepZen assuming you're comfortable with node.js. The platform automatically assign names to the database tables and fields based on [inflection](https://www.graphile.org/postgraphile/inflection/) rules. Many runtime options are available to control how the server behaves and exposes database, and plugin / extension can be installed to add functionalities.

### Which one to use?

I have not found the answer to this yet. Besides record level queries, some of the things I need to be able to do include:

- Access from Postman collection
- Compute aggregated counts /frequencies
- Being able to filter based on properties stored in the JSON fields
- Extract properties and statistics from the JSON fields (a subset of the JSON)

All three servers were straightforward to access from Postman through their GraphQL endpoints (local or public with relevant API keys configured). But it turns out that none of my other requirements appear to be straightforward with GraphQL. 

The inability to out of the box compute aggregated counts with GraphQL surprised me a bit. I'm basically looking for an equivalent of `SELECT foo, count(*) from some_table group by foo order by foo` SQL like queries. There are various documented techniques or work around for this, typically involving creating new database views, GraphQL types, or using extensions.
If find them neither elegant nor practical as this seem like a natural operation, and an API should isolate from the behind the scene data store. 
This is unfortunate and something I hope the GraphQL community and implementers will aim to address.

Using JSON database fields is possible in Hasura to a certain extend, and the other platforms can be extended as well, but this requires quite a bit of work and is often dataset specific. This is certainly kind of a corner case need, but at the same time I was hoping for GraphQL to fairly naturally being able to achieve this.

I find Graphile to meet a lot of my needs, but I bumped into a wall with the JSON fields. Maybe plugins or extensions can help. Hasura is the easiest to setup and use, has good performance, and is a solid choice. StepZen may lag a bit behind in terms of maturity, but is backed by a dynamic and responsive team. So I'll keep experimenting and exploring options.

### What's next?

Where do I go from here? I have clearly a lot more to learn about GraphQL, and other platforms to evaluate. I also want to weight the benefits of a GraphQL approach vs traditional SQL database access, which allows me to perform all the queries I need, but does not come with an API. On that note, I did deploy a [PostgREST](https://postgrest.org) server, which offer an API on top of PostreSQL, but found out that aggregation queries unfortunately are not yet supported either. 

So I have not found the right tool for the job yet, and maybe this will require a mix of various technologies. But in a short time, I have gain quite a bit of insights and expertise around what GraphQL is about and what it can do. Unfortunately this initial experiment is for an internal R&D project so I can't share much more beyond this story. But I'm very much looking forward to repeat this with public datasets. So keep an eye out for future articles on GraphQL, as this is a high topic topic on my agenda. 
