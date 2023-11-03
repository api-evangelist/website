---
published: true
layout: post
title: 'A Schema-Driven Address API Negotiation'
image: https://kinlane-productions2.s3.amazonaws.com/algorotoscope-master/uncle-sam-working-on-railroad-1.jpg
author:
    name: kinlane
tags:
- Schema
- OpenAPI
- APIs.json
- Contracts
- Design
---
I recently finished [Democracy's Data, The Hidden Stories in the U.S. Census and How to Read Them](https://us.macmillan.com/books/9780374602543/democracysdata), and the book was the closest thing to capturing how I see the Application Programming Interface, or simply the API. I regularly get frustrated with my role in the API universe because of the conflicting force’s between not just API producer and consumer, but also the API service and tooling providers, and the investors who do or do not support them. I am fascinated with this intersection, but also repeatedly horrified by what occurs at this intersection at scale online today. 

I study APIs not because I think there is a single right way or wrong way to do APIs. I study them because they are shaping who we are at scale within each moment of our increasingly online lives. APIs are defining who we are, and our usage of web and mobile applications like Facebook, TikTok, Instagram, and others are allowing API producers to shape who we are, and while we have some control within these digital templates to still be human, increasingly so much of what shapes us is decided very far out of our control. Like in the United States Census in Democracy’s data, I see stories in the API cracks I see just beneath the surface of our online lives, and this is my attempt to tell a single story about our perpetual negotiation of where we are in the world, which used to determined by our physical home, as described in Democracy’s Data, but increasingly is a real-time mix of IP addresses bound to longitude and latitude.

## Let’s Begin with Our Address
Let’s begin this journey with the negotiation of what is in the world which is within our control. Something we regularly negotiate online and offline—our address. Our address seems like a pretty straightforward thing to many of us, but if you’ve worked on a census, for any global business, or other complicated human scenarios, you know it is anything but straightforward. For me, the address represents so much about who we are in the world, which is something that has been evolved and abused significantly in an always online world. 

## A Machine-Readable Contract
In the world of APIs we have what is called the OpenAPI specification for describing the surface area of APIs. This YAML or JSON definition is used to describe an API for generating documentation and software development kits, but for me it is first and foremost about describing the surface area of the APIs that are governing our lives so that we can have a conversation about them. So, for this exercise I am going to use OpenAPI to describe and narrate the negotiation that occurs around where we are in the world. Instead of walking through each element of our Where We Are in the World API, I’ll start with this base definition.

```
# A machine and human readable contract.
openapi: 3.0.0
info:

    # Title and description of what we are defining.
    title: 'Where We Are In The World'
    description: 'This is an OpenAPI contract for negotiating an address.'

    # How we communicate changes.
    version: 1.0.0

    # Who is doing this work?
    contact:
      name: Kin Lane
      url: https://apievangelist.com
      email: info@kinlane.com

    # Legal
    license:
      name: Attribution 4.0 International (CC BY 4.0)
      url: 'https://creativecommons.org/licenses/by/4.0/'

# Tags for organizing these thoughts and interfaces.
tags:

  # A general descriptor of what is an address
  - name: Address
    description: 'The particulars of the place where someone lives or an organization is situated.'

# The ways in which this is accessed.
paths: {}

# These are centralized components referenced and reused across this definition.
components:

  examples:

    Address:
      description: A basic example of an address.
      value:
        address: 123 Main Street.

  # JSON Schema used to validate objects.
  schemas:

    Address:
      type: object
      description: 'Our address object.'
      properties: 	
        address: 
          type: string
          description: 'This is the address.'

```
My goal here is to define an API that could be used to power a contact form on a website, or many contact forms across many websites. However, I do not have any paths, or even a base URL for my API. At this point I just want to use this as a contract for defining an address, providing a machine and human readable way to collaborate and iterate on what an address means — ensuring we are all on the same page. First, OpenAPI provides me with a way of defining the basics, like the name and description of my API, but also who to contact, and license being applied. I have added a single tag, but there are no paths, and I am mostly interested in fleshing out what an address is using the components object, using an example, but then also ensuring their is a JSON Schema for my example—-showing what an address is, while also articulating the shape of an address in a precise way.

## Iterating Upon Our Address
Right after establishing the baseline for our address, it becomes clear that we will need more structure to our definition to make it support our needs. We need more than just the street, and we don’t want to just pack everything into an address. We need a city, state or province, a zip code, and country. As soon as I suggest a country, I immediately realize that zip code won’t work, and change my property to be postal code. To help articulate my changes I update the example and the supporting schema to reflect my intent—helping everyone else on my team get on the same page.

```
# A machine and human readable contract.
openapi: 3.0.0
info:

    # Title and description of what we are defining.
    title: 'Where We Are In The World'
    description: 'This is an OpenAPI contract for negotiating an address.'

    # How we communicate changes.
    version: 1.1.0

    # Who is doing this work?
    contact:
      name: Kin Lane
      url: https://apievangelist.com
      email: info@kinlane.com

    # Legal
    license:
      name: Attribution 4.0 International (CC BY 4.0)
      url: 'https://creativecommons.org/licenses/by/4.0/'

# Tags for organizing these thoughts and interfaces.
tags:

  - name: Address
    description: 'The particulars of the place where someone lives or an organization is situated.'
  - name: Countries
    description: 'Expanding beyond just a single location, and placing each address within a country.'

# The ways in which this is accessed.
paths: {}

# These are centralized components referenced and reused across this definition.
components:

  examples:

    Address:
      description: A basic example of an address.
      value:
        address: 123 Main Street.
        city: New York
        province: New York
        postalCode: 10019
        country: United States

  # JSON Schema used to validate objects.
  schemas:

    Address:
      type: object
      description: 'Our address object.'
      properties:   
        address: 
          type: string
          description: 'This is the address.'
        city: 
          type: string
          description: 'This is the city.'
        province: 
          type: string
          description: 'This is the state or province.'
        postalCode: 
          type: string
          description: 'This is the postal code.'        
        country: 
          type: string
          description: 'This is the country.'                                  
```
I am pretending like I have a group of people negotiating this address API--taking a schema-driven approach to designing an API, and negotiating changes, expands the value of the API by adding constraints like country, which influences our zip and postal code property. Our examples and schema provide a precise way for us to articulate, iterate, and expand on our address API, in a collaborative way. This is an API contract. Everyone involved is getting to negotiate what an address is, from the team producing, to the developers consuming, and even the end-users of applications that will put the address API to use.

# Constraining the Shape of Our Address
Before we agree on this definition of the object we will return using our address object, we want to not just define the name, but also the shape of our address properties. Our address, city, province, postalCode, and country are all strings, but let's narrow this down further using the JSON Schema properties of our OpenAPI contract. These additional constraints can be used by the gateway we use to deploy our API, as well as the applications using the API to validate the input of addresses into our API.

```
# A machine and human readable contract.
openapi: 3.0.0
info:

    # Title and description of what we are defining.
    title: 'Where We Are In The World'
    description: 'This is an OpenAPI contract for negotiating an address.'

    # How we communicate changes.
    version: 1.2.0

    # Who is doing this work?
    contact:
      name: Kin Lane
      url: https://apievangelist.com
      email: info@kinlane.com

    # Legal
    license:
      name: Attribution 4.0 International (CC BY 4.0)
      url: 'https://creativecommons.org/licenses/by/4.0/'

# Tags for organizing these thoughts and interfaces.
tags:

  # A general descriptor of what is an address
  - name: Address
    description: 'The particulars of the place where someone lives or an organization is situated.'

# The ways in which this is accessed.
paths: {}               

# These are centralized components referenced and reused across this definition.
components:

  examples:

    Address:
      description: A basic example of an address.
      value:
        address: 123 Main Street.
        city: New York
        province: New York
        postalCode: 10019
        country: United States

  # JSON Schema used to validate objects.
  schemas:

    Addresses:
      type: array
      items:
        $ref: "#/components/schemas/Address"

    Address:
      type: object
      description: 'Our address object.'
      properties: 	
        address: 
          type: string
          description: 'This is the address.'
          pattern: '^(\d{1,}) [a-zA-Z0-9\s]+(\,)? [a-zA-Z]+(\,)? [A-Z]{2} [0-9]{5,6}$'
          minimum: 5
          maximum: 100
        city: 
          type: string
          description: 'This is the city.'
          pattern: '^[a-zA-Z.-]+(?:[\s-][\/a-zA-Z.]+)*$'
          minimum: 5
          maximum: 50          
        province: 
          type: string
          description: 'This is the state or province.'
          pattern: '/^[a-zA-Z0-9 ]*$/'
          minimum: 5
          maximum: 50          
        postalCode: 
          type: string
          description: 'This is the postal code.'   
          pattern: '/^[a-zA-Z0-9 ]*$/'     
          minimum: 5
          maximum: 25          
        country: 
          type: string
          description: 'This is the country.'
          pattern: '/^[a-zA-Z0-9 ]*$/' 
          minimum: 5
          maximum: 50                                            
```
Now we have a regular expression (regex), as well as a minimum and maximum length for each of our address properties. This gives more shape to our address object, constraining the properties in a way that can be validated by gateways, user interfaces, and anywhere else you can run AJV (Another JSON Schema Validator). Additionally, we can validate our entire OpenAPI contract for our address API using the JSON Schema for the OpenAPI specification. This schema-driven approach keeps our address negotiation more structured, precise, and machine-readable, ensuring that we keep addresses as clean as possible in our API.

## Retrieving Our Addresses Using an API
Now we are ready to add an API path for accessing our addresses. This path can be appended to the HTTP URL for our API, allowing a JSON list of addresses to be returned. Our API uses HTTP to access our addresses, returning valid JSON according to our specification. Our single API operation references the JSON Schema iterated upon, returning an array of valid addresses, along with a 200 HTTP status code signaling a successful API call.

```
# A machine and human readable contract.
openapi: 3.0.0
info:

    # Title and description of what we are defining.
    title: 'Where We Are In The World'
    description: 'This is an OpenAPI contract for negotiating an address.'

    # How we communicate changes.
    version: 1.3.0

    # Who is doing this work?
    contact:
      name: Kin Lane
      url: https://apievangelist.com
      email: info@kinlane.com

    # Legal
    license:
      name: Attribution 4.0 International (CC BY 4.0)
      url: 'https://creativecommons.org/licenses/by/4.0/'

# Tags for organizing these thoughts and interfaces.
tags:

  # A general descriptor of what is an address
  - name: Address
    description: 'The particulars of the place where someone lives or an organization is situated.'

# The ways in which this is accessed.
paths:

  '/addresses':
  
    get:
      operationId: getAddresses
      summary: Addresses
      description: 'Returns a list of addresses.'
  
      tags:
  
        - Address
  
      responses:
        "200":
          description: Success
          content:
            application/json:
              schema:
                $ref: "#/components/schemas/Addresses"
              example:
                value:
                  address: 123 Main Street.
                  city: New York
                  province: New York
                  postalCode: 10019
                  country: United States                

# These are centralized components referenced and reused across this definition.
components:

  examples:

    Address:
      description: A basic example of an address.
      value:
        address: 123 Main Street.
        city: New York
        province: New York
        postalCode: 10019
        country: United States

  # JSON Schema used to validate objects.
  schemas:

    Addresses:
      type: array
      items:
        $ref: "#/components/schemas/Address"

    Address:
      type: object
      description: 'Our address object.'
      properties: 	
        address: 
          type: string
          description: 'This is the address.'
          pattern: '^(\d{1,}) [a-zA-Z0-9\s]+(\,)? [a-zA-Z]+(\,)? [A-Z]{2} [0-9]{5,6}$'
          minimum: 5
          maximum: 100
        city: 
          type: string
          description: 'This is the city.'
          pattern: '^[a-zA-Z.-]+(?:[\s-][\/a-zA-Z.]+)*$'
          minimum: 5
          maximum: 50          
        province: 
          type: string
          description: 'This is the state or province.'
          pattern: '/^[a-zA-Z0-9 ]*$/'
          minimum: 5
          maximum: 50          
        postalCode: 
          type: string
          description: 'This is the postal code.'   
          pattern: '/^[a-zA-Z0-9 ]*$/'     
          minimum: 5
          maximum: 25          
        country: 
          type: string
          description: 'This is the country.'
          pattern: '/^[a-zA-Z0-9 ]*$/' 
          minimum: 5
          maximum: 50                                             
```
Now we have an API. It is a simple example of the power of JSON Schema and OpenAPI. This API can now be mocked using a variety of commercial and open source tools, utilizing the example to emulate the behavior of our API. Since our API is defined as an OpenAPI you can easily render using common commercial and open source API documentation tooling. We have an API contract, documentation, and mocked implementation of our API, which we can use to further iterate on our API, and collaborate with our team, potential consumers, as well as end-users of the applications who put the API to work.

## Create, Read, Update, and Delete (CRUD)
To put the finishing touches on our API, we want the ability to not just read addresses, but we also need to create, update, and delete addresses. HTTP provides us with a handful of HTTP methods for articulating a create with POST, updated with PUT, and delete with, well DELETE. This will expand our API to have two separate paths, with a total of five operations that round off our address API into something that is pretty valuable to application developers.

```
# A machine and human readable contract.
openapi: 3.0.0
info:

    # Title and description of what we are defining.
    title: 'Where We Are In The World'
    description: 'This is an OpenAPI contract for negotiating an address.'

    # How we communicate changes.
    version: 1.4.0

    # Who is doing this work?
    contact:
      name: Kin Lane
      url: https://apievangelist.com
      email: info@kinlane.com

    # Legal
    license:
      name: Attribution 4.0 International (CC BY 4.0)
      url: 'https://creativecommons.org/licenses/by/4.0/'

# Tags for organizing these thoughts and interfaces.
tags:

  # A general descriptor of what is an address
  - name: Address
    description: 'The particulars of the place where someone lives or an organization is situated.'

# The ways in which this is accessed.
paths:

  '/addresses':
  
    get:
      operationId: getAddresses
      summary: Addresses
      description: 'Returns a list of addresses.'
  
      tags:
  
        - Address
  
      responses:
        "200":
          description: Success
          content:
            application/json:
              schema:
                $ref: "#/components/schemas/Addresses"
              example:
                value:
                  - addressId: 1
                    address: 123 Main Street.
                    city: New York
                    province: New York
                    postalCode: 10019
                    country: United States  

    post:

      summary: Add Address
      description: 'Adds a new address.'
      operationId: addAddress

      tags:

        - Address

      requestBody:
      
        $ref: "#/components/requestBodies/Address"

      responses:
        "201":
          description: Successfully Added
          content:
            application/json:
              schema:
                $ref: "#/components/schemas/Address"                                

  '/addresses/{addressId}':
  
    get:
      operationId: getAddress
      summary: Retrieve Address
      description: 'Returns a single address.'

      parameters:

        - name: addressId
          description: 'The unique address id.'       
          in: path
          required: true
          schema:
            type: string      
  
      tags:
  
        - Address
  
      responses:
        "200":
          description: Success
          content:
            application/json:
              schema:
                $ref: "#/components/schemas/Address"
              example:
                value:
                  addressId: 1
                  address: 123 Main Street.
                  city: New York
                  province: New York
                  postalCode: 10019
                  country: United States 

    put:

      summary: Update Address
      description: 'Updates an address.'
      operationId: updateAddress

      parameters:

        - name: addressId
          description: 'The unique address id.'       
          in: path
          required: true
          schema:
            type: string        

      tags:

        - Address

      requestBody:
        $ref: "#/components/requestBodies/Address"
        
      responses:
        "204":
          description: Successfully Added

    delete:

      summary: Delete Address
      description: 'Deletes an address.'
      operationId: deleteAddress

      parameters:

        - name: addressId
          description: 'The unique address id.'       
          in: path
          required: true
          schema:
            type: string        

      tags:

        - Address
        
      responses:
        "204":
          description: Successfully Added          

# These are centralized components referenced and reused across this definition.
components:

  # The Request Body for Address
  requestBodies:

    Address:
      content:
        application/json:
          schema:
            $ref: "#/components/schemas/Address"
      required: true  

  # Example JSON of Address
  examples:

    Address:
      description: A basic example of an address.
      value:
        addressId: 1
        address: 123 Main Street.
        city: New York
        province: New York
        postalCode: 10019
        country: United States

  # JSON Schema used to validate objects.
  schemas:

    Addresses:
      type: array
      items:
        $ref: "#/components/schemas/Address"

    Address:
      type: object
      description: 'Our address object.'
      properties: 	
        address: 
          type: string
          description: 'This is the address.'
          pattern: '^(\d{1,}) [a-zA-Z0-9\s]+(\,)? [a-zA-Z]+(\,)? [A-Z]{2} [0-9]{5,6}$'
          minimum: 5
          maximum: 100
        city: 
          type: string
          description: 'This is the city.'
          pattern: '^[a-zA-Z.-]+(?:[\s-][\/a-zA-Z.]+)*$'
          minimum: 5
          maximum: 50          
        province: 
          type: string
          description: 'This is the state or province.'
          pattern: '/^[a-zA-Z0-9 ]*$/'
          minimum: 5
          maximum: 50          
        postalCode: 
          type: string
          description: 'This is the postal code.'   
          pattern: '/^[a-zA-Z0-9 ]*$/'     
          minimum: 5
          maximum: 25          
        country: 
          type: string
          description: 'This is the country.'
          pattern: '/^[a-zA-Z0-9 ]*$/' 
          minimum: 5
          maximum: 50                                             
```
There are a number of other things we need to do to prepare our API for development, such as adding 400, 404, and 500 error responses for our APIs, but this provides us with a base contract for our API. We can develop and deploy our API, use our contract for documentation, but also as a baseline for ongoing negotiations with developers building applications, but also end-users of applications. This OpenAPI provides a precise way to articulate what creating, reading, updating, and deleting addresses mean, but also adding new properties such as address2, longitude, latitude, and introducing new paths and operations for handling directions and other address enabled capabilities. 

## A Record of Negotiations
The [Semantic Versioning[(https://semver.org/)] that OpenAPI provides, allows us to articulate which version of OpenAPI we are using, which also defines which version of JSON Schema we are using, as well as communicate the change of our address schema and API. I am exploring other ways of documenting the actual negotiations of our API contract, providing the reason behind the addition of paths, operations, schema, and properties. I am also thinking about how OpenAPI can record suggestions for changes by API designers, architects, or even developers and end-users. I am looking to add a change management extension layer to OpenAPI, or possibly some sort of change management overlay using an [APIs.json](https://apisjson.org/).

I am getting better at documenting my own APIs using this approach. While I am not technically documenting the negotiation of anything when an API is designed, developed, and deployed by a team of one. I am documenting change and recording the provenance of why I made certain decisions, which helps me out down the road when I go to iterate on an API I haven't touched in a while. Everything I need is right there. Plus there is a way to hang issues and feedback from consumers and end-users, so I can rapidly gather what is needed to iterate on my API in more meaningful ways. All of this is why I use OpenAPI and JSON Schema. Sure, the documentation and mock servers are a nice benefit of a schema-driven approach, but it really is the structure and constraints of delivering APIs using a contract. It just helps me stay on my game, and deliver APIs that are consistent, robust, and useful to consumers.