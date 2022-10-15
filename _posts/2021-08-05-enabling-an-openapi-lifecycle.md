---
published: true
layout: post
title: 'Enabling the API Lifecycle with the Postman Platform'
image: https://apievangelist.com/images/openapi-lifecycle-1.jpg
tags:
 - Lifecycle
 - OpenAPI
---

I have been working to define the lifecycle of an OpenAPI defined API, and working establish a way to talk about, but also describe in a machine readable way the lifecycle of an API. One of the reasons I joined Postman was to be able to get more hands on with much of my work on defining the API lifecycle. I wanted to stop just talking about it, and actually move to demonstrating it, and the Postman platform provides a great way to think through this, and to help me with this exercise I created this crude composition from the application to help me think through the lifecycle for each API.

![](/images/openapi-lifecycle-1.jpg)

![](/images/openapi-lifecycle-2.jpg)

Postman capabilities for iterating upon an OpenAPI, but this visual snippets from across the application provide me with a range of capabilities that I can use to define the overall API lifecycle. These elements of the Postman API platform provide me with a range of ways to define the API lifecycle, but also provides me with the ability see what exists in the cracks or needs pulling out via the interface. Ultimately I am looking to nail down what a range of API definitions could be for the API lifecycle, and what a machine readable definition might be for helping us define this API lifecycle as part of an OpenAPI-defined API lifecycle. To help me leverage these Postman capabilities to do this, I extracted this key.


1. **Import** - Importing an OpenAPI definition into a workspace.
1. **Overview** - An overview for each individual OpenAPI.
1. **Editor** - Editing an OpenAPI definition in API builder.
1. **Versioning** - Applying semantic versioning to an OpenAPI.
1. **Change Log** - Providing a change log for the OpenAPI.
1. **Activity** - Provide list of activity involving the OpenAPI.
1. **Reporting** - Offering reporting on API and the lifecycle.
1. **Documentation** - Publishing documentation to support an API.
        
                
    1. **Reference** - Providing complete reference documentation for entire API.
        
                
    1. **Starter** - Providing starter documentation for new users to onboard.
        
                
    1. **Workflow** - Providing workflow documentation for business use cases.
        
            
    

1. **Mocking** - Publishing a mock server for an API using it’s OpenAPI.
1. **Testing** - Producing a set of tests for an API using it’s OpenAPI.
        
                
    1. **Contract** - Providing contract tests derived from OpenAPI.
        
                
    1. **Performance** - Providing performance tests derived from OpenAPI.
        
                
    1. **Security** - Providing performance tests derived from OpenAPI.
        
                
    1. **Other** - Providing other types tests derived from OpenAPI.
        
            
    

1. **Monitoring** - Monitoring an API using it’s OpenAPI.
1. **Watching** - Watching an OpenAPI to be notified of changes.
1. **Sharing** - Sharing an OpenAPI to another workspace.
1. **Comments** - Commenting on an OpenAPI or part of an OpenAPI.
1. **RBAC** - Applying role based authentication controls to an OpenAPI.
1. **Notifications** - Receiving notifications of changes to an OpenAPI.
1. **Code Generation** - Generating code in a variety of programming languages.
1. **Environments** - Providing environments for working with each API.
1. **Github Sync** - Syncing the OpenAPI to and from a Github repository.
1. **Gateway Sync** - Syncing the OpenAPI to AWS API Gateway (others too).
1. **Private Network** - Publishing the OpenAPI to the public API network.
1. **Public Network** - Publishing the OpenAPI to the private API network.
1. **Search** - Making an API discoverable as part of search.


I have already identified a few capabilities that are missing through some preliminary work, but this provides me with a good way to root my API lifecycle work in our API platform which is used by 15M developers. The next part of my API lifecycle extension work is to iterate through all of the API lifecycle(s) people shared with me as part of my "what is your API lifecycle?" tweetstorm and story. Pushing the Postman platform, and our definition of what the API lifecycle is or isn't helps me harden some of these definitions, while making sure my extension can actually support what is happening. With that in mind, here are range of API lifecycle definitions where I have played bingo with using the Postman platform.
### Lifecycle One

    
- **Design** - Iterating upn the surface area of each API using OpenAPI.
        
                
    - **(3) Editor** - Editing an OpenAPI using the API builder.
        
                
    - **Examples** - Really need some examples I can work from.
        
                
    - **Linting** - Linting of OpenAPI, JSON Schema, but also for governance.
        
                
    - **(14) Comments** - Having a conversation about the design.
        
                
    - **(12) Watching** - Watching to see any changes occur.
        
                
    - **(16) Notifications** - Receiving notifications about changes.
        
            
    

- **Mock** - Mocking the interface and data for an API being delivered.
        
                
    - **(9) Mocking** - Firing up mock server for an OpenAPI.
        
                
    - **Examples** - I will add more references to examples in my next iteration.
        
            
    

- **Document** - Providing human readable documentation for an API.
        
                
    - **(8) Documentation** - Definitely have documentation covered.
        
            
    

- **Test** - Ensuring there are tests present for each API.
        
            
    - **(10) Testing** - Providing the contract, performance, security, and other testing.
        
    

- **Deploy** - Bringing an API to life in any stage of development.
        
            
    - **(19) Github Sync** - Codegen, pipeline, and other elements could reside here.
        
            
    - **CD/CD** - I don't have the CI/CD integrations listed here, will add in next iteration.
        
            
    - **(20) Gateway Sync** - Syncing the OpenAPI to various stages using AWS API gateway.
        
            
    - **(17) Code Generation** - Generating code in a variety of programming languages.
        
    

- **Manage** - Managing the access to an API.
        
            
    - **Plan** - Need some sort of plan management reference and capability.
        
            
    - **Keys / Token** - Obtaining and renewing keys and tokens as part of access.
        
    

- **SDKs** - Generating code for use by consumers of an API.
        
            
    - **(17) Code Generation** - Generating code in a variety of programming languages.
        
    

- **Secure** - Locking down the surface area of an API and the access to resources.
        
            
    - **(10) Testing** - Producing a set of tests for an API using it’s OpenAPI.
        
    

- **Performance** - Testing the performance of each individual API.
        
                
    - **(10) Testing** - Producing a set of tests for an API using it’s OpenAPI.
        
            
    

- **Monitor** - Monitoring a variety of aspects of an APIs operation and lifecycle.
        
            
    - **(11) Monitoring** - Monitoring an API using it’s OpenAPI.
        
    

- **Evangelize** - Getting the word out about an API to consumers.
        
            
    - **(21) Private Network** - Making available by publishing or consuming an API within a private network.
        
            
    - **Partner Network** - Not a Postman capability yet, but something coming very soon.
        
            
    - **(22) Public Network** -  - Making available by publishing or consuming an API within a private network.
          
    


### Lifecycle Two

- **Explore** - I'd consider this just another word for discovery.
        
                
    - **(23) Search** - Jumping on the search and discovering if an API already exists.
        
                
    - **(21) Private Network** - Publishing or consuming an API within a private network.
        
                
    - **Partner Network** - Not a Postman capability yet, but something coming very soon.
        
                
    - **(22) Public Network** -  - Publishing or consuming an API within a private network.
           
                
    - **(7) Reporting** - Learning about new APIs through their development and usage via reporting.
             
                
    - **Workspace** - I am adding this, it wasn't explicity called out on the list, and sometimes it isn't just the API you are looking for it is the workspace around it.
        
                
    - **(19) Github Sync** - Adding this because repos play a critical role in the API discovery conversation.
        
            
    


- **Select** - This is an interesting one to think about.
        
                
    - **Fork** - Need to add a reference for forking into next iteration.
        
                
    - **(13) Sharing** - Sharing an OpenAPI to another workspace.
        
            
    

- **Model** - Modeling the objects being passed as part of requests and responses.
        
                
    - **(3) Editor** - Using the editor to model within the JSON SChema in the OpenAPI.
        
                
    - **(14) Comments** - Having a conversation about the models.
        
                
    - **(12) Watching** - Watching to see any changes to models occur.
        
                
    - **(16) Notifications** - Receiving notifications about changes to models.
                
            
    

- **Design** - Iterating upn the surface area of each API using OpenAPI.
        
                
    - **(3) Editor** - Editing an OpenAPI using the API builder.
        
                
    - **Examples** - Really need some examples I can work from.
        
                
    - **Linting** - Linting of OpenAPI, JSON Schema, but also for governance.
        
                
    - **(14) Comments** - Having a conversation about the design.
        
                
    - **(12) Watching** - Watching to see any changes occur.
        
                
    - **(16) Notifications** - Receiving notifications about changes.
        
            
    

- **Describe** - Not sure how to handle this one beyond editor, examples, and documentation.
        
                
    - **(3) Editor** - Editing an OpenAPI using the API builder.
        
                
    - **Examples** - Really need some examples I can work from.
        
                
    - **(8) Documentation** - Publishing documentation to support an API.
        
            
    

- **Sketch** - This one is very interesting, and pushes our concept of how this works.
        
                
    - **Visual Design** - Having a visual user interface for sketching out APIs.
        
            
    

- **Prototype** - Developing working examples of what an API does.
        
                
    - **(9) Mocking** - Rapidly designing APIs that work.
        
                
    - **Examples** - Being able to rapidly delivery examples with sample data.
        
            
    

- **Build** - Putting this in the same category as deploy.
        
                
    - **(20) Gateway Sync** - Syncing the OpenAPI to AWS API Gateway (others too).
        
                
    - **(19) Github Sync** - Syncing the OpenAPI to and from a Github repository.
        
                
    - **CI/CD** - Need to add our CI/CD to the next iteration.
        
            
    

- **Document** - Providing human readable documentation for an API.
        
                
    - **(8) Documentation** - Definitely have documentation covered.
        
            
    

- **Test** - Ensuring there are tests present for each API.
        
                
    - **(10) Testing** - Producing a set of tests for an API using it’s OpenAPI.
        
            
    

- **Secure** - Locking down the surface area of an API and the access to resources.
        
                
    - **(10) Testing** - Producing a set of tests for an API using it’s OpenAPI.
        
            
    

- **Deploy** - Bringing an API to life in any stage of development.
        
                
    - **(19) Github Sync** - Codegen, pipeline, and other elements could reside here.
        
                
    - **CD/CD** - I don't have the CI/CD integrations listed here, will add in next iteration.
        
                
    - **(20) Gateway Sync** - Syncing the OpenAPI to various stages using AWS API gateway.
        
                
    - **(17) Code Generation** - Generating code in a variety of programming languages.
        
            
    

- **Freeze** - Interesting to think about how this could be done.
        
                
    - Will explore the various aspects of what is needed to freeze.
        
            
    

- **Redirect** - This seems like a simple gateway or management layer need.
        
                
    - Will explore how to handle the redirecting of APIs.
        
            
    

- **Deprecate** - Shutting down an API for good and ceasing operation.
        
                
    - Need more work to describe what is involved with deprecation.
        
            
    

- **Donate** - Interesting concept focusing on where a deprecated API goes -- heaven? hell?
        
                
    - Need more work to describe what is involved with donation.
        
            
    


### Lifecycle Three

- **Develop** - Not entirely clear on what the difference between develop and deploy?
        
                
    - **(19) Github Sync** - Codegen, pipeline, and other elements could reside here.
        
                
    - **CD/CD** - I don't have the CI/CD integrations listed here, will add in next iteration.
        
                
    - **(20) Gateway Sync** - Syncing the OpenAPI to various stages using AWS API gateway.
        
                
    - **(17) Code Generation** - Generating code in a variety of programming languages.
        
            
    

- **Deploy** - Bringing an API to life in any stage of development.
        
                
    - **(19) Github Sync** - Codegen, pipeline, and other elements could reside here.
        
                
    - **CD/CD** - I don't have the CI/CD integrations listed here, will add in next iteration.
        
                
    - **(20) Gateway Sync** - Syncing the OpenAPI to various stages using AWS API gateway.
        
                
    - **(17) Code Generation** - Generating code in a variety of programming languages.
        
            
    

- **Document** - Providing human readable documentation for an API.
        
                
    - **(8) Documentation** - Definitely have documentation covered.
        
            
    

- **Regret** - I really like this stop along the API lifecycle.
        
                
    - **Alcohol** - You need to drink.
        
                
    - **Memory** - Maybe we can erase memory.
        
                
    - **Pain** - You will just have to suffer.
        
                
    - **Therapy** - Can API therapist be a new role?
        
            
    

- **Forget** - For some this will be hard, but for others really easy.
        
                
    - **Alcohol** - You need to drink.
        
                
    - **Memory** - Maybe we can erase memory.
        
                
    - **Pain** - You will just have to suffer.
        
                
    - **Therapy** - Can API therapist be a new role?
        
            
    

- **Sunset** - Consider this another word for deprecation.
        
                
    - Need more work to describe what is involved with deprecation.
        
            
    


### Lifecycle Four

- **Discovery** - Learning about, finding, and having your APIs be found.
        
                
    - **(23) Search** - Jumping on the search and discovering if an API already exists.
        
                
    - **(21) Private Network** - Publishing or consuming an API within a private network.
        
                
    - **Partner Network** - Not a Postman capability yet, but something coming very soon.
        
                
    - **(22) Public Network** -  - Publishing or consuming an API within a private network.
           
                
    - **(7) Reporting** - Learning about new APIs through their development and usage via reporting.
             
                
    - **Workspace** - I am adding this, it wasn't explicity called out on the list, and sometimes it isn't just the API you are looking for it is the workspace around it.
        
                
    - **(19) Github Sync** - Adding this because repos play a critical role in the API discovery conversation.
        
            
    

- **Define** - You can start with a documentation collection and evolve to be full blown OpenAPI.
        
                
    - **(3) Editor** - Editing an OpenAPI using the API builder.
        
                
    - **Examples** - Really need some examples I can work from.
        
                
    - **(8) Documentation** - Publishing documentation to support an API.
        
            
    

- **Enhance** - This really is a reflection and iteration upon the design process.
        
                
    - **(3) Editor** - Editing an OpenAPI using the API builder.
        
                
    - **Examples** - Really need some examples I can work from.
        
                
    - **Linting** - Linting of OpenAPI, JSON Schema, but also for governance.
        
                
    - **(14) Comments** - Having a conversation about the design.
        
                
    - **(12) Watching** - Watching to see any changes occur.
        
                
    - **(16) Notifications** - Receiving notifications about changes.
        
            
    

- **Design** - Iterating upn the surface area of each API using OpenAPI.
        
                
    - **(3) Editor** - Editing an OpenAPI using the API builder.
        
                
    - **Examples** - Really need some examples I can work from.
        
                
    - **Linting** - Linting of OpenAPI, JSON Schema, but also for governance.
        
                
    - **(14) Comments** - Having a conversation about the design.
        
                
    - **(12) Watching** - Watching to see any changes occur.
        
                
    - **(16) Notifications** - Receiving notifications about changes.
        
            
    

- **Implement** - Going to put this in same bucket as develop and deploy.
        
                
    - **(19) Github Sync** - Codegen, pipeline, and other elements could reside here.
        
                
    - **CD/CD** - I don't have the CI/CD integrations listed here, will add in next iteration.
        
                
    - **(20) Gateway Sync** - Syncing the OpenAPI to various stages using AWS API gateway.
        
                
    - **(17) Code Generation** - Generating code in a variety of programming languages.
        
            
    

- **Iterate** - This is just the continuation of the API design process.
        
                
    - **(3) Editor** - Editing an OpenAPI using the API builder.
        
                
    - **Examples** - Really need some examples I can work from.
        
                
    - **Linting** - Linting of OpenAPI, JSON Schema, but also for governance.
        
                
    - **(14) Comments** - Having a conversation about the design.
        
                
    - **(12) Watching** - Watching to see any changes occur.
        
                
    - **(16) Notifications** - Receiving notifications about changes.
        
            
    

- **Deprecate** - Shutting down an API for good and ceasing operation.
        
                
    - Need more work to describe what is involved with deprecation.
        
            
    

- **Delete** - Do we ever really delete? Maybe we should be archiving?
        
                
    - **Workspace** - Archive or delete the entire workspace with all assets.
        
            
    


### Lifecycle Five

- **Understand** - Wow, this is a pretty tall order with some discovery, but other learning.
        
                
    - **(23) Search** - Jumping on the search and discovering if an API already exists.
        
                
    - **(21) Private Network** - Publishing or consuming an API within a private network.
        
                
    - **Partner Network** - Not a Postman capability yet, but something coming very soon.
        
                
    - **(22) Public Network** -  - Publishing or consuming an API within a private network.
           
                
    - **(7) Reporting** - Learning about new APIs through their development and usage via reporting.
             
                
    - **Workspace** - I am adding this, it wasn't explicity called out on the list, and sometimes it isn't just the API you are looking for it is the workspace around it.
        
                
    - **(19) Github Sync** - Adding this because repos play a critical role in the API discovery conversation.
        
                
    - **Knowledge Center** - Send folks over to, or continue piping in knowledge from the knowledge center.
            
                
    - **Blueprints** - Create more blueprint workspaces, APIs, and collections for people to learn from.
            
            
    


- **Design** - Iterating upn the surface area of each API using OpenAPI.
        
                
    - **(3) Editor** - Editing an OpenAPI using the API builder.
        
                
    - **Examples** - Really need some examples I can work from.
        
                
    - **Linting** - Linting of OpenAPI, JSON Schema, but also for governance.
        
                
    - **(14) Comments** - Having a conversation about the design.
        
                
    - **(12) Watching** - Watching to see any changes occur.
        
                
    - **(16) Notifications** - Receiving notifications about changes.
        
            
    

- **Mock** - Mocking the interface and data for an API being delivered.
        
                
    - **(9) Mocking** - Firing up mock server for an OpenAPI.
        
                
    - **Examples** - I will add more references to examples in my next iteration.
        
            
    

- **Review** - This is interesting to consider, what types of gates, reviews, and milestones are there?
        
                
    - Need more consideration of how to impose a review process for an API.
        
            
    

- **Develop** - Not entirely clear on what the difference between develop and deploy?
        
                
    - **(19) Github Sync** - Codegen, pipeline, and other elements could reside here.
        
                
    - **CD/CD** - I don't have the CI/CD integrations listed here, will add in next iteration.
        
                
    - **(20) Gateway Sync** - Syncing the OpenAPI to various stages using AWS API gateway.
        
                
    - **(17) Code Generation** - Generating code in a variety of programming languages.
        
            
    

- **Secure** - Locking down the surface area of an API and the access to resources.
        
                
    - **(10) Testing** - Producing a set of tests for an API using it’s OpenAPI.
        
            
    

- **Document** - Providing human readable documentation for an API.
        
                
    - **(8) Documentation** - Definitely have documentation covered.
        
            
    

- **Flows** - Ok, now we are getting interesting with flows being part of the lifecycle.
        
                
    - **(8) Documentation** - Publishing documentation to support an API.
        
            
    

- **Deploy** - Bringing an API to life in any stage of development.
        
                
    - **(19) Github Sync** - Codegen, pipeline, and other elements could reside here.
        
                
    - **CD/CD** - I don't have the CI/CD integrations listed here, will add in next iteration.
        
                
    - **(20) Gateway Sync** - Syncing the OpenAPI to various stages using AWS API gateway.
        
                
    - **(17) Code Generation** - Generating code in a variety of programming languages.
        
            
    

- **Maintain** - This is really about just stay aware of an APIs operations and consumption.
        
                
    - **(11) Monitoring** - Monitoring an API using it’s OpenAPI.
        
                
    - **(12) Watching** - Understanding scope of who is watching.
        
                
    - **(7) Reporting** - Offering reporting on API and the lifecycle.
        
            
    

- **Support** - This gets into interesting territory for the API lifecycle.
        
                
    - **(5) Change Log** - Providing a change log for the OpenAPI.
        
                
    - **(6) Activity** - Provide list of activity involving the OpenAPI.
        
                
    - **(7) Reporting** - Offering reporting on API and the lifecycle.
        
                
    - **(11) Monitoring** - Monitoring an API using it’s OpenAPI.
        
                
    - **(14) Comments** - Commenting on an OpenAPI or part of an OpenAPI.
        
                
    - **(16) Notifications** - Receiving notifications of changes to an OpenAPI.
        
            
    

- **Evolve** - Considering this a continuation of the API design process.
        
                
    - **(3) Editor** - Editing an OpenAPI using the API builder.
        
                
    - **Examples** - Really need some examples I can work from.
        
                
    - **Linting** - Linting of OpenAPI, JSON Schema, but also for governance.
        
                
    - **(14) Comments** - Having a conversation about the design.
        
                
    - **(12) Watching** - Watching to see any changes occur.
        
                
    - **(16) Notifications** - Receiving notifications about changes.
        
            
    


- **Retire** - An interesting stage before deprecation of an API.
        
                
    - Need more work to describe what is involved with retirement.
        
            
    

- **Deprecate** - Shutting down an API for good and ceasing operation.
        
                
    - Need more work to describe what is involved with deprecation.
        
            
    


### Lifecycle Six

- **Design** - Iterating upn the surface area of each API using OpenAPI.
        
                
    - **(3) Editor** - Editing an OpenAPI using the API builder.
        
                
    - **Examples** - Really need some examples I can work from.
        
                
    - **Linting** - Linting of OpenAPI, JSON Schema, but also for governance.
        
                
    - **(14) Comments** - Having a conversation about the design.
        
                
    - **(12) Watching** - Watching to see any changes occur.
        
                
    - **(16) Notifications** - Receiving notifications about changes.
        
            
    

- **Mock** - Mocking the interface and data for an API being delivered.
        
                
    - **(9) Mocking** - Firing up mock server for an OpenAPI.
        
                
    - **Examples** - I will add more references to examples in my next iteration.
        
            
    

- **Challenge** - I like this, and definitely should be part of the API lifecycle.
        
                
    - **(14) Comments** - Having a conversation about the design.
        
                
    - **(12) Watching** - Watching to see any changes occur.
        
                
    - **(16) Notifications** - Receiving notifications about changes.
        
            
    

- **Document** - Providing human readable documentation for an API.
        
                
    - **(8) Documentation** - Definitely have documentation covered.
        
            
    

- **Develop** - Not entirely clear on what the difference between develop and deploy?
        
                
    - **(19) Github Sync** - Codegen, pipeline, and other elements could reside here.
        
                
    - **CD/CD** - I don't have the CI/CD integrations listed here, will add in next iteration.
        
                
    - **(20) Gateway Sync** - Syncing the OpenAPI to various stages using AWS API gateway.
        
                
    - **(17) Code Generation** - Generating code in a variety of programming languages.
        
            
    

- **Test** - Ensuring there are tests present for each API.
        
                
    - **(10) Testing** - Producing a set of tests for an API using it’s OpenAPI.
        
            
    

- **Deploy** - Bringing an API to life in any stage of development.
        
                
    - **(19) Github Sync** - Codegen, pipeline, and other elements could reside here.
        
                
    - **CD/CD** - I don't have the CI/CD integrations listed here, will add in next iteration.
        
                
    - **(20) Gateway Sync** - Syncing the OpenAPI to various stages using AWS API gateway.
        
                
    - **(17) Code Generation** - Generating code in a variety of programming languages.
        
            
    

- **Fix** - Interesting look at what is needed to keep APIs working.
        
                
    - **(11) Monitoring** - Monitoring an API using it’s OpenAPI.
        
                
    - **(3) Editor** - Editing an OpenAPI using the API builder.
        
                
    - **(14) Comments** - Having a conversation about the design.
        
                
    - **(12) Watching** - Watching to see any changes occur.
        
                
    - **(16) Notifications** - Receiving notifications about changes.
        
            
    


### Lifecycle Seven

- **Discover** - Learning about, finding, and having your APIs be found.
        
                
    - **(23) Search** - Jumping on the search and discovering if an API already exists.
        
                
    - **(21) Private Network** - Publishing or consuming an API within a private network.
        
                
    - **Partner Network** - Not a Postman capability yet, but something coming very soon.
        
                
    - **(22) Public Network** -  - Publishing or consuming an API within a private network.
           
                
    - **(7) Reporting** - Learning about new APIs through their development and usage via reporting.
             
                
    - **Workspace** - I am adding this, it wasn't explicity called out on the list, and sometimes it isn't just the API you are looking for it is the workspace around it.
        
                
    - **(19) Github Sync** - Adding this because repos play a critical role in the API discovery conversation.
        
            
    

- **Define** - You can start with a documentation collection and evolve to be full blown OpenAPI.
        
                
    - **(3) Editor** - Editing an OpenAPI using the API builder.
        
                
    - **Examples** - Really need some examples I can work from.
        
                
    - **(8) Documentation** - Publishing documentation to support an API.
        
            
    

- **Design** - Iterating upn the surface area of each API using OpenAPI.
        
                
    - **(3) Editor** - Editing an OpenAPI using the API builder.
        
                
    - **Examples** - Really need some examples I can work from.
        
                
    - **Linting** - Linting of OpenAPI, JSON Schema, but also for governance.
        
                
    - **(14) Comments** - Having a conversation about the design.
        
                
    - **(12) Watching** - Watching to see any changes occur.
        
                
    - **(16) Notifications** - Receiving notifications about changes.
        
            
    

- **Mock** - Mocking the interface and data for an API being delivered.
        
                
    - **(9) Mocking** - Firing up mock server for an OpenAPI.
        
                
    - **Examples** - I will add more references to examples in my next iteration.
        
            
    

- **Develop** - Not entirely clear on what the difference between develop and deploy?
        
                
    - **(19) Github Sync** - Codegen, pipeline, and other elements could reside here.
        
                
    - **CD/CD** - I don't have the CI/CD integrations listed here, will add in next iteration.
        
                
    - **(20) Gateway Sync** - Syncing the OpenAPI to various stages using AWS API gateway.
        
                
    - **(17) Code Generation** - Generating code in a variety of programming languages.
        
            
    

- **Deploy** - Bringing an API to life in any stage of development.
        
                
    - **(19) Github Sync** - Codegen, pipeline, and other elements could reside here.
        
                
    - **CD/CD** - I don't have the CI/CD integrations listed here, will add in next iteration.
        
                
    - **(20) Gateway Sync** - Syncing the OpenAPI to various stages using AWS API gateway.
        
                
    - **(17) Code Generation** - Generating code in a variety of programming languages.
        
            
    

- **Test** - Ensuring there are tests present for each API.
        
                
    - **(10) Testing** - Producing a set of tests for an API using it’s OpenAPI.
        
            
    

- **Communicate** - I like this one, because it helps bring the humans to the lifecycle.
        
                
    - **(12) Watching** - Watching an OpenAPI to be notified of changes.
        
                
    - **(14) Comments** - Commenting on an OpenAPI or part of an OpenAPI.
        
                
    - **(16) Notifications** - Receiving notifications of changes to an OpenAPI.
        
                
    - **(8) Documentation** - Publishing documentation to support an API.
        
            
    

- **Deprecate** - Shutting down an API for good and ceasing operation.
        
                
    - Need more work to describe what is involved with deprecation.
        
            
    

- **Delete** - Do we ever really delete? Maybe we should be archiving?
        
                
    - **Workspace** - Archive or delete the entire workspace with all assets.
        
            
    


### Lifecycle Eight

- **Strategy** - I like where this is going, and is the reason behind this work.
        
                
    - More to come on this one as I continue this work.
        
            
    

- **Design** - Iterating upn the surface area of each API using OpenAPI.
        
                
    - **(3) Editor** - Editing an OpenAPI using the API builder.
        
                
    - **Examples** - Really need some examples I can work from.
        
                
    - **Linting** - Linting of OpenAPI, JSON Schema, but also for governance.
        
                
    - **(14) Comments** - Having a conversation about the design.
        
                
    - **(12) Watching** - Watching to see any changes occur.
        
                
    - **(16) Notifications** - Receiving notifications about changes.
        
            
    

- **Document** - Providing human readable documentation for an API.
        
                
    - **(8) Documentation** - Definitely have documentation covered.
        
            
    

- **Mock** - Mocking the interface and data for an API being delivered.
        
                
    - **(9) Mocking** - Firing up mock server for an OpenAPI.
        
                
    - **Examples** - I will add more references to examples in my next iteration.
        
            
    

- **Development** - Not entirely clear on what the difference between develop and deploy?
        
                
    - **(19) Github Sync** - Codegen, pipeline, and other elements could reside here.
        
                
    - **CD/CD** - I don't have the CI/CD integrations listed here, will add in next iteration.
        
                
    - **(20) Gateway Sync** - Syncing the OpenAPI to various stages using AWS API gateway.
        
                
    - **(17) Code Generation** - Generating code in a variety of programming languages.
        
            
    

- **Test** - Ensuring there are tests present for each API.
        
                
    - **(10) Testing** - Producing a set of tests for an API using it’s OpenAPI.
        
            
    

- **Virtualization** - Going to call this an extension of the mocking bucket.
        
                
    - **(9) Mocking** - Firing up mock server for an OpenAPI.
        
                
    - **Examples** - I will add more references to examples in my next iteration.
        
            
    

- **Deploy** - Bringing an API to life in any stage of development.
        
                
    - **(19) Github Sync** - Codegen, pipeline, and other elements could reside here.
        
                
    - **CD/CD** - I don't have the CI/CD integrations listed here, will add in next iteration.
        
                
    - **(20) Gateway Sync** - Syncing the OpenAPI to various stages using AWS API gateway.
        
                
    - **(17) Code Generation** - Generating code in a variety of programming languages.
        
            
    

- **Secure** - Locking down the surface area of an API and the access to resources.
        
                
    - **(10) Testing** - Producing a set of tests for an API using it’s OpenAPI.
        
            
    

- **Monitor** - Monitoring a variety of aspects of an APIs operation and lifecycle.
        
                
    - **(11) Monitoring** - Monitoring an API using it’s OpenAPI.
        
            
    

- **Promotion** - Going to put this in the same bucket as evangelism.
        
                
    - **(21) Private Network** - Making available by publishing or consuming an API within a private network.
        
                
    - **Partner Network** - Not a Postman capability yet, but something coming very soon.
        
                
    - **(22) Public Network** -  - Making available by publishing or consuming an API within a private network.
          
            
    
        
- **Discovery** - Learning about, finding, and having your APIs be found.
        
                
    - **(23) Search** - Jumping on the search and discovering if an API already exists.
        
                
    - **(21) Private Network** - Publishing or consuming an API within a private network.
        
                
    - **Partner Network** - Not a Postman capability yet, but something coming very soon.
        
                
    - **(22) Public Network** -  - Publishing or consuming an API within a private network.
           
                
    - **(7) Reporting** - Learning about new APIs through their development and usage via reporting.
             
                
    - **Workspace** - I am adding this, it wasn't explicity called out on the list, and sometimes it isn't just the API you are looking for it is the workspace around it.
        
                
    - **(19) Github Sync** - Adding this because repos play a critical role in the API discovery conversation.
        
            
    

- **Manage** - Managing access to an API.
        
                
    - **Plan** - Need some sort of plan management reference and capability.
        
                
    - **Keys / Token** - Obtaining and renewing keys and tokens as part of access.
        
            
    
        
- **Change** - Going to put this in the same bucket as design.
        
                
    - **(3) Editor** - Editing an OpenAPI using the API builder.
        
                
    - **Examples** - Really need some examples I can work from.
        
                
    - **Linting** - Linting of OpenAPI, JSON Schema, but also for governance.
        
                
    - **(14) Comments** - Having a conversation about the design.
        
                
    - **(12) Watching** - Watching to see any changes occur.
        
                
    - **(16) Notifications** - Receiving notifications about changes.
        
            
    

- **Version** - This is the first mention of versioning in anyone's lifecycle. ;-)
        
                
    - **(4) Versioning** - Applying semantic versioning to an OpenAPI.
        
            
    


### Lifecycle Nine

    
- **Design** - Iterating upn the surface area of each API using OpenAPI.
            
                    
    - **(3) Editor** - Editing an OpenAPI using the API builder.
        
                    
    - **Examples** - Really need some examples I can work from.
        
                    
    - **Linting** - Linting of OpenAPI, JSON Schema, but also for governance.
        
                    
    - **(14) Comments** - Having a conversation about the design.
        
                    
    - **(12) Watching** - Watching to see any changes occur.
        
                    
    - **(16) Notifications** - Receiving notifications about changes.
        
                
    
        
- **Feedback** - Ensuring there is always a feedback loop present.
        
                
    - **(12) Watching** - Watching an OpenAPI to be notified of changes.
        
                
    - **(14) Comments** - Commenting on an OpenAPI or part of an OpenAPI.
        
                
    - **(16) Notifications** - Receiving notifications of changes to an OpenAPI.
        
                
    - **(8) Documentation** - Publishing documentation to support an API.
        
                
    - **Forks** - Need to have forking and pull requests as part of this.
        
            
    

- **Mock** - Mocking the interface and data for an API being delivered.
        
                
    - **(9) Mocking** - Firing up mock server for an OpenAPI.
        
                
    - **Examples** - I will add more references to examples in my next iteration.
        
            
    

- **User Research** - Ok, an entirely new way at looking at the lifecycle.
        
                
    - Need more "research" to flesh this one out.
        
            
    

- **Document** - Providing human readable documentation for an API.
        
                
    - **(8) Documentation** - Definitely have documentation covered.
        
            
    

- **Test** - Ensuring there are tests present for each API.
        
                
    - **(10) Testing** - Producing a set of tests for an API using it’s OpenAPI.
        
            
    

- **Pipeline** - Establishing reliable, repeatable pipelines for deployment.
        
                
    - **CD/CD** - I don't have the CI/CD integrations listed here, will add in next iteration.
        
                
    - **(10) Testing** - Producing a set of tests for an API using it’s OpenAPI.
        
                
    - **(18) Environments** - Providing environments for working with each API.
        
            
    


### Lifecycle Ten

- **Design** - Iterating upn the surface area of each API using OpenAPI.
        
                
    - **(3) Editor** - Editing an OpenAPI using the API builder.
        
                
    - **Examples** - Really need some examples I can work from.
        
                
    - **Linting** - Linting of OpenAPI, JSON Schema, but also for governance.
        
                
    - **(14) Comments** - Having a conversation about the design.
        
                
    - **(12) Watching** - Watching to see any changes occur.
        
                
    - **(16) Notifications** - Receiving notifications about changes.
        
            
    

- **Write** - Just another word for developing and API, since design was separate.
        
                
    - **(19) Github Sync** - Codegen, pipeline, and other elements could reside here.
        
                
    - **CD/CD** - I don't have the CI/CD integrations listed here, will add in next iteration.
        
                
    - **(20) Gateway Sync** - Syncing the OpenAPI to various stages using AWS API gateway.
        
                
    - **(17) Code Generation** - Generating code in a variety of programming languages.
        
            
    

- **Refactor** - Just a continuation of the API design process.
        
                
    - **(3) Editor** - Editing an OpenAPI using the API builder.
        
                
    - **Examples** - Really need some examples I can work from.
        
                
    - **Linting** - Linting of OpenAPI, JSON Schema, but also for governance.
        
                
    - **(14) Comments** - Having a conversation about the design.
        
                
    - **(12) Watching** - Watching to see any changes occur.
        
                
    - **(16) Notifications** - Receiving notifications about changes.
        
            
    

- **Refactor** - Just a continuation of the API design process.
        
                
    - **(3) Editor** - Editing an OpenAPI using the API builder.
        
                
    - **Examples** - Really need some examples I can work from.
        
                
    - **Linting** - Linting of OpenAPI, JSON Schema, but also for governance.
        
                
    - **(14) Comments** - Having a conversation about the design.
        
                
    - **(12) Watching** - Watching to see any changes occur.
        
                
    - **(16) Notifications** - Receiving notifications about changes.
        
            
    

- **Refactor** - Just a continuation of the API design process.
        
                
    - **(3) Editor** - Editing an OpenAPI using the API builder.
        
                
    - **Examples** - Really need some examples I can work from.
        
                
    - **Linting** - Linting of OpenAPI, JSON Schema, but also for governance.
        
                
    - **(14) Comments** - Having a conversation about the design.
        
                
    - **(12) Watching** - Watching to see any changes occur.
        
                
    - **(16) Notifications** - Receiving notifications about changes.
        
            
    


### Lifecycle Eleven

- **Align** - Ooooooh. This one is cool. How do you do this? 
        
                
    - **Teams** - Bringing teams together?
        
                
    - **Training** - Providing training to folks?
        
                
    - **(14) Comments** - Having a conversation about the design.
        
                
    - **(12) Watching** - Watching to see any changes occur.
        
                
    - **(16) Notifications** - Receiving notifications about changes.
                
            
    

- **Define** - You can start with a documentation collection and evolve to be full blown OpenAPI.
        
                
    - **(3) Editor** - Editing an OpenAPI using the API builder.
        
                
    - **Examples** - Really need some examples I can work from.
        
                
    - **(8) Documentation** - Publishing documentation to support an API.
        
            
    

- **Design** - Iterating upn the surface area of each API using OpenAPI.
        
                
    - **(3) Editor** - Editing an OpenAPI using the API builder.
        
                
    - **Examples** - Really need some examples I can work from.
        
                
    - **Linting** - Linting of OpenAPI, JSON Schema, but also for governance.
        
                
    - **(14) Comments** - Having a conversation about the design.
        
                
    - **(12) Watching** - Watching to see any changes occur.
        
                
    - **(16) Notifications** - Receiving notifications about changes.
        
            
    

- **Deliver** - Same bucket as development.
        
                
    - **(19) Github Sync** - Codegen, pipeline, and other elements could reside here.
        
                
    - **CD/CD** - I don't have the CI/CD integrations listed here, will add in next iteration.
        
                
    - **(20) Gateway Sync** - Syncing the OpenAPI to various stages using AWS API gateway.
        
                
    - **(17) Code Generation** - Generating code in a variety of programming languages.
        
            
    

- **Manage** - Manager access to an API.
        
                
    - **Plan** - Need some sort of plan management reference and capability.
        
                
    - **Keys / Token** - Obtaining and renewing keys and tokens as part of access.
        
            
    
        
### Lifecycle Twelve

    - **Design** - Iterating upn the surface area of each API using OpenAPI.
            
                    
    - **(3) Editor** - Editing an OpenAPI using the API builder.
            
                    
    - **Examples** - Really need some examples I can work from.
            
                    
    - **Linting** - Linting of OpenAPI, JSON Schema, but also for governance.
            
                    
    - **(14) Comments** - Having a conversation about the design.
            
                    
    - **(12) Watching** - Watching to see any changes occur.
            
                    
    - **(16) Notifications** - Receiving notifications about changes.
            
                
        

    - **Mock** - Mocking the interface and data for an API being delivered.
            
                    
    - **(9) Mocking** - Firing up mock server for an OpenAPI.
            
                    
    - **Examples** - I will add more references to examples in my next iteration.
            
                
        

    - **Test** - Ensuring there are tests present for each API.
            
                    
    - **(10) Testing** - Producing a set of tests for an API using it’s OpenAPI.
            
                
        

    - **Requirements** - I'd say starting with docs and then doing API-first covers this.
            
                    
    - **(8) Documentation** - Publishing documentation to support an API.
            
                    
    - **(3) Editor** - Editing an OpenAPI using the API builder.
            
                    
    - **Examples** - Really need some examples I can work from.
            
                    
    - **Linting** - Linting of OpenAPI, JSON Schema, but also for governance.
            
                    
    - **(14) Comments** - Having a conversation about the design.
            
                    
    - **(12) Watching** - Watching to see any changes occur.
            
                    
    - **(16) Notifications** - Receiving notifications about changes.
                    
                
        

    - **Rewrite** - Continuation of the API design process.
            
                    
    - **(3) Editor** - Editing an OpenAPI using the API builder.
            
                    
    - **Examples** - Really need some examples I can work from.
            
                    
    - **Linting** - Linting of OpenAPI, JSON Schema, but also for governance.
            
                    
    - **(14) Comments** - Having a conversation about the design.
            
                    
    - **(12) Watching** - Watching to see any changes occur.
            
                    
    - **(16) Notifications** - Receiving notifications about changes.
            
                
        

    - **Test** - Ensuring there are tests present for each API.
            
                    
    - **(10) Testing** - Producing a set of tests for an API using it’s OpenAPI.
            
                
        

    - **Additions** - Continuation of the API design process.
            
                    
    - **(3) Editor** - Editing an OpenAPI using the API builder.
            
                    
    - **Examples** - Really need some examples I can work from.
            
                    
    - **Linting** - Linting of OpenAPI, JSON Schema, but also for governance.
            
                    
    - **(14) Comments** - Having a conversation about the design.
            
                    
    - **(12) Watching** - Watching to see any changes occur.
            
                    
    - **(16) Notifications** - Receiving notifications about changes.
            
                
        

    - **Deploy** - Bringing an API to life in any stage of development.
            
                    
    - **(19) Github Sync** - Codegen, pipeline, and other elements could reside here.
            
                    
    - **CD/CD** - I don't have the CI/CD integrations listed here, will add in next iteration.
            
                    
    - **(20) Gateway Sync** - Syncing the OpenAPI to various stages using AWS API gateway.
            
                    
    - **(17) Code Generation** - Generating code in a variety of programming languages.
            
                
        

    - **Break** - I like this one, guessing you can do with monitors and tests.
            
                    
    - **(10) Testing** - Producing a set of tests for an API using it’s OpenAPI.
            
                    
    - **(11) Monitoring** - Monitoring an API using it’s OpenAPI.
            
                
        

    - **Fix** - Testing monitoring is a cycle that can handle this. 
            
                    
    - **(10) Testing** - Producing a set of tests for an API using it’s OpenAPI.
            
                    
    - **(11) Monitoring** - Monitoring an API using it’s OpenAPI.
            
                
        

    - **Hair Loss** - I am beginning to worry more about this one.
            
                    
        - Goal is to reduce this by better defining the API lifecycle.
            
                
        

    - **Document** - Providing human readable documentation for an API.
            
                    
    - **(8) Documentation** - Definitely have documentation covered.
            
                
        


### Lifecycle Thirteen

    
    - **Design** - Iterating upn the surface area of each API using OpenAPI.
                
                        
    - **(3) Editor** - Editing an OpenAPI using the API builder.
            
                        
    - **Examples** - Really need some examples I can work from.
            
                        
    - **Linting** - Linting of OpenAPI, JSON Schema, but also for governance.
            
                        
    - **(14) Comments** - Having a conversation about the design.
            
                        
    - **(12) Watching** - Watching to see any changes occur.
            
                        
    - **(16) Notifications** - Receiving notifications about changes.
            
                    
        
            

    - **Test** - Ensuring there are tests present for each API.
            
                    
    - **(10) Testing** - Producing a set of tests for an API using it’s OpenAPI.
            
                
        

    - **Deploy** - Bringing an API to life in any stage of development.
            
                    
    - **(19) Github Sync** - Codegen, pipeline, and other elements could reside here.
            
                    
    - **CD/CD** - I don't have the CI/CD integrations listed here, will add in next iteration.
            
                    
    - **(20) Gateway Sync** - Syncing the OpenAPI to various stages using AWS API gateway.
            
                    
    - **(17) Code Generation** - Generating code in a variety of programming languages.
            
                
        

    - **Secure** - Locking down the surface area of an API and the access to resources.
            
                    
    - **(10) Testing** - Producing a set of tests for an API using it’s OpenAPI.
            
                
        

    - **Performance** - Testing the performance of each individual API.
            
                    
    - **(10) Testing** - Producing a set of tests for an API using it’s OpenAPI.
            
                
        

    - **Monitor** - Monitoring a variety of aspects of an APIs operation and lifecycle.
            
                    
    - **(11) Monitoring** - Monitoring an API using it’s OpenAPI.
            
                
        
            

<br>

Whewww!! That was a lot of thinking about the API lifecycle, using these thirteen separate definitions of what an API lifecycle can be. It is an interesting exercise because of the different words we use, and how precise or broad we can be with how we describe the API lifecycle. I find it also interesting that the lifecycle continues so few mentions of versioning and maturity. However, that is why I am doing this exercise. The next step of this is to take what I've learned and go back to my API lifecycle extension and see what else I need to add in to accommodate all of these definitions of what an API lifecycle is. It was an interesting exercise because it pushed me to think about how the Postman API platform enables the API lifecycle, grounding and providing a hands-on way to make the API lifecycle more tangible for me, something that the API lifecycle extension further grounds for me.

This exercise really shows how important the API design portion of this process is, and it is how you set APIs in motion, but also how you iterate upon them. It also shows me how important observability is to not only the reliability of APIs, but also the overall API lifecycle. It also reinforced for me the role that the feedback loop plays in the API lifecycle. Taking all of this and then hammering on my OpenAPI API lifecycle extension is going to really interesting now. At first I was just going to have all of the technical building blocks of the API lifecycle along with maturity and change management, but now I see the important of the design process, observability, and feedback loop is to all of this. Once I get one more draft of the API lifecycle extension the next challenge will be getting folks understanding what the hell I am talking about so I can start putting more scaffolding in place to demonstrate the value of this type of definition for helping guide our APIs forward throughout their lives.