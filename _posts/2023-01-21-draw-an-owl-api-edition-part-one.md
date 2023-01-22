---
published: true
layout: post
title: 'How to Draw an Owl, the API Edition - Part One'
image: https://kinlane-productions2.s3.amazonaws.com/how-to-draw-an-owl.png
author:
name: kinlane
tags:
- Governance
- Enablement
- Components
- Workspaces
- Changes
---
I am down in the quantum realm when it comes to API operations. Working at the atomic level when it comes to how we do APIs. One of my favorite ways to make fun of APIs is to use the How to Draw an Owl analogy for how we teach people to do APIs. TL;DR we leave out a lot of details when we talk about and teach people about APIs. To help me address this problem in my storytelling I am exploring how we can use common approaches to API governance to enable teams across the enterprise to do the right thing, take the right next logical step, and deliver consistent, simple, and useful APIs.

To help me work through exercise, I am using a common address resource to help me walk through all the invisible details of eventually what will be an API. I am purposefully trying to walk through each step of creating a new API resource in a way that can be automated at a mix of levels. This is an exercise I'll explore with dealing with existing APIs, and consuming APIs, but for now I am exploring the minutia of producing what I'd consider a digital resource, using an OpenAPI--eventually looking to deliver a real API.

## Start With a Workspace
I need a workspace to put this work in so that anyone can come and build on top of my resource, get involved, and understand what is happening. This workspace is created in Postman either manually or via the API, resulting in the following object.

```
id: 1f0df51a-8658-4ee8-a2a1-d2567dfa09a9
name: Address Workspace
type: team
description: For developing the address resource.
visibility: private-team
createdAt: '2023-01-01'
```

I now have an empty workspace where I can put my digital resource and manage the work that will occur around it. Providing a single place to get up to speed on what is happening, and get involved moving this resource forward.

## Define API Using OpenAPI
For the purposes of our digital resource exercise we are using OpenAPI to describe the surface area of this API, but for this part one we will not be adding paths, and just working on the schema. To get started we have added just a title and description.

```
openapi: '3.0.0'
info:
 title: 'Address'
 description: 'This is for defining an address object for storing the details of specific locations.'

# Empty Path
paths: {}

# Empty Components
components: {}   
```

This OpenAPI validates. It is the minimal viable OAS you can produce, which is perfect for any new digital resource, because at this point we only have a title and description for our digital resource--we haven't fleshed everything else out.

## Change Management
To help us manage change we will be using semantic versioning for this digital resource, adding a version property to the OAS info object, using it to communicate each major, minor, and patch release.

```
openapi: '3.0.0'
info:
 version: '1.0.0'
 title: 'Address'
 description: 'This is for defining an address object for storing the details of specific locations.'

# Empty Path
paths: {}

# Empty Components
components: {}  
```

We are using version 3.0 of OAS, but setting our own version for this resource to be 1.0.0, and we will work within this version for all of this release, as we iterate on our object, and eventually API.

## Licensing
Next, we want to make sure we cover our legal bases by having a licensing as part of our OAS license object. We are using CC BY-SA, or a creative commons license for the copyright on the interface, which is the precedent set by the Oracle v Google copyright case.

```
openapi: '3.0.0'
info:
 version: '1.0.0'
 title: 'Address'
 description: 'This is for defining an address object for storing the details of specific locations.'
 contact:
   name: Kin Lane
   email: kin.lane@postman.com
 license:
   name:  Attribution-ShareAlike 4.0 International (CC BY-SA 4.0)
   identifier:  CC BY-SA

# Empty Path
paths: {}

# Empty Components
components: {} 
```

Our interface is separate from our implementation. Code will be covered by the Apache 2.0 license, while the interface is covered by copyright using CC BY-SA.

## Use Existing Standards
Before we get to work actually defining our digital resource, let's do our homework and see if there are any existing standards we should be adopting. Avoiding reinventing the wheel, while also ensuring widest possible adoption.

```
name: Schema.org Postal Code
description: Open source objects.
link: https://schema.org/postalCode
```

We are going to use the Schema.org Postal Code object as the blueprint for our digital resource, adopting the properties we are most interested in as a starting point for this resource.

## Invite Stakeholders
Before we get started defining our digital resource let's add any stakeholders to the conversation, ensuring that we have the name, email, and title for anyone involved with the delivery of our address object.

```
givenName: Kin
familyName: Lane
email: kin.lane@postman.com
jobTitle: Chief Evangelist
```

I am just getting started, so I am the only stakeholder, but I'll do the hard work to get more stakeholders involved and excited about my new digital resources.

## Contact Information
Now we want to make sure at least one of the stakeholders is added to the OAS document as the contact, adding their name and email to the info contact object, ensuring there is always someone responsible.

```
openapi: '3.0.0'
info:
 version: '1.0.0'
 title: 'Address'
 description: 'This is for defining an address object for storing the details of specific locations.'
 contact:
   name: Kin Lane
   email: kin.lane@postman.com

# Empty Path
paths: {}

# Empty Components
components: {}  
```

There should always be someone responsible for an API, acting as the point person. Even if the email goes to a general account, there should be a person who can be held responsible for each API.

## Address Example
Let's flesh out our digital resource by adding an example of what it will look like, providing a real world example in YAMl or JSON of what it will look like in the wild--providing as much detail as possible.

```
openapi: '3.0.0'
info:
 version: '1.0.0'
 title: 'Address'
 description: 'This is for defining an address object for storing the details of specific locations.'

# Empty Path
paths: {}

# Adding address example
components:
 schemas:
   Address:
     type: object     
     example:
       streetAddress: 123 Main Street      
```

Now we are using the components schema object for OAS to begin fleshing out the JSON Schema for address object. All we've done so far is flesh out the name, type, and example for our address object--we will do more later.

## Address Properties
Now that we have a simple example of what we want, let's articulate this as JSON Schema properties, declaring the name and the type of the property--we can get into more detail later.

```
openapi: '3.0.0'
info:
 version: '1.0.0'
 title: 'Address'
 description: 'This is for defining an address object for storing the details of specific locations.'

# Empty Path
paths: {}

# Adding address properties
components:
 schemas:
   Address:
     type: object     
     example:
       streetAddress: 123 Main Street
     properties:
       streetAddress:
         type: string                
```

We will use these properties to validate our digital resource once it is being used, ensuring that the data being submitted or published is consistent with the contract for our schema.

## Address Required
Now we want to make sure that you just can't submit an empty address, requiring that you add something for the street address--something we can further define the limit and shape of later.

```
openapi: '3.0.0'
info:
 version: '1.0.0'
 title: 'Address'
 description: 'This is for defining an address object for storing the details of specific locations.'

# Empty Path
paths: {}

# Adding address required
components:
 schemas:
   Address:
     type: object     
     example:
       streetAddress: 123 Main Street
     properties:
       streetAddress:
         type: string         
     required:
       - streetAddress                                 
```

We now have a solid example of our address, the underlying properties of the data, and a requirement that some value is present, establishing the baseline for our address object--something we can evolve as part of future iterations.

## Tracking Change
It is important to track the changes occurring, breaking change down into incremental shifts to the contract, making it easy to see what is being proposed, and what is being changed to our digital resource.

```
- name: Created Workspace
 description: Created a new workspace for resources.
 from: [old]
 to: [new]
- name: Created OpenAPI
 description: Created the OpenAPI for the object.
 from: [old]
 to: [new]
- name: Added Version
 description: Added version to the resource.
 from: [old]
 to: [new]  
- name: Added License
 description: Added license to the resource.
 from: [old]
 to: [new]    
- name: Chose Standards
 description: Choose to use Schema.org standard.
 from: [old]
 to: [new] 
- name: Added Stakeholders
 description: Added stakeholders to the resource.
 from: [old]
 to: [new] 
- name: Added Contact
 description: Added stakeholders to the resource.
 from: [old]
 to: [new]   
- name: Address Example
 description: Added an example of the resource.
 from: [old]
 to: [new]
- name: Address Properties
 description: Added an example of the resource.
 from: [old]
 to: [new] 
- name: Address Required
 description: Ensure properties are required.
 from: [old]
 to: [new]  
```

Keeping change modular, well-defined, and incremental provides a nice road map when you are planning, and a change log after things have been put in motion. Allowing change to be queued up, communicated around, and then implemented and automated through consensus.

## Notifying Stakeholders
When changes are proposed, notifications can be sent to all stakeholders. Of course, when there are more stakeholders this would have more impact, but for now it gets the point across that we need to notify stakeholders with a summary of change.

```
- name: 'Change Summary'
 description: A list of changes that have been made.
 resource: Address
 pubDate: '2023-01-01'
```

Now everyone involved should be notified of proposed changes and have examples and technical detail of what is being changed, keeping everyone involved and part of the conversation when it comes to the changes to the object.

## Comments
With all stakeholders informed of changes, comments are open, allowing every stakeholder to log a comment on the changes being made, included in reporting and change log.

```
- name: 'Feature Support'
 description: I support all of these changes.
 resource: Address
 from: kin.lane@postman.com
 pubDate: '2023-01-01'
```

Comments are a way to log feedback from all stakeholders involved in the forward motion of each digital resource, making sure every change has the required architecture decision records for the future.

# Votes
One additional dimension could involve voting by stakeholders on each individual change proposal, allowing a consensus model to be applied to the forward motion of each of our digital resources.

```
- vote: Yes
 resource: Address
 change: Address Properties
 by: kin.lane@postman.com
 pubDate: '2023-01-01'
- vote: Yes
 resource: Address
 change: Address Requirements
 by: kin.lane@postman.com
 pubDate: '2023-01-01' 
```

Votes can be the easy way to get consensus amongst stakeholders, allowing everyone to respond via message or API request to vote yes or no on each individual action, or possibly a summary of changes.

## Policies
Everything we have done so far can be defined as an official policy, shaping how all digital resources get defined as human readable, but also very formal policies defined to shape business operations. Providing a series of common steps that get used to move our address object forward, but reflect activities across all API.  

```
- name: Workspaces
 description: Every resource should have its own workspace.
 scope: Implementation
- name: OpenAPI
 description: Every resource should have its own OpenAPI.
 scope: Implementation
- name: Title
 description: Every resource should have an information title.
 scope: Implementation
- name: Description
 description: Every resource should have an information description.
 scope: Implementation
- name: Version
 description: Every resource should have an information version.
 scope: Implementation
- name: License
 description: Every resource should have an information license.
 scope: Implementation
- name: Standards
 description: Every resource should use existing standards.
 scope: Implementation    
- name: Stakeholders
 description: Every resource should have associated stakeholders.
 scope: Implementation 
- name: Contact
 description: Every resource should have an information contact.
 scope: Implementation
- name: Schema Examples
 description: Every resource schema should have an example.
 scope: Implementation 
- name: Schema Properties
 description: Every resource schema should have properties.
 scope: Implementation   
- name: Schema Required
 description: Every resource schema should be required.
 scope: Implementation     
```

These policies are the formal business definition of what needs to happen, providing a straightforward explanation of each building block of API operations. Policies provide the human definition of what occurs, which is mapped to machine-readable Spectral rules tha automate the policy.

## Rules
Rules are machine readable Spectral rules designed for specific sources of information, with the workspace and OpenAPI artifacts pulled using the Postman API. These rules are examples of what can be applied to each of the existing outputs for this work, automating whether or not each individual policy is applied or not.

```
- postman-workspace-exists:
   policy: Workspace
   points: 10
   description: Ensures that a postman workspace exists.
   message: The resource should have a workspace.
   given: "$.example"
   severity: info
   recommended: true
   type: style
   formats:
   - postman_workspace
   then: [example]
- postman-api-openapi-exists:
   policy: OpenAPI
   points: 10
   description: Ensures that a postman API OpenAPI exists.
   message: The resource should have an API OpenAPI.
   given: "$.example"
   severity: info
   recommended: true
   type: style
   formats:
   - postman_workspace
   then: [example]
- openapi-v3-info-title:
   policy: Title
   points: 10
   description: Ensures that all OpenAPIs have an information object title.
   message: The info object should have a title.
   given: "$.example"
   severity: info
   recommended: true
   type: style
   formats:
   - oas3
   then: [example]
- openapi-v3-info-description:
   policy: Description
   points: 8
   description: Ensures that all OpenAPIs have an information object description.
   message: The info object should have a description.
   given: "$.example"
   severity: info
   recommended: true
   type: style
   formats:
   - oas3
   then: [example] 
- openapi-v3-info-version:
   policy: Version
   points: 10
   description: Ensures that all OpenAPIs have an information object version.
   message: The info object should have a version.
   given: "$.example"
   severity: info
   recommended: true
   type: style
   formats:
   - oas3
   then: [example]
- openapi-v3-info-license:
   policy: License
   points: 10
   description: Ensures that all OpenAPIs have an information object license.
   message: The info object should have a license.
   given: "$.example"
   severity: info
   recommended: true
   type: style
   formats:
   - oas3
   then: [example] 
- openapi-v3-info-contact:
   policy: Contact
   points: 10
   description: Ensures that all OpenAPIs have an information object contact.
   message: The info object should have a contact.
   given: "$.example"
   severity: info
   recommended: true
   type: style
   formats:
   - oas3
   then: [example]
- openapi-v3-schema-examples:
   policy: Schema Examples
   points: 10
   description: Ensures that every schema has an example.
   message: Each schema object needs an example.
   given: "$.example"
   severity: info
   recommended: true
   type: style
   formats:
   - oas3
   then: [example]  
- openapi-v3-schema-properties:
   policy: Schema Properties
   points: 10
   description: Ensures that every schema has properties.
   message: Each schema object needs properties.
   given: "$.example"
   severity: info
   recommended: true
   type: style
   formats:
   - oas3
   then: [example]   
- openapi-v3-schema-required:
   policy: Schema Required
   points: 5
   description: Ensures that every schema has required properties.
   message: Each schema object needs a required property.
   given: "$.example"
   severity: info
   recommended: true
   type: style
   formats:
   - oas3
   then: [example]                           
```

This is an increasingly common way of applying a variety of rules against OpenAPI. The only unique thing here is I pull the OpenAPI from the Postman API, as well as beginning to lint workspace artifacts. With this approach I am looking to expand the boundaries of how we apply rules across API operations.

## Outcomes
Augmenting policies and rules with real world outcomes to help incentivize the application of rules and policies. A policy is the formal business description, a rule is the machine readable automated portion, and outcomes are about linking the application of these policies to real world outcomes that stakeholders will care about.

```
- name: Easy Discovery
 description: A workspace ensures that the work behind every digital
 scope: Implementation
- name: Contract
 description: Each digital resource possesses a machine readable contract.
 scope: Implementation
- name: Simple Name
 description: The title of each resource is clear and easy to understand.
 scope: Implementation
- name: Adequate Description
 description: A digital resource has an adequate description of what it does.
 scope: Implementation    
- name: Managing Change
 description: Each resource is versioned to manage change.
 scope: Implementation
- name: Managing Legal
 description: A license is properly applied to each individual object.
 scope: Implementation  
- name: Person to Contact
 description: There is some to contact about each individual resource.
 scope: Implementation
- name: Consistency with Standards
 description: Utilizing standards make the digital resource easier to use.
 scope: Implementation   
- name: Bring in Stakeholders
 description: Make sure you have multiple stakeholders involved in things.
 scope: Implementation     
- name: Someone Home
 description: There is someone to contact when it comes to needing help.
 scope: Implementation  
- name: Someone Home
 description: There is someone to contact when it comes to needing help.
 scope: Implementation
- name: Schema Examples Help
 description: Examples for each schema help demonstrate what is possible.
 scope: Implementation
- name: Validate with Schema Properties
 description: The JSON Schema properties allow each resource to be validated.
 scope: Implementation
- name: Required Properties
 description: Makes sure digital resources contain the data necessary.
 scope: Implementation                     
```

These outcomes are meant to augment policies and rules with meaningful outcomes that people care about. Adding a property to a YAML or JSON document doesn't get people motivated, but linking it to real-world outcomes that impact people during their regular work can have different results.

## Components
Now I am looking to flip policies, rules, and outcomes on their head and see if I can use rules to nudge and enable stakeholders to do the right thing in the moment. I am looking to augment policies and the machine readable rules that automate them with reusable components that can be used to enable stakeholders at each step along the way.

```
- workspace:
   policy: Workspace
   name: Workspace
   description: A workspace component.
   component:
     name: Workspace
     type: team
     description: For developing the address resource.
     visibility: private-team
     createdAt: '2023-01-01'   
- api-openapi:
   policy: OpenAPI
   name: OpenAPI
   description: A simple OAS component.
   component:
     openapi: '3.0.0'
     info:
       title: 'Address'
       description: 'This is for defining an address object for storing the details of specific locations.'
     paths: {}
     components: {}      
- openapi-info-title:
   policy: Title
   description: An example title.
   component:
     title: 'Title'
- openapi-v3-info-description:
   policy: Description
   description: Ensures that all OpenAPIs have an information object description.
   component:
     description: 'A description'
- openapi-v3-info-version:
   policy: Version
   description: Ensures that all OpenAPIs have an information object version.
   component:
     version: '1.0.0'
- openapi-v3-info-license:
   policy: License
   description: Ensures that all OpenAPIs have an information object license.
   component:
     license:
       name: Apache 2.0
       identifier: Apache-2.0 
- openapi-v3-info-contact:
   policy: Contact
   description: Ensures that all OpenAPIs have an information object contact.
   component:
     contact:
       name: Kin Lane
       email: kin.lane@postman.com   
- openapi-v3-schema-examples:
   policy: Schema Examples
   description: Ensures that every schema has an example.
   component: 
     example:
       streetAddress: 123 Main Street  
- openapi-v3-schema-properties:
   policy: Schema Properties
   description: Ensures that every schema has properties.
   component:  
     properties:
       streetAddress:
         type: string              
- openapi-v3-schema-required:
   policy: Schema Required
   description: Ensures that every schema has required properties.
   component:
     required:
       - streetAddress    
```

I am looking to come full circle with these components. I am looking to understand how we can use policies and rules to not govern stakeholders throughout their journey, but enable them. When someone is staring at the beginnings of an OpenAPI contract, wondering what they need to do next, there is a nudge, with a ready-to-go reusable component available to put to work.

## Turning Governance into Enablement
This exercise was about connecting all of the dots when it comes to delivering an entirely new API, but slowing down and being very deliberate about each step. So much so, I barely even got the schema for our digital resource defined. In part two I am looking to further flesh out this object and then define some simple access using an HTTP API. Similar to this, I am looking to step through the addition of each element of my digital resource, and carefully craft a policy that guides, a machine readable rule that automates, and a reusable component that enables--all leading to logical business outcomes.

## Gamifying Instead of Governance
If you notice, each of the Spectral rules have a point property. When a rule is applied against our OpenAPI artifact the points accumulate and remain a property of our object. I am exploring ways in which rules can be applied to our APIs, as well as the operations around them. I am also looking to iterate and evolve upon rules and other reusable components in the same way I am governing my address object. Spectral rules should have points. Reusable components should have points. All of these building blocks of our API operations should be improved upon and gamify the evolution of building blocks. 

## A Platform-Level Artifact
I am not satisfied with beginning this journey with OpenAPI. It should be a higher level abstract artifact like APIs.json or something. The JSON Schema should be developed independently of OpenAPI, or partially AsyncAPI. A workspace could contain multiple APIs, and there will be multiple collections eventually--once I get to mocking, documentation, and testing for my API. Regardless, I am still learning as part of this exercise. I am pushing the boundaries of governance here, flipping governance on its head and making it more about nudging and enablement of everyone involved. To be able to make this intelligent and relevant to what teams are doing, it will have to have a platform or at least program level artifact to keep track of everything.

## Iterate Upon My Address Resource
Next I will add more properties to our address object, and begin iterating upon the API paths. I am looking to keep with my How to Draw an Owl analogy and show my homework. Developing policies and rules along the way that help automate and translate each step into business outcomes. I am looking to translate each step in how to do an API into guidance and enablement. I don't want all of these policies and rules to be seen as governance. I don't want these policies and rules to be seen as a checklist of what has to happen. I want policies and rules to be seen as helpful guidance along the way, delivered when they are needed. I want this guidance to be right there under the fingertips of anyone involved with moving an API forward. To do this we'll need an overarching program lifecycle and artifacts, for our standards, as well as each individual API we are delivering.