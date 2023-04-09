---
published: true
layout: post
title: 'The JSON Schema Tooling In My Life'
date: 2019-07-10T09:00:00.000Z
tags:
  - API Evangelist
  - JSON Schema
  - Definitions
  - Tools
image: >-
  https://s3.amazonaws.com/kinlane-productions2/algorotoscope-master/udnie-DSC_0033.jpg
---

I am always pushing for more schema order in my life. I spend way too much time talking about APIs, when a significant portion of the API foundation is schema. I don’t have as many tools to help me make sense of my schema, and to improve them as definitions of meaningful objects. I don’t have the ability to properly manage and contain the growing number of schema objects that pop up in my world on a daily basis, and this is a problem. There is no reason I should be making schema objects available to other consumers if I do not have a full handle on what schema objects exist, let alone a full awareness of everything that has been defined when it comes to the role that each schema object plays in my operations.

To help me better understand the landscape when it comes to JSON Schema tooling, I wanted to take a moment and inventory the tools I have bookmarked and regularly use as part of my daily work with JSON Schema:

- **JSON Schema Editor** - https://json-schema-editor.tangramjs.com/ - An editor for JSON Schema.
- **JSON Schema Generator** - https://github.com/jackwootton/json-schema - Generates JSON Schema from JSON
- **JSON Editor** - https://json-editor.github.io/json-editor/ - Generates form and JSON from JSON Schema.
- **JSON Editor Online** -https://github.com/josdejong/jsoneditor/ - Allows me to work with JSON in a web interface.
- **Another JSON Schema Validator (AJV)** - https://github.com/epoberezkin/ajv - Validates my JSON using JSON Schema.

I am going to spend some time consolidating these tools into a single interface. They are all open source, and there is no reason I shouldn’t be localizing their operation, and maybe even evolving and contributing back. This helps me understand some of my existing needs and behavior when it comes to working with JSON Schema, which I’m going to use to seed a list of my JSON Schema needs, as drive a road map for things I’d like to see developed. Getting a little more structure regarding how I work with JSON Schema.

- **Visual Editor** - Being able to visual render and edit JSON Schema in browser.
- **YAML / JSON Editor** - Being able to edit JSON Schema in YAML or JSON.
- **YAML to JSON Converter** - Converting my YAML JSON Schema into JSON.
- **JSON to YAML Converter** - Converting my JSON JSON Schema into YAML.
- **JSON to JSON Schema Generator** - Generate JSON Schema from JSON object.
- **JSON Schema to JSON Generator** - Generate a JSON object from JSON Schema.
- **JSON Validation Using JSON Schema** - Validate my JSON using JSON Schema.
- **Enumerators** - Help me manage enumerators used across many objects.
- **Search** - Help me search across my JSON Schema objects, wherever they are.
- **Guidance** - Help me create better JSON Schema objects with standard guidelines.

This is a good start. If I can bring some clarity and coherence to these areas, I’m going to be able to step up my API design and development game. If I can’t, I’m afraid I’m going to be laying a poor foundation for any API I’m designing in this environment. I mean, how can I consciously provide access to any schema object that I don’t have properly defined, indexed, versioned, and managed? If I don’t fully grasp my schema objects, my API design is going to be off kilter, and most likely be causing friction with my consumers. Granted, I could be offloading the responsibility for making sense of my schema to my consumers using a GraphQL solution, but I’m more in the business of doing the heavy lifting in this area, as it pertains to my business—-I’m the one who should know what is going on with each and every object that passes through my business servers.

I wish there was a schema tool out there to help me do everything that I need. Unfortunately I haven’t seen it. The tooling that has rose up around the OpenAPI specification helps us better invest in schema objects when they are in the service of our API contracts, but nothing just for the sake of schema management. I will keep taking inventory of what tooling is available, as well as what I am needing when it comes to JSON Schema management. Who knows, something might pop up out there on the landscape. Or, more realistically I’m hoping little individual open source solutions keep popping up, allowing me to stitch them together and create the experience I’m looking for. I’m a big fan of this approach, rather than one service provider swooping in and providing the one tool to rule them all, only to get acquired and then be shut down--breaking my heart all over again.
