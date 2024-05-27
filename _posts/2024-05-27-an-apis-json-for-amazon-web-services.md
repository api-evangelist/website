---
published: true
layout: post
title: 'An APIs.json for Amazon Web Services'
image: https://kinlane-productions2.s3.amazonaws.com/algorotoscope-master/bf-skinner-seatlle-shipping-mountain.jpg
author:
    name: kinlane
tags:
- Cloud
- API.json
- Profiling
---
It takes time to properly craft an [APIs.json](https://apisjson.org/) for an API provider. It is something I wish API providers would do on their own, but in an effort to help jump start this I am profiling many of the top API providers. I've been working on Amazon Web Services (AWS) for a while now, but finally got the [core AWS APIs.json index](https://github.com/api-search/cloud/blob/main/_apis/amazon-web-services/apis.md?plain=1), but more importantly the [APIs.io APIs.json overlay for [AWS](https://github.com/api-search/cloud/blob/main/_apis/amazon-web-services/overlays/apis-io-search.yml) to a state where I am pretty happy with the quality. 

```
aid: amazon-web-services
type: Overlay
name: Amazon Web Services
description: >-
  Amazon Web Services, Inc. is a subsidiary of Amazon that provides on-demand
  cloud computing platforms and APIs to individuals, companies, and governments,
  on a metered, pay-as-you-go basis. Clients will often use this in combination
  with autoscaling.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
url: >-
  https://raw.githubusercontent.com/apis-json/artisanal/main/apis/amazon-web-services.yml
created: 2023/11/06
modified: 2024/05/27
specificationVersion: '0.18'
tags:
  - Cloud
apis:
  - name: AWS Certificate Manager
    description: >-
      Utilize the AWS Certificate Manager (ACM) to effortlessly handle the
      provisioning, management, and deployment of SSL/TLS certificates for both
      public and private use with AWS services and internal connected resources.
      With ACM, the tedious tasks of purchasing, uploading, and renewing SSL/TLS
      certificates are streamlined and automated, saving you valuable time and
      effort.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/certificate-manager/
    baseURL: https://example.com
    tags:
      - Certificates
      - Options
    properties:
      - type: Documentation
        url: https://aws.amazon.com/certificate-manager/
      - type: OpenAPI
        url: properties/acm-openapi-original.yml
      - type: Pricing
        url: https://aws.amazon.com/certificate-manager//pricing/
      - type: Getting Started
        url: https://aws.amazon.com/certificate-manager//getting-started/
      - type: Partners
        url: https://aws.amazon.com/certificate-manager//partners/
      - type: Events
        url: https://aws.amazon.com/certificate-manager//events/
      - type: Features
        url: https://aws.amazon.com/certificate-manager/features/
      - type: Resources
        url: https://aws.amazon.com/certificate-manager/resources/
      - type: FAQ
        url: https://aws.amazon.com/certificate-manager/faqs/
    overlays:
      - type: APIs.io Search
        url: overlays/acm-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/acm-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:acm
  - name: Amazon Identity and Access Management Access Analyzer
    description: >-
      The API for IAM Access Analyzer offers users a variety of tools to
      effectively manage their Identity and Access Management policies. These
      tools include the ability to identify external and unused access, perform
      basic and custom policy checks, and create highly detailed policies.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/iam/access-analyzer/
    baseURL: https://example.com
    tags:
      - ARN
      - Access
      - Analyzed
      - Analyzer
      - Analyzers
      - Archive
      - Checks
      - Findings
      - Generated
      - Generation
      - Grants
      - Names
      - Policies
      - Previews
      - Resources
      - Rules
      - Scans
      - Untag
      - Validate
      - Validations
    properties:
      - type: Documentation
        url: https://aws.amazon.com/iam/access-analyzer/
      - type: OpenAPI
        url: properties/accessanalyzer-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/accessanalyzer-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/accessanalyzer-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:accessanalyzer
  - name: AWS Migration Hub
    description: >-
      The AWS Migration Hub API provides users with the ability to view server
      and application migration progress and easily incorporate
      resource-specific migration tools through a code-based interface. To
      ensure smooth operation, it is crucial to specify your AWS Migration Hub
      home region before using any API functions to prevent encountering a
      HomeRegionNotSetException error. Furthermore, all API requests should
      originate from within your assigned home region for proper functioning.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/migration-hub/
    baseURL: https://example.com
    tags:
      - Attributes
      - Migrations
      - Resources
    properties:
      - type: Documentation
        url: https://aws.amazon.com/migration-hub/
      - type: OpenAPI
        url: properties/awsmigrationhub-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/migration-hub/features/
      - type: Pricing
        url: https://aws.amazon.com/migration-hub/pricing/
      - type: Getting Started
        url: https://aws.amazon.com/migration-hub/getting-started/
      - type: Resources
        url: https://aws.amazon.com/migration-hub/resources/
      - type: FAQ
        url: https://aws.amazon.com/migration-hub/faqs/
      - type: Partners
        url: https://aws.amazon.com/migration-hub/partners/
    overlays:
      - type: APIs.io Search
        url: overlays/awsmigrationhub-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/awsmigrationhub-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:awsmigrationhub
  - name: Amazon Managed Service for Prometheus
    description: >-
      The Amazon Managed Service for Prometheus API is a serverless monitoring
      service designed for container metrics. It allows users to securely
      monitor container environments at scale using the familiar open-source
      Prometheus data model and query language. This service provides improved
      scalability, availability, and security without the need to manage
      underlying infrastructure. The API includes both an Amazon Web Services
      API for managing resources such as workspaces, rule groups, and alert
      managers, as well as a Prometheus-compatible API for working within the
      Prometheus workspace.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/prometheus/
    baseURL: https://example.com
    tags:
      - ARN
      - Alert  Management
      - Alerts
      - Ali
      - Alias
      - Configurations
      - Default
      - Definitions
      - Describe
      - Groups
      - Logging
      - Managers
      - Names
      - Namespaces
      - Resources
      - Rule  Groups  Namespaces
      - Rule Groups
      - Rules
      - Scraper  Configurations
      - Scraper Configurations
      - Scrapers
      - Untag
      - Workspaces
    properties:
      - type: Documentation
        url: https://aws.amazon.com/prometheus/
      - type: OpenAPI
        url: properties/amp-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/prometheus/features/
      - type: Pricing
        url: https://aws.amazon.com/prometheus/pricing/
      - type: FAQ
        url: https://aws.amazon.com/prometheus/faqs/
      - type: Customers
        url: https://aws.amazon.com/prometheus/customers/
      - type: Partners
        url: https://aws.amazon.com/prometheus/partners/
      - type: Resources
        url: https://aws.amazon.com/prometheus/resources/
      - type: Videos
        url: https://aws.amazon.com/prometheus/videos/
    overlays:
      - type: APIs.io Search
        url: overlays/amp-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/amp-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:amp
  - name: Amazon API Gateway
    description: >-
      Amazon API Gateway is a powerful tool that enables developers to create
      and manage secure and scalable back ends for mobile and web applications.
      With API Gateway, developers can easily connect their applications to APIs
      running on Lambda, Amazon EC2, or other external web services. This
      ensures robust and reliable communication between applications and APIs,
      all within a secure environment.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/api-gateway/
    baseURL: https://example.com
    tags:
      - ARN
      - Accounts
      - Authorizers
      - Base Paths
      - Cache
      - Certificates
      - Clients
      - Data
      - Default
      - Deployments
      - Documentation
      - Domain Names
      - Domains
      - Exports
      - Flush
      - Gateways
      - Import
      - Integrations
      - Keys
      - Links
      - Mapping
      - Methods
      - Model Name
      - Models
      - Names
      - Parts
      - Paths
      - Plans
      - REST
      - Request Validators
      - Resources
      - Response Types
      - Responses
      - Stage Name
      - Stages
      - Status Codes
      - Tags
      - Templates
      - Types
      - Untag
      - Usage
      - Usage Plans
      - VPC
      - VPC Links
      - Validators
      - Versions
      - Vpclink
    properties:
      - type: Documentation
        url: https://aws.amazon.com/api-gateway/
      - type: OpenAPI
        url: properties/apigateway-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/api-gateway/features/
      - type: Pricing
        url: https://aws.amazon.com/api-gateway/pricing/
      - type: Getting Started
        url: https://aws.amazon.com/api-gateway/getting-started/
      - type: Resources
        url: https://aws.amazon.com/api-gateway/resources/
      - type: FAQ
        url: https://aws.amazon.com/api-gateway/faqs/
      - type: Documentation
        url: https://console.aws.amazon.com/apigateway/
      - type: Websockets
        url: >-
          https://docs.aws.amazon.com/apigateway/latest/developerguide/apigateway-websocket-api-overview.html
    overlays:
      - type: APIs.io Search
        url: overlays/apigateway-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/apigateway-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:apigateway
  - name: Amazon Web Services Private Certificate Authority
    description: >-
      The API Reference for Amazon Web Services Private Certificate Authority
      offers a detailed overview on setting up and controlling a private
      certificate authority (CA) for your organization. It provides in-depth
      explanations on each action and data type, including syntax and usage
      examples. The documentation for each action includes information on API
      request parameters and JSON responses. Additionally, users have the option
      to utilize Amazon Web Services SDKs for accessing APIs that are customized
      for their preferred programming language or platform.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/private-ca/
    baseURL: https://example.com
    tags:
      - Authorization
      - Certificates
    properties:
      - type: Documentation
        url: https://aws.amazon.com/private-ca/
      - type: OpenAPI
        url: properties/acm-pca-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/acm-pca-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/acm-pca-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:acm-pca
  - name: AWS Application Fabric
    description: >-
      The Amazon Web Services AppFabric API offers effortless incorporation of
      SaaS applications into your company's infrastructure, facilitating
      streamlined oversight and protection by IT and security professionals
      using a standardized data structure. Leveraging the capabilities of
      generative AI, employees can simplify their daily workflows.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/appfabric/
    baseURL: https://example.com
    tags:
      - ARN
      - Access
      - Application  Authorizations
      - Application  Bundles
      - Applications
      - Authorization
      - Batches
      - Bundles
      - Connect
      - Destinations
      - Ingestion  Destinations
      - Ingestions
      - Resources
      - Stop
      - Tasks
      - Untag
      - User  Access
      - Users
    properties:
      - type: Documentation
        url: https://aws.amazon.com/appfabric/
      - type: OpenAPI
        url: properties/appfabric-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/appfabric-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/appfabric-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:appfabric
  - name: Amazon AppFlow
    description: >-
      This API, Amazon AppFlow, allows for seamless automation of data flows
      between SaaS applications and AWS services with just a few clicks. You can
      run these data flows at your preferred frequency, whether on a schedule,
      in response to a business event, or on demand. Simplify data preparation
      through transformations, partitioning, and aggregation. Additionally,
      automate the preparation and registration of your schema with the AWS Glue
      Data Catalog for easy discovery and sharing of data with AWS analytics and
      machine learning services.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/appflow/
    baseURL: https://example.com
    tags:
      - ARN
      - Cache
      - Cancel
      - Connectors
      - Describe
      - Entities
      - Execution
      - Executions
      - Flows
      - Metadata
      - Profiles
      - Records
      - Register
      - Registrations
      - Reset
      - Resources
      - Stop
      - Unregister
      - Untag
    properties:
      - type: Documentation
        url: https://aws.amazon.com/appflow/
      - type: OpenAPI
        url: properties/appflow-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/appflow-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/appflow-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:appflow
  - name: AWS Auto Scaling
    description: >-
      AWS Auto Scaling is a service that automatically adjusts the capacity of
      your applications to maintain consistent performance at the most
      cost-effective rate. It allows you to easily set up scaling for multiple
      resources across various services in just minutes. With a user-friendly
      interface, you can create scaling plans for resources such as Amazon EC2
      instances, Amazon ECS tasks, Amazon DynamoDB tables, Amazon Aurora
      Replicas, and Spot Fleets.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/autoscaling/
    baseURL: https://example.com
    tags:
      - Resources
      - Tags
      - Untag
    properties:
      - type: Documentation
        url: https://aws.amazon.com/autoscaling/
      - type: OpenAPI
        url: properties/application-autoscaling-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/autoscaling/features/
      - type: Pricing
        url: https://aws.amazon.com/autoscaling/pricing/
      - type: Resources
        url: https://aws.amazon.com/autoscaling/resources/
      - type: FAQ
        url: https://aws.amazon.com/autoscaling/faqs/
    overlays:
      - type: APIs.io Search
        url: overlays/application-autoscaling-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/application-autoscaling-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:application-autoscaling
  - name: AWS Application Cost Profiler
    description: >-
      The AWS Application Cost Profiler API enables users to manage application
      cost report definitions, including viewing, creating, updating, and
      deleting them. It also allows users to import usage data into the
      Application Cost Profiler service. For more information on using this API,
      please consult the AWS Application Cost Profiler User Guide.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/aws-cost-management/aws-application-cost-profiler/
    baseURL: https://example.com
    tags:
      - Applications
      - Definitions
      - Import
      - Reports
      - Usage
    properties:
      - type: Documentation
        url: >-
          https://aws.amazon.com/aws-cost-management/aws-application-cost-profiler/
      - type: OpenAPI
        url: properties/applicationcostprofiler-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/applicationcostprofiler-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/applicationcostprofiler-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:applicationcostprofiler
  - name: AWS App Mesh
    description: >-
      The AWS App Mesh is a service mesh powered by the Envoy proxy that
      streamlines the monitoring and management of containerized microservices.
      It simplifies communication between microservices, providing in-depth
      visibility and ensuring reliable availability for applications. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/app-mesh/
    baseURL: https://example.com
    tags:
      - Gateways
      - Mesh
      - Meshes
      - Names
      - Nodes
      - Resources
      - Router
      - Routers
      - Routes
      - Services
      - Tags
      - Untag
      - Virtual
    properties:
      - type: Documentation
        url: https://aws.amazon.com/app-mesh/
      - type: OpenAPI
        url: properties/appmesh-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/app-mesh/features/
      - type: Pricing
        url: https://aws.amazon.com/app-mesh/pricing/
      - type: Getting Started
        url: https://aws.amazon.com/app-mesh/getting-started/
      - type: FAQ
        url: https://aws.amazon.com/app-mesh/faqs/
      - type: Resources
        url: https://aws.amazon.com/app-mesh/resources/
    overlays:
      - type: APIs.io Search
        url: overlays/appmesh-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/appmesh-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:appmesh
  - name: AWS AppSync
    description: >-
      With AWS AppSync, easily create serverless GraphQL and Pub/Sub APIs that
      streamline application development by providing a secure endpoint for
      querying, updating, and publishing data.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/appsync/
    baseURL: https://example.com
    tags:
      - ARN
      - Associate
      - Associations
      - Cache
      - Caches
      - Code
      - Creation
      - Data
      - Data Planes
      - Data Source
      - Disassociate
      - Domain Names
      - Domains
      - Environments
      - Evaluate
      - Evaluate Code
      - Evaluate Template
      - Fields
      - Flush
      - Functions
      - Graph QL
      - Introspections
      - Keys
      - Mapping
      - Merge
      - Merged
      - Names
      - Resolvers
      - Resources
      - Schemas
      - Sources
      - Tags
      - Templates
      - Types
      - Untag
      - Variables
    properties:
      - type: Documentation
        url: https://aws.amazon.com/appsync/
      - type: OpenAPI
        url: properties/appsync-openapi-original.yml
      - type: Pricing
        url: https://aws.amazon.com/appsync/pricing/
      - type: FAQ
        url: https://aws.amazon.com/appsync/faqs/
      - type: Customers
        url: https://aws.amazon.com/appsync/customers/
      - type: Resources
        url: https://aws.amazon.com/appsync/resources/
      - type: Blog
        url: https://aws.amazon.com/appsync/blog/
      - type: Introspection
        url: >-
          https://docs.aws.amazon.com/appsync/latest/devguide/rds-introspection.html
    overlays:
      - type: APIs.io Search
        url: overlays/appsync-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/appsync-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:appsync
  - name: Amazon AppStream
    description: >-
      Explore the Amazon AppStream 2.0 API Reference to access detailed
      descriptions and syntax for actions and data types within the service.
      Amazon AppStream 2.0 is a secure, fully managed application streaming
      service that allows you to effortlessly stream desktop applications to
      users without the need for application rewriting. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/appstream2/
    baseURL: https://example.com
    tags:
      - Stack
    properties:
      - type: Documentation
        url: https://aws.amazon.com/appstream2/
      - type: OpenAPI
        url: properties/appstream-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/appstream2/features/
      - type: Pricing
        url: https://aws.amazon.com/appstream2/pricing/
      - type: Getting Started
        url: https://aws.amazon.com/appstream2/getting-started/
      - type: Resources
        url: https://aws.amazon.com/appstream2/resources/
      - type: FAQ
        url: https://aws.amazon.com/appstream2/faqs/
      - type: Customers
        url: https://aws.amazon.com/appstream2/customers/
      - type: Vendors
        url: https://aws.amazon.com/appstream2/software-vendors/
      - type: Enterprise
        url: https://aws.amazon.com/appstream2/enterprises/
      - type: Education
        url: https://aws.amazon.com/appstream2/education/
    overlays:
      - type: APIs.io Search
        url: overlays/appstream-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/appstream-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:appstream
  - name: Amplify
    description: >-
      Amplify is an API designed to facilitate the development and deployment of
      cloud-powered mobile and web applications. Amplify Hosting offers a
      continuous delivery and hosting service specifically tailored for web
      applications. To learn more about Amplify Hosting, refer to the user
      guide. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/amplify/
    baseURL: https://example.com
    tags:
      - ARN
      - Access
      - Access Logs
      - Applications
      - Artifacts
      - Associations
      - Backend Environments
      - Backends
      - Branch
      - Branches
      - Deployments
      - Domains
      - Environments
      - Generate
      - Jobs
      - Logs
      - Names
      - Resources
      - Stop
      - Tags
      - URL
      - Untag
      - Webhooks
    properties:
      - type: Documentation
        url: https://aws.amazon.com/amplify/
      - type: OpenAPI
        url: properties/amplify-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/amplify-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/amplify-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:amplify
  - name: AWS App Runner
    description: >-
      App Runner is an application service on Amazon Web Services that allows
      you to quickly and easily deploy container images or source code to the
      cloud. It eliminates the need to learn new technologies or manually
      provision resources. App Runner seamlessly connects to your container
      registry or source code repository, providing a fully managed delivery
      pipeline with high performance, scalability, and security. For more
      information, refer to the App Runner Developer Guide and Release Notes. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/apprunner/
    baseURL: https://example.com
    tags:
      - Connections
      - Ingress
      - VPC
    properties:
      - type: Documentation
        url: https://aws.amazon.com/apprunner/
      - type: OpenAPI
        url: properties/apprunner-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/apprunner/features/
      - type: Pricing
        url: https://aws.amazon.com/apprunner/pricing/
      - type: Getting Started
        url: https://aws.amazon.com/apprunner/getting-started/
      - type: Resources
        url: https://aws.amazon.com/apprunner/resources/
      - type: FAQ
        url: https://aws.amazon.com/apprunner/faqs/
      - type: Customers
        url: https://aws.amazon.com/apprunner/customers/
      - type: Partners
        url: https://aws.amazon.com/apprunner/partners/
    overlays:
      - type: APIs.io Search
        url: overlays/apprunner-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/apprunner-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:apprunner
  - name: Amazon Athena
    description: >-
      Amazon Athena is a user-friendly query service that allows you to analyze
      data stored in Amazon S3 using standard SQL. By pointing Athena to your
      data in S3, you can easily run ad-hoc queries and receive results within
      seconds. This serverless tool eliminates the need for infrastructure setup
      and management, as you only pay for the queries you execute. Athena is
      designed to scale automatically, executing queries in parallel to deliver
      fast results even with large datasets and complex queries. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/athena/
    baseURL: https://example.com
    tags:
      - Group
      - Work
    properties:
      - type: Documentation
        url: https://aws.amazon.com/athena/
      - type: OpenAPI
        url: properties/athena-openapi-original.yml
      - type: Pricing
        url: https://aws.amazon.com/athena/pricing/
      - type: Getting Started
        url: https://aws.amazon.com/athena/getting-started/
      - type: Resources
        url: https://aws.amazon.com/athena/resources/
      - type: FAQ
        url: https://aws.amazon.com/athena/faqs/
      - type: Features
        url: https://aws.amazon.com/athena/features/
      - type: Spark
        url: https://aws.amazon.com/athena/spark/
      - type: Connectors
        url: https://docs.aws.amazon.com/athena/latest/ug/connectors-prebuilt.html
    overlays:
      - type: APIs.io Search
        url: overlays/athena-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/athena-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:athena
  - name: Amazon EC2 Auto Scaling
    description: >-
      The Amazon EC2 Auto Scaling API allows users to automate the launching and
      terminating of EC2 instances based on predefined scaling policies,
      scheduled actions, and health checks. Refer to the Amazon EC2 Auto Scaling
      User Guide and API Reference for further details.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/ec2/autoscaling/
    baseURL: https://example.com
    tags:
      - Auto
      - Group
      - Scaling
    properties:
      - type: Documentation
        url: https://aws.amazon.com/ec2/autoscaling/
      - type: OpenAPI
        url: properties/autoscaling-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/ec2/autoscaling/features/
      - type: Pricing
        url: https://aws.amazon.com/ec2/autoscaling/pricing/
      - type: Getting Started
        url: https://aws.amazon.com/ec2/autoscaling/getting-started/
      - type: Resources
        url: https://aws.amazon.com/ec2/autoscaling/resources/
      - type: FAQ
        url: https://aws.amazon.com/ec2/autoscaling/faqs/
      - type: Tutorial
        url: >-
          https://docs.aws.amazon.com/autoscaling/latest/userguide/GettingStartedTutorial.html
    overlays:
      - type: APIs.io Search
        url: overlays/autoscaling-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/autoscaling-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:autoscaling
  - name: AWS B2B Data Interchange
    description: >-
      The Amazon Web Services B2B Data Interchange API Reference is a
      comprehensive guide that includes detailed descriptions, API request
      parameters, and XML responses for each of the B2BI API actions. B2BI
      facilitates the seamless exchange of EDI-based business transactions at
      cloud scale, offering elasticity and pay-as-you-go pricing. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/b2b-data-interchange/
    baseURL: https://example.com
    tags:
      - Transformers
    properties:
      - type: Documentation
        url: https://aws.amazon.com/b2b-data-interchange/
      - type: OpenAPI
        url: properties/b2bi-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/b2b-data-interchange/features/
      - type: Pricing
        url: https://aws.amazon.com/b2b-data-interchange/features/
      - type: FAQ
        url: https://aws.amazon.com/b2b-data-interchange/faqs/
    overlays:
      - type: APIs.io Search
        url: overlays/b2bi-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/b2bi-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:b2bi
  - name: AWS Audit Manager
    description: >-
      Introducing the Audit Manager API reference, a comprehensive resource for
      developers looking for in-depth insights into Audit Manager API
      functionalities, data structures, and error handling. Audit Manager is a
      robust service designed to automate the collection of evidence to support
      ongoing auditing of your Amazon Web Services usage. With this tool, users
      can evaluate the effectiveness of controls, mitigate risks, and simplify
      compliance procedures.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/audit-manager/
    baseURL: https://example.com
    tags:
      - ARN
      - Accounts
      - Administrative
      - Assessments
      - Associate
      - Attributes
      - Batches
      - Change
      - Change Logs
      - Controls
      - Data
      - Delegation
      - Delegations
      - Deregister
      - Disassociate
      - Domains
      - Evidence
      - File
      - Folders
      - Frameworks
      - Import
      - Insights
      - Integrity
      - Keywords
      - Logs
      - Notifications
      - Organizations
      - Register
      - Reports
      - Resources
      - Scopes
      - Services
      - Sets
      - Settings
      - Share
      - Sources
      - Status
      - Tags
      - URL
      - Untag
      - Uploads
      - Validate
    properties:
      - type: Documentation
        url: https://aws.amazon.com/audit-manager/
      - type: OpenAPI
        url: properties/auditmanager-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/audit-manager/features/
      - type: Pricing
        url: https://aws.amazon.com/audit-manager/pricing/
      - type: Getting Started
        url: https://aws.amazon.com/audit-manager/getting-started/
      - type: FAQ
        url: https://aws.amazon.com/audit-manager/faqs/
      - type: User Guide
        url: >-
          https://docs.aws.amazon.com/audit-manager/latest/userguide/framework-overviews.html
      - type: Examples
        url: >-
          https://docs.aws.amazon.com/audit-manager/latest/userguide/security_iam_id-based-policy-examples.html
      - type: Dashboard
        url: >-
          https://docs.aws.amazon.com/audit-manager/latest/userguide/dashboard.html
    overlays:
      - type: APIs.io Search
        url: overlays/auditmanager-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/auditmanager-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:auditmanager
  - name: AWS Auto Scaling
    description: >-
      This API allows you to easily create and manage scaling plans for your
      applications using AWS Auto Scaling. With this service, you can define
      target tracking scaling policies to automatically scale your AWS resources
      based on utilization, as well as scale Amazon EC2 Auto Scaling groups
      using predictive scaling and dynamic scaling to quickly adjust your
      capacity. You can also set minimum and maximum capacity limits, retrieve
      information on existing scaling plans, and access forecast data for up to
      56 days previous.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/autoscaling/
    baseURL: https://example.com
    tags:
      - Plan
      - Scaling
    properties:
      - type: Documentation
        url: https://aws.amazon.com/autoscaling/
      - type: OpenAPI
        url: properties/autoscaling-plans-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/autoscaling/features/
      - type: Pricing
        url: https://aws.amazon.com/autoscaling/pricing/
      - type: Resources
        url: https://aws.amazon.com/autoscaling/resources/
      - type: FAQ
        url: https://aws.amazon.com/autoscaling/faqs/
    overlays:
      - type: APIs.io Search
        url: overlays/autoscaling-plans-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/autoscaling-plans-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:autoscaling-plans
  - name: AWS Backup
    description: >-
      This API, Backup Backup, offers a comprehensive backup solution
      specifically tailored for Amazon Web Services (AWS) and its related data.
      With features such as simplified backup creation, migration, restoration,
      and deletion, as well as robust reporting and auditing capabilities,
      Backup Backup ensures the protection of your AWS services and data.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/backup/
    baseURL: https://example.com
    tags:
      - ARN
      - Access
      - Accounts
      - Air
      - Associations
      - Audit
      - Backup
      - Cancel
      - Configurations
      - Copy
      - Describe
      - Disassociate
      - Exports
      - Frameworks
      - Gapped
      - Global
      - Hold
      - Holds
      - Inferred
      - JSON
      - Jobs
      - Legal
      - Lifecycle
      - Locks
      - Logically
      - Metadata
      - Names
      - Notifications
      - Parents
      - Plan
      - Plans
      - Points
      - Policies
      - Protected
      - Recovery
      - Regions
      - Reports
      - Resources
      - Restore
      - Results
      - Selections
      - Settings
      - Stop
      - Summaries
      - Supported
      - Tags
      - Templates
      - Testing
      - Types
      - Untag
      - Val
      - Validations
      - Vault
      - Vaults
      - Versions
    properties:
      - type: Documentation
        url: https://aws.amazon.com/backup/
      - type: OpenAPI
        url: properties/backup-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/backup/#
      - type: Pricing
        url: https://aws.amazon.com/backup/pricing/?nc=sn&loc=3
      - type: Getting Started
        url: https://aws.amazon.com/backup/getting-started/?nc=sn&loc=4
      - type: Resources
        url: https://aws.amazon.com/backup/resources/
      - type: FAQ
        url: https://aws.amazon.com/backup/faqs/?nc=sn&loc=6
      - type: Customers
        url: https://aws.amazon.com/backup/customers/?nc=sn&loc=7
    overlays:
      - type: APIs.io Search
        url: overlays/backup-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/backup-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:backup
  - name: AWS Batch
    description: >-
      Batch Using Batch, you can run batch computing workloads on the Amazon Web
      Services Cloud. Batch computing is a common means for developers,
      scientists, and engineers to access large amounts of compute resources.
      Batch uses the advantages of the batch computing to remove the
      undifferentiated heavy lifting of configuring and managing required
      infrastructure. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/batch/
    baseURL: https://example.com
    tags:
      - ARN
      - Cancel
      - Cancel Jobs
      - Compute
      - Computer Environments
      - Definitions
      - Deregister
      - Deregister Job Definitions
      - Describe
      - Environments
      - Job Definitions
      - Job Queues
      - Jobs
      - Policies
      - Queues
      - Register
      - Register Job Definitions
      - Resources
      - Scheduling
      - Scheduling Policies
      - Scheduling Policy
      - Submit
      - Submit Jobs
      - Tags
      - Terminate
      - Terminate Jobs
      - Untag
    properties:
      - type: Documentation
        url: https://aws.amazon.com/batch/
      - type: OpenAPI
        url: properties/batch-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/batch/features/?nc=sn&loc=2
      - type: Pricing
        url: https://aws.amazon.com/batch/pricing/?nc=sn&loc=3
      - type: FAQ
        url: https://aws.amazon.com/batch/faqs/
    overlays:
      - type: APIs.io Search
        url: overlays/batch-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/batch-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:batch
  - name: Amazon Bedrock Agent
    description: >-
      Enhance the capabilities of generative AI applications by allowing them to
      seamlessly perform complex multi-step tasks across various company systems
      and data sources. Amazon Bedrock agents improve operational efficiency,
      customer service, and decision-making processes whilst simultaneously
      driving down costs and fostering innovation within the organization.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/bedrock/agents/
    baseURL: https://example.com
    tags:
      - Agent
      - Agents
      - Alias
      - Aliases
      - Base
      - Generate
      - Invoke
      - Knowledge
      - Knowledgebases
      - Retrieve
      - Sessions
      - Text
    properties:
      - type: Documentation
        url: https://aws.amazon.com/bedrock/agents/
      - type: OpenAPI
        url: properties/bedrock-agent-runtime-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/bedrock/agents/#
      - type: Pricing
        url: >-
          https://aws.amazon.com/bedrock/pricing/?refid=0eaabb80-ee46-4e73-94ae-368ffb759b62
      - type: Models
        url: https://aws.amazon.com/bedrock/agents/
      - type: FAQ
        url: >-
          https://aws.amazon.com/bedrock/faqs/?refid=0eaabb80-ee46-4e73-94ae-368ffb759b62
      - type: Testimonials
        url: https://aws.amazon.com/bedrock/testimonials/
      - type: Resources
        url: >-
          https://aws.amazon.com/bedrock/resources/?refid=0eaabb80-ee46-4e73-94ae-368ffb759b62
    overlays:
      - type: APIs.io Search
        url: overlays/bedrock-agent-runtime-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/bedrock-agent-runtime-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:bedrock-agent-runtime
  - name: AWS Billing Conductor
    description: >-
      The Amazon Web Services Billing Conductor API is a fully managed service
      that allows you to customize your billing data each month for accurate
      showback or chargeback to your end customers. It does not alter the way
      you are billed by AWS, but rather enables you to configure, generate, and
      display rates for specific customers during a billing period. You can also
      compare the rates you set to your actual AWS rates. With the API, payer
      accounts can view custom rates on the billing details page or set up cost
      and usage reports per billing group. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/aws-cost-management/aws-billing-conductor/
    baseURL: https://example.com
    tags:
      - ARN
      - Accounts
      - Associate
      - Associated
      - Associations
      - Batches
      - Billing
      - Cost
      - Custom
      - Disassociate
      - Groups
      - Items
      - Line
      - Plan
      - Plans
      - Pricing
      - Reports
      - Resources
      - Rules
      - Tags
      - Untag
      - Versions
    properties:
      - type: Documentation
        url: https://aws.amazon.com/aws-cost-management/aws-billing-conductor/
      - type: OpenAPI
        url: properties/billingconductor-openapi-original.yml
      - type: Features
        url: >-
          https://aws.amazon.com/aws-cost-management/aws-billing-conductor/features/
      - type: Pricing
        url: >-
          https://aws.amazon.com/aws-cost-management/aws-billing-conductor/pricing/
      - type: Getting Started
        url: >-
          https://aws.amazon.com/aws-cost-management/aws-billing-conductor/getting-started/
      - type: FAQ
        url: https://aws.amazon.com/aws-cost-management/aws-billing-conductor/faqs/
    overlays:
      - type: APIs.io Search
        url: overlays/billingconductor-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/billingconductor-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:billingconductor
  - name: AWS Budgets
    description: >-
      Manage your expenses and usage with ease using the AWS Budgets API. Create
      personalized budgets to monitor your costs and usage, and receive instant
      notifications via email or SNS alerts if you surpass your set threshold.
      Stay on top of your spending and act swiftly to prevent overages.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/aws-cost-management/aws-budgets/
    baseURL: https://example.com
    tags:
      - Subscribers
    properties:
      - type: Documentation
        url: https://aws.amazon.com/aws-cost-management/aws-budgets/
      - type: OpenAPI
        url: properties/budgets-openapi-original.yml
      - type: Pricing
        url: https://aws.amazon.com/aws-cost-management/aws-budgets/pricing/
      - type: FAQ
        url: https://aws.amazon.com/aws-cost-management/aws-budgets/faqs/
      - type: Reports
        url: >-
          https://aws.amazon.com/blogs/aws-cloud-financial-management/launch-aws-budgets-reports/
    overlays:
      - type: APIs.io Search
        url: overlays/budgets-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/budgets-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:budgets
  - name: AWS  Cost Explorer
    description: >-
      The Cost Explorer API allows you to access your cost and usage data
      programmatically. You can retrieve aggregated information like total
      monthly costs or daily usage, as well as more detailed data such as
      specific operations for services like Amazon DynamoDB. The service
      endpoint for the Cost Explorer API is https://ce.us-east-1.amazonaws.com.
      For pricing details, refer to Amazon Web Services Cost Management Pricing.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/aws-cost-management/aws-cost-explorer/
    baseURL: https://ce.us-east-1.amazonaws.com
    tags:
      - Categories
      - Cost
      - Definitions
    properties:
      - type: Documentation
        url: https://aws.amazon.com/aws-cost-management/aws-cost-explorer/
      - type: OpenAPI
        url: properties/ce-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/aws-cost-management/aws-cost-explorer/features/
      - type: Pricing
        url: https://aws.amazon.com/aws-cost-management/aws-cost-explorer/pricing/
      - type: FAQ
        url: https://aws.amazon.com/aws-cost-management/aws-cost-explorer/faqs/
      - type: Getting Started
        url: >-
          https://aws.amazon.com/aws-cost-management/aws-cost-explorer/getting-started/
    overlays:
      - type: APIs.io Search
        url: overlays/ce-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/ce-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:ce
  - name: AWS Chime
    description: >-
      The Amazon Chime API is a comprehensive communications solution that
      allows users to host online meetings, chat, and make business calls from a
      single platform. Key features include hosting high-quality video meetings,
      audio calls, screen sharing, meeting chat, dial-in numbers, and in-room
      video conferencing. The API also includes chat and chat room functionality
      for ongoing communications, as well as user management and advanced
      features like single sign-on (SSO) via the Amazon Chime management
      console. The user-friendly app is compatible with Windows, Mac, web, iOS,
      and Android devices. Developers can further enhance their applications
      with messaging, audio, video, and screen sharing capabilities using the
      Amazon Chime SDK.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/chime/
    baseURL: https://example.com
    tags:
      - ARN
      - Accounts
      - Addresses
      - Administrative
      - Administrator
      - Applications
      - Arn?scope=app
      - Associate
      - Attendees
      - Available
      - Batches
      - Bots
      - Call
      - Calling
      - Calls
      - Capture
      - Channels
      - Configurations
      - Connectors
      - Conversations
      - Countries
      - Credentials
      - Delegate
      - Describe
      - Dial
      - Disassociate
      - Emergency
      - Endpoints
      - Events
      - Global
      - Groups
      - Health
      - Id?operation=disassociate
      - Id?operation=logout
      - Instances
      - Invite
      - Logging
      - Logout
      - Marker
      - Media
      - Meetings
      - Members
      - Memberships
      - Messages
      - Messaging
      - Moderated
      - Moderators
      - Numbers
      - Orders
      - Origination
      - Out
      - PIN
      - Personal
      - Phone
      - Pin
      - Pipelines
      - Programmable
      - Proxy
      - Read
      - Redact
      - Regenerate
      - Reset
      - Resources
      - Restore
      - Retention
      - Rooms
      - Rules
      - SIP
      - Search
      - Security
      - Send
      - Sessions
      - Settings
      - Sign In
      - Stop
      - Streaming
      - Supported
      - Suspend
      - Tags
      - Termination
      - Tokens
      - Transactions
      - Transcriptions
      - Unsuspend
      - Untag
      - Users
      - Validate
    properties:
      - type: Documentation
        url: https://aws.amazon.com/chime/
      - type: OpenAPI
        url: properties/chime-openapi-original.yml
      - type: Contact
        url: https://pages.awscloud.com/chime-contact-us
      - type: SDK
        url: https://aws.amazon.com/chime/chime-sdk/
      - type: Downloads
        url: https://aws.amazon.com/chime/download/
      - type: Answers
        url: http://answers.chime.aws
      - type: Pricing
        url: https://aws.amazon.com/chime/pricing/
      - type: Customers
        url: https://aws.amazon.com/chime/customers/
      - type: FAQ
        url: https://aws.amazon.com/chime/faq/
      - type: Getting Started
        url: https://aws.amazon.com/chime/getting-started/
      - type: Features
        url: https://aws.amazon.com/chime/features/
    overlays:
      - type: APIs.io Search
        url: overlays/chime-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/chime-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:chime
  - name: AWS Clean Rooms
    description: >-
      Introducing the Clean Rooms API, designed for use with Amazon Web
      Services. This API allows multiple parties to securely collaborate and
      combine their data in a shared workspace. This collaborative environment
      enables members to query and receive insights from aggregated datasets
      without exposing raw data to other parties. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/clean-rooms/
    baseURL: https://example.com
    tags:
      - ARN
      - Accounts
      - Analysis
      - Analysis Templates
      - Associations
      - Audience
      - Batches
      - Budgets
      - Collaboration
      - Collaborations
      - Configuration Audience Model Associations
      - Configured
      - Impact
      - Members
      - Memberships
      - Models
      - Names
      - Previews
      - Privacy
      - Privacy Budget Templates
      - Privacy Budgets
      - Protected
      - Queries
      - Resources
      - Rules
      - Schemas
      - Tables
      - Tags
      - Templates
      - Types
      - Untag
    properties:
      - type: Documentation
        url: https://aws.amazon.com/clean-rooms/
      - type: OpenAPI
        url: properties/cleanrooms-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/clean-rooms/#
      - type: FAQ
        url: https://aws.amazon.com/clean-rooms/faqs/
      - type: Customers
        url: https://aws.amazon.com/clean-rooms/customers/
      - type: Partners
        url: https://aws.amazon.com/clean-rooms/partners/
      - type: Pricing
        url: https://aws.amazon.com/clean-rooms/pricing/
      - type: Resources
        url: https://aws.amazon.com/clean-rooms/resources/
    overlays:
      - type: APIs.io Search
        url: overlays/cleanrooms-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/cleanrooms-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:cleanrooms
  - name: ' Amazon Braket'
    description: >-
      Amazon Braket is a comprehensive and user-friendly quantum computing
      service designed to support researchers and developers in leveraging the
      power of quantum technology to enhance their research and speed up
      discovery processes. With Amazon Braket, users have access to an
      integrated development environment that enables them to experiment with
      and create quantum algorithms, validate them using quantum circuit
      simulators, and execute them on a variety of quantum hardware platforms.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/braket/
    baseURL: https://example.com
    tags:
      - ARN
      - Cancel
      - Device
      - Devices
      - Jobs
      - Quantum
      - Resources
      - Search
      - Tags
      - Tasks
      - Untag
    properties:
      - type: Documentation
        url: https://aws.amazon.com/braket/
      - type: OpenAPI
        url: properties/braket-openapi-original.yml
      - type: Getting Started
        url: https://aws.amazon.com/braket/#
      - type: Quantum Computers
        url: https://aws.amazon.com/braket/#
      - type: Customers
        url: https://aws.amazon.com/braket/customers/
      - type: Features
        url: https://aws.amazon.com/braket/features/
      - type: Pricing
        url: https://aws.amazon.com/braket/pricing/
      - type: FAQ
        url: https://aws.amazon.com/braket/faqs/
    overlays:
      - type: APIs.io Search
        url: overlays/braket-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/braket-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:braket
  - name: AWS Cloud Control
    description: >-
      The AWS Cloud Control API simplifies the management of AWS and third-party
      services by providing a standardized set of APIs for developers and
      partners. With five key operations (CRUDL), users can easily create, read,
      update, delete, and list their cloud infrastructure.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/cloudcontrolapi/
    baseURL: https://example.com
    tags:
      - Resources
    properties:
      - type: Documentation
        url: https://aws.amazon.com/cloudcontrolapi/
      - type: OpenAPI
        url: properties/cloudcontrol-openapi-original.yml
      - type: Pricing
        url: https://aws.amazon.com/cloudcontrolapi/pricing/
      - type: Resources
        url: https://aws.amazon.com/cloudcontrolapi/resources/
      - type: FAQ
        url: https://aws.amazon.com/cloudcontrolapi/faqs/
      - type: User Guide
        url: >-
          https://docs.aws.amazon.com/cloudcontrolapi/latest/userguide/what-is-cloudcontrolapi.html
    overlays:
      - type: APIs.io Search
        url: overlays/cloudcontrol-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/cloudcontrol-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:cloudcontrol
  - name: Amazon Cloud Directory
    description: >-
      The Amazon Cloud Directory is a feature within the AWS Directory Service
      designed to streamline the creation and organization of large-scale cloud
      applications for web, mobile, and IoT platforms. This documentation
      provides a comprehensive overview of Cloud Directory operations that can
      be accessed programmatically, offering detailed insights into data types
      and potential errors. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/cloud-directory/
    baseURL: https://example.com
    tags:
      - ARN
      - Applied Schema
      - Attach
      - Attached
      - Attachments
      - Attributes
      - Batches
      - Children
      - Detach
      - Development
      - Directories
      - Directory
      - Disable
      - Enable
      - Facets
      - Incoming
      - Index
      - Indices
      - Information
      - JSON
      - Link
      - Links
      - Lookups
      - Managed
      - Names
      - Objects
      - Outgoing
      - Parent Paths
      - Parents
      - Paths
      - Policies
      - Publish
      - Published
      - Read
      - Removes
      - Resources
      - Schemas
      - Tags
      - Targets
      - Typed
      - Typed Links
      - Untag
      - Upgrade
      - Upgrade Applied
      - Upgradepublished
      - Versions
      - Write
    properties:
      - type: Documentation
        url: https://aws.amazon.com/cloud-directory/
      - type: OpenAPI
        url: properties/clouddirectory-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/cloud-directory/features/
      - type: Pricing
        url: https://aws.amazon.com/cloud-directory/pricing/
      - type: Getting Started
        url: https://aws.amazon.com/cloud-directory/getting-started/
      - type: FAQ
        url: https://aws.amazon.com/cloud-directory/faqs/
    overlays:
      - type: APIs.io Search
        url: overlays/clouddirectory-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/clouddirectory-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:clouddirectory
  - name: AWS CloudFormation
    description: >-
      CloudFormation is an Amazon Web Services tool that allows users to easily
      create and manage infrastructure deployments in a predictable and
      repeatable manner. With CloudFormation, you can utilize various AWS
      products like EC2, EBS, SNS, ELB, and Auto Scaling to build reliable and
      scalable applications without needing to manually configure the underlying
      infrastructure. By declaring resources and their dependencies in a
      template file, CloudFormation organizes them into a stack, enabling
      seamless creation and deletion of all resources within the stack while
      managing dependencies between them.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/cloudformation/
    baseURL: https://example.com
    tags:
      - Templates
      - Validate
    properties:
      - type: Documentation
        url: https://aws.amazon.com/cloudformation/
      - type: OpenAPI
        url: properties/cloudformation-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/cloudformation/features/
      - type: Pricing
        url: https://aws.amazon.com/cloudformation/pricing/
      - type: Getting Started
        url: https://aws.amazon.com/cloudformation/getting-started/
      - type: Resources
        url: https://aws.amazon.com/cloudformation/resources/
      - type: Partners
        url: https://aws.amazon.com/cloudformation/partners/
      - type: FAQ
        url: https://aws.amazon.com/cloudformation/faqs/
    overlays:
      - type: APIs.io Search
        url: overlays/cloudformation-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/cloudformation-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:cloudformation
  - name: AWS Cloud9
    description: >-
      The Cloud9 API provides a wide range of tools for coding, building,
      running, testing, debugging, and releasing software in the cloud. Users
      can access these features through operations such as creating a
      development environment on Amazon EC2, managing environment memberships,
      deleting environments and members, getting information about environments
      and members, listing environments, managing tags, and updating environment
      settings. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/cloud9/
    baseURL: https://example.com
    tags:
      - Environments
      - Memberships
    properties:
      - type: Documentation
        url: https://aws.amazon.com/cloud9/
      - type: OpenAPI
        url: properties/cloud9-openapi-original.yml
      - type: Pricing
        url: https://aws.amazon.com/cloud9/pricing/
      - type: Getting Started
        url: https://aws.amazon.com/cloud9/getting-started/
      - type: FAQ
        url: https://aws.amazon.com/cloud9/faqs/
      - type: Environments
        url: >-
          https://aws.amazon.com/blogs/aws/aws-cloud9-cloud-developer-environments/
    overlays:
      - type: APIs.io Search
        url: overlays/cloud9-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/cloud9-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:cloud9
  - name: Amazon CloudFront
    description: >-
      Amazon CloudFront is a reliable global content delivery network (CDN)
      service that speeds up the delivery of websites, APIs, video content, and
      other web assets. By seamlessly integrating with various Amazon Web
      Services products, developers and businesses can effortlessly optimize
      content delivery to end users without any mandatory usage requirements.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/cloudfront/
    baseURL: https://example.com
    tags:
      - Access
      - Alias
      - Aliases
      - Associate
      - Cache
      - Cloud
      - Cloudfront
      - Configurations
      - Conflicting
      - Continuous
      - Controls
      - Copy
      - Deployments
      - Describe
      - Distributions
      - Encryption
      - Entities
      - Fields
      - Front
      - Functions
      - Groups
      - Headers
      - Identities
      - Identity
      - Invalidations
      - Keys
      - Levels
      - Logs
      - Monitoring
      - Names
      - Operations
      - Origin
      - Policies
      - Primary
      - Profiles
      - Promote
      - Public
      - Publish
      - Real Time
      - Resources
      - Responses
      - Staging
      - Store
      - Stores
      - Streaming
      - Subscriptions
      - Tagging
      - Tags
      - Targets
      - Tests
      - Untag
      - Value
      - Web
    properties:
      - type: Documentation
        url: https://aws.amazon.com/cloudfront/
      - type: OpenAPI
        url: properties/cloudfront-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/cloudfront/features/
      - type: Pricing
        url: https://aws.amazon.com/cloudfront/pricing/
      - type: Getting Started
        url: https://aws.amazon.com/cloudfront/getting-started/
      - type: Media
        url: https://aws.amazon.com/cloudfront/media/
      - type: Custoners
        url: https://aws.amazon.com/cloudfront/customers/
      - type: Partners
        url: https://aws.amazon.com/cloudfront/partners/
      - type: Resources
        url: https://aws.amazon.com/cloudfront/resources/
      - type: FAQ
        url: https://aws.amazon.com/cloudfront/faqs/
    overlays:
      - type: APIs.io Search
        url: overlays/cloudfront-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/cloudfront-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:cloudfront
  - name: AWS Clean Rooms ML
    description: >-
      Introducing the Amazon Web Services Clean Rooms ML API Reference, a
      solution that offers a secure way for two parties to identify similar
      users in their datasets without sharing their data. First, one party
      provides training data to create and configure an audience model, which is
      associated with a collaboration. Then, the second party brings their seed
      data to generate an audience that closely resembles the training data.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/clean-rooms/ml/
    baseURL: https://example.com
    tags:
      - ARN
      - Audience
      - Configured
      - Datasets
      - Exports
      - Generation
      - Jobs
      - Models
      - Policies
      - Resources
      - Tags
      - Training
      - Untag
    properties:
      - type: Documentation
        url: https://aws.amazon.com/clean-rooms/ml/
      - type: OpenAPI
        url: properties/cleanroomsml-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/clean-rooms/ml/
      - type: FAQ
        url: https://aws.amazon.com/clean-rooms/faqs/
      - type: Customers
        url: https://aws.amazon.com/clean-rooms/customers/
      - type: Partners
        url: https://aws.amazon.com/clean-rooms/partners/
      - type: Pricing
        url: https://aws.amazon.com/clean-rooms/pricing/
      - type: Resources
        url: https://aws.amazon.com/clean-rooms/resources/
    overlays:
      - type: APIs.io Search
        url: overlays/cleanroomsml-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/cleanroomsml-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:cleanroomsml
  - name: AWS CloudHSM
    description: >-
      The AWS CloudHSM API provides a secure and compliant solution for managing
      and accessing keys on FIPS-validated hardware. With customer-owned,
      single-tenant HSM instances running in your Virtual Private Cloud (VPC),
      you can easily meet corporate, contractual, and regulatory data security
      requirements.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/cloudhsm/
    baseURL: https://example.com
    tags:
      - Resources
      - Untag
    properties:
      - type: Documentation
        url: https://aws.amazon.com/cloudhsm/
      - type: OpenAPI
        url: properties/cloudhsmv2-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/cloudhsm/features/
      - type: Pricing
        url: https://aws.amazon.com/cloudhsm/pricing/
      - type: Getting Started
        url: https://aws.amazon.com/cloudhsm/getting-started/
      - type: Resources
        url: https://aws.amazon.com/cloudhsm/resources/
      - type: Customers
        url: https://aws.amazon.com/cloudhsm/customers/
      - type: FAQ
        url: https://aws.amazon.com/cloudhsm/faqs/
    overlays:
      - type: APIs.io Search
        url: overlays/cloudhsmv2-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/cloudhsmv2-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:cloudhsmv2
  - name: Amazon CloudSearch
    description: >-
      Amazon CloudSearch, is a cloud-based service that simplifies the process
      of setting up, managing, and expanding a search solution for your website.
      It allows you to easily search through extensive datasets, including web
      pages, documents, forum posts, and product information. With Amazon
      CloudSearch, you can enhance your website with search functionality
      without the need for extensive expertise or concerns about hardware
      management. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://docs.aws.amazon.com/cloudsearch/
    baseURL: https://example.com
    tags:
      - Access
      - Policies
      - Services
    properties:
      - type: Documentation
        url: https://docs.aws.amazon.com/cloudsearch/
      - type: OpenAPI
        url: properties/cloudsearch-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/cloudsearch-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/cloudsearch-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:cloudsearch
  - name: AWS CloudTrail
    description: >-
      With AWS CloudTrail, you can monitor your AWS deployments in the cloud by
      getting a history of AWS API calls for your account, including API calls
      made by using the AWS Management Console, the AWS SDKs, the command line
      tools, and higher-level AWS services. You can also identify which users
      and accounts called AWS APIs for services that support CloudTrail, the
      source IP address from which the calls were made, and when the calls
      occurred. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://docs.aws.amazon.com/cloudtrail/
    baseURL: https://example.com
    tags:
      - Audit
      - Events
    properties:
      - type: Documentation
        url: https://docs.aws.amazon.com/cloudtrail/
      - type: OpenAPI
        url: properties/cloudtrail-data-openapi-original.yml
      - type: User Guide
        url: https://docs.aws.amazon.com/awscloudtrail/latest/userguide/index.html
      - type: Partners
        url: >-
          https://docs.aws.amazon.com/awscloudtrail/latest/partner-onboarding/cloudtrail-lake-partner-onboarding.html
    overlays:
      - type: APIs.io Search
        url: overlays/cloudtrail-data-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/cloudtrail-data-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:cloudtrail-data
  - name: Amazon CodeCatalyst
    description: >-
      Amazon CodeCatalyst is a unified software development service for
      development teams to quickly build, deliver and scale applications on AWS
      while adhering to organization-specific best practices. Developers can
      automate development tasks and innovate faster with generative AI
      capabilities, and spend less time setting up project tools, managing CI/CD
      pipelines, provisioning and configuring various development environments
      or coordinating with team members.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/codecatalyst/
    baseURL: https://example.com
    tags:
      - Access
      - Branch
      - Branches
      - Clone
      - Details
      - Environments
      - Events
      - Logs
      - Names
      - Projects
      - Repositories
      - Runs
      - Sessions
      - Sources
      - Space
      - Spaces
      - Stop
      - Subscriptions
      - Tokens
      - URL
      - Users
      - Verify
      - Workflows
    properties:
      - type: Documentation
        url: https://aws.amazon.com/codecatalyst/
      - type: OpenAPI
        url: properties/codecatalyst-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/codecatalyst-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/codecatalyst-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:codecatalyst
  - name: AWS CodeBuild
    description: >+
      AWS CodeBuild is a fully managed continuous integration service that
      compiles source code, runs tests, and produces ready-to-deploy software
      packages. With CodeBuild, you don’t need to provision, manage, and scale
      your own build servers. You just specify the location of your source code
      and choose your build settings, and CodeBuild will run your build scripts
      for compiling, testing, and packaging your code.

    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/codebuild/
    baseURL: https://example.com
    tags:
      - Webhooks
    properties:
      - type: Documentation
        url: https://aws.amazon.com/codebuild/
      - type: OpenAPI
        url: properties/codebuild-openapi-original.yml
      - type: Testimonials
        url: https://aws.amazon.com/codebuild/customer-testimonials/
      - type: Integrations
        url: https://aws.amazon.com/codebuild/product-integrations/
      - type: FAQ
        url: https://aws.amazon.com/codebuild/faqs/
      - type: Getting Started
        url: https://aws.amazon.com/codebuild/getting-started/
      - type: Pricing
        url: https://aws.amazon.com/codebuild/pricing/
      - type: Features
        url: https://aws.amazon.com/codebuild/features/
    overlays:
      - type: APIs.io Search
        url: overlays/codebuild-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/codebuild-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:codebuild
  - name: Amazon CodeGuru Reviewer
    description: >-
      Amazon CodeGuru Reviewer is a service that uses program analysis and
      machine learning to detect potential defects that are difficult for
      developers to find and offers suggestions for improving your Java and
      Python code. This service has been released for general availability in
      several Regions.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://docs.aws.amazon.com/codeguru/latest/reviewer-api/index.html
    baseURL: https://example.com
    tags:
      - ARN
      - Associations
      - Code
      - Code Reviews
      - Describe
      - Disassociate
      - Feedback
      - Recommendations
      - Repositories
      - Resources
      - Reviews
      - Tags
      - Untag
    properties:
      - type: Documentation
        url: https://docs.aws.amazon.com/codeguru/latest/reviewer-api/index.html
      - type: OpenAPI
        url: properties/codeguru-reviewer-openapi-original.yml
      - type: User Guide
        url: https://docs.aws.amazon.com/codeguru/latest/reviewer-ug/index.html
      - type: CLI
        url: >-
          https://awscli.amazonaws.com/v2/documentation/api/latest/reference/codeguru-reviewer/index.html
    overlays:
      - type: APIs.io Search
        url: overlays/codeguru-reviewer-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/codeguru-reviewer-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:codeguru-reviewer
  - name: AWS CodeArtifact
    description: >-
      CodeArtifact is a managed artifact repository that supports various
      language-native package managers and build tools like npm, Apache Maven,
      pip, and dotnet. It allows teams to share and pull packages from both
      public and CodeArtifact repositories. Additionally, CodeArtifact enables
      the creation of upstream relationships between repositories, effectively
      combining their contents for package manager clients.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/codeartifact/
    baseURL: https://example.com
    tags:
      - Assets
      - Authorization
      - Configurations
      - Connections
      - Copy
      - Dependencies
      - Describe
      - Disassociate
      - Dispose
      - Domains
      - Endpoints
      - External
      - Origin
      - Packages
      - Permissions
      - Policies
      - Publish
      - Readme
      - Repositories
      - Resources
      - Status
      - Tags
      - Tokens
      - Untag
      - Versions
    properties:
      - type: Documentation
        url: https://aws.amazon.com/codeartifact/
      - type: OpenAPI
        url: properties/codeartifact-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/codeartifact-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/codeartifact-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:codeartifact
  - name: AWS CloudTrail
    description: >-
      The CloudTrail API Reference provides detailed information on actions,
      data types, parameters, and errors for CloudTrail, a web service that
      records Amazon Web Services API calls and stores log files in an Amazon S3
      bucket. The recorded information includes user identity, API call start
      time, source IP address, request parameters, and response elements. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/cloudtrail/
    baseURL: https://example.com
    tags:
      - Trails
    properties:
      - type: Documentation
        url: https://aws.amazon.com/cloudtrail/
      - type: OpenAPI
        url: properties/cloudtrail-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/cloudtrail/features/
      - type: Pricing
        url: https://aws.amazon.com/cloudtrail/pricing/
      - type: Getting Started
        url: https://aws.amazon.com/cloudtrail/getting-started/
      - type: Resources
        url: https://aws.amazon.com/cloudtrail/resources/
      - type: FAQ
        url: https://aws.amazon.com/cloudtrail/faqs/
      - type: Partners
        url: https://aws.amazon.com/cloudtrail/partners/
    overlays:
      - type: APIs.io Search
        url: overlays/cloudtrail-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/cloudtrail-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:cloudtrail
  - name: AWS CodeDeploy
    description: >-
      AWS CodeDeploy is a deployment service that effortlessly automates
      software deployments to a range of compute services including Amazon EC2,
      ECS, AWS Lambda, and on-premises servers. By utilizing CodeDeploy, you can
      streamline software deployments, reducing the risk of errors associated
      with manual operations.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/codedeploy/
    baseURL: https://example.com
    tags:
      - Deployments
      - Group
    properties:
      - type: Documentation
        url: https://aws.amazon.com/codedeploy/
      - type: OpenAPI
        url: properties/codedeploy-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/codedeploy/features/
      - type: Pricing
        url: https://aws.amazon.com/codedeploy/pricing/
      - type: Getting Started
        url: https://aws.amazon.com/codedeploy/getting-started/
      - type: Resources
        url: https://aws.amazon.com/codedeploy/resources/
      - type: FAQ
        url: https://aws.amazon.com/codedeploy/faqs/
      - type: Integrations
        url: https://aws.amazon.com/codedeploy/product-integrations/
    overlays:
      - type: APIs.io Search
        url: overlays/codedeploy-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/codedeploy-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:codedeploy
  - name: Amazon CodeGuru Security
    description: >-
      Amazon CodeGuru Security is a static application security tool that uses
      machine learning to detect security policy violations and vulnerabilities.
      It provides suggestions for addressing security risks and generates
      metrics so you can track the security posture of your applications.
      CodeGuru Security’s policies, which are informed by years of Amazon.com
      and AWS security best practices, help you to create and deploy secure,
      high-quality applications.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://docs.aws.amazon.com/codeguru/latest/security-api/index.html
    baseURL: https://example.com
    tags:
      - ARN
      - Accounts
      - Batches
      - Configurations
      - Findings
      - Metrics
      - Names
      - Resources
      - Scans
      - Summaries
      - Tags
      - URL
      - Untag
      - Uploads
    properties:
      - type: Documentation
        url: https://docs.aws.amazon.com/codeguru/latest/security-api/index.html
      - type: OpenAPI
        url: properties/codeguru-security-openapi-original.yml
      - type: User Guide
        url: https://docs.aws.amazon.com/codeguru/latest/security-ug/index.html
      - type: CLI
        url: >-
          https://awscli.amazonaws.com/v2/documentation/api/latest/reference/codeguru-security/index.html
    overlays:
      - type: APIs.io Search
        url: overlays/codeguru-security-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/codeguru-security-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:codeguru-security
  - name: AWS CodeCommit
    description: >-
      Securely host highly scalable private Git repositories and collaborate on
      code. AWS CodeCommit is a secure, highly scalable, fully managed source
      control service that hosts private Git repositories.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/codecommit/
    baseURL: https://example.com
    tags:
      - Names
      - Repositories
    properties:
      - type: Documentation
        url: https://aws.amazon.com/codecommit/
      - type: OpenAPI
        url: properties/codecommit-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/codecommit/features/
      - type: Pricing
        url: https://aws.amazon.com/codecommit/pricing/
      - type: Getting Started
        url: https://aws.amazon.com/codecommit/getting-started/
      - type: Resources
        url: https://aws.amazon.com/codecommit/resources/
      - type: FAQ
        url: https://aws.amazon.com/codecommit/faqs/
      - type: User Guide
        url: https://docs.aws.amazon.com/codecommit/latest/userguide/welcome.html
    overlays:
      - type: APIs.io Search
        url: overlays/codecommit-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/codecommit-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:codecommit
  - name: Amazon CodeGuru Profiler
    description: >-
      The Amazon CodeGuru Profiler API gathers real-time performance data from
      your applications and offers tailored suggestions to optimize their
      performance. By leveraging machine learning techniques, CodeGuru Profiler
      assists in pinpointing the most resource-intensive lines of code and
      suggests enhancements to increase efficiency and overcome CPU bottlenecks.
      With various visualization tools, the API allows you to track CPU usage,
      identify time-consuming code segments, and offers actionable insights to
      minimize CPU consumption.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://docs.aws.amazon.com/codeguru/latest/profiler-api/index.html
    baseURL: https://example.com
    tags:
      - ARN
      - Accounts
      - Actions
      - Agent
      - Anomalies
      - Anomaly
      - Batches
      - Channels
      - Configurations
      - Configure
      - Data
      - Feedback
      - Findings
      - Frames
      - Groups
      - Instances
      - Internal
      - Metrics
      - Names
      - Notifications
      - Permission
      - Policies
      - Posts
      - Profiles
      - Profiling
      - Recommendations
      - Removes
      - Reports
      - Resources
      - Submit
      - Summaries
      - Tags
      - Times
      - Untag
    properties:
      - type: Documentation
        url: https://docs.aws.amazon.com/codeguru/latest/profiler-api/index.html
      - type: OpenAPI
        url: properties/codeguruprofiler-openapi-original.yml
      - type: User Guide
        url: https://docs.aws.amazon.com/codeguru/latest/profiler-ug/index.html
      - type: CLI
        url: >-
          https://awscli.amazonaws.com/v2/documentation/api/latest/reference/codeguruprofiler/index.html
    overlays:
      - type: APIs.io Search
        url: overlays/codeguruprofiler-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/codeguruprofiler-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:codeguruprofiler
  - name: AWS CodePipeline
    description: >-
      The API provided by AWS CodePipeline is a comprehensive continuous
      delivery service that simplifies the automation of release pipelines,
      facilitating swift and dependable updates to both applications and
      infrastructure.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/codepipeline/
    baseURL: https://example.com
    tags:
      - Pipelines
    properties:
      - type: Documentation
        url: https://aws.amazon.com/codepipeline/
      - type: OpenAPI
        url: properties/codepipeline-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/codepipeline/features/
      - type: Pricing
        url: https://aws.amazon.com/codepipeline/pricing/
      - type: Getting Started
        url: https://aws.amazon.com/codepipeline/getting-started/
      - type: FAQ
        url: https://aws.amazon.com/codepipeline/faqs/
      - type: Integrations
        url: https://aws.amazon.com/codepipeline/product-integrations/
    overlays:
      - type: APIs.io Search
        url: overlays/codepipeline-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/codepipeline-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:codepipeline
  - name: AWS CodeStar Notifications
    description: >-
      The AWS CodeStar Notifications API Reference offers detailed explanations
      and practical examples on using the various operations and data types
      within the AWS CodeStar Notifications API.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: >-
      https://docs.aws.amazon.com/codestar-notifications/latest/APIReference/Welcome.html
    baseURL: https://example.com
    tags:
      - ARN
      - Describe
      - Events
      - Notifications
      - Resources
      - Rules
      - Subscribe
      - Tags
      - Targets
      - Targets
      - Types
      - Unsubscribe
      - Untag
    properties:
      - type: Documentation
        url: >-
          https://docs.aws.amazon.com/codestar-notifications/latest/APIReference/Welcome.html
      - type: OpenAPI
        url: properties/codestar-notifications-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/codestar-notifications-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/codestar-notifications-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:codestar-notifications
  - name: AWS CodeStar Connections
    description: >-
      AWS CodeStar Connections is an API provided by Amazon Web Services that
      allows you to work with connections and installations. Connections are
      configurations used to connect AWS resources to external code
      repositories, allowing services like CodePipeline to trigger actions based
      on changes in third-party code repositories.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: >-
      https://docs.aws.amazon.com/codeconnections/latest/APIReference/Welcome.html
    baseURL: https://example.com
    tags:
      - Configurations
      - Sync
    properties:
      - type: Documentation
        url: >-
          https://docs.aws.amazon.com/codeconnections/latest/APIReference/Welcome.html
      - type: OpenAPI
        url: properties/codestar-connections-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/codestar-connections-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/codestar-connections-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:codestar-connections
  - name: Amazon Cognito User Pools
    description: >-
      Amazon Cognito user pool, serves as a user directory for authenticating
      and authorizing users in web and mobile applications. When integrated into
      your app, the user pool functions as an OpenID Connect (OIDC) identity
      provider, offering enhanced security features, identity federation
      capabilities, seamless app integration, and customizable user experiences.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: >-
      https://docs.aws.amazon.com/cognito/latest/developerguide/cognito-user-identity-pools.html
    baseURL: https://example.com
    tags:
      - Attributes
      - Users
      - Verify
    properties:
      - type: Documentation
        url: >-
          https://docs.aws.amazon.com/cognito/latest/developerguide/cognito-user-identity-pools.html
      - type: OpenAPI
        url: properties/cognito-idp-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/cognito-idp-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/cognito-idp-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:cognito-idp
  - name: Amazon Cognito Sync
    description: >-
      Amazon Cognito Sync is an AWS service and client library that allows for
      seamless syncing of user data across multiple devices. With high-level
      client libraries available for iOS and Android, developers can easily
      persist data locally for offline access without the need to store
      credentials on the device. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: >-
      https://docs.aws.amazon.com/cognito/latest/developerguide/cognito-sync.html
    baseURL: https://example.com
    tags:
      - Bulk
      - Bulk Publish
      - Cognito
      - Configurations
      - Datasets
      - Describe
      - Details
      - Device
      - Entities
      - Entity Pools
      - Events
      - Identity
      - Names
      - Pools
      - Publish
      - Records
      - Register
      - Sets
      - Subscriptions
      - Unsubscribe
      - Usage
    properties:
      - type: Documentation
        url: >-
          https://docs.aws.amazon.com/cognito/latest/developerguide/cognito-sync.html
      - type: OpenAPI
        url: properties/cognito-sync-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/cognito-sync-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/cognito-sync-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:cognito-sync
  - name: Amazon Comprehend Medical
    description: >-
      The Amazon Comprehend Medical API is designed to extract structured
      information from unstructured clinical text, allowing users to gain
      valuable insights from their documents. It should be noted, however, that
      this API only detects entities in English language texts and imposes size
      limits on files for various API operations.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/comprehend/medical/
    baseURL: https://example.com
    tags:
      - Inference
      - Jobs
      - Stop
    properties:
      - type: Documentation
        url: https://aws.amazon.com/comprehend/medical/
      - type: OpenAPI
        url: properties/comprehendmedical-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/comprehend/medical/features/
      - type: Pricing
        url: https://aws.amazon.com/comprehend/medical/pricing/
      - type: FAQ
        url: https://aws.amazon.com/comprehend/medical/faqs/
      - type: Resources
        url: https://aws.amazon.com/comprehend/medical/resources/
      - type: Customers
        url: https://aws.amazon.com/comprehend/medical/customers/
    overlays:
      - type: APIs.io Search
        url: overlays/comprehendmedical-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/comprehendmedical-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:comprehendmedical
  - name: Amazon Cognito Federated Identities
    description: >-
      Amazon Cognito Federated Identities is a web service that provides scoped
      temporary credentials for mobile devices and other untrusted environments.
      It offers consistent identity management for users throughout the lifespan
      of an application. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: >-
      https://docs.aws.amazon.com/cognitoidentity/latest/APIReference/Welcome.html
    baseURL: https://example.com
    tags:
      - Identity
      - Pools
    properties:
      - type: Documentation
        url: >-
          https://docs.aws.amazon.com/cognitoidentity/latest/APIReference/Welcome.html
      - type: OpenAPI
        url: properties/cognito-identity-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/cognito-identity-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/cognito-identity-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:cognito-identity
  - name: Amazon Connect
    description: >-
      The API for Amazon Connect is a cloud-based solution for setting up and
      managing customer contact centers, offering reliable customer engagement
      at any scale. It provides metrics and real-time reporting for optimizing
      contact routing and efficiently resolving customer issues by connecting
      them with the appropriate agents. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/connect/
    baseURL: https://example.com
    tags:
      - ARN
      - Activate
      - Agent
      - Analysis
      - Analytics
      - Applications
      - Approved
      - Associate
      - Associations
      - Attributes
      - Availability
      - Available
      - Batches
      - Bots
      - Caller
      - Case
      - Cases
      - Chat
      - Claim
      - Code
      - Concurrency
      - Configurations
      - Connect
      - Connects
      - Contacts
      - Content
      - Current
      - Data
      - Deactivate
      - Default
      - Describe
      - Disassociate
      - Dismiss
      - Distributions
      - Entities
      - Evaluations
      - Events
      - Federate
      - Federation
      - File
      - Flows
      - Forms
      - Functions
      - Groups
      - Hierarchy
      - Historical
      - Hours
      - Identity
      - Import
      - Info
      - Initial
      - Instances
      - Integrations
      - Keys
      - Lambda
      - Languages
      - Maximum
      - Metadata
      - Metrics
      - Modules
      - Monitors
      - Names
      - Numbers
      - Operation
      - Operations
      - Origin
      - Origins
      - Outbound
      - Participants
      - Pause
      - Permissions
      - Persistent
      - Phone
      - Predefined
      - Proficiencies
      - Profiles
      - Prompts
      - Queues
      - RTC
      - Real Time
      - Recording
      - References
      - Removes
      - Replicate
      - Resources
      - Resume
      - Roles
      - Routing
      - Rules
      - Schedules
      - Search
      - Security
      - Segments
      - Send
      - Sets
      - Status
      - Statuses
      - Stop
      - Storage
      - Streaming
      - Structures
      - Submit
      - Summaries
      - Suspend
      - Tags
      - Tasks
      - Templates
      - Time
      - Timer
      - Tokens
      - Traffic
      - Transfers
      - Types
      - Untag
      - Userdata
      - Users
      - Versions
      - View
      - Views
      - Vocabularies
      - Web
      - Web RTC
    properties:
      - type: Documentation
        url: https://aws.amazon.com/connect/
      - type: OpenAPI
        url: properties/connect-openapi-original.yml
      - type: Use Cases
        url: https://aws.amazon.com/connect/
      - type: Featured
        url: https://aws.amazon.com/connect/
      - type: Pricing
        url: https://aws.amazon.com/connect/pricing/
      - type: Getting Started
        url: https://aws.amazon.com/connect/getting-started/
      - type: Resources
        url: https://aws.amazon.com/connect/resources/
      - type: Customers
        url: https://aws.amazon.com/connect/customers/
      - type: Partners
        url: https://aws.amazon.com/connect/partners/
    overlays:
      - type: APIs.io Search
        url: overlays/connect-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/connect-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:connect
  - name: AWS Config
    description: >-
      Config provides a comprehensive solution for monitoring and managing the
      configurations of Amazon Web Services resources within your AWS account.
      With Config, you can easily access current and historical configurations
      for resources such as Amazon EC2 instances, EBS volumes, ENIs, and
      security groups.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/config/
    baseURL: https://example.com
    tags:
      - Resources
      - Untag
    properties:
      - type: Documentation
        url: https://aws.amazon.com/config/
      - type: OpenAPI
        url: properties/config-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/config/features/
      - type: Pricing
        url: https://aws.amazon.com/config/pricing/
      - type: Getting Started
        url: https://aws.amazon.com/config/getting-started/
      - type: Resources
        url: https://aws.amazon.com/config/resources/
      - type: FAQ
        url: https://aws.amazon.com/config/faq/
      - type: Customers
        url: https://aws.amazon.com/config/customers/
      - type: Partners
        url: https://aws.amazon.com/config/partners/
    overlays:
      - type: APIs.io Search
        url: overlays/config-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/config-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:config
  - name: Contact Lens for Amazon Connect
    description: >-
      The Contact Lens API for Amazon Connect allows users to analyze
      conversations between customers and agents through features such as speech
      transcription, natural language processing, and intelligent search. It
      includes sentiment analysis, issue detection, and automatic contact
      categorization. This tool provides real-time and post-call analytics for
      customer-agent interactions.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/connect/contact-lens/
    baseURL: https://example.com
    tags:
      - Analysis
      - Contacts
      - Real Time
      - Segments
    properties:
      - type: Documentation
        url: https://aws.amazon.com/connect/contact-lens/
      - type: OpenAPI
        url: properties/connect-contact-lens-openapi-original.yml
      - type: Use Cases
        url: https://aws.amazon.com/connect/contact-lens/
      - type: Features
        url: https://aws.amazon.com/connect/contact-lens/
      - type: Pricing
        url: https://aws.amazon.com/connect/pricing/
      - type: Getting Started
        url: https://aws.amazon.com/connect/getting-started/
      - type: Resources
        url: https://aws.amazon.com/connect/resources/
      - type: Customers
        url: https://aws.amazon.com/connect/customers/
      - type: Partners
        url: https://aws.amazon.com/connect/partners/
    overlays:
      - type: APIs.io Search
        url: overlays/connect-contact-lens-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/connect-contact-lens-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:connect-contact-lens
  - name: AWS Compute Optimizer
    description: >-
      Compute Optimizer is an API that evaluates the configuration and usage
      metrics of your AWS compute resources, including EC2 instances, Auto
      Scaling groups, Lambda functions, EBS volumes, and ECS services on
      Fargate. It provides optimization recommendations to enhance performance
      and reduce costs, based on current and projected utilization data.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/compute-optimizer/
    baseURL: https://example.com
    tags:
      - Enrollment
      - Status
    properties:
      - type: Documentation
        url: https://aws.amazon.com/compute-optimizer/
      - type: OpenAPI
        url: properties/compute-optimizer-openapi-original.yml
      - type: Metrics
        url: https://docs.aws.amazon.com/compute-optimizer/latest/ug/metrics.html
      - type: FAQ
        url: https://aws.amazon.com/compute-optimizer/faqs/
      - type: Getting Started
        url: https://aws.amazon.com/compute-optimizer/getting-started/
      - type: Pricing
        url: https://aws.amazon.com/compute-optimizer/pricing/
    overlays:
      - type: APIs.io Search
        url: overlays/compute-optimizer-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/compute-optimizer-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:compute-optimizer
  - name: Amazon Comprehend
    description: >-
      Amazon Comprehend is an AI-powered service from Amazon Web Services that
      provides deep analysis of document content. It allows users to extract
      topics, sentiment, language, and other insights from their documents.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/comprehend/
    baseURL: https://example.com
    tags:
      - Flywheel
    properties:
      - type: Documentation
        url: https://aws.amazon.com/comprehend/
      - type: OpenAPI
        url: properties/comprehend-openapi-original.yml
      - type: Pricing
        url: https://aws.amazon.com/comprehend/pricing/
      - type: FAQ
        url: https://aws.amazon.com/comprehend/faqs/
      - type: Customers
        url: https://aws.amazon.com/comprehend/customers/
      - type: Resources
        url: https://aws.amazon.com/comprehend/resources/
      - type: Features
        url: https://aws.amazon.com/comprehend/features/
      - type: Intelligent Document Processing
        url: https://aws.amazon.com/comprehend/idp/
      - type: Trust and Safety
        url: https://aws.amazon.com/comprehend/trust-and-safety/
    overlays:
      - type: APIs.io Search
        url: overlays/comprehend-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/comprehend-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:comprehend
  - name: AWS Cost Optimization Hub
    description: >-
      The Cost Optimization Hub API allows you to automate the identification,
      filtering, aggregation, and quantification of cost savings for your
      optimization recommendations across various Amazon Web Services Regions
      and accounts within your organization. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/aws-cost-management/cost-optimization-hub/
    baseURL: https://example.com
    tags:
      - Preferences
    properties:
      - type: Documentation
        url: https://aws.amazon.com/aws-cost-management/cost-optimization-hub/
      - type: OpenAPI
        url: properties/cost-optimization-hub-openapi-original.yml
      - type: Getting Started
        url: >-
          https://aws.amazon.com/aws-cost-management/cost-optimization-hub/getting-started/
      - type: FAQ
        url: https://aws.amazon.com/aws-cost-management/cost-optimization-hub/faqs/
    overlays:
      - type: APIs.io Search
        url: overlays/cost-optimization-hub-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/cost-optimization-hub-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:cost-optimization-hub
  - name: AWS Control Tower
    description: >-
      Use AWS Control Tower to set up and operate your multi-account AWS
      environment with prescriptive controls designed to accelerate your cloud
      journey.  AWS Control Tower orchestrates multiple AWS services on your
      behalf while maintaining the security and compliance needs of your new or
      existing organization.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/controltower/
    baseURL: https://example.com
    tags:
      - ARN
      - Baselines
      - Controls
      - Disable
      - Enable
      - Enabled
      - Landing
      - Landing Zones
      - Operation
      - Reset
      - Resources
      - Tags
      - Untag
      - Zones
    properties:
      - type: Documentation
        url: https://aws.amazon.com/controltower/
      - type: OpenAPI
        url: properties/controltower-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/controltower/features/
      - type: Pricing
        url: https://aws.amazon.com/controltower/pricing/
      - type: FAQ
        url: https://aws.amazon.com/controltower/faqs/
      - type: Customers
        url: https://aws.amazon.com/controltower/customers/
      - type: Partners
        url: https://aws.amazon.com/controltower/partners/
    overlays:
      - type: APIs.io Search
        url: overlays/controltower-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/controltower-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:controltower
  - name: AWS Glue DataBrew
    description: >-
      DataBrew is a user-friendly API designed to simplify the data preparation
      process by allowing users of all technical levels to visualize and
      transform data with just one click. This visual, cloud-scale service
      targets and resolves data issues that are difficult to identify and
      time-consuming to address, making data preparation more efficient and
      accessible. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/glue/features/databrew/
    baseURL: https://example.com
    tags:
      - ARN
      - Actions
      - Batches
      - Datasets
      - Describe
      - Jobs
      - Names
      - Profiles
      - Projects
      - Publish
      - Recipes
      - Resources
      - Rulesets
      - Runs
      - Schedules
      - Send
      - Sessions
      - Stop
      - Tags
      - Untag
      - Versions
    properties:
      - type: Documentation
        url: https://aws.amazon.com/glue/features/databrew/
      - type: OpenAPI
        url: properties/databrew-openapi-original.yml
      - type: About
        url: https://docs.aws.amazon.com/databrew/latest/dg/what-is.html
    overlays:
      - type: APIs.io Search
        url: overlays/databrew-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/databrew-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:databrew
  - name: Amazon Connect Customer Profiles
    description: >-
      The Amazon Connect Customer Profiles API offers a centralized customer
      profile solution for contact centers, featuring pre-built connectors
      utilizing AppFlow technology. These connectors seamlessly integrate
      customer data from third-party applications like Salesforce, ServiceNow,
      and ERP systems with contact history from your Amazon Connect contact
      center. If you are a new user, the Amazon Connect Administrator Guide can
      assist you in familiarizing yourself with the platform.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/connect/customer-profiles/
    baseURL: https://example.com
    tags:
      - ARN
      - Accounts
      - Attributes
      - Auto
      - Based
      - Calculated
      - Definitions
      - Detect
      - Domains
      - Entities
      - Events
      - Identity
      - Integrations
      - Jobs
      - Keys
      - Matches
      - Merge
      - Merging
      - Names
      - Objects
      - Previews
      - Profiles
      - Resolutions
      - Resources
      - Rules
      - Search
      - Similar
      - Steps
      - Stream
      - Streams
      - Tags
      - Templates
      - Types
      - Untag
      - Workflows
    properties:
      - type: Documentation
        url: https://aws.amazon.com/connect/customer-profiles/
      - type: OpenAPI
        url: properties/customer-profiles-openapi-original.yml
      - type: Use Cases
        url: https://aws.amazon.com/connect/customer-profiles/
    overlays:
      - type: APIs.io Search
        url: overlays/customer-profiles-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/customer-profiles-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:customer-profiles
  - name: AWS Cost and Usage Report
    description: >-
      With the Amazon Web Services Cost and Usage Report API, you can manage
      Cost and Usage Report definitions programmatically. This API allows you to
      create, query, and delete Cost and Usage Report definitions, which track
      monthly costs and usage associated with your Amazon Web Services account.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/aws-cost-management/aws-cost-and-usage-reporting/
    baseURL: https://example.com
    tags:
      - Resources
      - Untag
    properties:
      - type: Documentation
        url: >-
          https://aws.amazon.com/aws-cost-management/aws-cost-and-usage-reporting/
      - type: OpenAPI
        url: properties/cur-openapi-original.yml
      - type: Features
        url: >-
          https://aws.amazon.com/aws-cost-management/aws-cost-and-usage-reporting/features/
      - type: FAQ
        url: >-
          https://aws.amazon.com/aws-cost-management/aws-cost-and-usage-reporting/faqs/
    overlays:
      - type: APIs.io Search
        url: overlays/cur-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/cur-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:cur
  - name: AWS DataSync
    description: >
      AWS DataSync is a secure, online service that automates and accelerates
      moving data between on premises and AWS Storage services.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/datasync/
    baseURL: https://example.com
    tags:
      - Data
      - Execution
      - Tasks
    properties:
      - type: Documentation
        url: https://aws.amazon.com/datasync/
      - type: OpenAPI
        url: properties/datasync-openapi-original.yml
      - type: Discovery
        url: https://aws.amazon.com/datasync/discovery/
      - type: Customers
        url: https://aws.amazon.com/datasync/customers/
      - type: FAQ
        url: https://aws.amazon.com/datasync/faqs/
      - type: Resources
        url: https://aws.amazon.com/datasync/resources/
      - type: Getting Started
        url: https://aws.amazon.com/datasync/getting-started/
      - type: Pricing
        url: https://aws.amazon.com/datasync/pricing/
    overlays:
      - type: APIs.io Search
        url: overlays/datasync-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/datasync-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:datasync
  - name: Amazon DataZone
    description: >-
      Amazon DataZone is a comprehensive data management service designed to
      streamline the organization, governance, and analysis of your data. This
      API allows you to easily catalog, discover, and share your data across
      accounts and regions. With Amazon DataZone, you can seamlessly integrate
      with various Amazon Web Services offerings such as Redshift, Athena, Glue,
      and Lake Formation to enhance your data management capabilities.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/datazone/
    baseURL: https://example.com
    tags:
      - ARN
      - Accept
      - Activities
      - Assets
      - Blueprints
      - Cancel
      - Change
      - Configurations
      - Data
      - Domains
      - Environments
      - Forms
      - Glossaries
      - Glossary
      - Grants""
      - Grants
      - Groups
      - Groups
      - IAM
      - Listings
      - Listings
      - Login
      - Memberships
      - Notifications
      - Portals
      - Predictions
      - Profiles
      - Projects
      - Reject
      - Resources
      - Revisions
      - Revoke
      - Runs
      - Search
      - Sets
      - Sources
      - Sources
      - Status
      - Subscriptions
      - Tags
      - Targets
      - Targets
      - Term
      - Terms
      - Types
      - URL
      - Untag
      - Users
    properties:
      - type: Documentation
        url: https://aws.amazon.com/datazone/
      - type: OpenAPI
        url: properties/datazone-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/datazone/features/
      - type: FAQ
        url: https://aws.amazon.com/datazone/faqs/
      - type: Getting Started
        url: https://aws.amazon.com/datazone/getting-started/
      - type: Pricing
        url: https://aws.amazon.com/datazone/pricing/
      - type: Resources
        url: https://aws.amazon.com/datazone/resources/
    overlays:
      - type: APIs.io Search
        url: overlays/datazone-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/datazone-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:datazone
  - name: AWS Data Exchange
    description: >-
      AWS Data Exchange is a service that makes it easy for AWS customers to
      exchange data in the cloud. You can use the AWS Data Exchange APIs to
      create, update, manage, and access file-based data set in the AWS Cloud. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/data-exchange/
    baseURL: https://example.com
    tags:
      - ARN
      - Actions
      - Assets
      - Data
      - Events
      - Jobs
      - Notifications
      - Resources
      - Revisions
      - Revoke
      - Send
      - Sets
      - Tags
      - Untag
    properties:
      - type: Documentation
        url: https://aws.amazon.com/data-exchange/
      - type: OpenAPI
        url: properties/dataexchange-openapi-original.yml
      - type: Updates
        url: https://aws.amazon.com/data-exchange/latest-updates/
      - type: Updates
        url: https://aws.amazon.com/data-exchange/latest-updates/
      - type: Providers
        url: https://aws.amazon.com/data-exchange/providers/
    overlays:
      - type: APIs.io Search
        url: overlays/dataexchange-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/dataexchange-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:dataexchange
  - name: AWS Data Pipeline
    description: >-
      AWS Data Pipeline configures and manages a data-driven workflow called a
      pipeline. AWS Data Pipeline handles the details of scheduling and ensuring
      that data dependencies are met so that your application can focus on
      processing the data. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://docs.aws.amazon.com/data-pipeline/
    baseURL: https://example.com
    tags:
      - Definitions
      - Pipelines
      - Validate
    properties:
      - type: Documentation
        url: https://docs.aws.amazon.com/data-pipeline/
      - type: OpenAPI
        url: properties/datapipeline-openapi-original.yml
      - type: Guide
        url: >-
          https://docs.aws.amazon.com/datapipeline/latest/DeveloperGuide/index.html
    overlays:
      - type: APIs.io Search
        url: overlays/datapipeline-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/datapipeline-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:datapipeline
  - name: AWS Device Farm
    description: >-
      Explore the AWS Device Farm API documentation, offering APIs for two main
      testing services: desktop browser testing and real mobile device testing.
      Use Device Farm to test your web applications on desktop browsers with
      Selenium through the TestGrid-named APIs. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/device-farm/
    baseURL: https://example.com
    tags:
      - Configurations
      - VPCE
    properties:
      - type: Documentation
        url: https://aws.amazon.com/device-farm/
      - type: OpenAPI
        url: properties/devicefarm-openapi-original.yml
      - type: Device List
        url: https://aws.amazon.com/device-farm/device-list/
      - type: Pricing
        url: https://aws.amazon.com/device-farm/pricing/
      - type: Resources
        url: https://aws.amazon.com/device-farm/resources/
      - type: FAQ
        url: https://aws.amazon.com/device-farm/faqs/
    overlays:
      - type: APIs.io Search
        url: overlays/devicefarm-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/devicefarm-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:devicefarm
  - name: AWS Direct Connect
    description: >-
      Direct Connect allows you to establish a high-speed, private connection
      between your internal network and an Direct Connect location using a
      standard Ethernet fiber-optic cable. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/directconnect/
    baseURL: https://example.com
    tags:
      - Attributes
      - Interfaces
      - Virtual
    properties:
      - type: Documentation
        url: https://aws.amazon.com/directconnect/
      - type: OpenAPI
        url: properties/directconnect-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/directconnect/features/
      - type: Pricing
        url: https://aws.amazon.com/directconnect/pricing/
      - type: Getting Started
        url: https://aws.amazon.com/directconnect/getting-started/
      - type: FAQ
        url: https://aws.amazon.com/directconnect/faqs/
      - type: Partners
        url: https://aws.amazon.com/directconnect/partners/
    overlays:
      - type: APIs.io Search
        url: overlays/directconnect-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/directconnect-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:directconnect
  - name: AWS Detective
    description: >-
      The Amazon Detective API streamlines the investigation process for
      security teams, enabling faster and more efficient analysis. By leveraging
      prebuilt data aggregations, summaries, and context provided by Amazon
      Detective, users can quickly assess and understand potential security
      threats.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/detective/
    baseURL: https://example.com
    tags:
      - ARN
      - Accept
      - Accounts
      - Accounts List
      - Administrative
      - Batches
      - Configurations
      - Data Source
      - Describe
      - Disable
      - Disassociate
      - Enable
      - Graphs
      - Indicators
      - Investigations
      - Invitation
      - Invitations
      - Members
      - Memberships
      - Monitoring
      - Monitoring State
      - Organizations
      - Packages
      - Reject
      - Removal
      - Resources
      - States
      - Tags
      - Untag
    properties:
      - type: Documentation
        url: https://aws.amazon.com/detective/
      - type: OpenAPI
        url: properties/detective-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/detective/features/
      - type: Pricing
        url: https://aws.amazon.com/detective/pricing/
      - type: Getting Started
        url: https://aws.amazon.com/detective/getting-started/
      - type: FAQ
        url: https://aws.amazon.com/detective/faqs/
      - type: FAQ
        url: https://aws.amazon.com/detective/faqs/
    overlays:
      - type: APIs.io Search
        url: overlays/detective-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/detective-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:detective
  - name: Amazon Data Lifecycle Manager
    description: >-
      Amazon Data Lifecycle Manager With Amazon Data Lifecycle Manager, you can
      manage the lifecycle of your Amazon Web Services resources. You create
      lifecycle policies, which are used to automate operations on the specified
      resources. Amazon Data Lifecycle Manager supports Amazon EBS volumes and
      snapshots.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://docs.aws.amazon.com/ebs/latest/userguide/snapshot-lifecycle.html
    baseURL: https://example.com
    tags:
      - ARN
      - Lifecycle
      - Policies
      - Resources
      - Tags
      - Untag
    properties:
      - type: Documentation
        url: >-
          https://docs.aws.amazon.com/ebs/latest/userguide/snapshot-lifecycle.html
      - type: OpenAPI
        url: properties/dlm-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/dlm-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/dlm-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:dlm
  - name: Amazon DevOps Guru
    description: >-
      Amazon DevOps Guru is a managed service designed to detect abnormal
      behavior in critical operational applications. Users can select the Amazon
      Web Services resources they want DevOps Guru to monitor, allowing the
      service to analyze CloudWatch metrics and CloudTrail events related to
      those resources. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/devops-guru/
    baseURL: https://example.com
    tags:
      - Accounts
      - Anomalies
      - Anomalous
      - Anomaly
      - Channels
      - Collections
      - Configurations
      - Cost
      - Describe
      - Estimation
      - Events
      - Feedback
      - Groups
      - Health
      - Insights
      - Integrations
      - Logs
      - Monitored
      - Notifications
      - Organizations
      - Overview
      - Recommendations
      - Removes
      - Resources
      - Search
      - Services
      - Sources
      - Types
    properties:
      - type: Documentation
        url: https://aws.amazon.com/devops-guru/
      - type: OpenAPI
        url: properties/devops-guru-openapi-original.yml
      - type: Pricing
        url: https://aws.amazon.com/devops-guru/pricing/
      - type: Resources
        url: https://aws.amazon.com/devops-guru/resources/
      - type: FAQ
        url: https://aws.amazon.com/devops-guru/faqs/
      - type: Customers
        url: https://aws.amazon.com/devops-guru/customers/
      - type: Partners
        url: https://aws.amazon.com/devops-guru/partners/
      - type: Features
        url: https://aws.amazon.com/devops-guru/features/
    overlays:
      - type: APIs.io Search
        url: overlays/devops-guru-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/devops-guru-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:devops-guru
  - name: Amazon DynamoDB Accelerator (DAX)
    description: >-
      DAX is a managed caching service designed specifically for Amazon
      DynamoDB. It significantly boosts database read speeds by storing
      frequently accessed data from DynamoDB, allowing applications to retrieve
      that data with extremely low latency. Setting up a DAX cluster is a
      straightforward process through the AWS Management Console. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/dynamodbaccelerator/
    baseURL: https://example.com
    tags:
      - Subnets
    properties:
      - type: Documentation
        url: https://aws.amazon.com/dynamodbaccelerator/
      - type: OpenAPI
        url: properties/dax-openapi-original.yml
      - type: Customers
        url: https://aws.amazon.com/dynamodbaccelerator/customers/
    overlays:
      - type: APIs.io Search
        url: overlays/dax-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/dax-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:dax
  - name: AWS Application Discovery Service
    description: >-
      The Amazon Web Services Application Discovery Service helps users plan
      application migration projects by automatically identifying servers,
      virtual machines, and network dependencies in on-premises data centers. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/application-discovery/
    baseURL: https://example.com
    tags:
      - Applications
    properties:
      - type: Documentation
        url: https://aws.amazon.com/application-discovery/
      - type: OpenAPI
        url: properties/discovery-openapi-original.yml
      - type: Feature
        url: https://aws.amazon.com/application-discovery/features/
      - type: Pricing
        url: https://aws.amazon.com/application-discovery/pricing/
      - type: Getting Started
        url: https://aws.amazon.com/application-discovery/getting-started/
      - type: Resources
        url: https://aws.amazon.com/application-discovery/resources/
      - type: FAQ
        url: https://aws.amazon.com/application-discovery/faqs/
      - type: Partners
        url: https://aws.amazon.com/application-discovery/partners/
    overlays:
      - type: APIs.io Search
        url: overlays/discovery-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/discovery-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:discovery
  - name: AWS Directory Service
    description: >-
      API for Directory Service is a convenient web service designed to help
      users easily establish and manage directories in the Amazon Web Services
      cloud. It also allows users to connect their Amazon Web Services resources
      to an existing Microsoft Active Directory that they manage themselves. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/directoryservice/
    baseURL: https://example.com
    tags:
      - Trust
      - Verify
    properties:
      - type: Documentation
        url: https://aws.amazon.com/directoryservice/
      - type: OpenAPI
        url: properties/ds-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/directoryservice/features/
      - type: Pricing
        url: https://aws.amazon.com/directoryservice/pricing/
      - type: Getting Started
        url: https://aws.amazon.com/directoryservice/getting-started/
      - type: FAQ
        url: https://aws.amazon.com/directoryservice/faqs/
    overlays:
      - type: APIs.io Search
        url: overlays/ds-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/ds-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:ds
  - name: AWS Elastic Disaster Recovery Service
    description: >-
      AWS Elastic Disaster Recovery (AWS DRS), helps to reduce downtime and
      prevent data loss by quickly and reliably recovering on-premises and
      cloud-based applications. It utilizes cost-effective storage, minimal
      computing resources, and offers point-in-time recovery for optimal
      efficiency.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/disaster-recovery/
    baseURL: https://example.com
    tags:
      - ARN
      - Accounts
      - Actions
      - Associate
      - Configurations
      - Data
      - Describe
      - Disconnect
      - Exports
      - Extended
      - Extensible
      - Failback
      - Initialize
      - Instances
      - Items
      - Jobs
      - Launch
      - Logs
      - Networks
      - Recovery
      - Replication
      - Resources
      - Retry
      - Reverse
      - Servers
      - Services
      - Snapshots
      - Sources
      - Stack
      - Staging
      - Stop
      - Tags
      - Templates
      - Terminate
      - Untag
    properties:
      - type: Documentation
        url: https://aws.amazon.com/disaster-recovery/
      - type: OpenAPI
        url: properties/drs-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/disaster-recovery/features/
      - type: Pricing
        url: https://aws.amazon.com/disaster-recovery/pricing/
      - type: Resources
        url: https://aws.amazon.com/disaster-recovery/resources/
      - type: FAQ
        url: https://aws.amazon.com/disaster-recovery/faqs/
    overlays:
      - type: APIs.io Search
        url: overlays/drs-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/drs-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:drs
  - name: AWS Database Migration Service
    description: >-
      Our Database Migration Service (DMS) is a flexible tool that can
      seamlessly move data between a variety of commercial and open-source
      databases, including Oracle, PostgreSQL, Microsoft SQL Server, Amazon
      Redshift, MariaDB, Amazon Aurora, MySQL, and SAP Adaptive Server
      Enterprise (ASE). 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/dms/
    baseURL: https://example.com
    tags:
      - Database
      - Migrations
      - Subscriptions
      - Events
    properties:
      - type: Documentation
        url: https://aws.amazon.com/dms/
      - type: OpenAPI
        url: properties/dms-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/dms/features/
      - type: Schema Conversion Tool
        url: https://aws.amazon.com/dms/schema-conversion-tool/
      - type: Pricing
        url: https://aws.amazon.com/dms/pricing/
      - type: Resources
        url: https://docs.aws.amazon.com/dms/
      - type: Partners
        url: https://aws.amazon.com/dms/partners/
      - type: Customers
        url: https://aws.amazon.com/dms/testimonials/
    overlays:
      - type: APIs.io Search
        url: overlays/dms-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/dms-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:dms
  - name: Amazon Elastic Block Store
    description: >-
      Use the Amazon Elastic Block Store (Amazon EBS) direct APIs to easily
      create Amazon EBS snapshots, write data directly to your snapshots, read
      data on your snapshots, and identify differences or changes between two
      snapshots. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/ebs/
    baseURL: https://example.com
    tags:
      - Blocks
      - Changed
      - Changed Blocks
      - Complete
      - Completions
      - Index
      - Second
      - Snapshots
      - Storage
    properties:
      - type: Documentation
        url: https://aws.amazon.com/ebs/
      - type: OpenAPI
        url: properties/ebs-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/ebs/features/
      - type: Pricing
        url: https://aws.amazon.com/ebs/pricing/
      - type: Volume Types
        url: https://aws.amazon.com/ebs/volume-types/
      - type: Resources
        url: https://aws.amazon.com/ebs/resources/
      - type: Getting Started
        url: https://aws.amazon.com/ebs/getting-started/
      - type: FAQ
        url: https://aws.amazon.com/ebs/faqs/
      - type: Customers
        url: https://aws.amazon.com/ebs/customers/
    overlays:
      - type: APIs.io Search
        url: overlays/ebs-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/ebs-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:ebs
  - name: Amazon DocumentDB
    description: >-
      Amazon DocumentDB is a cloud-based database service that offers fast and
      reliable performance. It is fully managed and compatible with MongoDB,
      making it easy to set up, operate, and scale databases. With Amazon
      DocumentDB, you can seamlessly run your existing application code and
      access the same drivers and tools you currently use with MongoDB.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/documentdb/
    baseURL: https://example.com
    tags:
      - Stop
      - Database Cluster
      - Database
    properties:
      - type: Documentation
        url: https://aws.amazon.com/documentdb/
      - type: OpenAPI
        url: properties/docdb-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/documentdb/features/
      - type: Pricing
        url: https://aws.amazon.com/documentdb/pricing/
      - type: Resources
        url: https://aws.amazon.com/documentdb/resources/
      - type: Getting Started
        url: https://aws.amazon.com/documentdb/getting-started/
      - type: FAQ
        url: https://aws.amazon.com/documentdb/faqs/
      - type: Customers
        url: https://aws.amazon.com/documentdb/customers/
    overlays:
      - type: APIs.io Search
        url: overlays/docdb-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/docdb-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:docdb
  - name: Amazon Elastic DocumentDB
    description: >-
      The Amazon DocumentDB API offers elastic clusters that can handle high
      volumes of reads/writes per second and store petabytes of data. These
      clusters make it easier for developers to work with Amazon DocumentDB by
      removing the need to select, oversee, or update instances.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: >-
      https://docs.aws.amazon.com/documentdb/latest/developerguide/docdb-using-elastic-clusters.html
    baseURL: https://example.com
    tags:
      - ARN
      - Cluster
      - Clusters
      - Resources
      - Restore
      - Snapshots
      - Tags
      - Untag
    properties:
      - type: Documentation
        url: >-
          https://docs.aws.amazon.com/documentdb/latest/developerguide/docdb-using-elastic-clusters.html
      - type: OpenAPI
        url: properties/docdb-elastic-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/docdb-elastic-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/docdb-elastic-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:docdb-elastic
  - name: Amazon EC2 Instance Connect
    description: >-
      Amazon EC2 Instance Connect allows system administrators to generate and
      share one-time use SSH public keys on EC2, offering users a convenient and
      reliable method to access their instances securely.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: >-
      https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/connect-linux-inst-eic.html
    baseURL: https://example.com
    tags:
      - Console
      - Keys
      - SSHPublic
      - Send
      - Serial
    properties:
      - type: Documentation
        url: >-
          https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/connect-linux-inst-eic.html
      - type: OpenAPI
        url: properties/ec2-instance-connect-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/ec2-instance-connect-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/ec2-instance-connect-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:ec2-instance-connect
  - name: Amazon DynamoDB
    description: >-
      Amazon DynamoDB, is a NoSQL database service that operates in a serverless
      environment, allowing you to build modern applications of any size. With
      DynamoDB, you only pay for the resources you use, and the database can
      scale down to zero, eliminating cold starts, version upgrades, maintenance
      windows, patching, and downtime. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/dynamodb/
    baseURL: https://example.com
    tags:
      - Database
      - ' NoSQL'
      - ' Live'
      - Time
    properties:
      - type: Documentation
        url: https://aws.amazon.com/dynamodb/
      - type: OpenAPI
        url: properties/dynamodb-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/dynamodb/features/
      - type: Pricing
        url: https://aws.amazon.com/dynamodb/pricing/
      - type: Resources
        url: https://aws.amazon.com/dynamodb/resources/
      - type: Getting Started
        url: https://aws.amazon.com/dynamodb/getting-started/
      - type: Migrations
        url: https://aws.amazon.com/dynamodb/migrations/
      - type: Partners
        url: https://aws.amazon.com/dynamodb/partners/
      - type: Solutions
        url: https://aws.amazon.com/dynamodb/solutions-by-industry/
      - type: FAQ
        url: https://aws.amazon.com/dynamodb/faqs/
      - type: Customers
        url: https://aws.amazon.com/dynamodb/customers/
    overlays:
      - type: APIs.io Search
        url: overlays/dynamodb-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/dynamodb-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:dynamodb
  - name: Amazon Elastic Compute Cloud
    description: >-
      The Amazon Elastic Compute Cloud (Amazon EC2) API provides a comprehensive
      compute platform with a wide range of instance options and the latest
      technology choices in processors, storage, networking, operating systems,
      and purchase models to suit your workload requirements. We are the leading
      cloud provider to support Intel, AMD, and Arm processors, offer on-demand
      EC2 Mac instances, and feature 400 Gbps Ethernet networking. This API
      delivers exceptional price performance for machine learning training and
      the most cost-effective inference instances in the cloud. AWS has the
      largest number of SAP, high performance computing (HPC), ML, and Windows
      workloads compared to any other cloud provider.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/ec2/
    baseURL: https://example.com
    tags:
      - Withdraw
      - CIDR
      - Storage
    properties:
      - type: Documentation
        url: https://aws.amazon.com/ec2/
      - type: OpenAPI
        url: properties/ec2-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/ec2/features/
      - type: Pricing
        url: https://aws.amazon.com/ec2/pricing/
      - type: Instance Types
        url: https://aws.amazon.com/ec2/instance-types/
      - type: FAQ
        url: https://aws.amazon.com/ec2/faqs/
      - type: Getting Started
        url: https://aws.amazon.com/ec2/getting-started/
      - type: Resources
        url: https://aws.amazon.com/ec2/resources/
      - type: Videos
        url: https://aws.amazon.com/ec2/videos/
      - type: Customers
        url: https://aws.amazon.com/ec2/customers/
      - type: Cost Optimizations
        url: https://aws.amazon.com/ec2/cost-and-capacity/
    overlays:
      - type: APIs.io Search
        url: overlays/ec2-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/ec2-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:ec2
  - name: Amazon Elastic Kubernetes Service
    description: >-
      Amazon Elastic Kubernetes Service (Amazon EKS) is a fully managed service
      designed to simplify the process of running Kubernetes on Amazon Web
      Services. With Amazon EKS, users can easily deploy, scale, and manage
      containerized applications without the need to set up or maintain their
      own Kubernetes control plane. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/eks/
    baseURL: https://example.com
    tags:
      - ARN
      - Access
      - Addons
      - Anywhere
      - Associate
      - Associated
      - Associations
      - Clusters
      - Configurations
      - Deregister
      - Describe
      - Disassociate
      - EKS
      - Encryption
      - Entities
      - Entries
      - Entry
      - Er
      - Fargate
      - Groups
      - Identity
      - Insights
      - Names
      - Node Groups
      - Nodes
      - Pods
      - Policies
      - Principals
      - Profiles
      - Prov
      - Providers
      - Register
      - Registrations
      - Resources
      - Schemas
      - Subscriptions
      - Supported
      - Tags
      - Untag
      - Versions
    properties:
      - type: Documentation
        url: https://aws.amazon.com/eks/
      - type: OpenAPI
        url: properties/eks-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/eks/features/
      - type: Pricing
        url: https://aws.amazon.com/eks/pricing/
      - type: Getting Started
        url: https://aws.amazon.com/eks/getting-started/
      - type: FAQ
        url: https://aws.amazon.com/eks/faqs/
      - type: Customers
        url: https://aws.amazon.com/eks/customers/
      - type: Partners
        url: https://aws.amazon.com/eks/partners/
    overlays:
      - type: APIs.io Search
        url: overlays/eks-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/eks-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:eks
  - name: Amazon Elastic Container Registry
    description: >-
      The Amazon Elastic Container Registry (Amazon ECR) is a managed service
      that allows customers to store and manage container images securely. Users
      can easily push, pull, and manage images using the Docker CLI or their
      preferred client. Amazon ECR supports private repositories with
      resource-based permissions using IAM, allowing specific users or Amazon
      EC2 instances to access repositories and images. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/ecr/
    baseURL: https://example.com
    tags:
      - Cache
      - Pull
      - Rules
      - Validate
    properties:
      - type: Documentation
        url: https://aws.amazon.com/ecr/
      - type: OpenAPI
        url: properties/ecr-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/ecr/features/
      - type: Pricing
        url: https://aws.amazon.com/ecr/pricing/
      - type: Getting Started
        url: https://aws.amazon.com/ecr/getting-started/
      - type: Resources
        url: https://aws.amazon.com/ecr/resources/
      - type: FAQ
        url: https://aws.amazon.com/ecr/faqs/
      - type: Customers
        url: https://aws.amazon.com/ecr/customers/
    overlays:
      - type: APIs.io Search
        url: overlays/ecr-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/ecr-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:ecr
  - name: Amazon Elastic Container Service
    description: >-
      Amazon Elastic Container Service (Amazon ECS) is a robust container
      management service provided by Amazon. It enables easy running, stopping,
      and management of Docker containers with high scalability and speed.
      Amazon ECS allows you to host your container clusters on a serverless
      infrastructure using Fargate or on Amazon EC2 instances that you manage.
      With Amazon ECS, you can effortlessly launch and stop container-based
      applications through simple API calls and benefit from centralized
      monitoring capabilities and familiar Amazon EC2 features. Additionally,
      Amazon ECS offers advanced scheduling capabilities for placing containers
      based on resource requirements, isolation policies, and availability
      needs. By using Amazon ECS, you can simplify cluster management,
      configuration, and scalability, eliminating the need for your own cluster
      and configuration management systems.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/ecs/
    baseURL: https://example.com
    tags:
      - Tasks
    properties:
      - type: Documentation
        url: https://aws.amazon.com/ecs/
      - type: OpenAPI
        url: properties/ecs-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/ecs/features/
      - type: Pricing
        url: https://aws.amazon.com/ecs/pricing/
      - type: Getting Started
        url: https://aws.amazon.com/ecs/getting-started/
      - type: Resources
        url: https://aws.amazon.com/ecs/resources/
      - type: FAQ
        url: https://aws.amazon.com/ecs/faqs/
      - type: Customers
        url: https://aws.amazon.com/ecs/customers/
      - type: Partners
        url: https://aws.amazon.com/ecs/partners/
    overlays:
      - type: APIs.io Search
        url: overlays/ecs-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/ecs-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:ecs
  - name: Amazon ElastiCache
    description: >-
      Amazon ElastiCache is a convenient web service that simplifies the process
      of setting up, operating, and expanding a distributed cache in the cloud.
      By utilizing ElastiCache, users can enjoy the advantages of a
      high-performance, in-memory cache without the extensive administrative
      tasks typically associated with launching and maintaining a distributed
      cache. The service streamlines setup, scaling, and cluster failure
      management compared to a self-managed cache deployment. Additionally,
      Amazon ElastiCache offers integration with Amazon CloudWatch, providing
      users with increased visibility into the important performance metrics of
      their cache and the ability to receive alerts if any parts of their cache
      become overloaded.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/elasticache/
    baseURL: https://example.com
    tags:
      - Migrations
      - Tests
      - Cache
    properties:
      - type: Documentation
        url: https://aws.amazon.com/elasticache/
      - type: OpenAPI
        url: properties/elasticache-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/elasticache/features/
      - type: Pricing
        url: https://aws.amazon.com/elasticache/pricing/
      - type: Resources
        url: https://aws.amazon.com/elasticache/resources/
      - type: Migrations
        url: https://aws.amazon.com/elasticache/migrations/
      - type: FAQ
        url: https://aws.amazon.com/elasticache/faqs/
      - type: Customers
        url: https://aws.amazon.com/elasticache/customers/
    overlays:
      - type: APIs.io Search
        url: overlays/elasticache-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/elasticache-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:elasticache
  - name: Amazon Elastic Container Registry Public
    description: >-
      The Amazon Elastic Container Registry Public (Amazon ECR Public) is a
      managed service that allows you to host and manage container images in
      both public and private registries. You can utilize popular tools like the
      Docker CLI to push, pull, and manage images within a secure, scalable, and
      reliable registry for Docker or OCI images. This API specifically supports
      public repositories within Amazon ECR, while private repository
      functionality can be found in the Amazon Elastic Container Registry API
      Reference.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://docs.aws.amazon.com/AmazonECR/latest/public/what-is-ecr.html
    baseURL: https://example.com
    tags:
      - Layers
      - Uploads
      - Containers
      - Registry
    properties:
      - type: Documentation
        url: https://docs.aws.amazon.com/AmazonECR/latest/public/what-is-ecr.html
      - type: OpenAPI
        url: properties/ecr-public-openapi-original.yml
      - type: Gallery
        url: https://gallery.ecr.aws/
    overlays:
      - type: APIs.io Search
        url: overlays/ecr-public-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/ecr-public-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:ecr-public
  - name: Amazon Elastic File System
    description: >-
      Introducing Amazon Elastic File System (Amazon EFS), a user-friendly,
      scalable file storage solution designed for seamless integration with
      Amazon EC2 Linux and Mac instances within the AWS Cloud. With Amazon EFS,
      storage capacity dynamically adjusts to accommodate your changing file
      needs, ensuring your applications always have the necessary storage
      resources available. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/efs/
    baseURL: https://example.com
    tags:
      - Access
      - Accounts
      - Backup
      - Configurations
      - Describe
      - File
      - Groups
      - Lifecycle
      - Modify
      - Mount
      - Points
      - Policies
      - Preferences
      - Protection
      - Replication
      - Resources
      - Security
      - Sources
      - Systems
      - Tags
      - Targets
      - Targets
      - Untag
    properties:
      - type: Documentation
        url: https://aws.amazon.com/efs/
      - type: OpenAPI
        url: properties/elasticfilesystem-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/efs/features/
      - type: Pricing
        url: https://aws.amazon.com/efs/pricing/
      - type: Getting Started
        url: https://aws.amazon.com/efs/getting-started/
      - type: Resources
        url: https://aws.amazon.com/efs/resources/
      - type: FAQ
        url: https://aws.amazon.com/efs/faq/
      - type: Customers
        url: https://aws.amazon.com/efs/customers/
    overlays:
      - type: APIs.io Search
        url: overlays/elasticfilesystem-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/elasticfilesystem-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:elasticfilesystem
  - name: AWS Elastic Load Balancing
    description: >-
      Elastic Load Balancing is a feature that allows you to distribute incoming
      traffic across your EC2 instances, increasing the availability of your
      application. The load balancer monitors the health of registered instances
      and ensures that traffic is only routed to healthy instances. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/elasticloadbalancing/
    baseURL: https://example.com
    tags:
      - Balancer
      - Listeners
      - Load
      - Policies
      - Sets
    properties:
      - type: Documentation
        url: https://aws.amazon.com/elasticloadbalancing/
      - type: OpenAPI
        url: properties/elasticloadbalancing-openapi-original.yml
      - type: Pricing
        url: https://aws.amazon.com/elasticloadbalancing/pricing/
      - type: Getting Started
        url: https://aws.amazon.com/elasticloadbalancing/getting-started/
      - type: FAQ
        url: https://aws.amazon.com/elasticloadbalancing/faqs/
      - type: Partners
        url: https://aws.amazon.com/elasticloadbalancing/partners/
      - type: Customers
        url: https://aws.amazon.com/elasticloadbalancing/customers/
      - type: Features
        url: https://aws.amazon.com/elasticloadbalancing/features/
      - type: Application Load Balancers
        url: https://aws.amazon.com/elasticloadbalancing/application-load-balancer/
      - type: Network Load Balancers
        url: https://aws.amazon.com/elasticloadbalancing/network-load-balancer/
      - type: Gateway Load Balancers
        url: https://aws.amazon.com/elasticloadbalancing/gateway-load-balancer/
      - type: Classic Load Balancers
        url: https://aws.amazon.com/elasticloadbalancing/classic-load-balancer/
    overlays:
      - type: APIs.io Search
        url: overlays/elasticloadbalancing-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/elasticloadbalancing-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:elasticloadbalancing
  - name: AWS Elastic Beanstalk
    description: >-
      AWS Elastic Beanstalk makes it easy to develop, deploy, and maintain
      resilient and scalable applications in the Amazon Web Services cloud.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/elasticbeanstalk/
    baseURL: https://example.com
    tags:
      - Configurations
      - Settings
      - Validate
      - Applications
    properties:
      - type: Documentation
        url: https://aws.amazon.com/elasticbeanstalk/
      - type: OpenAPI
        url: properties/elasticbeanstalk-openapi-original.yml
      - type: Pricing
        url: https://aws.amazon.com/elasticbeanstalk/pricing/
      - type: Getting Started
        url: https://aws.amazon.com/elasticbeanstalk/getting-started/
      - type: Resources
        url: https://aws.amazon.com/elasticbeanstalk/developer-resources/
      - type: FAQ
        url: https://aws.amazon.com/elasticbeanstalk/faqs/
      - type: Partners
        url: https://aws.amazon.com/elasticbeanstalk/partners/
    overlays:
      - type: APIs.io Search
        url: overlays/elasticbeanstalk-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/elasticbeanstalk-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:elasticbeanstalk
  - name: Amazon EMR
    description: >-
      The API provided by Amazon EMR is a powerful web service designed to
      streamline the processing of large datasets with efficiency. By leveraging
      Hadoop processing and integrating various Amazon Web Services, this tool
      allows for seamless execution of tasks like web indexing, data mining, log
      file analysis, machine learning, scientific simulation, and data warehouse
      management.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/emr/
    baseURL: https://example.com
    tags:
      - Mapping
      - Sessions
      - Studios
      - Datasets
    properties:
      - type: Documentation
        url: https://aws.amazon.com/emr/
      - type: OpenAPI
        url: properties/elasticmapreduce-openapi-original.yml
      - type: Pricing
        url: https://aws.amazon.com/emr/pricing/
      - type: FAQ
        url: https://aws.amazon.com/emr/faqs/
      - type: Partners
        url: https://aws.amazon.com/emr/partners/
      - type: Getting Started
        url: https://aws.amazon.com/emr/getting-started/
      - type: Features
        url: https://aws.amazon.com/emr/features/
      - type: Studio
        url: https://aws.amazon.com/emr/features/studio/
      - type: Notebooks
        url: https://aws.amazon.com/emr/features/notebooks/
      - type: Serverless
        url: https://aws.amazon.com/emr/serverless/
    overlays:
      - type: APIs.io Search
        url: overlays/elasticmapreduce-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/elasticmapreduce-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:elasticmapreduce
  - name: Amazon EMR on EKS
    description: >-
      Amazon EMR on EKS is a deployment option that allows you to run big data
      frameworks on Amazon EKS. This option allows you to focus on analytics
      workloads while Amazon EMR on EKS manages containers for open-source
      applications. The API name for this service is Amazon EMR containers, and
      it is used for CLI commands, IAM policy actions, and service endpoints
      related to Amazon EMR on EKS. For more information about Amazon EMR on EKS
      concepts and tasks, please refer to the documentation.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: >-
      https://docs.aws.amazon.com/emr/latest/EMR-on-EKS-DevelopmentGuide/emr-eks.html
    baseURL: https://example.com
    tags:
      - ARN
      - Clusters
      - Credentials
      - Describe
      - Endpoints
      - Job RUns
      - Job Templates
      - Jobs
      - Managed
      - Resources
      - Runs
      - Sessions
      - Tags
      - Templates
      - Untag
      - Virtual
      - Virtual Clusters
    properties:
      - type: Documentation
        url: >-
          https://docs.aws.amazon.com/emr/latest/EMR-on-EKS-DevelopmentGuide/emr-eks.html
      - type: OpenAPI
        url: properties/emr-containers-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/emr-containers-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/emr-containers-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:emr-containers
  - name: AWS Elastic Transcoder Service
    description: >-
      Amazon Elastic Transcoder is media transcoding in the cloud. It is
      designed to be a highly scalable, easy to use and a cost effective way for
      developers and businesses to convert (or “transcode”) media files from
      their source format into versions that will playback on devices like
      smartphones, tablets and PCs.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/elastictranscoder/
    baseURL: https://example.com
    tags:
      - Jobs
      - Notifications
      - Pipelines
      - Presets
      - Read
      - Roles
      - Status
      - Tests
      - Transcoder
    properties:
      - type: Documentation
        url: https://aws.amazon.com/elastictranscoder/
      - type: OpenAPI
        url: properties/elastictranscoder-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/elastictranscoder-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/elastictranscoder-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:elastictranscoder
  - name: Amazon Simple Email Service
    description: >-
      This document provides detailed information about the Amazon Simple Email
      Service (Amazon SES) API version 2010-12-01. It is recommended to refer to
      the Amazon SES Developer Guide in conjunction with this document. The
      Amazon SES Developer Guide also includes a list of Amazon SES endpoints
      for service requests. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/ses/
    baseURL: https://example.com
    tags:
      - Emails
      - Identity
      - Verify
    properties:
      - type: Documentation
        url: https://aws.amazon.com/ses/
      - type: OpenAPI
        url: properties/email-openapi-original.yml
      - type: Pricing
        url: https://aws.amazon.com/ses/pricing/
      - type: Getting Started
        url: https://aws.amazon.com/ses/getting-started/
      - type: FAQ
        url: https://aws.amazon.com/ses/faqs/
      - type: Resources
        url: https://aws.amazon.com/ses/developer-resources/
      - type: Customers
        url: https://aws.amazon.com/ses/customers/
      - type: Partners
        url: https://aws.amazon.com/ses/partners/
    overlays:
      - type: APIs.io Search
        url: overlays/email-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/email-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:email
  - name: Amazon EMR Serverless
    description: >-
      Introducing Amazon EMR Serverless, a new deployment option for Amazon EMR
      that offers a serverless runtime environment for running analytics
      applications with popular open source frameworks like Apache Spark and
      Apache Hive. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: >-
      https://docs.aws.amazon.com/emr/latest/EMR-Serverless-UserGuide/emr-serverless.html
    baseURL: https://emr-serverless.[region].amazonaws.com
    tags:
      - ARN
      - Applications
      - Dashboard
      - Job RUns
      - Jobs
      - Resources
      - Runs
      - Stop
      - Tags
      - Untag
    properties:
      - type: Documentation
        url: >-
          https://docs.aws.amazon.com/emr/latest/EMR-Serverless-UserGuide/emr-serverless.html
      - type: OpenAPI
        url: properties/emr-serverless-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/emr-serverless-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/emr-serverless-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:emr-serverless
  - name: Amazon Elasticsearch Configuration Service
    description: >-
      Utilize the Amazon Elasticsearch Configuration Service API for creating,
      customizing, and overseeing Elasticsearch domains. Developers can refer to
      the Amazon Elasticsearch Service Developer Guide for sample code
      showcasing the Configuration API in action, as well as instructions for
      sending signed HTTP requests to Elasticsearch APIs.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: >-
      https://docs.aws.amazon.com/opensearch-service/latest/developerguide/createupdatedomains.html
    baseURL: https://es.[region].amazonaws.com
    tags:
      - Accept
      - Access
      - Associate
      - Authorize
      - Auto
      - Cancel
      - Change
      - Clusters
      - Compatible
      - Configurations
      - Connections
      - Describe
      - Dissociate
      - Domains
      - Elasticsearch
      - Endpoints
      - History
      - Inbound
      - Info
      - Instances
      - Limits
      - Names
      - Offerings
      - Outbound
      - Packages
      - Progress
      - Purchase
      - Reject
      - Removal
      - Removes
      - Reserved
      - Revoke
      - Roles
      - Search
      - Services
      - Software
      - Status
      - Tags
      - Tunes
      - Types
      - Upgrade
      - VPC
      - Versions
    properties:
      - type: Documentation
        url: >-
          https://docs.aws.amazon.com/opensearch-service/latest/developerguide/createupdatedomains.html
      - type: OpenAPI
        url: properties/es-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/es-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/es-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:es
  - name: AWS Marketplace Entitlement Service
    description: >-
      The AWS Marketplace Entitlement Service API documentation provides an
      overview of how to use the service to determine a customer's entitlement
      to a specific product. Entitlements represent the capacity or access a
      customer has to a particular product, such as user seats in an SaaS
      application or data capacity in a database. The GetEntitlements function
      retrieves entitlement records for a Marketplace product.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: >-
      https://docs.aws.amazon.com/marketplace/latest/userguide/checking-entitlements.html
    baseURL: https://example.com
    tags:
      - Entitlements
    properties:
      - type: Documentation
        url: >-
          https://docs.aws.amazon.com/marketplace/latest/userguide/checking-entitlements.html
      - type: OpenAPI
        url: properties/entitlementmarketplace-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/entitlementmarketplace-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/entitlementmarketplace-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:entitlementmarketplace
  - name: AWS Entity Resolution
    description: >-
      Discover the capabilities of the Entity Resolution API, a part of Amazon
      Web Services that simplifies the process of matching consumer identifiers
      within source records. By utilizing Entity Resolution, developers and
      analysts in the advertising and marketing industries can effortlessly
      create a comprehensive and accurate view of their customers.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/entity-resolution/
    baseURL: https://example.com
    tags:
      - ARN
      - Er
      - Erservices
      - Jobs
      - Mapping
      - Mappingworkflows
      - Match
      - Matches
      - Matching
      - Matching Workflows
      - Names
      - Prov
      - Providers
      - Resources
      - Schemas
      - Services
      - Tags
      - Untag
      - Workflows
    properties:
      - type: Documentation
        url: https://aws.amazon.com/entity-resolution/
      - type: OpenAPI
        url: properties/entityresolution-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/entity-resolution/features/
      - type: FAQ
        url: https://aws.amazon.com/entity-resolution/faqs/
      - type: Pricing
        url: https://aws.amazon.com/entity-resolution/pricing/
      - type: Resources
        url: https://aws.amazon.com/entity-resolution/resources/
      - type: Customers
        url: https://aws.amazon.com/entity-resolution/customers/
      - type: Partners
        url: https://aws.amazon.com/entity-resolution/partners/
    overlays:
      - type: APIs.io Search
        url: overlays/entityresolution-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/entityresolution-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:entityresolution
  - name: Amazon EventBridge
    description: >-
      With Amazon EventBridge, you can easily monitor and respond to changes in
      your AWS resources by setting up rules that trigger actions based on
      specific events. Events generated by your resources are sent to an event
      stream, allowing you to create customized rules that match certain events
      and direct them to designated targets for further processing. You can also
      schedule actions to be performed at specific intervals. For example, you
      can automate tasks such as updating DNS entries, analyzing API records for
      security risks, or creating snapshots of EBS volumes. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/eventbridge/
    baseURL: https://example.com
    tags:
      - Endpoints
      - ' Events'
    properties:
      - type: Documentation
        url: https://aws.amazon.com/eventbridge/
      - type: OpenAPI
        url: properties/eventbridge-openapi-original.yml
      - type: Pricing
        url: https://aws.amazon.com/eventbridge/pricing/
      - type: Resources
        url: https://aws.amazon.com/eventbridge/resources/
      - type: FAQ
        url: https://aws.amazon.com/eventbridge/faqs/
      - type: Integrations
        url: https://aws.amazon.com/eventbridge/integrations/
      - type: Features
        url: https://aws.amazon.com/eventbridge/features/
      - type: Event Bus
        url: https://aws.amazon.com/eventbridge/event-bus/
      - type: Pipes
        url: https://aws.amazon.com/eventbridge/pipes/
      - type: Scheduler
        url: https://aws.amazon.com/eventbridge/scheduler/
    overlays:
      - type: APIs.io Search
        url: overlays/eventbridge-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/eventbridge-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:eventbridge
  - name: Amazon Kinesis Data Firehose
    description: >-
      The Amazon Kinesis Data Firehose API is a comprehensive tool for managing
      real-time streaming data delivery to a variety of destinations, including
      Amazon S3, Amazon OpenSearch Service, Amazon Redshift, Splunk, and more.
      This fully managed service streamlines the process of transmitting data
      effectively and efficiently.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/firehose/
    baseURL: https://example.com
    tags:
      - Destinations
      - Data
      - Delivery
    properties:
      - type: Documentation
        url: https://aws.amazon.com/firehose/
      - type: OpenAPI
        url: properties/firehose-openapi-original.yml
      - type: FAQ
        url: https://aws.amazon.com/firehose/faqs/
      - type: Resources
        url: https://aws.amazon.com/firehose/resources/
      - type: Customers
        url: https://aws.amazon.com/firehose/customers/
      - type: Partners
        url: https://aws.amazon.com/firehose/partners/
      - type: Pricing
        url: https://aws.amazon.com/firehose/pricing/
      - type: Features
        url: https://aws.amazon.com/firehose/features/
    overlays:
      - type: APIs.io Search
        url: overlays/firehose-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/firehose-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:firehose
  - name: Amazon CloudWatch Evidently
    description: >-
      Utilize Amazon CloudWatch Evidently API to securely introduce and test new
      features to a percentage of your user base before full deployment.
      Monitoring the performance of these new features allows you to make
      informed decisions on when to increase user traffic. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: >-
      https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/CloudWatch-Evidently.html
    baseURL: https://example.com
    tags:
      - ARN
      - Batches
      - Cancel
      - Data
      - Deliveries
      - Evaluate
      - Evaluations
      - Events
      - Experiment
      - Experiments
      - Feature
      - Features
      - Launch
      - Launches
      - Patterns
      - Projects
      - References
      - Resources
      - Results
      - Segments
      - Stop
      - Tags
      - Tests
      - Untag
    properties:
      - type: Documentation
        url: >-
          https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/CloudWatch-Evidently.html
      - type: OpenAPI
        url: properties/evidently-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/evidently-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/evidently-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:evidently
  - name: Amazon Forecast
    description: >-
      Amazon Forecast, is a powerful tool designed for businesses looking to
      analyze and predict time-series data using machine learning.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/forecast/
    baseURL: https://example.com
    tags:
      - Datasets
      - Groups
    properties:
      - type: Documentation
        url: https://aws.amazon.com/forecast/
      - type: OpenAPI
        url: properties/forecast-openapi-original.yml
      - type: Partners
        url: https://aws.amazon.com/forecast/partners/
      - type: Customers
        url: https://aws.amazon.com/forecast/customers/
      - type: Resources
        url: https://aws.amazon.com/forecast/resources/
      - type: Embedded Solutions
        url: https://aws.amazon.com/forecast/embedded-solutions/
      - type: Pricing
        url: https://aws.amazon.com/forecast/pricing/
      - type: Features
        url: https://aws.amazon.com/forecast/features/
    overlays:
      - type: APIs.io Search
        url: overlays/forecast-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/forecast-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:forecast
  - name: AWS Fault Injection Simulator
    description: >-
      AWS Fault Injection Service (FIS), a component of the AWS Resilience Hub,
      is a comprehensive service designed to enhance an application's
      performance, observability, and resilience through the implementation of
      fault injection experiments. By streamlining the setup and execution of
      controlled fault injection tests across various AWS services, FIS empowers
      teams to increase their confidence in the reliability of their
      applications.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/fis/
    baseURL: https://example.com
    tags:
      - ARN
      - Accounts
      - Actions
      - Configurations
      - Experiment
      - Experiments
      - Resolved
      - Resources
      - Stop
      - Tags
      - Targets
      - Targets
      - Templates
      - Types
      - Untag
    properties:
      - type: Documentation
        url: https://aws.amazon.com/fis/
      - type: OpenAPI
        url: properties/fis-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/fis/features/
      - type: Pricing
        url: https://aws.amazon.com/fis/pricing/
      - type: FAQ
        url: https://aws.amazon.com/fis/faqs/
      - type: Pricing
        url: https://aws.amazon.com/fis/pricing/
    overlays:
      - type: APIs.io Search
        url: overlays/fis-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/fis-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:fis
  - name: Amazon Fraud Detector
    description: >-
      Build, deploy, and manage fraud detection models without previous machine
      learning (ML) experience. Gain insights from your historical data, plus
      20+ years of Amazon experience, to construct an accurate, customized fraud
      detection model. Start detecting fraud immediately, easily enhance models
      with customized business rules, and deploy results to generate critical
      predictions.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/fraud-detector/
    baseURL: https://example.com
    tags:
      - Variables
      - Fraud
      - ' Detection'
    properties:
      - type: Documentation
        url: https://aws.amazon.com/fraud-detector/
      - type: OpenAPI
        url: properties/frauddetector-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/fraud-detector/features/
      - type: Pricing
        url: https://aws.amazon.com/fraud-detector/pricing/
      - type: FAQ
        url: https://aws.amazon.com/fraud-detector/faqs/
      - type: Resources
        url: https://aws.amazon.com/fraud-detector/resources/
      - type: Customers
        url: https://aws.amazon.com/fraud-detector/customers/
    overlays:
      - type: APIs.io Search
        url: overlays/frauddetector-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/frauddetector-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:frauddetector
  - name: AWS Firewall Manager
    description: >-
      Welcome to the Firewall Manager API Reference. This comprehensive guide is
      designed for developers seeking in-depth information on the various
      actions, data types, and errors associated with the Firewall Manager API.
      For a more detailed overview of Firewall Manager features, please refer to
      the Firewall Manager Developer Guide. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/firewall-manager/
    baseURL: https://example.com
    tags:
      - Resources
      - Untag
    properties:
      - type: Documentation
        url: https://aws.amazon.com/firewall-manager/
      - type: OpenAPI
        url: properties/fms-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/firewall-manager/features/
      - type: Pricing
        url: https://aws.amazon.com/firewall-manager/pricing/
      - type: Getting-started
        url: https://aws.amazon.com/firewall-manager/getting-started/
      - type: Resources
        url: https://aws.amazon.com/firewall-manager/resources/
      - type: FAQ
        url: https://aws.amazon.com/firewall-manager/faqs/
    overlays:
      - type: APIs.io Search
        url: overlays/fms-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/fms-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:fms
  - name: Amazon GameLift
    description: >-
      The Amazon GameLift API offers comprehensive cloud hosting solutions for
      session-based multiplayer game servers. It includes features for
      deploying, managing, and expanding game servers seamlessly. Leveraging
      Amazon Web Services' robust global computing network, GameLift ensures
      top-tier performance, reliability, and cost-efficiency for your game
      servers.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/gamelift/
    baseURL: https://example.com
    tags:
      - Matchmaking
      - Rules
      - Sets
      - Validate
      - Games
    properties:
      - type: Documentation
        url: https://aws.amazon.com/gamelift/
      - type: OpenAPI
        url: properties/gamelift-openapi-original.yml
      - type: Pricing
        url: https://aws.amazon.com/gamelift/pricing/
      - type: Features
        url: https://aws.amazon.com/gamelift/features/
      - type: Resources
        url: https://aws.amazon.com/gamelift/resources/
      - type: FAQ
        url: https://aws.amazon.com/gamelift/faq/
      - type: Getting-started
        url: https://aws.amazon.com/gamelift/getting-started/
    overlays:
      - type: APIs.io Search
        url: overlays/gamelift-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/gamelift-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:gamelift
  - name: Global Accelerator
    description: >-
      Global Accelerator is a powerful API service that allows developers to
      create accelerators to enhance the performance of their applications for
      both local and global users. This API Reference provides detailed
      information on Global Accelerator API actions, data types, and errors,
      catering to developers looking to leverage Global Accelerator features.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/global-accelerator/
    baseURL: https://example.com
    tags:
      - CIDR
      - Withdraw
    properties:
      - type: Documentation
        url: https://aws.amazon.com/global-accelerator/
      - type: OpenAPI
        url: properties/globalaccelerator-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/global-accelerator/features/
      - type: Pricing
        url: https://aws.amazon.com/global-accelerator/pricing/
      - type: FAQ
        url: https://aws.amazon.com/global-accelerator/faqs/
      - type: Customers
        url: https://aws.amazon.com/global-accelerator/customers/
    overlays:
      - type: APIs.io Search
        url: overlays/globalaccelerator-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/globalaccelerator-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:globalaccelerator
  - name: Amazon S3 Glacier
    description: >-
      Amazon S3 Glacier (Glacier) is a cost-effective storage solution designed
      for long-term storage of infrequently accessed data. It provides secure,
      durable, and easy-to-use storage for data backup and archival purposes.
      With Glacier, users can store data for extended periods without worrying
      about capacity planning or hardware management. Glacier is ideal for when
      low storage costs are a priority and data retrieval is rare. For
      applications requiring fast or frequent access to data, Amazon S3 is
      recommended. Users can store data in any format without limits on the
      total amount of data stored in Glacier. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/s3/storage-classes/glacier/
    baseURL: https://example.com
    tags:
      - Access
      - Accounts
      - Archive
      - Archives
      - Capacity
      - Complete
      - Configurations
      - Data
      - Describe
      - Initiate
      - Jobs
      - Locks
      - Multipart
      - Names
      - Notifications
      - Output
      - Policies
      - Provisioned
      - Purchase
      - Removes
      - Retrieval
      - Sets
      - Tags
      - Uploads
      - Vault
      - Vaults
    properties:
      - type: Documentation
        url: https://aws.amazon.com/s3/storage-classes/glacier/
      - type: OpenAPI
        url: properties/glacier-openapi-original.yml
      - type: Instant-retrieval
        url: https://aws.amazon.com/s3/storage-classes/glacier/instant-retrieval/
    overlays:
      - type: APIs.io Search
        url: overlays/glacier-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/glacier-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:glacier
  - name: AWS FinSpace
    description: >-
      Experience seamless data processing and analytics tailored for Capital
      Markets with our API, which offers Managed kdb Insights. Take advantage of
      our free AWS training to enhance your skills and advance your career with
      AWS Cloud Practitioner Essentials. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/finspace/
    baseURL: https://example.com
    tags:
      - Access
      - Change Sets
      - Credentials
      - Data
      - Data Views
      - Datasets
      - Details
      - Disable
      - Disassociate
      - Enable
      - External
      - Groups
      - Locations
      - Password
      - Permission
      - Programmatic
      - Reset
      - Users
      - View
      - Views
      - Working
    properties:
      - type: Documentation
        url: https://aws.amazon.com/finspace/
      - type: OpenAPI
        url: properties/finspace-data-openapi-original.yml
      - type: Pricing
        url: https://aws.amazon.com/finspace/pricing/
      - type: Getting-started
        url: https://aws.amazon.com/finspace/getting-started/
      - type: Partners
        url: https://aws.amazon.com/finspace/partners/
      - type: FAQ
        url: https://aws.amazon.com/finspace/faqs/
      - type: Getting-started
        url: https://aws.amazon.com/finspace/getting-started/
    overlays:
      - type: APIs.io Search
        url: overlays/finspace-data-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/finspace-data-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:finspace-data
  - name: Amazon FSx
    description: >-
      The Amazon FSx API simplifies the process of launching, managing, and
      expanding feature-rich, high-performance file systems in the cloud. With
      its reliability, security, scalability, and numerous capabilities, Amazon
      FSx supports a variety of workloads. Leveraging the latest AWS
      technologies in compute, networking, and disk storage, Amazon FSx delivers
      high performance at a lower total cost of ownership.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/fsx/
    baseURL: https://example.com
    tags:
      - Volumes
      - File Systems
    properties:
      - type: Documentation
        url: https://aws.amazon.com/fsx/
      - type: OpenAPI
        url: properties/fsx-openapi-original.yml
      - type: Pricing
        url: https://aws.amazon.com/fsx/pricing/
      - type: Netapp-ontap
        url: https://aws.amazon.com/fsx/netapp-ontap/
      - type: Openzfs
        url: https://aws.amazon.com/fsx/openzfs/
      - type: Windows
        url: https://aws.amazon.com/fsx/windows/
      - type: Lustre
        url: https://aws.amazon.com/fsx/lustre/
    overlays:
      - type: APIs.io Search
        url: overlays/fsx-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/fsx-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:fsx
  - name: AWS IoT Greengrass
    description: >-
      IoT Greengrass brings local compute, messaging, data management, sync, and
      ML inference capabilities to edge devices. This enables devices to collect
      and analyze data closer to the source of information, react autonomously
      to local events, and communicate securely with each other on local
      networks. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/greengrass/
    baseURL: https://example.com
    tags:
      - ARN
      - Accounts
      - Artifacts
      - Associate
      - Associated
      - Ates
      - Batches
      - Cancel
      - Cand
      - Candidates
      - Clients
      - Components
      - Connectivity
      - Core
      - Deployments
      - Describe
      - Device
      - Devices
      - Disassociate
      - Effective
      - Green Grass
      - Info
      - Installed
      - Metadata
      - Names
      - Resolve
      - Resources
      - Roles
      - Service Roles
      - Services
      - Tags
      - Things
      - Untag
      - Versions
    properties:
      - type: Documentation
        url: https://aws.amazon.com/greengrass/
      - type: OpenAPI
        url: properties/greengrassv2-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/greengrass/features/
      - type: Ml
        url: https://aws.amazon.com/greengrass/ml/
      - type: Pricing
        url: https://aws.amazon.com/greengrass/pricing/
      - type: Partners
        url: https://aws.amazon.com/greengrass/partners/
      - type: Getting-started
        url: https://aws.amazon.com/greengrass/getting-started/
      - type: FAQ
        url: https://aws.amazon.com/greengrass/faqs/
    overlays:
      - type: APIs.io Search
        url: overlays/greengrassv2-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/greengrassv2-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:greengrassv2
  - name: AWS Glue
    description: >-
      The first step in any analytics or machine learning project is ensuring
      your data is prepared for quality results. AWS Glue is a serverless data
      integration service that streamlines and simplifies the data preparation
      process, making it faster and more cost-effective. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/glue/
    baseURL: https://example.com
    tags:
      - Workflows
    properties:
      - type: Documentation
        url: https://aws.amazon.com/glue/
      - type: OpenAPI
        url: properties/glue-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/glue/features/
      - type: Pricing
        url: https://aws.amazon.com/glue/pricing/
      - type: Partners
        url: https://aws.amazon.com/glue/partners/
      - type: Getting Started
        url: https://aws.amazon.com/glue/getting-started/
      - type: Resources
        url: https://aws.amazon.com/glue/resources/
      - type: FAQ
        url: https://aws.amazon.com/glue/faqs/
      - type: Customers
        url: https://aws.amazon.com/glue/customers/
    overlays:
      - type: APIs.io Search
        url: overlays/glue-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/glue-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:glue
  - name: Amazon Managed Grafana
    description: >-
      Amazon Managed Grafana is a managed and secure data visualization service
      that allows you to easily query, correlate, and visualize operational
      metrics, logs, and traces from various sources. It simplifies the
      deployment, operation, and scalability of Grafana, a popular data
      visualization tool known for its flexible data support. Users can create
      isolated Grafana servers, called workspaces, where they can design
      dashboards and visualizations to analyze their data without the need for
      hardware deployment.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/grafana/
    baseURL: https://example.com
    tags:
      - ARN
      - Authentication
      - Configurations
      - Disassociate
      - Keys
      - Licenses
      - Names
      - Permissions
      - Resources
      - Tags
      - Types
      - Untag
      - Versions
      - Workspaces
    properties:
      - type: Documentation
        url: https://aws.amazon.com/grafana/
      - type: OpenAPI
        url: properties/grafana-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/grafana/features/
      - type: Pricing
        url: https://aws.amazon.com/grafana/pricing/
      - type: Resources
        url: https://aws.amazon.com/grafana/resources/
      - type: FAQ
        url: https://aws.amazon.com/grafana/faqs/
      - type: Customers
        url: https://aws.amazon.com/grafana/customers/
      - type: Partners
        url: https://aws.amazon.com/grafana/partners/
    overlays:
      - type: APIs.io Search
        url: overlays/grafana-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/grafana-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:grafana
  - name: Amazon GuardDuty
    description: >-
      Amazon GuardDuty is a security monitoring service that continuously
      analyzes various data sources within your Amazon Web Services environment,
      such as VPC flow logs, CloudTrail event logs, EKS audit logs, DNS logs,
      and more. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/guardduty/
    baseURL: https://example.com
    tags:
      - ARN
      - Accounts
      - Administrative
      - Administrator
      - Archive
      - Configurations
      - Count
      - Coverage
      - Days
      - Decline
      - Describe
      - Destinations
      - Detectors
      - Disable
      - Disassociate
      - Enable
      - Feedback
      - Filter
      - Filters
      - Findings
      - Free
      - IP
      - IPSet
      - IPSets
      - Intelligence
      - Invitation
      - Invitations
      - Invite
      - Malware
      - Master
      - Members
      - Monitoring
      - Names
      - Organizations
      - Publishing
      - Remaining
      - Resources
      - Samples
      - Scans
      - Sets
      - Settings
      - Statistics
      - Stop
      - Tags
      - Threat
      - Trials
      - Unarchive
      - Untag
      - Usage
    properties:
      - type: Documentation
        url: https://aws.amazon.com/guardduty/
      - type: OpenAPI
        url: properties/guardduty-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/guardduty/features/
      - type: Pricing
        url: https://aws.amazon.com/guardduty/pricing/
      - type: Getting Started
        url: https://aws.amazon.com/guardduty/getting-started/
      - type: Resources
        url: https://aws.amazon.com/guardduty/resources/
      - type: FAQ
        url: https://aws.amazon.com/guardduty/faqs/
      - type: Partners
        url: https://aws.amazon.com/guardduty/resources/partners/
      - type: Customers
        url: https://aws.amazon.com/guardduty/customers/
    overlays:
      - type: APIs.io Search
        url: overlays/guardduty-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/guardduty-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:guardduty
  - name: AWS IoT Greengrass
    description: >-
      This API, AWS IoT Greengrass, extends the capabilities of AWS to physical
      devices, enabling them to process data locally while still utilizing the
      cloud for management, analytics, and storage. This allows devices to
      respond quickly to local events even with intermittent connectivity,
      minimizing the cost of transmitting data to the cloud by enabling the
      execution of AWS Lambda functions locally.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/greengrass/
    baseURL: https://example.com
    tags:
      - $Reset
      - $Stop
      - ARN
      - Accounts
      - Associated
      - Authorities
      - Authority
      - Bulk
      - Certificate Authorities
      - Certificates
      - Configurations
      - Connectivity
      - Connectors
      - Core
      - Cores
      - Definitions
      - Deployments
      - Detailed
      - Device
      - Devices
      - Expiry
      - Functions
      - Green Grass
      - Groups
      - Info
      - Jobs
      - Loggers
      - Names
      - Reports
      - Reset
      - Resources
      - Roles
      - Runtime
      - Runtime Configurations
      - Service Roles
      - Services
      - Software
      - Status
      - Stop
      - Subscriptions
      - Tags
      - Things
      - Untag
      - Versions
    properties:
      - type: Documentation
        url: https://aws.amazon.com/greengrass/
      - type: OpenAPI
        url: properties/greengrass-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/greengrass/features/
      - type: Ml
        url: https://aws.amazon.com/greengrass/ml/
      - type: Pricing
        url: https://aws.amazon.com/greengrass/pricing/
      - type: Partners
        url: https://aws.amazon.com/greengrass/partners/
      - type: Getting-started
        url: https://aws.amazon.com/greengrass/getting-started/
      - type: FAQ
        url: https://aws.amazon.com/greengrass/faqs/
      - type: Device-tester
        url: https://aws.amazon.com/greengrass/device-tester/
    overlays:
      - type: APIs.io Search
        url: overlays/greengrass-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/greengrass-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:greengrass
  - name: AWS HealthLake
    description: >-
      AWS HealthLake is a service designed for healthcare companies that need a
      comprehensive view of individual and patient population health data. This
      HIPAA-eligible service utilizes FHIR API transactions to securely store
      and transform data into a queryable format at a large scale.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/healthlake/
    baseURL: https://example.com
    tags:
      - Resources
      - Untag
    properties:
      - type: Documentation
        url: https://aws.amazon.com/healthlake/
      - type: OpenAPI
        url: properties/healthlake-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/healthlake/features/
      - type: Pricing
        url: https://aws.amazon.com/healthlake/pricing/
      - type: Getting Started
        url: https://aws.amazon.com/healthlake/getting-started/
      - type: Resources
        url: https://aws.amazon.com/healthlake/resources/
      - type: Customers
        url: https://aws.amazon.com/healthlake/faqs/
      - type: Customers
        url: https://aws.amazon.com/healthlake/customers/
      - type: Partners
        url: https://aws.amazon.com/healthlake/partners/
    overlays:
      - type: APIs.io Search
        url: overlays/healthlake-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/healthlake-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:healthlake
  - name: AWS Identity and Access Management
    description: >-
      IAM is a trusted web service that enables secure access control for Amazon
      Web Services. It offers centralized management of users, access keys, and
      permissions to regulate access to AWS resources. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/iam/
    baseURL: https://example.com
    tags:
      - Certificates
      - Signing
      - Uploads
      - ' Identity'
      - ' IAM'
    properties:
      - type: Documentation
        url: https://aws.amazon.com/iam/
      - type: OpenAPI
        url: properties/iam-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/iam/features/
      - type: Getting Started
        url: https://aws.amazon.com/iam/getting-started/
      - type: Resources
        url: https://aws.amazon.com/iam/resources/
      - type: FAQ
        url: https://aws.amazon.com/iam/faqs/
    overlays:
      - type: APIs.io Search
        url: overlays/iam-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/iam-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:iam
  - name: AWS Ground Station
    description: >-
      Welcome to the AWS Ground Station API Reference. AWS Ground Station is a
      fully managed service that enables you to control satellite
      communications, downlink and process satellite data, and scale your
      satellite operations efficiently and cost-effectively without having to
      build or manage your own ground station infrastructure.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/ground-station/
    baseURL: https://example.com
    tags:
      - ARN
      - Agent
      - Configurations
      - Contacts
      - Dataflow
      - Describe
      - Endpoints
      - Ephemer
      - Ground
      - Groundstation
      - Groups
      - Minute
      - Mission
      - Mission Profile
      - Profiles
      - Register
      - Reserve
      - Resources
      - Satellites
      - Stations
      - Status
      - Tags
      - Types
      - Untag
      - Usage
    properties:
      - type: Documentation
        url: https://aws.amazon.com/ground-station/
      - type: OpenAPI
        url: properties/groundstation-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/ground-station/features/
      - type: Locations
        url: https://aws.amazon.com/ground-station/locations/
      - type: Pricing
        url: https://aws.amazon.com/ground-station/pricing/
      - type: Getting-started
        url: https://aws.amazon.com/ground-station/getting-started/
      - type: FAQ
        url: https://aws.amazon.com/ground-station/faqs/
      - type: Features
        url: https://aws.amazon.com/ground-station/features/
    overlays:
      - type: APIs.io Search
        url: overlays/groundstation-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/groundstation-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:groundstation
  - name: AWS  Identity Store
    description: >-
      The API for the Identity Store service within IAM Identity Center is a
      central hub for accessing all user and group identities. You can find
      detailed information on how to use this service in the IAM Identity Center
      User Guide, which outlines the available identity store operations that
      can be accessed programmatically. The API utilizes the sso and
      identitystore namespaces for seamless integration with your systems.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: >-
      https://docs.aws.amazon.com/singlesignon/latest/IdentityStoreAPIReference/welcome.html
    baseURL: https://example.com
    tags:
      - Users
      - Identity
    properties:
      - type: Documentation
        url: >-
          https://docs.aws.amazon.com/singlesignon/latest/IdentityStoreAPIReference/welcome.html
      - type: OpenAPI
        url: properties/identitystore-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/identitystore-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/identitystore-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:identitystore
  - name: AWS EC2 Image Builder
    description: >-
      The API for EC2 Image Builder is a comprehensive AWS service designed to
      streamline the process of automating the creation, control, and
      distribution of personalized, secure, and current server images which are
      pre-loaded and pre-configured with software and settings according to
      required IT guidelines.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/image-builder/
    baseURL: https://example.com
    tags:
      - ARN
      - Actions
      - Aggregations
      - Build
      - Cancel
      - Components
      - Configurations
      - Container
      - Creation
      - Distributions
      - Execution
      - Executions
      - Findings
      - Images
      - Import
      - Infrastructure
      - Lifecycle
      - Packages
      - Pipelines
      - Policies
      - Recipes
      - Resources
      - Scans
      - Send
      - States
      - Steps
      - Tags
      - Untag
      - Versions
      - Waiting
      - Workflows
    properties:
      - type: Documentation
        url: https://aws.amazon.com/image-builder/
      - type: OpenAPI
        url: properties/imagebuilder-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/image-builder/features/
      - type: FAQ
        url: https://aws.amazon.com/image-builder/faqs/
    overlays:
      - type: APIs.io Search
        url: overlays/imagebuilder-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/imagebuilder-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:imagebuilder
  - name: Amazon Inspector Scan
    description: >-
      The Amazon Inspector API effortlessly identifies workloads, such as Amazon
      EC2 instances, containers, and Lambda functions, and conducts thorough
      scans to detect software vulnerabilities and unintentional network risks.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/inspector/
    baseURL: https://example.com
    tags:
      - Inspector
      - Scans
    properties:
      - type: Documentation
        url: https://aws.amazon.com/inspector/
      - type: OpenAPI
        url: properties/inspector-scan-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/inspector/features/
      - type: Pricing
        url: https://aws.amazon.com/inspector/pricing/
      - type: Resources
        url: https://aws.amazon.com/inspector/resources/
      - type: Getting Started
        url: https://aws.amazon.com/inspector/getting-started/
      - type: FAQ
        url: https://aws.amazon.com/inspector/faqs/
      - type: Customers
        url: https://aws.amazon.com/inspector/customers/
      - type: Partners
        url: https://aws.amazon.com/inspector/partners/
    overlays:
      - type: APIs.io Search
        url: overlays/inspector-scan-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/inspector-scan-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:inspector-scan
  - name: AWS Health
    description: >-
      The Health API grants access to Health information displayed in the Health
      Dashboard. Users can utilize API operations to retrieve data on events
      that may impact their Amazon Web Services and resources. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/health/
    baseURL: https://example.com
    tags:
      - Access
      - Enable
      - Health
      - Organizations
      - Services
      - Healthcare
    properties:
      - type: Documentation
        url: https://aws.amazon.com/health/
      - type: OpenAPI
        url: properties/health-openapi-original.yml
      - type: Case-studies
        url: https://aws.amazon.com/health/case-studies/
      - type: Life Science Solutions
        url: https://aws.amazon.com/health/life-sciences/solutions/
      - type: Genomics Solutions
        url: https://aws.amazon.com/health/genomics/solutions/
      - type: Healthcare Solutions
        url: https://aws.amazon.com/health/healthcare/solutions/
      - type: Providers
        url: https://aws.amazon.com/health/providers/
      - type: Payors
        url: https://aws.amazon.com/health/payors/
      - type: Healthtech
        url: https://aws.amazon.com/health/healthtech/
    overlays:
      - type: APIs.io Search
        url: overlays/health-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/health-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:health
  - name: AWS IoT
    description: >-
      The IoT API enables secure communication between Internet-connected
      devices and the Amazon Web Services cloud. Users can access custom
      IoT-Data endpoints, set up data processing rules, integrate with other
      services, manage device resources, configure logging, and create
      authentication policies and credentials. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/iot/
    baseURL: https://example.com
    tags:
      - ARN
      - Accept
      - Accounts
      - Actions
      - Active
      - Aggregation
      - Alias
      - Aliases
      - Associate
      - Ate
      - Attached
      - Audit
      - Audits
      - Authorization
      - Authorizers
      - Behavior
      - Behaviors
      - Billing
      - Buckets
      - CA
      - CACertificate
      - CACertificates
      - Cancel
      - Cardinality
      - Certificates
      - Claim
      - Code
      - Configurations
      - Confirm
      - Confirmation
      - Confirmdestination
      - Custom
      - Default
      - Demand
      - Deprecate
      - Describe
      - Destinations
      - Detach
      - Detect
      - Dimensions
      - Disable
      - Documents
      - Domains
      - Dynamic
      - Effective
      - Enable
      - Endpoints
      - Er
      - Ers
      - Events
      - Execution
      - Executions
      - Findings
      - Fleets
      - Groups
      - Index
      - Indexing
      - Indices
      - Invoke
      - Jobs
      - Keys
      - Levels
      - Logging
      - Managed
      - Metrics
      - Mitigation
      - Mitigation Actions
      - Models
      - Names
      - Numbers
      - OTAUpdate
      - OTAUpdates
      - 'On'
      - Options
      - Out
      - Outgoing
      - Packages
      - Percentiles
      - Policies
      - Principals
      - Profiles
      - Prov
      - Providers
      - Provisioning
      - Register
      - Registration Codes
      - Registrations
      - Reject
      - Related
      - Removes
      - Replace
      - Reports
      - Resources
      - Roles
      - Rules
      - Scheduled
      - Scheduled Audits
      - Search
      - Security
      - Sets
      - States
      - Statistics
      - Stop
      - Stream
      - Streams
      - Summaries
      - Suppressions
      - Tags
      - Targets
      - Tasks
      - Templates
      - Tests
      - Things
      - Tokens
      - Topics
      - Training
      - Transfers
      - Types
      - Untag
      - Validate
      - Values
      - Verification
      - Versions
      - Violations
    properties:
      - type: Documentation
        url: https://aws.amazon.com/iot/
      - type: OpenAPI
        url: properties/iot-openapi-original.yml
      - type: Customers
        url: https://aws.amazon.com/iot/customers/
      - type: News
        url: https://aws.amazon.com/iot/iot-events-partner-news/
      - type: Partners
        url: https://aws.amazon.com/iot/partner-solutions/
      - type: Solutions
        url: https://aws.amazon.com/iot/solutions/
      - type: Resources
        url: https://aws.amazon.com/iot/resources/
      - type: Blog
        url: https://aws.amazon.com/iot/blog/
      - type: Customers
        url: https://aws.amazon.com/iot/customers/
      - type: Edukit
        url: https://aws.amazon.com/iot/edukit/
    overlays:
      - type: APIs.io Search
        url: overlays/iot-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/iot-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:iot
  - name: AWS IoT Jobs
    description: >-
      AWS IoT Jobs is a service that allows you to create and manage a set of
      remote operations to be executed on devices connected to AWS IoT. These
      operations can include tasks such as downloading updates, installing
      firmware, rebooting devices, rotating certificates, and troubleshooting. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://docs.aws.amazon.com/iot/latest/developerguide/iot-jobs.html
    baseURL: https://example.com
    tags:
      - Executions
      - Jobs
      - Names
      - Next
      - Pending
      - Things
    properties:
      - type: Documentation
        url: https://example.com
      - type: OpenAPI
        url: properties/iot-jobs-data-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/iot-jobs-data-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/iot-jobs-data-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:iot-jobs-data
  - name: Amazon CloudWatch Internet Monitor
    description: >-
      Amazon CloudWatch Internet Monitor provides visibility into how internet
      issues impact the performance and availability between your applications
      hosted on Amazon Web Services and your end users. It can reduce the time
      it takes for you to diagnose internet issues from days to minutes. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: >-
      https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/CloudWatch-InternetMonitor.html
    baseURL: https://example.com
    tags:
      - ARN
      - Events
      - Health
      - Monitors
      - Names
      - Queries
      - Resources
      - Results
      - Status
      - Stop
      - Tags
      - Untag
    properties:
      - type: Documentation
        url: >-
          https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/CloudWatch-InternetMonitor.html
      - type: OpenAPI
        url: properties/internetmonitor-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/internetmonitor-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/internetmonitor-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:internetmonitor
  - name: AWS IoT Analytics
    description: >-
      IoT Analytics is a powerful tool designed to streamline the collection,
      processing, storage, and analysis of large amounts of device data. This
      API allows users to easily query and run sophisticated analytics on IoT
      data, enabling advanced exploration and visualization through integration
      with Jupyter Notebooks and Amazon QuickSight. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/iot-analytics/
    baseURL: https://example.com
    tags:
      - Activity
      - Batches
      - Cancel
      - Channels
      - Content
      - Contents
      - Data
      - Data Store
      - Datasets
      - Logging
      - Messages
      - Names
      - Options
      - Pipeline Activities
      - Pipelines
      - Reprocessing
      - Resources
      - Runs
      - Samples
      - Tags
      - Untag
    properties:
      - type: Documentation
        url: https://aws.amazon.com/iot-analytics/
      - type: OpenAPI
        url: properties/iotanalytics-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/iot-analytics/features/
      - type: Pricing
        url: https://aws.amazon.com/iot-analytics/pricing/
      - type: FAQ
        url: https://aws.amazon.com/iot-analytics/faq/
      - type: Resources
        url: https://aws.amazon.com/iot-analytics/resources/
      - type: Partners
        url: https://aws.amazon.com/iot-analytics/partners/
    overlays:
      - type: APIs.io Search
        url: overlays/iotanalytics-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/iotanalytics-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:iotanalytics
  - name: AWS IoT Core Device Advisor
    description: >-
      Amazon Web Services IoT Core Device Advisor is a cloud-based testing
      service designed to verify the functionality and security of IoT devices
      before deployment. It offers a range of pre-built tests to ensure reliable
      connectivity with Amazon Web Services IoT Core. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/iot-core/device-advisor/
    baseURL: https://example.com
    tags:
      - ARN
      - Definitions
      - Endpoints
      - Reports
      - Resources
      - Runs
      - Stop
      - Suites
      - Tags
      - Untag
    properties:
      - type: Documentation
        url: https://aws.amazon.com/iot-core/device-advisor/
      - type: OpenAPI
        url: properties/iotdeviceadvisor-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/iot-core/features/
      - type: Pricing
        url: https://aws.amazon.com/iot-core/pricing/
      - type: Getting Started
        url: https://aws.amazon.com/iot-core/getting-started/
      - type: Features
        url: https://aws.amazon.com/iot-core/faqs/
      - type: Customers
        url: https://aws.amazon.com/iot/customers/
    overlays:
      - type: APIs.io Search
        url: overlays/iotdeviceadvisor-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/iotdeviceadvisor-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:iotdeviceadvisor
  - name: ' AWS IoT 1-Click Projects'
    description: >-
      This API allows AWS IoT 1-Click devices to easily and securely connect to
      AWS IoT Core upon deployment, eliminating the need for manual certificate
      management.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/iot-1-click/
    baseURL: https://example.com
    tags:
      - ARN
      - Device
      - Devices
      - Disassociate
      - Names
      - Placements
      - Projects
      - Resources
      - Tags
      - Templates
      - Untag
    properties:
      - type: Documentation
        url: https://aws.amazon.com/iot-1-click/
      - type: OpenAPI
        url: properties/iot1click-projects-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/iot-1-click/features/
      - type: Pricing
        url: https://aws.amazon.com/iot-1-click/pricing/
      - type: Devices
        url: https://aws.amazon.com/iot-1-click/devices/
      - type: FAQ
        url: https://aws.amazon.com/iot-1-click/faq/
      - type: Features
        url: https://aws.amazon.com/iot-1-click/features/
    overlays:
      - type: APIs.io Search
        url: overlays/iot1click-projects-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/iot1click-projects-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:iot1click-projects
  - name: AWS IoT Events
    description: >-
      The IoT Events API allows you to track the status and performance of your
      equipment or device fleets, enabling you to detect failures or changes in
      operation and take appropriate actions. With IoT Events Data API, you can
      interact with detectors by sending inputs, listing detectors, and
      accessing or modifying their status. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/iot-events/
    baseURL: https://example.com
    tags:
      - Acknowledge
      - Alarm
      - Alarms
      - Batches
      - Describe
      - Detectors
      - Disable
      - Enable
      - Inputs
      - Keys
      - Messages
      - Models
      - Names
      - Reset
      - Snooze
      - Values
      - Events
      - IoT
    properties:
      - type: Documentation
        url: https://aws.amazon.com/iot-events/
      - type: OpenAPI
        url: properties/iotevents-data-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/iot-events/features/
      - type: Pricing
        url: https://aws.amazon.com/iot-events/pricing/
      - type: FAQ
        url: https://aws.amazon.com/iot-events/faqs/
      - type: Features
        url: https://aws.amazon.com/iot-events/features/
    overlays:
      - type: APIs.io Search
        url: overlays/iotevents-data-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/iotevents-data-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:iotevents-data
  - name: AWS IoT Device Management
    description: >-
      AWS IoT Device Management simplifies the process of registering,
      organizing, monitoring, and remotely managing IoT devices on a large
      scale. Seamlessly integrate with AWS IoT Core for cloud device
      connectivity and management, as well as with AWS IoT Device Defender for
      auditing and monitoring the security posture of your fleet.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/iot-device-management/
    baseURL: https://example.com
    tags:
      - Applications
      - ARN
      - Resources
      - Tags
      - Untag
      - Devices
    properties:
      - type: Documentation
        url: https://aws.amazon.com/iot-device-management/
      - type: OpenAPI
        url: properties/iotfleethub-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/iot-device-management/features/
      - type: Pricing
        url: https://aws.amazon.com/iot-device-management/pricing/
      - type: Resources
        url: https://aws.amazon.com/iot-device-management/resources/
      - type: FAQ
        url: https://aws.amazon.com/iot-device-management/faq/
    overlays:
      - type: APIs.io Search
        url: overlays/iotfleethub-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/iotfleethub-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:iotfleethub
  - name: AWS IoT Data
    description: >-
      This API, IoT data, facilitates secure communication between
      Internet-connected devices and the Amazon Web Services cloud. It acts as a
      broker for devices to publish messages via HTTP and manage shadows,
      persistent representations of the device state in the AWS cloud. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: >-
      https://docs.aws.amazon.com/iot/latest/apireference/API_Operations_AWS_IoT_Data_Plane.html
    baseURL: https://example.com
    tags:
      - Messages
      - Named
      - Names
      - Publish
      - Retained
      - Shadow
      - Shadows
      - Things
      - Topics
    properties:
      - type: Documentation
        url: >-
          https://docs.aws.amazon.com/iot/latest/apireference/API_Operations_AWS_IoT_Data_Plane.html
      - type: OpenAPI
        url: properties/iot-data-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/iot-data-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/iot-data-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:iot-data
  - name: AWS IoT 1-Click devices
    description: >-
      Manufacturing partners of AWS IoT 1-Click develop devices that
      effortlessly connect to the AWS Cloud upon unboxing. These supported
      devices come pre-provisioned with certificates during manufacturing,
      eliminating the need for writing firmware or device-specific code to
      utilize them.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/iot-1-click/devices/
    baseURL: https://example.com
    tags:
      - ARN
      - Claim
      - Claims
      - Code
      - Describe
      - Device
      - Devices
      - Events
      - Finalize
      - Initiate
      - Invoke
      - Methods
      - Resources
      - States
      - Tags
      - Unclaim
      - Untag
    properties:
      - type: Documentation
        url: https://aws.amazon.com/iot-1-click/devices/
      - type: OpenAPI
        url: properties/iot1click-devices-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/iot1click-devices-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/iot1click-devices-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:iot1click-devices
  - name: AWS oT Secure Tunneling
    description: >-
      This API, IoT Secure Tunneling, allows users to establish secure remote
      connections to devices deployed in the field. This is particularly useful
      for devices situated behind restricted firewalls at remote sites. With IoT
      Secure Tunneling, users can troubleshoot, perform configuration updates,
      and execute other operational tasks on these devices. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: >-
      https://docs.aws.amazon.com/iot/latest/developerguide/secure-tunneling.html
    baseURL: https://example.com
    tags:
      - Resources
      - Untag
    properties:
      - type: Documentation
        url: >-
          https://docs.aws.amazon.com/iot/latest/developerguide/secure-tunneling.html
      - type: OpenAPI
        url: properties/iotsecuretunneling-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/iotsecuretunneling-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/iotsecuretunneling-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:iotsecuretunneling
  - name: AWS IoT FleetWise
    description: >-
      The Amazon Web Services IoT FleetWise API is a comprehensive solution for
      efficiently gathering and transmitting vehicle data to the AWS cloud. This
      fully managed service allows users to standardize data models, regardless
      of communication systems in use, and set up rules for transferring only
      essential data to the cloud.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/iot-fleetwise/
    baseURL: https://example.com
    tags:
      - Vehicles
      - ' Fleets'
    properties:
      - type: Documentation
        url: https://aws.amazon.com/iot-fleetwise/
      - type: OpenAPI
        url: properties/iotfleetwise-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/iot-fleetwise/features/
      - type: Pricing
        url: https://aws.amazon.com/iot-fleetwise/pricing/
      - type: FAQ
        url: https://aws.amazon.com/iot-fleetwise/faqs/
      - type: Customers
        url: https://aws.amazon.com/iot-fleetwise/customers/
      - type: Partners
        url: https://aws.amazon.com/iot-fleetwise/partners/
    overlays:
      - type: APIs.io Search
        url: overlays/iotfleetwise-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/iotfleetwise-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:iotfleetwise
  - name: Amazon Interactive Video Service (IVS)
    description: >-
      The Amazon IVS API is a REST-compatible interface utilizing standard HTTP
      requests and an EventBridge event stream for responses. JSON format is
      used for both requests and responses, including error messages. This
      regional service is compatible with various Amazon IVS HTTPS endpoints
      across supported regions as detailed in the Amazon Web Services General
      Reference. API Request Parameters and URLs are case-sensitive. For a
      detailed account of documentation changes in each release, please refer to
      the Document History section.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/ivs/
    baseURL: https://example.com
    tags:
      - ARN
      - Batches
      - Channels
      - Configurations
      - Import
      - Keys
      - Metadata
      - Pairs
      - Playback
      - Policies
      - Recording
      - Resources
      - Restrictions
      - Revocations
      - Sessions
      - Stop
      - Stream
      - Streams
      - Tags
      - Untag
      - Videos
      - Viewers
    properties:
      - type: Documentation
        url: https://aws.amazon.com/ivs/
      - type: OpenAPI
        url: properties/ivs-openapi-original.yml
      - type: Pricing
        url: https://aws.amazon.com/ivs/pricing/
      - type: FAQ
        url: https://aws.amazon.com/ivs/faqs/
      - type: Features
        url: https://aws.amazon.com/ivs/features/
      - type: Resources
        url: https://aws.amazon.com/ivs/resources/
      - type: Blogs
        url: https://aws.amazon.com/ivs/blogs/
    overlays:
      - type: APIs.io Search
        url: overlays/ivs-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/ivs-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:ivs
  - name: AWS IoT Events
    description: >-
      With AWS IoT Events, you can effortlessly monitor your equipment or device
      fleets for any failures or operational changes, and automatically trigger
      actions in response to these events. The API provides operations to manage
      inputs and detector models, including creating, reading, updating, and
      deleting them, as well as listing their versions.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/iot-events/
    baseURL: https://example.com
    tags:
      - Alarm
      - Analysis
      - Describe
      - Detectors
      - Events
      - Inputs
      - Logging
      - Models
      - Names
      - Options
      - Resources
      - Results
      - Routings
      - Tags
      - Untag
      - Versions
    properties:
      - type: Documentation
        url: https://aws.amazon.com/iot-events/
      - type: OpenAPI
        url: properties/iotevents-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/iot-events/features/
      - type: Pricing
        url: https://aws.amazon.com/iot-events/pricing/
      - type: FAQ
        url: https://aws.amazon.com/iot-events/faqs/
      - type: Features
        url: https://aws.amazon.com/iot-events/features/
    overlays:
      - type: APIs.io Search
        url: overlays/iotevents-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/iotevents-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:iotevents
  - name: AWS IoT SiteWise
    description: >-
      Introducing the IoT SiteWise API, a powerful tool for connecting
      Industrial Internet of Things (IIoT) devices to the Amazon Web Services
      Cloud. Dive into the IoT SiteWise User Guide for further details and
      resources.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/iot-sitewise/
    baseURL: https://example.com
    tags:
      - Access
      - Accounts
      - Actions
      - Aggregates
      - Assets
      - Associate
      - Associated
      - Batches
      - Bulk
      - Capabilities
      - Composite
      - Compositions
      - Configurations
      - Dashboard
      - Dashboards
      - Default
      - Describe
      - Disassociate
      - Encryption
      - Execute
      - Execution
      - Gateways
      - Hierarchy
      - History
      - Import
      - Interpolated
      - Jobs
      - Latest
      - Logging
      - Models
      - Namespaces
      - Options
      - Policies
      - Portals
      - Projects
      - Properties
      - Queries
      - Relationships
      - Resources
      - Series
      - Storage
      - Tags
      - Time
      - Time Series
      - Untag
      - Value
      - Values
    properties:
      - type: Documentation
        url: https://aws.amazon.com/iot-sitewise/
      - type: OpenAPI
        url: properties/iotsitewise-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/iot-sitewise/features/
      - type: Pricing
        url: https://aws.amazon.com/iot-sitewise/pricing/
      - type: Resources
        url: https://aws.amazon.com/iot-sitewise/resources/
      - type: FAQ
        url: https://aws.amazon.com/iot-sitewise/faqs/
      - type: Customers
        url: https://aws.amazon.com/iot-sitewise/customers/
    overlays:
      - type: APIs.io Search
        url: overlays/iotsitewise-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/iotsitewise-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:iotsitewise
  - name: IoT TwinMaker
    description: >-
      IoT TwinMaker is a cutting-edge service that allows users to create
      accurate digital replicas, also known as digital twins, of physical
      systems. By integrating data from a variety of sources including sensors,
      cameras, and enterprise applications, users can generate detailed
      visualizations to effectively monitor the performance of their factories,
      buildings, or industrial plants. This real-time data can be utilized for
      operational monitoring, error detection, and troubleshooting purposes.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/iot-twinmaker/
    baseURL: https://example.com
    tags:
      - Batches
      - Cancel
      - Components
      - Entities
      - Execute
      - Execution
      - History
      - Jobs
      - Metadata
      - Plan
      - Pricing
      - Pricing Plans
      - Properties
      - Queries
      - Resources
      - Scenes
      - Sources
      - Sync
      - Tags
      - Transfers
      - Types
      - Untag
      - Value
      - Values
      - Workspaces
    properties:
      - type: Documentation
        url: https://aws.amazon.com/iot-twinmaker/
      - type: OpenAPI
        url: properties/iottwinmaker-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/iot-twinmaker/features/
      - type: Pricing
        url: https://aws.amazon.com/iot-twinmaker/pricing/
      - type: Resources
        url: https://aws.amazon.com/iot-twinmaker/resources/
      - type: FAQ
        url: https://aws.amazon.com/iot-twinmaker/faqs/
      - type: Customers
        url: https://aws.amazon.com/iot-twinmaker/customers/
      - type: Partners
        url: https://aws.amazon.com/iot-twinmaker/partners/
    overlays:
      - type: APIs.io Search
        url: overlays/iottwinmaker-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/iottwinmaker-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:iottwinmaker
  - name: Amazon IVS Chat
    description: >-
      The Amazon IVS Chat control-plane API allows you to create and manage
      resources for Amazon IVS Chat, and integrate with the Amazon IVS Chat
      Messaging API for real-time chat room interactions. This regional AWS
      service includes resources such as LoggingConfiguration and Room, which
      can be tagged for organization and access management.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/ivs/features/chat/
    baseURL: https://example.com
    tags:
      - ARN
      - Chat
      - Configurations
      - Disconnect
      - Events
      - Logging
      - Messages
      - Resources
      - Rooms
      - Send
      - Tags
      - Tokens
      - Untag
      - Users
    properties:
      - type: Documentation
        url: https://aws.amazon.com/ivs/features/chat/
      - type: OpenAPI
        url: properties/ivschat-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/ivschat-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/ivschat-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:ivschat
  - name: Amazon MSK
    description: >-
      Amazon Managed Streaming for Apache Kafka (Amazon MSK) simplifies the
      process of ingesting and processing real-time streaming data by offering a
      fully managed Apache Kafka service.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/msk/
    baseURL: https://example.com
    tags:
      - ARN
      - Bootstrap
      - Brokers
      - Clients
      - Clusters
      - Compatible
      - Configurations
      - Connections
      - Connectivity
      - Count
      - Describe
      - Info
      - Kafka
      - Monitoring
      - Nodes
      - Operation
      - Operations
      - Policies
      - Reboot
      - Replication
      - Replicators
      - Resources
      - Revisions
      - Secrets
      - Security
      - Storage
      - Tags
      - Types
      - Untag
      - VPC
      - Versions
    properties:
      - type: Documentation
        url: https://aws.amazon.com/msk/
      - type: OpenAPI
        url: properties/kafka-openapi-original.yml
      - type: Pricing
        url: https://aws.amazon.com/msk/pricing/
      - type: Getting-started
        url: https://aws.amazon.com/msk/getting-started/
      - type: Partners
        url: https://aws.amazon.com/msk/partners/
      - type: Customer-success
        url: https://aws.amazon.com/msk/customer-success/
      - type: Resources
        url: https://aws.amazon.com/msk/resources/
      - type: FAQ
        url: https://aws.amazon.com/msk/faqs/
      - type: Features
        url: https://aws.amazon.com/msk/features/
    overlays:
      - type: APIs.io Search
        url: overlays/kafka-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/kafka-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:kafka
  - name: Amazon Kendra
    description: >-
      Amazon Kendra is a sophisticated enterprise search tool that simplifies
      the process of searching through multiple content repositories by
      providing pre-installed connectors.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/kendra/
    baseURL: https://example.com
    tags:
      - Thesaurus
    properties:
      - type: Documentation
        url: https://aws.amazon.com/kendra/
      - type: OpenAPI
        url: properties/kendra-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/kendra/features/
      - type: Connectors
        url: https://aws.amazon.com/kendra/connectors/
      - type: Pricing
        url: https://aws.amazon.com/kendra/pricing/
      - type: Resources
        url: https://aws.amazon.com/kendra/resources/
      - type: FAQ
        url: https://aws.amazon.com/kendra/faqs/
      - type: Customers
        url: https://aws.amazon.com/kendra/customers/
    overlays:
      - type: APIs.io Search
        url: overlays/kendra-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/kendra-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:kendra
  - name: Amazon Keyspaces
    description: >-
      Amazon Keyspaces (for Apache Cassandra) is a managed, highly scalable, and
      reliable database service that is compatible with Apache Cassandra. This
      service makes it simple to migrate, operate, and expand Cassandra
      workloads within the Amazon Web Services Cloud environment. Users can
      easily create keyspaces and tables in Amazon Keyspaces with just a few
      clicks on the Amazon Web Services Management Console or through a few
      lines of code, without the need to set up any infrastructure or install
      software. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/keyspaces/
    baseURL: https://example.com
    tags:
      - Tables
      - KeySpaces
      - Cassandra
    properties:
      - type: Documentation
        url: https://aws.amazon.com/keyspaces/
      - type: OpenAPI
        url: properties/keyspaces-openapi-original.yml
      - type: Pricing
        url: https://aws.amazon.com/keyspaces/pricing/
      - type: FAQ
        url: https://aws.amazon.com/keyspaces/faqs/
      - type: Customers
        url: https://aws.amazon.com/keyspaces/customers/
      - type: Resources
        url: https://aws.amazon.com/keyspaces/resources/
      - type: Getting-started
        url: https://aws.amazon.com/keyspaces/getting-started/
      - type: Scaling-data
        url: https://aws.amazon.com/keyspaces/scaling-data/
      - type: Features
        url: https://aws.amazon.com/keyspaces/features/
      - type: Regions
        url: https://aws.amazon.com/keyspaces/multi-region-replication/
    overlays:
      - type: APIs.io Search
        url: overlays/keyspaces-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/keyspaces-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:keyspaces
  - name: AWS IoT Wireless
    description: >-
      The AWS IoT Wireless API allows for bi-directional communication between
      internet-connected wireless devices and the AWS Cloud. It supports
      onboarding of LoRaWAN and Sidewalk devices, which use the Low Power Wide
      Area Networking (LPWAN) protocol to communicate with AWS IoT. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://docs.aws.amazon.com/iot-wireless/
    baseURL: https://example.com
    tags:
      - Accounts
      - Analyzer
      - Associate
      - Bulk
      - Certificates
      - Configurations
      - Data
      - Definitions
      - Deregister
      - Destinations
      - Device
      - Devices
      - Disassociate
      - Endpoints
      - Estimates
      - Events
      - Firmware
      - Gateways
      - Groups
      - Import
      - Information
      - Levels
      - Logs
      - Multicast
      - Names
      - Networks
      - Partners
      - Positions
      - Profiles
      - Reset
      - Resources
      - Send
      - Services
      - Sessions
      - Single
      - Statistics
      - Tags
      - Tasks
      - Tests
      - Things
      - Types
      - Untag
      - Wireless
    properties:
      - type: Documentation
        url: https://docs.aws.amazon.com/iot-wireless/
      - type: OpenAPI
        url: properties/iotwireless-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/iotwireless-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/iotwireless-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:iotwireless
  - name: Amazon Kendra Intelligent Ranking
    description: >-
      Amazon Kendra Intelligent Ranking leverages the advanced semantic search
      capabilities of Amazon Kendra to intelligently re-prioritize the search
      results provided by a search service.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://docs.aws.amazon.com/kendra/latest/dg/intelligent-rerank.html
    baseURL: https://example.com
    tags:
      - Execution
      - Plan
      - Rescore
    properties:
      - type: Documentation
        url: https://docs.aws.amazon.com/kendra/latest/dg/intelligent-rerank.html
      - type: OpenAPI
        url: properties/kendra-ranking-openapi-original.yml
      - type: Pricing
        url: https://aws.amazon.com/kendra/intelligent-ranking-pricing/
    overlays:
      - type: APIs.io Search
        url: overlays/kendra-ranking-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/kendra-ranking-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:kendra-ranking
  - name: AWS Lambda
    description: >-
      This is the API Reference for AWS Lambda, a serverless computing service
      provided by Amazon Web Services. For a more in-depth understanding of AWS
      Lambda, please refer to the AWS Lambda Developer Guide. You can also visit
      "What is AWS Lambda" for a service overview and "AWS Lambda How it Works"
      in the AWS Lambda Developer Guide for detailed information on how the
      service functions.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/lambda/
    baseURL: https://example.com
    tags:
      - ARN
      - Accounts
      - Alias
      - Aliases
      - Async
      - Code
      - Concurrency
      - Configurations
      - Events
      - Functions
      - Invocations
      - Invoke
      - Layers
      - Management
      - Mapping
      - Names
      - Numbers
      - Permission
      - Policies
      - Provisioned
      - Publish
      - Removes
      - Resources
      - Responses
      - Runtime
      - Settings
      - Signing
      - Sources
      - Statements
      - Stream
      - Streaming
      - Tags
      - URL
      - Untag
      - Versions
    properties:
      - type: Documentation
        url: https://aws.amazon.com/lambda/
      - type: OpenAPI
        url: properties/lambda-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/lambda/features/
      - type: Pricing
        url: https://aws.amazon.com/lambda/pricing/
      - type: Getting Started
        url: https://aws.amazon.com/lambda/getting-started/
      - type: Resources
        url: https://aws.amazon.com/lambda/resources/
      - type: FAQ
        url: https://aws.amazon.com/lambda/faqs/
      - type: Partners
        url: https://aws.amazon.com/lambda/partners/
    overlays:
      - type: APIs.io Search
        url: overlays/lambda-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/lambda-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:lambda
  - name: Amazon Kinesis Data Streams
    description: >-
      The Amazon Kinesis Data Streams Service API Reference provides developers
      with access to a managed service that can dynamically scale for processing
      streaming big data in real-time.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/kinesis/data-streams/
    baseURL: https://example.com
    tags:
      - Mode
      - Stream
    properties:
      - type: Documentation
        url: https://aws.amazon.com/kinesis/data-streams/
      - type: OpenAPI
        url: properties/kinesis-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/kinesis/data-streams/features/
      - type: Pricing
        url: https://aws.amazon.com/kinesis/data-streams/pricing/
      - type: Getting-started
        url: https://aws.amazon.com/kinesis/data-streams/getting-started/
      - type: Customers
        url: https://aws.amazon.com/kinesis/data-streams/customers/
      - type: Integrations
        url: https://aws.amazon.com/kinesis/data-streams/integrations/
      - type: Resources
        url: https://aws.amazon.com/kinesis/data-streams/resources/
      - type: FAQ
        url: https://aws.amazon.com/kinesis/data-streams/faqs/
    overlays:
      - type: APIs.io Search
        url: overlays/kinesis-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/kinesis-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:kinesis
  - name: AWS Key Management Service
    description: >-
      The Key Management Service (KMS) API is an encryption and key management
      web service that allows you to programmatically call various operations.
      KMS has replaced the term customer master key (CMK) with KMS key, but the
      concept remains the same. Amazon Web Services provides SDKs for various
      programming languages and platforms to create programmatic access to KMS. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://example.com
    baseURL: https://example.com
    tags:
      - Verify
      - Keys
    properties:
      - type: Documentation
        url: https://aws.amazon.com/kms/
      - type: OpenAPI
        url: properties/kms-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/kms/features/
      - type: Pricing
        url: https://aws.amazon.com/kms/pricing/
      - type: Getting-started
        url: https://aws.amazon.com/kms/getting-started/
      - type: Resources
        url: https://aws.amazon.com/kms/resources/
      - type: FAQ
        url: https://aws.amazon.com/kms/faqs/
    overlays:
      - type: APIs.io Search
        url: overlays/kms-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/kms-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:kms
  - name: AWS Launch Wizard
    description: >-
      Launch Wizard is a tool that simplifies the process of sizing,
      configuring, and deploying Amazon Web Services resources for third party
      applications, including Microsoft SQL Server Always On and HANA based SAP
      systems. This streamlined approach eliminates the need for manual
      identification and provisioning of individual AWS resources.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/launchwizard/
    baseURL: https://example.com
    tags:
      - Deployments
      - Events
      - Patterns
      - Workloads
    properties:
      - type: Documentation
        url: https://aws.amazon.com/launchwizard/
      - type: OpenAPI
        url: properties/launch-wizard-openapi-original.yml
      - type: FAQ
        url: https://aws.amazon.com/launchwizard/faq/
    overlays:
      - type: APIs.io Search
        url: overlays/launch-wizard-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/launch-wizard-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:launch-wizard
  - name: Amazon Lex Build-Time Actions
    description: >-
      Build voice and text conversational interfaces with Amazon Lex API for
      AWS. These actions will allow you to easily create, update, and delete
      chatbots for both new and existing client applications.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://docs.aws.amazon.com/lex/latest/dg/API_Operations.html
    baseURL: https://example.com
    tags:
      - ARN
      - Alias
      - Aliases
      - Associations
      - Bot Name
      - Bots
      - Built In
      - Channels
      - Exports
      - Import
      - Imports
      - Intent
      - Intents
      - Migrations
      - Names
      - Resources
      - Signatures
      - Slot Types
      - Slots
      - Tags
      - Types
      - Untag
      - Users
      - Utterances
      - Versions
      - View
    properties:
      - type: Documentation
        url: https://docs.aws.amazon.com/lex/latest/dg/API_Operations.html
      - type: OpenAPI
        url: properties/lex-models-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/lex-models-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/lex-models-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:lex-models
  - name: AWS License Manager
    description: >-
      The License Manager API simplifies the management of software licenses for
      various vendors across numerous Amazon Web Services accounts and physical
      servers located on-premises.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/license-manager/
    baseURL: https://example.com
    tags:
      - Services
      - Settings
    properties:
      - type: Documentation
        url: https://aws.amazon.com/license-manager/
      - type: OpenAPI
        url: properties/license-manager-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/license-manager/features/
      - type: Pricing
        url: https://aws.amazon.com/license-manager/pricing/
      - type: Customers
        url: https://aws.amazon.com/license-manager/customers/
      - type: Resources
        url: https://aws.amazon.com/license-manager/resources/
      - type: FAQ
        url: https://aws.amazon.com/license-manager/faqs/
    overlays:
      - type: APIs.io Search
        url: overlays/license-manager-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/license-manager-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:license-manager
  - name: Amazon Lightsail
    description: >-
      The Amazon Lightsail API is a user-friendly platform that offers
      developers a simple way to leverage Amazon Web Services for building
      websites and web applications. It provides a wide range of essential
      features, including virtual private servers, container services, storage
      options, managed databases, and more, all at a cost-effective monthly
      rate. With the ability to manage resources through the Lightsail console,
      API, CLI, and SDKs, developers can easily launch and maintain their
      projects.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/lightsail/
    baseURL: https://example.com
    tags:
      - Databases
      - Parameters
      - Relational
    properties:
      - type: Documentation
        url: https://aws.amazon.com/lightsail/
      - type: OpenAPI
        url: properties/lightsail-openapi-original.yml
      - type: Pricing
        url: https://aws.amazon.com/lightsail/pricing/
      - type: Getting-started
        url: https://aws.amazon.com/lightsail/getting-started/
      - type: Resources
        url: https://aws.amazon.com/lightsail/resources/
      - type: FAQ
        url: https://aws.amazon.com/lightsail/faq/
      - type: Customers
        url: https://aws.amazon.com/lightsail/customers/
      - type: Features
        url: https://aws.amazon.com/lightsail/features/
      - type: Research
        url: https://aws.amazon.com/lightsail/research/
    overlays:
      - type: APIs.io Search
        url: overlays/lightsail-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/lightsail-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:lightsail
  - name: Amazon Lookout for Equipment
    description: >-
      Amazon Lookout for Equipment is a machine learning service that uses
      advanced analytics to identify anomalies in machines from sensor data for
      use in predictive maintenance.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/lookout-for-equipment/
    baseURL: https://example.com
    tags:
      - Retraining
      - Scheduler
    properties:
      - type: Documentation
        url: https://aws.amazon.com/lookout-for-equipment/
      - type: OpenAPI
        url: properties/lookoutequipment-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/lookout-for-equipment/features/
      - type: Pricing
        url: https://aws.amazon.com/lookout-for-equipment/pricing/
      - type: FAQ
        url: https://aws.amazon.com/lookout-for-equipment/faqs/
      - type: Resources
        url: https://aws.amazon.com/lookout-for-equipment/resources/
      - type: Customers
        url: https://aws.amazon.com/lookout-for-equipment/customers/
      - type: Partners
        url: https://aws.amazon.com/lookout-for-equipment/partners/
    overlays:
      - type: APIs.io Search
        url: overlays/lookoutequipment-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/lookoutequipment-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:lookoutequipment
  - name: AWS Lake Formation
    description: >-
      The AWS Lake Formation API streamlines data permissions management and
      facilitates seamless sharing within and outside your organization.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/lake-formation/
    baseURL: https://example.com
    tags:
      - Assume
      - Batches
      - Cancel
      - Cells
      - Center
      - Commit
      - Configurations
      - Credentials
      - Data
      - Databases
      - Decorated
      - Deregister
      - Describe
      - Effective
      - Extend
      - Filter
      - Formation
      - Glue
      - Grants
      - Identity
      - LFTag
      - LFTags
      - Lakes
      - Lftag
      - Objects
      - 'On'
      - Opt
      - Optimizers
      - Partition
      - Paths
      - Permissions
      - Planning
      - Queries
      - Register
      - Removes
      - Resources
      - Results
      - Revoke
      - Roles
      - SAML
      - Saml
      - Search
      - Settings
      - States
      - Statistics
      - Storage
      - Tables
      - Temporary
      - Transactions
      - Units
      - Work
    properties:
      - type: Documentation
        url: https://aws.amazon.com/lake-formation/
      - type: OpenAPI
        url: properties/lakeformation-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/lake-formation/features/
      - type: Pricing
        url: https://aws.amazon.com/lake-formation/pricing/
      - type: Resources
        url: https://aws.amazon.com/lake-formation/resources/
      - type: FAQ
        url: https://aws.amazon.com/lake-formation/faqs/
    overlays:
      - type: APIs.io Search
        url: overlays/lakeformation-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/lakeformation-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:lakeformation
  - name: Amazon CloudWatch Logs
    description: >-
      This API allows you to monitor, store, and access log files from EC2
      instances, CloudTrail, and other sources using Amazon CloudWatch Logs. You
      can retrieve log data through the CloudWatch console, AWS CLI, API, or
      SDK. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: >-
      https://docs.aws.amazon.com/AmazonCloudWatch/latest/logs/WhatIsCloudWatchLogs.html
    baseURL: https://example.com
    tags:
      - Anomaly
      - Detectors
      - Logs
    properties:
      - type: Documentation
        url: >-
          https://docs.aws.amazon.com/AmazonCloudWatch/latest/logs/WhatIsCloudWatchLogs.html
      - type: OpenAPI
        url: properties/logs-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/logs-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/logs-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:logs
  - name: Amazon Lookout for Metrics
    description: >-
      Amazon Lookout for Metrics, leverages machine learning technology to
      identify and explain abnormal patterns in business and operational
      datasets.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/lookout-for-metrics/
    baseURL: https://example.com
    tags:
      - ARN
      - Activate
      - Alerts
      - Anomaly
      - Configurations
      - Data
      - Deactivate
      - Describe
      - Detect
      - Detections
      - Detectors
      - Executions
      - Feedback
      - Groups
      - Metrics
      - Quality
      - Related
      - Resources
      - Samples
      - Series
      - Sets
      - Summaries
      - Tags
      - Tests
      - Time
      - Untag
    properties:
      - type: Documentation
        url: https://aws.amazon.com/lookout-for-metrics/
      - type: OpenAPI
        url: properties/lookoutmetrics-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/lookout-for-metrics/features/
      - type: Pricing
        url: https://aws.amazon.com/lookout-for-metrics/pricing/
      - type: Resources
        url: https://aws.amazon.com/lookout-for-metrics/resources/
      - type: FAQ
        url: https://aws.amazon.com/lookout-for-metrics/faqs/
      - type: Customers
        url: https://aws.amazon.com/lookout-for-metrics/customers/
    overlays:
      - type: APIs.io Search
        url: overlays/lookoutmetrics-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/lookoutmetrics-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:lookoutmetrics
  - name: Amazon Lookout for Vision
    description: >-
      The Amazon Lookout for Vision API offers details on actions, data types,
      parameters, and errors. This API allows users to detect visual defects in
      various industrial products with precision and efficiency. By utilizing
      computer vision technology, it can identify missing parts in products,
      damages in vehicles or structures, inconsistencies in manufacturing lines,
      and even tiny imperfections in items like silicon wafers or printed
      circuit boards. Lookout for Vision is a powerful tool for ensuring quality
      in production processes.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/lookout-for-vision/
    baseURL: https://example.com
    tags:
      - ARN
      - Anomalies
      - Datasets
      - Describe
      - Detect
      - Entries
      - Jobs
      - Model Packaging Jobs
      - Models
      - Names
      - Packaging
      - Projects
      - Resources
      - Stop
      - Tags
      - Types
      - Untag
      - Versions
    properties:
      - type: Documentation
        url: https://aws.amazon.com/lookout-for-vision/
      - type: OpenAPI
        url: properties/lookoutvision-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/lookout-for-vision/features/
      - type: Pricing
        url: https://aws.amazon.com/lookout-for-vision/pricing/
      - type: FAQ
        url: https://aws.amazon.com/lookout-for-vision/faqs/
      - type: Resources
        url: https://aws.amazon.com/lookout-for-vision/resources/
      - type: Partners
        url: https://aws.amazon.com/lookout-for-vision/partners/
      - type: Customers
        url: https://aws.amazon.com/lookout-for-vision/customers/
    overlays:
      - type: APIs.io Search
        url: overlays/lookoutvision-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/lookoutvision-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:lookoutvision
  - name: Amazon Machine Learning
    description: >-
      Amazon Machine Learning allows users to leverage machine learning
      capabilities at scale, offering a wide range of services, infrastructure,
      and deployment resources. Trusted by over 100,000 customers, from major
      corporations to new businesses, AWS machine learning services are used to
      tackle business challenges and foster innovation. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/ai/machine-learning/
    baseURL: https://example.com
    tags:
      - Machine Learning
      - Model
    properties:
      - type: Documentation
        url: https://aws.amazon.com/ai/machine-learning/
      - type: OpenAPI
        url: properties/machinelearning-openapi-original.yml
      - type: Infrastructure
        url: https://aws.amazon.com/ai/infrastructure/
      - type: Learn
        url: https://aws.amazon.com/machine-learning/learn/
      - type: Resources
        url: https://aws.amazon.com/ai/resources/
      - type: Use Cases
        url: https://aws.amazon.com/machine-learning/ai-use-cases/
      - type: Partners
        url: https://aws.amazon.com/machine-learning/partner-solutions/
    overlays:
      - type: APIs.io Search
        url: overlays/machinelearning-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/machinelearning-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:machinelearning
  - name: Amazon Macie
    description: >-
      Amazon Macie is a fully managed data security and data privacy service
      that uses machine learning and pattern matching to help you discover and
      protect your sensitive data in AWS. Macie automates the discovery of
      sensitive data, such as PII and intellectual property, to provide you with
      insight into the data that your organization stores in AWS. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/macie/
    baseURL: https://example.com
    tags:
      - ARN
      - Accept
      - Accounts
      - Administrative
      - Administrator
      - Allow
      - Artifacts
      - Automated
      - Availability
      - Batches
      - Buckets
      - Buckets
      - Classifications
      - Configurations
      - Count
      - Custom
      - Data
      - Data Source
      - Decline
      - Describe
      - Detections
      - Disassociate
      - Discovery
      - Entifiers
      - Exports
      - Filter
      - Filters
      - Findings
      - Findings Filter
      - Inspections
      - Invitation
      - Invitations
      - Jobs
      - Managed
      - Master
      - Members
      - Occurrences
      - Organizations
      - Profiles
      - Publication
      - Resources
      - Reveal
      - Samples
      - Scopes
      - Search
      - Sensitive
      - Sensitivity
      - Sessions
      - Statistics
      - Tags
      - Templates
      - Tests
      - Totals
      - Untag
      - Usage
    properties:
      - type: Documentation
        url: https://aws.amazon.com/macie/
      - type: OpenAPI
        url: properties/macie2-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/macie/features/
      - type: Pricing
        url: https://aws.amazon.com/macie/pricing/
      - type: Getting-started
        url: https://aws.amazon.com/macie/getting-started/
      - type: FAQ
        url: https://aws.amazon.com/macie/faq/
      - type: Resources
        url: https://aws.amazon.com/macie/resources/
    overlays:
      - type: APIs.io Search
        url: overlays/macie2-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/macie2-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:macie2
  - name: AWS Mainframe Modernization
    description: >-
      The Amazon Web Services Mainframe Modernization API offers a comprehensive
      suite of tools and support for seamlessly transitioning from mainframes to
      AWS managed runtime environments. It includes features for examining
      current mainframe applications, creating or enhancing applications with
      COBOL or PL/I, and setting up a streamlined automated process for
      continuous integration and delivery of the applications.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/mainframe-modernization/
    baseURL: https://example.com
    tags:
      - ARN
      - Applications
      - Batches
      - Cancel
      - Data
      - Datasets
      - Definitions
      - Deployments
      - Details
      - Engines
      - Environments
      - Execution
      - Executions
      - History
      - Import
      - Jobs
      - Names
      - Resources
      - Sets
      - Signed
      - Stop
      - Tags
      - Tasks
      - URL
      - Untag
      - Versions
    properties:
      - type: Documentation
        url: https://aws.amazon.com/mainframe-modernization/
      - type: OpenAPI
        url: properties/m2-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/mainframe-modernization/features/
      - type: Pricing
        url: https://aws.amazon.com/mainframe-modernization/pricing/
      - type: Resources
        url: https://aws.amazon.com/mainframe-modernization/resources/
      - type: FAQ
        url: https://aws.amazon.com/mainframe-modernization/faqs/
    overlays:
      - type: APIs.io Search
        url: overlays/m2-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/m2-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:m2
  - name: AWS Location
    description: >-
      Amazon Location Service makes it easy for developers to add location
      functionality, such as maps, points of interest, geocoding, routing,
      tracking, and geofencing, to their applications without sacrificing data
      security and user privacy.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/location/
    baseURL: https://example.com
    tags:
      - ARN
      - Associate
      - Batches
      - Calculate
      - Calculators
      - Collections
      - Consumer
      - Consumers
      - Descriptions
      - Device
      - Devices
      - Disassociate
      - Evaluate
      - File
      - Fonts
      - Geofences
      - Geofencing
      - Glyphs
      - History
      - Index
      - Indexes
      - Keys
      - Latest
      - Maps
      - Matrix
      - Metadata
      - Names
      - Places
      - Positions
      - Ranges
      - Resources
      - Routes
      - Search
      - Sprites
      - Stack
      - Styles
      - Suggestions
      - Tags
      - Text
      - Tiles
      - Trackers
      - Tracking
      - Unicode
      - Untag
    properties:
      - type: Documentation
        url: https://aws.amazon.com/location/
      - type: OpenAPI
        url: properties/location-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/location/features/
      - type: Pricing
        url: https://aws.amazon.com/location/pricing/
      - type: Getting-started
        url: https://aws.amazon.com/location/getting-started/
      - type: FAQ
        url: https://aws.amazon.com/location/faqs/
      - type: Customers
        url: https://aws.amazon.com/location/customers/
      - type: Data-providers
        url: https://aws.amazon.com/location/data-providers/
    overlays:
      - type: APIs.io Search
        url: overlays/location-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/location-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:location
  - name: AWS Marketplace Catalog
    description: >-
      The AWS Marketplace Catalog API enables users to interact with their
      entities, such as products or offers on AWS Marketplace, by providing
      functionality for listing, describing, and updating them. By integrating
      the AWS Marketplace Catalog API with product build or deployment
      pipelines, users can streamline the process of updating entities. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: >-
      https://docs.aws.amazon.com/marketplace-catalog/latest/api-reference/welcome.html
    baseURL: https://example.com
    tags:
      - Batches
      - Cancel
      - Change
      - Describe
      - Entities
      - Policies
      - Resources
      - Sets
      - Tags
      - Untag
    properties:
      - type: Documentation
        url: >-
          https://docs.aws.amazon.com/marketplace-catalog/latest/api-reference/welcome.html
      - type: OpenAPI
        url: properties/marketplace-catalog-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/marketplace-catalog-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/marketplace-catalog-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:marketplace-catalog
  - name: Amazon Managed Blockchain (AMB)
    description: >-
      The Amazon Managed Blockchain (AMB) Query API allows users to easily
      access multi-blockchain network data, enabling them to extract relevant
      information regarding blockchain activity. This API allows users to read
      data from public blockchain networks like Bitcoin Mainnet and Ethereum
      Mainnet, providing details such as current and historical balances of
      addresses, as well as a list of blockchain transactions within a specified
      time frame. Users can also retrieve specific transaction details,
      including transaction events, which can be further analyzed or
      incorporated into business logic for various applications.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/managed-blockchain/
    baseURL: https://example.com
    tags:
      - Assets
      - Balance
      - Balances
      - Batches
      - Blockchain
      - Contracts
      - Events
      - Tokens
      - Transactions
    properties:
      - type: Documentation
        url: https://aws.amazon.com/managed-blockchain/
      - type: OpenAPI
        url: properties/managedblockchain-query-openapi-original.yml
      - type: Getting-started
        url: https://aws.amazon.com/managed-blockchain/getting-started/
      - type: Pricing
        url: https://aws.amazon.com/managed-blockchain/pricing/
      - type: Resources
        url: https://aws.amazon.com/managed-blockchain/resources/
      - type: FAQ
        url: https://aws.amazon.com/managed-blockchain/faqs/
    overlays:
      - type: APIs.io Search
        url: overlays/managedblockchain-query-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/managedblockchain-query-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:managedblockchain-query
  - name: AWS Marketplace Deployment
    description: >-
      The AWS Marketplace Deployment Service supports the Quick Launch
      experience, which is a deployment option for software as a service (SaaS)
      products. Quick Launch simplifies and reduces the time, resources, and
      steps required to configure, deploy, and launch a products. The AWS
      Marketplace Deployment Service provides sellers with a secure method for
      passing deployment parameters (for example, API keys and external IDs) to
      buyers during the Quick Launch experience.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: >-
      https://docs.aws.amazon.com/marketplace-deployment/latest/api-reference/welcome.html
    baseURL: https://example.com
    tags:
      - ARN
      - Resources
      - Tags
      - Untag
      - Catalog
      - Catalogs
      - Deployments
      - Parameters
      - Products
    properties:
      - type: Documentation
        url: >-
          https://docs.aws.amazon.com/marketplace-deployment/latest/api-reference/welcome.html
      - type: OpenAPI
        url: properties/marketplace-deployment-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/marketplace-deployment-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/marketplace-deployment-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:marketplace-deployment
  - name: AWS Elemental MediaConnect
    description: >-
      AWS Elemental MediaConnect is an advanced live video transport service
      that combines the reliability and security of satellite and fiber-optic
      technology with the flexibility, agility, and cost-effectiveness of
      IP-based networks.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/mediaconnect/
    baseURL: https://example.com
    tags:
      - ARN
      - Bridges
      - Describe
      - Entitlements
      - Flows
      - Gateways
      - Grants
      - Instances
      - Interfaces
      - Media
      - Metadata
      - Names
      - Offerings
      - Output
      - Outputs
      - Purchase
      - Removes
      - Reservations
      - Resources
      - Sources
      - States
      - Stop
      - Stream
      - Streams
      - Tags
      - Untag
      - VPC
    properties:
      - type: Documentation
        url: https://aws.amazon.com/mediaconnect/
      - type: OpenAPI
        url: properties/mediaconnect-openapi-original.yml
      - type: Pricing
        url: https://aws.amazon.com/mediaconnect/pricing/
      - type: Getting-started
        url: https://aws.amazon.com/mediaconnect/getting-started/
      - type: FAQ
        url: https://aws.amazon.com/mediaconnect/faqs/
      - type: Ready
        url: https://aws.amazon.com/mediaconnect/ready/
      - type: Features
        url: https://aws.amazon.com/mediaconnect/features/
    overlays:
      - type: APIs.io Search
        url: overlays/mediaconnect-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/mediaconnect-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:mediaconnect
  - name: AWS Elemental MediaConvert
    description: >-
      AWS Elemental MediaConvert is a high-quality video transcoding service
      designed for creating live stream content for broadcast and multi-screen
      delivery on a large scale.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/mediaconvert/
    baseURL: https://example.com
    tags:
      - ARN
      - Associate
      - Certificates
      - Describe
      - Disassociate
      - Endpoints
      - Jobs
      - Names
      - Policies
      - Presets
      - Queues
      - Resources
      - Tags
      - Templates
      - Untag
    properties:
      - type: Documentation
        url: https://aws.amazon.com/mediaconvert/
      - type: OpenAPI
        url: properties/mediaconvert-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/mediaconvert/features/
      - type: Pricing
        url: https://aws.amazon.com/mediaconvert/pricing/
      - type: Getting-started
        url: https://aws.amazon.com/mediaconvert/getting-started/
      - type: Resources
        url: https://aws.amazon.com/mediaconvert/resources/
      - type: FAQ
        url: https://aws.amazon.com/mediaconvert/faqs/
    overlays:
      - type: APIs.io Search
        url: overlays/mediaconvert-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/mediaconvert-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:mediaconvert
  - name: AWS Elemental MediaLive
    description: >-
      AWS Elemental MediaLive is a professional live video processing service
      designed to produce high-quality streams for distribution to both
      broadcast televisions and internet-connected devices.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/medialive/
    baseURL: https://example.com
    tags:
      - ARN
      - Accept
      - Accounts
      - Batches
      - Cancel
      - Channels
      - Claim
      - Classes
      - Configurations
      - Data
      - Describe
      - Device
      - Devices
      - Groups
      - Inputs
      - Maintenance
      - Multiplex
      - Multiplexes
      - Names
      - Offerings
      - Partners
      - Program
      - Programs
      - Purchase
      - Reboot
      - Reject
      - Reservations
      - Resources
      - Schedules
      - Security
      - Stop
      - Tags
      - Thumbnails
      - Transfers
      - Window
    properties:
      - type: Documentation
        url: https://aws.amazon.com/medialive/
      - type: OpenAPI
        url: properties/medialive-openapi-original.yml
      - type: Pricing
        url: https://aws.amazon.com/medialive/pricing/
      - type: Getting-started
        url: https://aws.amazon.com/medialive/getting-started/
      - type: Resources
        url: https://aws.amazon.com/medialive/resources/
      - type: FAQ
        url: https://aws.amazon.com/medialive/faqs/
      - type: Features
        url: https://aws.amazon.com/medialive/features/
    overlays:
      - type: APIs.io Search
        url: overlays/medialive-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/medialive-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:medialive
  - name: AWS Marketplace Agreement
    description: >-
      The AWS Marketplace API enables sellers to manage product-related
      agreements, including listing, searching, and filtering agreements. To use
      this API, sellers must ensure that their AWS IAM policies and roles are
      properly configured. Users must have the necessary permissions to carry
      out actions such as describing agreements, getting agreement terms, and
      searching through all agreements.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: >-
      https://docs.aws.amazon.com/marketplace-agreements/latest/api-reference/welcome.html
    baseURL: https://example.com
    tags:
      - Agreements
      - Search
    properties:
      - type: Documentation
        url: >-
          https://docs.aws.amazon.com/marketplace-agreements/latest/api-reference/welcome.html
      - type: OpenAPI
        url: properties/marketplace-agreement-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/marketplace-agreement-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/marketplace-agreement-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:marketplace-agreement
  - name: AWS Marketplace
    description: >-
      The AWS Elemental MediaStore API is designed to provide high-performance
      storage specifically tailored for media content, offering reliable
      consistency and minimal latency to support the seamless delivery of live
      streaming video content.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/mediastore/
    baseURL: https://example.com
    tags:
      - Resources
      - Untag
    properties:
      - type: Documentation
        url: https://aws.amazon.com/mediastore/
      - type: OpenAPI
        url: properties/mediastore-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/mediastore/features/
      - type: Pricing
        url: https://aws.amazon.com/mediastore/pricing/
      - type: Getting-started
        url: https://aws.amazon.com/mediastore/getting-started/
      - type: Resources
        url: https://aws.amazon.com/mediastore/resources/
      - type: FAQ
        url: https://aws.amazon.com/mediastore/faqs/
    overlays:
      - type: APIs.io Search
        url: overlays/mediastore-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/mediastore-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:mediastore
  - name: AWS Marketplace Commerce Analytics Service
    description: >-
      The AWS Marketplace Commerce Analytics Service allows you to access
      product and customer data from AWS Marketplace through a programmable
      interface. Upon signing up for the service, you can retrieve usage,
      subscription, and billing reports using the AWS SDK.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: >-
      https://docs.aws.amazon.com/marketplace/latest/userguide/commerce-analytics-service.html
    baseURL: https://example.com
    tags:
      - Data
      - Exports
      - Support
    properties:
      - type: Documentation
        url: >-
          https://docs.aws.amazon.com/marketplace/latest/userguide/commerce-analytics-service.html
      - type: OpenAPI
        url: properties/marketplacecommerceanalytics-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/marketplacecommerceanalytics-openapi-search.yml
      - type: API Evangelist Ratings
        url: >-
          overlays/marketplacecommerceanalytics-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:marketplacecommerceanalytics
  - name: AWS Marketplace Metering Service
    description: >-
      The AWS Marketplace Metering Service API allows AWS Marketplace sellers to
      submit usage data for custom usage dimensions. This reference provides
      detailed descriptions of the low-level API functions available for use.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://docs.aws.amazon.com/marketplace/
    baseURL: https://example.com
    tags:
      - Customers
      - Resolve
    properties:
      - type: Documentation
        url: https://docs.aws.amazon.com/marketplace/
      - type: OpenAPI
        url: properties/meteringmarketplace-openapi-original.yml
      - type: Seller Guide
        url: https://docs.aws.amazon.com/marketplace/latest/userguide/index.html
      - type: Buyer Guide
        url: https://docs.aws.amazon.com/marketplace/latest/buyerguide/index.html
    overlays:
      - type: APIs.io Search
        url: overlays/meteringmarketplace-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/meteringmarketplace-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:meteringmarketplace
  - name: AWS Application Migration Service
    description: >-
      The AWS Application Migration Service streamlines the migration of your
      source servers to run directly on AWS, reducing the need for manual
      processes that are time-consuming and prone to errors. It also offers
      convenient optimization options for modernizing your applications, both
      through pre-built configurations and custom settings.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/application-migration-service/
    baseURL: https://example.com
    tags:
      - ARN
      - Accounts
      - Actions
      - Applications
      - Archive
      - Archived
      - Associate
      - Change
      - Clients
      - Configurations
      - Connectors
      - Cycle
      - Data
      - Describe
      - Disassociate
      - Disconnect
      - Errors
      - Exports
      - Finalize
      - Import
      - Imports
      - Initialize
      - Instances
      - Items
      - Jobs
      - Launch
      - Life
      - Logs
      - Managed
      - Mark
      - Pause
      - Removes
      - Replication
      - Resources
      - Resume
      - Retry
      - Servers
      - Services
      - Sources
      - States
      - Stop
      - Tags
      - Targets
      - Templates
      - Terminate
      - Tests
      - Types
      - Unarchive
      - Untag
      - Waves
    properties:
      - type: Documentation
        url: https://aws.amazon.com/application-migration-service/
      - type: OpenAPI
        url: properties/mgn-openapi-original.yml
      - type: Pricing
        url: https://aws.amazon.com/application-migration-service/pricing/
      - type: FAQ
        url: https://aws.amazon.com/application-migration-service/faqs/
      - type: Resources
        url: https://aws.amazon.com/application-migration-service/resources/
      - type: Windows
        url: https://aws.amazon.com/application-migration-service/windows/
    overlays:
      - type: APIs.io Search
        url: overlays/mgn-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/mgn-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:mgn
  - name: AWS HealthImaging
    description: >-
      The AWS HealthImaging API is a secure service that meets HIPAA compliance
      standards. It is specifically built to help healthcare providers and their
      medical imaging ISV partners effectively store, manipulate, and utilize
      machine learning techniques on medical images.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://example.com
    baseURL: https://example.com
    tags:
      - ARN
      - Copy
      - Data Store
      - Frames
      - Images
      - Jobs
      - Metadata
      - Resources
      - Search
      - Sets
      - Sources
      - Tags
      - Untag
      - Versions
    properties:
      - type: Documentation
        url: https://example.com
      - type: OpenAPI
        url: properties/medical-imaging-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/healthimaging/features/
      - type: Pricing
        url: https://aws.amazon.com/healthimaging/pricing/
      - type: FAQ
        url: https://aws.amazon.com/healthimaging/faqs/
      - type: Customers
        url: https://aws.amazon.com/healthimaging/customers/
      - type: Resources
        url: https://aws.amazon.com/healthimaging/resources/
    overlays:
      - type: APIs.io Search
        url: overlays/medical-imaging-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/medical-imaging-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:medical-imaging
  - name: Amazon Web Services Migration Hub Refactor Spaces
    description: >-
      Refactor Spaces within AWS Migration Hub serves as a comprehensive
      solution for gradually refactoring applications into microservices within
      the AWS ecosystem. By leveraging Refactor Spaces, users can seamlessly
      transition from monolithic to microservices architecture, minimizing the
      manual effort involved in setting up and managing AWS infrastructure. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: >-
      https://docs.aws.amazon.com/migrationhub-refactor-spaces/latest/userguide/what-is-mhub-refactor-spaces.html
    baseURL: https://example.com
    tags:
      - ARN
      - Applications
      - Environments
      - Policies
      - Resource Policies
      - Resources
      - Routes
      - Services
      - Tags
      - Untag
      - VPC
    properties:
      - type: Documentation
        url: >-
          https://docs.aws.amazon.com/migrationhub-refactor-spaces/latest/userguide/what-is-mhub-refactor-spaces.html
      - type: OpenAPI
        url: properties/migration-hub-refactor-spaces-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/migration-hub-refactor-spaces-openapi-search.yml
      - type: API Evangelist Ratings
        url: >-
          overlays/migration-hub-refactor-spaces-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:migration-hub-refactor-spaces
  - name: AWS MemoryDB
    description: >-
      MemoryDB for Redis is a managed in-memory database that offers fast
      performance and Multi-AZ durability for microservices applications. It
      stores the entire database in-memory for low latency and high throughput
      access. Compatible with Redis, it supports Redis' data structures, APIs,
      and commands.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/memorydb/
    baseURL: https://example.com
    tags:
      - Users
    properties:
      - type: Documentation
        url: https://aws.amazon.com/memorydb/
      - type: OpenAPI
        url: properties/memorydb-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/memorydb/features/
      - type: Pricing
        url: https://aws.amazon.com/memorydb/pricing/
      - type: Resources
        url: https://aws.amazon.com/memorydb/resources/
      - type: FAQ
        url: https://aws.amazon.com/memorydb/faqs/
      - type: Sla
        url: https://aws.amazon.com/memorydb/sla/
    overlays:
      - type: APIs.io Search
        url: overlays/memorydb-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/memorydb-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:memorydb
  - name: Migration Hub Strategy Recommendations
    description: >-
      AWS Migration Hub offers a centralized platform for monitoring migration
      tasks from various AWS tools and partner solutions. Through Migration Hub,
      users can select the migration tools that align with their requirements
      and gain insight into the progress of their migration projects.
      Additionally, Migration Hub delivers essential metrics and progress
      updates for specific applications, regardless of the tools employed for
      their migration.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://docs.aws.amazon.com/migrationhub/
    baseURL: https://example.com
    tags:
      - Analyzable
      - Application Components
      - Applications
      - Assessments
      - Collectors
      - Components
      - Configurations
      - Details
      - File
      - Generation
      - Import
      - Latest
      - Portfolio
      - Preferences
      - Recommendations
      - Reports
      - Servers
      - Stop
      - Strategies
      - Summaries
      - Tasks
    properties:
      - type: Documentation
        url: https://docs.aws.amazon.com/migrationhub/
      - type: OpenAPI
        url: properties/migrationhubstrategy-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/migrationhubstrategy-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/migrationhubstrategy-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:migrationhubstrategy
  - name: AWS Migration Hub Orchestrator.
    description: >-
      This API reference provides descriptions, syntax, and other details about
      each of the actions and data types for AWS Migration Hub Orchestrator. he
      topic for each action shows the API request parameters and the response.
      Alternatively, you can use one of the AWS SDKs to access an API that is
      tailored to the programming language or platform that you're using.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: >-
      https://docs.aws.amazon.com/migrationhub-orchestrator/latest/userguide/what-is-migrationhub-orchestrator.html
    baseURL: https://example.com
    tags:
      - ARN
      - Groups
      - Migration Workflow Templates
      - Migration Workflows
      - Plugins
      - Resources
      - Retry
      - Retry Workflow Steps
      - Step Groups
      - Steps
      - Stop
      - Tags
      - Template Steps
      - Templates
      - Templatestepgroups
      - Untag
      - Workflow Step
      - Workflow Step Group
      - Workflow Step Groups
      - Workflow Steps
      - Workflows
    properties:
      - type: Documentation
        url: >-
          https://docs.aws.amazon.com/migrationhub-orchestrator/latest/userguide/what-is-migrationhub-orchestrator.html
      - type: OpenAPI
        url: properties/migrationhuborchestrator-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/migrationhuborchestrator-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/migrationhuborchestrator-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:migrationhuborchestrator
  - name: AWS Elemental MediaTailor
    description: >-
      AWS Elemental MediaTailor is a versatile platform designed for video
      providers to easily create customized linear over-the-top (OTT) channels
      by leveraging their existing video content. With this service, users can
      seamlessly monetize their channels and live streams through personalized
      ad insertion, enhancing the overall viewing experience for audiences.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/mediatailor/
    baseURL: https://example.com
    tags:
      - ARN
      - Alerts
      - Channels
      - Configurations
      - Configure
      - Live
      - Locations
      - Logs
      - Names
      - Playback
      - Policies
      - Prefetch
      - Program
      - Resources
      - Schedules
      - Sources
      - Stop
      - Tags
      - Untag
    properties:
      - type: Documentation
        url: https://aws.amazon.com/mediatailor/
      - type: OpenAPI
        url: properties/mediatailor-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/mediatailor/features/
      - type: Pricing
        url: https://aws.amazon.com/mediatailor/pricing/
      - type: Getting-started
        url: https://aws.amazon.com/mediatailor/getting-started/
      - type: FAQ
        url: https://aws.amazon.com/mediatailor/faqs/
      - type: Resources
        url: https://aws.amazon.com/mediatailor/resources/
      - type: Integrations
        url: https://aws.amazon.com/mediatailor/integrations/
    overlays:
      - type: APIs.io Search
        url: overlays/mediatailor-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/mediatailor-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:mediatailor
  - name: Amazon Mechanical Turk
    description: >-
      This API, Amazon Mechanical Turk (MTurk), offers a platform for
      individuals and businesses to easily outsource tasks to a distributed
      workforce. These tasks can range from data validation and research to more
      subjective tasks like survey participation and content moderation. MTurk
      allows companies to leverage a global workforce to streamline processes,
      improve data collection and analysis, and enhance machine learning
      projects.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://www.mturk.com/
    baseURL: https://example.com
    tags:
      - Qualification
      - Types
    properties:
      - type: Documentation
        url: https://www.mturk.com/
      - type: OpenAPI
        url: properties/mturk-requester-openapi-original.yml
      - type: Worker
        url: https://www.mturk.com/worker
      - type: Product
        url: https://www.mturk.com/product-details
      - type: Pricing
        url: https://www.mturk.com/pricing
      - type: Help
        url: https://www.mturk.com/help
      - type: Resources
        url: https://www.mturk.com/resources
      - type: Customers
        url: https://www.mturk.com/customers
    overlays:
      - type: APIs.io Search
        url: overlays/mturk-requester-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/mturk-requester-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:mturk-requester
  - name: Amazon CloudWatch
    description: >+
      Amazon CloudWatch is a service that monitors applications, responds to
      performance changes, optimizes resource use, and provides insights into
      operational health. By collecting data across AWS resources, CloudWatch
      gives visibility into system-wide performance and allows users to set
      alarms, automatically react to changes, and gain a unified view of
      operational health.

    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/cloudwatch/
    baseURL: https://example.com
    tags:
      - Resources
      - Untag
    properties:
      - type: Documentation
        url: https://aws.amazon.com/cloudwatch/
      - type: OpenAPI
        url: properties/monitoring-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/cloudwatch/features/
      - type: Pricing
        url: https://aws.amazon.com/cloudwatch/pricing/
      - type: Getting Started
        url: https://aws.amazon.com/cloudwatch/getting-started/
      - type: FAQ
        url: https://aws.amazon.com/cloudwatch/faqs/
      - type: Customers
        url: https://aws.amazon.com/cloudwatch/customers/
    overlays:
      - type: APIs.io Search
        url: overlays/monitoring-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/monitoring-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:monitoring
  - name: Amazon Managed Workflows for Apache Airflow
    description: >-
      Amazon Managed Workflows for Apache Airflow (Amazon MWAA) is a service
      that helps you organize and automate your tasks by utilizing Directed
      Acyclic Graphs (DAGs) written in Python. Your DAGs, plugins, and Python
      requirements are stored in an Amazon Simple Storage Service (S3) bucket
      provided by you. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/managed-workflows-for-apache-airflow/
    baseURL: https://example.com
    tags:
      - ARN
      - CLI
      - Environments
      - Login
      - Metrics
      - Names
      - Publish
      - Resources
      - Tags
      - Tokens
      - Untag
      - Web
    properties:
      - type: Documentation
        url: https://aws.amazon.com/managed-workflows-for-apache-airflow/
      - type: OpenAPI
        url: properties/mwaa-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/managed-workflows-for-apache-airflow/features/
      - type: Pricing
        url: https://aws.amazon.com/managed-workflows-for-apache-airflow/pricing/
      - type: Getting-started
        url: >-
          https://aws.amazon.com/managed-workflows-for-apache-airflow/getting-started/
      - type: Resources
        url: https://aws.amazon.com/managed-workflows-for-apache-airflow/resources/
      - type: FAQ
        url: https://aws.amazon.com/managed-workflows-for-apache-airflow/faqs/
    overlays:
      - type: APIs.io Search
        url: overlays/mwaa-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/mwaa-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:mwaa
  - name: Amazon Neptune
    description: >-
      Amazon Neptune Amazon Neptune is a fast, reliable, fully-managed graph
      database service that makes it easy to build and run applications that
      work with highly connected datasets. The core of Amazon Neptune is a
      purpose-built, high-performance graph database engine optimized for
      storing billions of relationships and querying the graph with milliseconds
      latency.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/neptune/
    baseURL: https://example.com
    tags:
      - DBCluster
      - Stop
    properties:
      - type: Documentation
        url: https://aws.amazon.com/neptune/
      - type: OpenAPI
        url: properties/neptune-openapi-original.yml
      - type: Pricing
        url: https://aws.amazon.com/neptune/pricing/
      - type: FAQ
        url: https://aws.amazon.com/neptune/faqs/
      - type: Features
        url: https://aws.amazon.com/neptune/features/
      - type: Global-database
        url: https://aws.amazon.com/neptune/global-database/
      - type: Machine-learning
        url: https://aws.amazon.com/neptune/machine-learning/
      - type: Serverless
        url: https://aws.amazon.com/neptune/serverless/
      - type: Getting-started
        url: https://aws.amazon.com/neptune/getting-started/
    overlays:
      - type: APIs.io Search
        url: overlays/neptune-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/neptune-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:neptune
  - name: Amazon MQ
    description: >-
      Amazon MQ is an API service that manages message brokers for Apache
      ActiveMQ and RabbitMQ, simplifying the setup and operation of message
      brokers in the cloud. Message brokers enable communication between
      software applications and components, supporting multiple programming
      languages, operating systems, and messaging protocols.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/amazon-mq/
    baseURL: https://example.com
    tags:
      - Brokers
      - ActiveMQ
      - RabbitMQ
      - Real-Time
    properties:
      - type: Documentation
        url: https://aws.amazon.com/amazon-mq/
      - type: OpenAPI
        url: properties/mq-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/amazon-mq/features/
      - type: Pricing
        url: https://aws.amazon.com/amazon-mq/pricing/
      - type: Resources
        url: https://aws.amazon.com/amazon-mq/resources/
      - type: FAQ
        url: https://aws.amazon.com/amazon-mq/faqs/
      - type: Customers
        url: https://aws.amazon.com/amazon-mq/customers/
    overlays:
      - type: APIs.io Search
        url: overlays/mq-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/mq-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:mq
  - name: Neptune Analytics
    description: >-
      Neptune Analytics is a cutting-edge analytics database engine designed for
      Amazon Neptune, enabling users to efficiently analyze vast amounts of
      graph data. By leveraging high-speed processing capabilities and executing
      popular graph analytic algorithms through rapid queries, Neptune Analytics
      greatly accelerates the insights generation process, delivering analytics
      results within seconds.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: >-
      https://docs.aws.amazon.com/neptune-analytics/latest/userguide/what-is-neptune-analytics.html
    baseURL: https://example.com
    tags:
      - ARN
      - Endpoints
      - Graphs
      - Import
      - Import Tasks
      - Private
      - Queries
      - Resources
      - Restore
      - Snapshots
      - Summaries
      - Tags
      - Tasks
      - Untag
      - VPC
    properties:
      - type: Documentation
        url: >-
          https://docs.aws.amazon.com/neptune-analytics/latest/userguide/what-is-neptune-analytics.html
      - type: OpenAPI
        url: properties/neptune-graph-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/neptune-graph-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/neptune-graph-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:neptune-graph
  - name: Amazon Nimble Studio
    description: >-
      Thank you for visiting the Amazon Nimble Studio API documentation. This
      comprehensive reference guide offers detailed information on methods,
      schema, resources, and parameters to maximize your utilization of Nimble
      Studio. Nimble Studio is a cutting-edge virtual studio designed to support
      visual effects, animation, and interactive content teams, enabling them to
      create securely within a flexible, private cloud environment.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/nimble-studio/
    baseURL: https://example.com
    tags:
      - ARN
      - Acceptances
      - Backup
      - Backups
      - Components
      - Configurations
      - Details
      - EULA
      - Eulas
      - Images
      - Initialization
      - Initialize
      - Launch
      - Members
      - Memberships
      - Principals
      - Profiles
      - Repair
      - Resources
      - SSO
      - SSOConfiguration
      - Sessions
      - Stop
      - Stream
      - Streaming
      - Streams
      - Studios
      - Tags
      - Untag
    properties:
      - type: Documentation
        url: https://aws.amazon.com/nimble-studio/
      - type: OpenAPI
        url: properties/nimble-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/nimble-studio/features/
      - type: Pricing
        url: https://aws.amazon.com/nimble-studio/pricing/
      - type: Getting-started
        url: https://aws.amazon.com/nimble-studio/getting-started/
      - type: FAQ
        url: https://aws.amazon.com/nimble-studio/faqs/
    overlays:
      - type: APIs.io Search
        url: overlays/nimble-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/nimble-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:nimble
  - name: Amazon CloudWatch Network Monitor
    description: >-
      Amazon CloudWatch Network Monitor is an active network monitoring service
      provided by Amazon Web Services. It is designed to identify network issues
      within either the AWS network or your own company's network. With Network
      Monitor, users can select source VPCs and subnets from AWS and specify
      destination IP addresses from their own on-premises network. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://example.com
    baseURL: https://example.com
    tags:
      - ARN
      - Monitors
      - Names
      - Probes
      - Resources
      - Tags
      - Untag
    properties:
      - type: Documentation
        url: >-
          https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/what-is-network-monitor.html
      - type: OpenAPI
        url: properties/networkmonitor-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/networkmonitor-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/networkmonitor-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:networkmonitor
  - name: AWS HealthOmics
    description: >-
      AWS HealthOmics is a specialized platform designed to assist healthcare
      and life science organizations, as well as their software partners, in
      storing, retrieving, and analyzing various omics data including genomic
      and transcriptomic data. By leveraging this service, users can extract
      valuable insights from the data to enhance health outcomes. The platform
      also enables large-scale analysis and facilitates collaborative research
      efforts.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/healthomics/
    baseURL: https://example.com
    tags:
      - ARN
      - Abort
      - Activation
      - Activation Jobs
      - Annotations
      - Batches
      - Cancel
      - Complete
      - Export Jobs
      - Exports
      - Groups
      - Import
      - Import JObs
      - Import Jobs
      - Jobs
      - Metadata
      - Multipart
      - Names
      - Parts
      - Read
      - Readsets
      - Reference Store
      - References
      - Resources
      - Runs
      - Sequence
      - Sequence Stores
      - Sets
      - Share
      - Shares
      - Store
      - Stores
      - Tags
      - Tasks
      - Untag
      - Uploads
      - Variants
      - Versions
      - Workflows
    properties:
      - type: Documentation
        url: https://aws.amazon.com/healthomics/
      - type: OpenAPI
        url: properties/omics-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/healthomics/features/
      - type: Pricing
        url: https://aws.amazon.com/healthomics/pricing/
      - type: Resources
        url: https://aws.amazon.com/healthomics/resources/
      - type: FAQ
        url: https://aws.amazon.com/healthomics/faqs/
      - type: Customers
        url: https://aws.amazon.com/healthomics/customers/
    overlays:
      - type: APIs.io Search
        url: overlays/omics-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/omics-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:omics
  - name: Amazon CloudWatch Observability Access Manager
    description: >-
      Use Amazon CloudWatch Observability Access Manager to establish and manage
      connections between source accounts and monitoring accounts for CloudWatch
      cross-account observability. This feature allows you to effectively
      monitor and troubleshoot applications that span across multiple accounts
      within a specific region. With CloudWatch cross-account observability, you
      can seamlessly search, visualize, and analyze metrics, logs, traces, and
      Application Insights applications from linked accounts without any account
      limitations. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://docs.aws.amazon.com/OAM/latest/APIReference/Welcome.html
    baseURL: https://example.com
    tags:
      - ARN
      - Attached
      - Link
      - Links
      - Policies
      - Resources
      - Sink
      - Sinks
      - Tags
      - Untag
    properties:
      - type: Documentation
        url: https://example.com
      - type: OpenAPI
        url: properties/oam-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/oam-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/oam-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:oam
  - name: AWS Network Firewall
    description: >-
      Utilize AWS Network Firewall to establish customized firewall rules that
      offer precise management of network traffic and seamlessly implement
      firewall security measures across your VPCs.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://example.comhttps://aws.amazon.com/network-firewall/
    baseURL: https://example.com
    tags:
      - Configurations
      - TLSInspection
    properties:
      - type: Documentation
        url: https://aws.amazon.com/network-firewall/
      - type: OpenAPI
        url: properties/network-firewall-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/network-firewall/features/
      - type: Pricing
        url: https://aws.amazon.com/network-firewall/pricing/
      - type: Resources
        url: https://aws.amazon.com/network-firewall/resources/
      - type: FAQ
        url: https://aws.amazon.com/network-firewall/faqs/
      - type: Partners
        url: https://aws.amazon.com/network-firewall/partners/
      - type: Customers
        url: https://aws.amazon.com/network-firewall/customers/
    overlays:
      - type: APIs.io Search
        url: overlays/network-firewall-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/network-firewall-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:network-firewall
  - name: Amazon OpenSearch Serverless
    description: >-
      Use the Amazon OpenSearch Serverless API to create, configure, and manage
      OpenSearch Serverless collections and security policies. OpenSearch
      Serverless is an on-demand, pre-provisioned serverless configuration for
      Amazon OpenSearch Service. OpenSearch Serverless removes the operational
      complexities of provisioning, configuring, and tuning your OpenSearch
      clusters. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/opensearch-service/features/serverless/
    baseURL: https://example.com
    tags:
      - Endpoints
      - VPC
      - Search
      - Serverless
    properties:
      - type: Documentation
        url: https://aws.amazon.com/opensearch-service/features/serverless/
      - type: OpenAPI
        url: properties/opensearchserverless-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/opensearch-service/features/
      - type: Pricing
        url: https://aws.amazon.com/opensearch-service/pricing/
      - type: Getting Started
        url: https://aws.amazon.com/opensearch-service/getting-started/
      - type: Resources
        url: https://aws.amazon.com/opensearch-service/resources/
      - type: Customers
        url: https://aws.amazon.com/opensearch-service/customers/
      - type: Migrations
        url: https://aws.amazon.com/big-data/datalakes-and-analytics/migrations/
      - type: Partners
        url: >-
          https://aws.amazon.com/big-data/datalakes-and-analytics/partner-solutions/
      - type: Customers
        url: https://aws.amazon.com/big-data/datalakes-and-analytics/customers/
    overlays:
      - type: APIs.io Search
        url: overlays/opensearchserverless-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/opensearchserverless-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:opensearchserverless
  - name: Amazon OpenSearch Service
    description: >-
      Amazon OpenSearch Service makes it easy for you to perform interactive log
      analytics, real-time application monitoring, website search, and more.
      OpenSearch is an open source, distributed search and analytics suite
      derived from Elasticsearch. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/opensearch-service/
    baseURL: https://example.com
    tags:
      - Accept
      - Access
      - Actions
      - Associate
      - Authorize
      - Auto
      - Cancel
      - Change
      - Compatible
      - Configurations
      - Connections
      - Data
      - Describe
      - Details
      - Dissociate
      - Domains
      - Dry
      - Endpoints
      - Engines
      - Health
      - History
      - Inbound
      - Info
      - Instances
      - Limits
      - Maintenance
      - Maintenances
      - Names
      - Nodes
      - Offerings
      - Open Search
      - Outbound
      - Packages
      - Progress
      - Purchase
      - Reject
      - Removal
      - Removes
      - Reserved
      - Revoke
      - Runs
      - Scheduled
      - Search
      - Services
      - Software
      - Sources
      - Status
      - Tags
      - Tunes
      - Types
      - Upgrade
      - VPC
      - Versions
    properties:
      - type: Documentation
        url: https://aws.amazon.com/opensearch-service/
      - type: OpenAPI
        url: properties/opensearch-openapi-original.yml
      - type: Pricing
        url: https://aws.amazon.com/opensearch-service/pricing/
      - type: Partners
        url: https://aws.amazon.com/opensearch-service/partners/
      - type: FAQ
        url: https://aws.amazon.com/opensearch-service/faqs/
      - type: Getting-started
        url: https://aws.amazon.com/opensearch-service/getting-started/
      - type: Resources
        url: https://aws.amazon.com/opensearch-service/resources/
      - type: Customers
        url: https://aws.amazon.com/opensearch-service/customers/
      - type: Features
        url: https://aws.amazon.com/opensearch-service/features/
      - type: Migrations
        url: https://aws.amazon.com/opensearch-service/migrations/
    overlays:
      - type: APIs.io Search
        url: overlays/opensearch-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/opensearch-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:opensearch
  - name: AWS Organizations
    description: >-
      AWS Organizations simplifies the management of policies across multiple
      AWS accounts by providing a policy-based management system. This feature
      enables users to efficiently manage policies for groups of accounts and
      streamline the process of creating new accounts through automation.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/organizations/
    baseURL: https://example.com
    tags:
      - Policies
    properties:
      - type: Documentation
        url: https://aws.amazon.com/organizations/
      - type: OpenAPI
        url: properties/organizations-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/organizations/features/
      - type: Resources
        url: https://aws.amazon.com/organizations/resources/
      - type: Best Practices
        url: https://aws.amazon.com/organizations/getting-started/best-practices/
      - type: Resources
        url: https://aws.amazon.com/organizations/resources/
      - type: FAQ
        url: https://aws.amazon.com/organizations/faqs/
      - type: Customers
        url: https://aws.amazon.com/organizations/customers/
    overlays:
      - type: APIs.io Search
        url: overlays/organizations-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/organizations-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:organizations
  - name: AWS OpsWorks
    description: >-
      The API offered by AWS OpsWorks allows for seamless configuration
      management through the utilization of Chef and Puppet, powerful automation
      platforms that enable code-based automation of server configurations. With
      OpsWorks, users can leverage Chef and Puppet to automate the setup,
      deployment, and maintenance of servers within Amazon EC2 instances or
      on-premises compute environments. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/opsworks/
    baseURL: https://example.com
    tags:
      - Attributes
      - Engines
      - Servers
    properties:
      - type: Documentation
        url: https://aws.amazon.com/opsworks/
      - type: OpenAPI
        url: properties/opsworkscm-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/opsworkscm-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/opsworkscm-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:opsworkscm
  - name: Amazon OpenSearch Ingestion
    description: >-
      The Amazon OpenSearch Ingestion API is a fully managed, serverless data
      collection tool designed to deliver real-time log, metric, and trace data
      to Amazon OpenSearch Service domains and OpenSearch Serverless
      collections. With OpenSearch Ingestion, there is no longer a need for
      third-party solutions like Logstash or Jaeger to ingest data into your
      OpenSearch Service domains and OpenSearch Serverless collections. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: >-
      https://docs.aws.amazon.com/opensearch-service/latest/developerguide/ingestion.html
    baseURL: https://example.com
    tags:
      - Blueprints
      - Change
      - Names
      - Pipelines
      - Progress
      - Resources
      - Stop
      - Tags
      - Untag
      - Validate
    properties:
      - type: Documentation
        url: >-
          https://docs.aws.amazon.com/opensearch-service/latest/developerguide/ingestion.html
      - type: OpenAPI
        url: properties/osis-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/osis-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/osis-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:osis
  - name: AWS Panorama
    description: >-
      AWS Panorama is a set of machine learning (ML) tools and software
      development kit (SDK) that enables the integration of computer vision (CV)
      capabilities into on-site internet protocol (IP) cameras.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/panorama/
    baseURL: https://example.com
    tags:
      - ARN
      - Applications
      - Dependencies
      - Describe
      - Details
      - Device
      - Devices
      - Import
      - Instances
      - Jobs
      - Metadata
      - Nodes
      - Packages
      - Patch
      - Provision
      - Register
      - Removes
      - Resources
      - Signals
      - Tags
      - Templates
      - Untag
      - Versions
    properties:
      - type: Documentation
        url: https://aws.amazon.com/panorama/
      - type: OpenAPI
        url: properties/panorama-openapi-original.yml
      - type: Pricing
        url: https://aws.amazon.com/panorama/pricing/
      - type: Resources
        url: https://aws.amazon.com/panorama/resources/
      - type: FAQ
        url: https://aws.amazon.com/panorama/faqs/
      - type: Customers
        url: https://aws.amazon.com/panorama/customers/
      - type: Partners
        url: https://aws.amazon.com/panorama/partners/
      - type: Partners
        url: https://aws.amazon.com/panorama/partners/
      - type: Use-cases
        url: https://aws.amazon.com/panorama/use-cases/
      - type: Developers
        url: https://aws.amazon.com/panorama/developers/
      - type: Appliance
        url: https://aws.amazon.com/panorama/appliance/
    overlays:
      - type: APIs.io Search
        url: overlays/panorama-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/panorama-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:panorama
  - name: AWS Payment Cryptography Control Plane
    description: >-
      The Amazon Web Services Payment Cryptography Control Plane APIs are used
      to manage encryption keys for payment-related cryptographic operations.
      With these APIs, you can create, import, export, share, manage, and delete
      keys, as well as manage Identity and Access Management (IAM) policies. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://docs.aws.amazon.com/payment-cryptography/
    baseURL: https://example.com
    tags:
      - Alias
    properties:
      - type: Documentation
        url: https://docs.aws.amazon.com/payment-cryptography/
      - type: OpenAPI
        url: properties/payment-cryptography-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/payment-cryptography-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/payment-cryptography-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:payment-cryptography
  - name: AWS Private CA Connector for Active Directory
    description: >-
      The Amazon Web Services Private CA Connector for Active Directory
      establishes a connection between Amazon Web Services Private CA and Active
      Directory, allowing you to generate security certificates for Active
      Directory that are signed by your own private CA. For further details,
      visit the Amazon Web Services Private CA Connector for Active Directory
      documentation.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: >-
      https://docs.aws.amazon.com/privateca/latest/userguide/connector-for-ad.html
    baseURL: https://example.com
    tags:
      - ARN
      - Access
      - Connectors
      - Controls
      - Directory
      - Entries
      - Entry
      - Groups
      - Names
      - Principals
      - Registrations
      - Resources
      - Security
      - Services
      - Tags
      - Templates
      - Untag
    properties:
      - type: Documentation
        url: >-
          https://docs.aws.amazon.com/privateca/latest/userguide/connector-for-ad.html
      - type: OpenAPI
        url: properties/pca-connector-ad-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/pca-connector-ad-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/pca-connector-ad-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:pca-connector-ad
  - name: Amazon Personalize
    description: >-
      The Amazon Personalize API enables the consumption of real-time user event
      data, such as streaming or click data, for model training purposes. This
      data can be used on its own or in combination with historical data. For
      further details, refer to the documentation on Recording item interaction
      events.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: >-
      https://docs.aws.amazon.com/personalize/latest/dg/API_Types_Amazon_Personalize_Events.html
    baseURL: https://example.com
    tags:
      - Actions
      - Interactions
      - Events
      - Items
      - Users
    properties:
      - type: Documentation
        url: >-
          https://docs.aws.amazon.com/personalize/latest/dg/API_Types_Amazon_Personalize_Events.html
      - type: OpenAPI
        url: properties/personalize-events-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/personalize-events-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/personalize-events-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:personalize-events
  - name: 'AWS Cloud WAN Core Network '
    description: >-
      This API allows you to efficiently manage your Amazon Web Services Cloud
      WAN core network and Transit Gateway network across multiple AWS accounts,
      Regions, and on-premises locations.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: >-
      https://docs.aws.amazon.com/network-manager/latest/cloudwan/what-is-cloudwan.html
    baseURL: https://example.com
    tags:
      - Accept
      - Attachments
      - Associations
      - Connect
      - Global
      - Networks
      - Peer
      - Customers
      - Gateways
      - Link
      - Transit
      - Peers
      - Connections
      - Core
      - Devices
      - Describe
      - Links
      - Sites
      - VPN
      - Peerings
      - Routes
      - Tables
      - VPC
      - Policies
      - Versions
      - Device
      - ARN
      - Resources
      - Deregister
      - Registrations
      - Disassociate
      - Change
      - Execute
      - Sets
      - Events
      - Count
      - Counts
      - Relationships
      - Telemetry
      - Analysis
      - Register
      - Access
      - Organizations
      - Services
      - Tags
      - Untag
      - Reject
      - Restore
      - Metadata
    properties:
      - type: Documentation
        url: >-
          https://docs.aws.amazon.com/network-manager/latest/cloudwan/what-is-cloudwan.html
      - type: OpenAPI
        url: properties/networkmanager-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/networkmanager-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/networkmanager-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:networkmanager
  - name: AWS Outposts
    description: >-
      Amazon Web Services Outposts is a service that brings Amazon Web Services
      infrastructure, APIs, and tools to customer premises in a fully managed
      capacity. With Outposts, customers can access AWS managed infrastructure
      locally, allowing for the development and operation of applications on
      premises with the same programming interfaces as in AWS Regions.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/outposts/
    baseURL: https://example.com
    tags:
      - ARN
      - Addresses
      - Assets
      - Cancel
      - Catalog
      - Connections
      - Instances
      - Items
      - Orders
      - Outposts
      - Physical
      - Properties
      - Rack
      - Resources
      - Sites
      - Tags
      - Types
      - Untag
    properties:
      - type: Documentation
        url: https://aws.amazon.com/outposts/
      - type: OpenAPI
        url: properties/outposts-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/outposts-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/outposts-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:outposts
  - name: Amazon Personalize
    description: >-
      Amazon Personalize simplifies the process of integrating personalized
      recommendations powered by machine learning into various platforms,
      including websites, applications, and email marketing systems, thereby
      facilitating your digital transformation.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/personalize/
    baseURL: https://example.com
    tags:
      - Recommenders
    properties:
      - type: Documentation
        url: https://aws.amazon.com/personalize/
      - type: OpenAPI
        url: properties/personalize-openapi-original.yml
      - type: Featurs
        url: https://aws.amazon.com/personalize/features/
      - type: Pricing
        url: https://aws.amazon.com/personalize/pricing/
      - type: Resources
        url: https://aws.amazon.com/personalize/resources/
      - type: FAQ
        url: https://aws.amazon.com/personalize/faqs/
      - type: Customers
        url: https://aws.amazon.com/personalize/customers/
      - type: Partners
        url: https://aws.amazon.com/personalize/partners/
    overlays:
      - type: APIs.io Search
        url: overlays/personalize-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/personalize-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:personalize
  - name: Amazon Pinpoint Email
    description: >-
      The Amazon Pinpoint Email API is a specialized feature within the AWS
      service that allows businesses to connect with customers through email
      messaging. This API enhances the functionality of the Amazon Pinpoint
      platform, enabling users to send personalized email campaigns and track
      performance metrics.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: >-
      https://docs.aws.amazon.com/pinpoint-email/latest/APIReference/Welcome.html
    baseURL: https://example.com
    tags:
      - Accounts
      - Attributes
      - Blacklist
      - Campaigns
      - Configurations
      - DKIM
      - Dashboard
      - Dedicated
      - Deliverability
      - Deliveries
      - Destinations
      - Domains
      - Emails
      - Entities
      - Events
      - Feedback
      - IP
      - IP Addresses
      - Identities
      - Identity
      - Mail
      - Names
      - Options
      - Outbound
      - Pools
      - Reports
      - Reputation
      - Resources
      - Send
      - Sending
      - Sets
      - Statistics
      - Subscribed
      - Tags
      - Tests
      - Tracking
      - Untag
      - Warmup
    properties:
      - type: Documentation
        url: >-
          https://docs.aws.amazon.com/pinpoint-email/latest/APIReference/Welcome.html
      - type: OpenAPI
        url: properties/pinpoint-email-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/pinpoint-email-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/pinpoint-email-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:pinpoint-email
  - name: Amazon Pinpoint SMS and Voice
    description: >-
      The Amazon Pinpoint SMS and Voice, version 2 API allows developers to
      access specialized features for sending SMS messages and making voice
      calls, expanding upon the functionalities available in the Amazon Pinpoint
      API.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: >-
      https://docs.aws.amazon.com/pinpoint-sms-voice/latest/APIReference/welcome.html
    baseURL: https://example.com
    tags:
      - Destinations
      - Numbers
      - Verify
    properties:
      - type: Documentation
        url: >-
          https://docs.aws.amazon.com/pinpoint-sms-voice/latest/APIReference/welcome.html
      - type: OpenAPI
        url: properties/pinpoint-sms-voice-v2-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/pinpoint-sms-voice-v2-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/pinpoint-sms-voice-v2-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:pinpoint-sms-voice-v2
  - name: Amazon EventBridge Pipes
    description: >-
      The Amazon EventBridge Pipes API seamlessly connects event sources to
      targets, simplifying the development of event-driven architectures by
      eliminating the need for specialized knowledge and integration code. This
      tool ensures consistency across a company's applications by allowing any
      available EventBridge target to be used. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://docs.aws.amazon.com/eventbridge/latest/userguide/eb-pipes.html
    baseURL: https://example.com
    tags:
      - ARN
      - Names
      - Pipe
      - Pipes
      - Resources
      - Stop
      - Tags
      - Untag
    properties:
      - type: Documentation
        url: https://docs.aws.amazon.com/eventbridge/latest/userguide/eb-pipes.html
      - type: OpenAPI
        url: properties/pipes-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/pipes-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/pipes-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:pipes
  - name: AWS Proton
    description: >-
      The Proton Service API Reference provides detailed descriptions, syntax,
      and usage examples for the various actions and data types available within
      the Proton service. The API documentation includes Query API request
      parameters and XML responses for each action. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/proton/
    baseURL: https://example.com
    tags:
      - Configurations
      - Sync
      - Templates
    properties:
      - type: Documentation
        url: https://aws.amazon.com/proton/
      - type: OpenAPI
        url: properties/proton-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/proton/features/
      - type: Pricing
        url: https://aws.amazon.com/proton/pricing/
      - type: Getting-started
        url: https://aws.amazon.com/proton/getting-started/
      - type: FAQ
        url: https://aws.amazon.com/proton/faqs/
      - type: Partners
        url: https://aws.amazon.com/proton/partners/
      - type: Features
        url: https://aws.amazon.com/proton/features/
    overlays:
      - type: APIs.io Search
        url: overlays/proton-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/proton-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:proton
  - name: AWS Private 5G
    description: >-
      The Amazon Web Services Private 5G API offers a managed solution for
      setting up and expanding your private mobile network on-site. It includes
      pre-configured hardware and software, simplifies setup with automation,
      and allows for seamless scalability to accommodate more devices when
      necessary.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/private5g/
    baseURL: https://example.com
    tags:
      - ARN
      - Access
      - Acknowledge
      - Activate
      - Configure
      - Deactivate
      - Device
      - Entifiers
      - Networks
      - Orders
      - Ping
      - Plan
      - Points
      - Receipts
      - Resources
      - Sites
      - Tags
      - Untag
    properties:
      - type: Documentation
        url: https://aws.amazon.com/private5g/
      - type: OpenAPI
        url: properties/privatenetworks-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/private5g/features/
      - type: Pricing
        url: https://aws.amazon.com/private5g/pricing/
      - type: Getting-started
        url: https://aws.amazon.com/private5g/getting-started/
      - type: FAQ
        url: https://aws.amazon.com/private5g/faqs/
    overlays:
      - type: APIs.io Search
        url: overlays/privatenetworks-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/privatenetworks-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:privatenetworks
  - name: Amazon Polly
    description: >-
      Amazon Polly is a web service that makes it easy to synthesize speech from
      text. The Amazon Polly service provides API operations for synthesizing
      high-quality speech from plain text and Speech Synthesis Markup Language
      (SSML), along with managing pronunciations lexicons that enable you to get
      the best results for your application domain.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/polly/
    baseURL: https://example.com
    tags:
      - Describe
      - Lexicons
      - Names
      - Speech
      - Synthesis
      - Synthesize
      - Tasks
      - Voices
    properties:
      - type: Documentation
        url: https://aws.amazon.com/polly/
      - type: OpenAPI
        url: properties/polly-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/polly/features/
      - type: Pricing
        url: https://aws.amazon.com/polly/pricing/
      - type: Getting-started
        url: https://aws.amazon.com/polly/getting-started/
      - type: Resources
        url: https://aws.amazon.com/polly/resources/
      - type: Customers
        url: https://aws.amazon.com/polly/customers/
    overlays:
      - type: APIs.io Search
        url: overlays/polly-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/polly-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:polly
  - name: Amazon Q in Connect
    description: >-
      The Amazon Q in Connect API is an upgraded version of Amazon Connect
      Wisdom that utilizes generative AI to provide agents with suggested
      responses and actions to resolve customer inquiries quickly and enhance
      customer satisfaction. Instead of having knowledge articles, wikis, and
      FAQs scattered across various repositories, Amazon Q in Connect integrates
      them into one platform. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/connect/q/
    baseURL: https://example.com
    tags:
      - ARN
      - Assistants
      - Associations
      - Base
      - Bases
      - Content
      - Contents
      - Feedback
      - Import
      - Jobs
      - Knowledge
      - Notify
      - Queries
      - Received
      - Recommendations
      - Resources
      - Responses
      - Search
      - Sessions
      - Summaries
      - Tags
      - Templates
      - URI
      - Untag
      - Uploads
    properties:
      - type: Documentation
        url: https://aws.amazon.com/connect/q/
      - type: OpenAPI
        url: properties/qconnect-openapi-original.yml
      - type: Pricing
        url: https://aws.amazon.com/connect/pricing/
      - type: Getting Started
        url: https://aws.amazon.com/connect/getting-started/
      - type: Resources
        url: https://aws.amazon.com/connect/resources/
      - type: Customers
        url: https://aws.amazon.com/connect/customers/
      - type: Partners
        url: https://aws.amazon.com/connect/partners/
    overlays:
      - type: APIs.io Search
        url: overlays/qconnect-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/qconnect-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:qconnect
  - name: Amazon Q
    description: >-
      Amazon Q generates code, tests, debugs, and has multistep planning and
      reasoning capabilities that can transform and implement new code generated
      from developer requests. Amazon Q also makes it easier for employees to
      get answers to questions across business data—such as company policies,
      product information, business results, code base, employees, and many
      other topics—by connecting to enterprise data repositories to summarize
      the data logically, analyze trends, and engage in dialogue about the data.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/q/
    baseURL: https://example.com
    tags:
      - ARN
      - Applications
      - Batches
      - Chat
      - Chat Controls
      - Configurations
      - Controls
      - Conversations
      - Data
      - Data Source
      - Documents
      - Experience
      - Experiences
      - Feedback
      - Groups
      - Index
      - Indices
      - Jobs
      - Messages
      - Names
      - Plugins
      - Resources
      - Sources
      - Start Sync
      - Stop
      - Stopsync
      - Sync
      - Sync Jobs
      - Tags
      - Untag
      - Users
      - Web
    properties:
      - type: Documentation
        url: https://aws.amazon.com/q/
      - type: OpenAPI
        url: properties/qbusiness-openapi-original.yml
      - type: Getting Started
        url: https://aws.amazon.com/q/getting-started/
      - type: Customers
        url: https://aws.amazon.com/q/customers/
    overlays:
      - type: APIs.io Search
        url: overlays/qbusiness-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/qbusiness-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:qbusiness
  - name: Amazon RDS Performance Insights
    description: >-
      The Amazon RDS Performance Insights API allows you to monitor and analyze
      various aspects of database load by capturing data from a running DB
      instance. This guide provides detailed information on Performance Insights
      data types, parameters, and errors. With Performance Insights enabled, the
      API offers visibility into the performance of your DB instance. Amazon
      CloudWatch serves as the source for monitoring metrics, while Performance
      Insights provides a specialized view of DB load, measured in average
      active sessions. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/rds/performance-insights/
    baseURL: https://example.com
    tags:
      - Resources
      - Untag
    properties:
      - type: Documentation
        url: https://aws.amazon.com/rds/performance-insights/
      - type: OpenAPI
        url: properties/pi-openapi-original.yml
      - type: Pricing
        url: https://aws.amazon.com/rds/performance-insights/pricing/
      - type: FAQ
        url: https://aws.amazon.com/rds/performance-insights/faqs/
      - type: Customers
        url: https://aws.amazon.com/rds/performance-insights/customers/
    overlays:
      - type: APIs.io Search
        url: overlays/pi-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/pi-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:pi
  - name: AWS Price List
    description: >-
      The Amazon Web Services Price List API is a user-friendly tool that allows
      you to access Amazon Web Services' services, products, and pricing
      information through programmatic queries. The API utilizes standardized
      product attributes like Location, Storage Class, and Operating System, and
      provides pricing at the SKU level. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/pricing/
    baseURL: https://example.com
    tags:
      - Prices
    properties:
      - type: Documentation
        url: https://aws.amazon.com/pricing/
      - type: OpenAPI
        url: properties/pricing-openapi-original.yml
      - type: Cost-optimization
        url: https://aws.amazon.com/pricing/cost-optimization/
    overlays:
      - type: APIs.io Search
        url: overlays/pricing-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/pricing-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:pricing
  - name: Amazon QLDB
    description: >-
      The recommended way to interact with the transactional data APIs for
      Amazon QLDB is to use the QLDB driver or the QLDB shell for executing data
      transactions on a ledger. When working with an AWS SDK, it is advised to
      use the QLDB driver, which abstracts the data plane and manages
      SendCommand API calls.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/qldb/
    baseURL: https://example.com
    tags:
      - Command
      - Send
    properties:
      - type: Documentation
        url: https://aws.amazon.com/qldb/
      - type: OpenAPI
        url: properties/qldb-session-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/qldb/features/
      - type: Pricing
        url: https://aws.amazon.com/qldb/pricing/
      - type: Resources
        url: https://aws.amazon.com/qldb/resources/
      - type: FAQ
        url: https://aws.amazon.com/qldb/faqs/
      - type: Customers
        url: https://aws.amazon.com/qldb/customers/
    overlays:
      - type: APIs.io Search
        url: overlays/qldb-session-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/qldb-session-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:qldb-session
  - name: Resource Access Manager
    description: >-
      The Resource Access Manager API Reference is a comprehensive guide that
      details all actions and data types available in RAM. RAM is a service
      designed to facilitate secure resource sharing between different Amazon
      Web Services accounts. This documentation provides users with the
      necessary information to effectively utilize RAM's features, including the
      ability to share resources with entire Organizations or specific
      organizational units. Additionally, supported resource types can be shared
      with individual IAM roles and users. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/ram/
    baseURL: https://example.com
    tags:
      - Accept
      - Accept Resource Share Invitation
      - Associate
      - Associate Resource Share
      - Associate Resource Share Permission
      - Associations
      - Default
      - Disassociate
      - Disassociate Resource Share
      - Disassociate Resource Share Permissions
      - Enable
      - Enable Sharing
      - Invitation
      - Invitations
      - Organizations
      - Pending
      - Pending Invitation Resources
      - Permission
      - Permission Associations
      - Permission Verions
      - Permission Version
      - Permission Versions
      - Permissions
      - Policies
      - Principals
      - Promote
      - Promote Permission From Policy
      - Promote Resource Share From Policy
      - Reject
      - Reject Resource Share Invitations
      - Replace
      - Replace Permission Associations
      - Resource Policies
      - Resource Share
      - Resource Share Associations
      - Resource Share Invitations
      - Resource Share Permissions
      - Resource Shares
      - Resource Types
      - Resources
      - Set Default Permission Versions
      - Sets
      - Share
      - Shares
      - Sharing
      - Tag Resources
      - Tags
      - Types
      - Untag
      - Updateresourceshare
      - Versions
      - Work
    properties:
      - type: Documentation
        url: https://aws.amazon.com/ram/
      - type: OpenAPI
        url: properties/ram-openapi-original.yml
      - type: FAQ
        url: https://aws.amazon.com/ram/faqs/
    overlays:
      - type: APIs.io Search
        url: overlays/ram-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/ram-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:ram
  - name: AWS RDS
    description: >-
      The RDS Data API from Amazon RDS allows users to execute SQL statements on
      an Amazon Aurora DB cluster via an HTTP endpoint. This API is compatible
      with various types of Aurora databases, including Aurora PostgreSQL
      (Serverless v2, Serverless v1, and provisioned) and Aurora MySQL
      (Serverless v1). Detailed instructions on utilizing the Data API can be
      found in the Amazon Aurora User Guide.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/rds/
    baseURL: https://example.com
    tags:
      - Batches
      - Execute
      - Statements
      - Begins
      - Transactions
      - Commit
      - SQL
      - Rollback
    properties:
      - type: Documentation
        url: https://aws.amazon.com/rds/
      - type: OpenAPI
        url: properties/rds-data-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/rds/features/
      - type: Pricing
        url: https://aws.amazon.com/rds/pricing/
      - type: Resources
        url: https://aws.amazon.com/rds/resources/
      - type: FAQ
        url: https://aws.amazon.com/rds/faqs/
      - type: Customers
        url: https://aws.amazon.com/rds/customers/
      - type: Partners
        url: https://aws.amazon.com/rds/partners/
    overlays:
      - type: APIs.io Search
        url: overlays/rds-data-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/rds-data-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:rds-data
  - name: Amazon QuickSight
    description: >-
      Amazon QuickSight provides businesses with expansive and unified business
      intelligence solutions. Through modern interactive dashboards, paginated
      reports, natural language queries, and embedded analytics, all users can
      access reliable data to meet their analytical needs. With Amazon Q
      integration, business analysts and users can quickly build, discover, and
      share valuable insights using natural language, ultimately making informed
      decisions faster.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/quicksight/
    baseURL: https://example.com
    tags:
      - ARN
      - Accounts
      - Alias
      - Aliases
      - Analysis
      - Anonymous
      - Assets
      - Assignment
      - Assignments
      - Bundles
      - Configurations
      - Connections
      - Custom
      - Customizations
      - Dashboard
      - Dashboards
      - Data
      - Datasets
      - Definitions
      - Describe
      - Embed
      - Entities
      - Exports
      - Folders
      - Generate
      - Groups
      - IAM
      - IAMPolicy
      - IP
      - Identity
      - Import
      - Ingestions
      - Jobs
      - Linked
      - Links
      - Members
      - Memberships
      - Names
      - Namespaces
      - Numbers
      - Permission
      - Permissions
      - Policies
      - Principals
      - Propagation
      - Properties
      - Public
      - Published
      - Refresh
      - Register
      - Registered
      - Resolved
      - Resources
      - Restore
      - Restrictions
      - Results
      - Roles
      - Schedules
      - Search
      - Services
      - Sessions
      - Sets
      - Settings
      - Sharing
      - Snapshots
      - Sources
      - Subscriptions
      - Tags
      - Templates
      - Theme
      - Themes
      - Topics
      - Types
      - URL
      - Untag
      - Users
      - VPC
      - VPCConnection
      - VPCConnections
      - Versions
      - Vpcconnection
    properties:
      - type: Documentation
        url: https://aws.amazon.com/quicksight/
      - type: OpenAPI
        url: properties/quicksight-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/quicksight/features/
      - type: Gallery
        url: https://aws.amazon.com/quicksight/gallery/
      - type: Pricing
        url: https://aws.amazon.com/quicksight/pricing/
      - type: Customers
        url: https://aws.amazon.com/quicksight/customers/
      - type: Partners
        url: https://aws.amazon.com/quicksight/partners/
      - type: Blogs
        url: https://aws.amazon.com/quicksight/resources/blog/
      - type: Case Studies
        url: https://aws.amazon.com/quicksight/resources/case_studies/
      - type: Learning Resources
        url: https://aws.amazon.com/quicksight/resources/
      - type: FAQ
        url: https://aws.amazon.com/quicksight/resources/faqs/
    overlays:
      - type: APIs.io Search
        url: overlays/quicksight-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/quicksight-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:quicksight
  - name: Amazon Redshift
    description: >-
      Amazon Redshift is a comprehensive data warehouse solution offered by
      Amazon Web Services. This API reference provides documentation for the
      various programming and command line interfaces available for managing
      Amazon Redshift clusters. It is important to note that Amazon Redshift
      operates asynchronously, requiring techniques such as polling or
      asynchronous callback handlers to track the status of commands. The
      parameter descriptions in this reference specify whether a change takes
      effect immediately, upon the next instance reboot, or during the next
      maintenance window. Amazon Redshift handles tasks such as provisioning
      capacity, monitoring, backup, and applying patches and upgrades to the
      engine, allowing users to focus on leveraging their data for business
      insights.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/redshift/
    baseURL: https://example.com
    tags:
      - Partners
      - Status
    properties:
      - type: Documentation
        url: https://aws.amazon.com/redshift/
      - type: OpenAPI
        url: properties/redshift-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/redshift/features/
      - type: Pricing
        url: https://aws.amazon.com/redshift/pricing/
      - type: Customer Success
        url: https://aws.amazon.com/redshift/customer-success/
      - type: Solutions
        url: https://aws.amazon.com/redshift/solutions/
      - type: Resources
        url: https://aws.amazon.com/redshift/resources/
      - type: Getting Started
        url: https://aws.amazon.com/redshift/getting-started/
      - type: FAQ
        url: https://aws.amazon.com/redshift/faqs/
      - type: Migrations
        url: https://aws.amazon.com/big-data/datalakes-and-analytics/migrations/
      - type: Partners
        url: https://aws.amazon.com/redshift/partners/
    overlays:
      - type: APIs.io Search
        url: overlays/redshift-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/redshift-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:redshift
  - name: AWS Recycle Bin
    description: >-
      This is the API Reference for Recycle Bin, a feature that allows you to
      recover accidentally deleted snapshots and EBS-backed AMIs. The
      documentation provides detailed descriptions and syntax for each action
      and data type within Recycle Bin. When you use Recycle Bin, any deleted
      resources are stored in the bin for a specified time period. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://docs.aws.amazon.com/recyclebin/latest/APIReference/Welcome.html
    baseURL: https://example.com
    tags:
      - ARN
      - Locks
      - Resources
      - Rules
      - Tags
      - Unlock
      - Untag
    properties:
      - type: Documentation
        url: >-
          https://docs.aws.amazon.com/recyclebin/latest/APIReference/Welcome.html
      - type: OpenAPI
        url: properties/rbin-openapi-original.yml
      - type: User Guide
        url: https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/recycle-bin.html
      - type: Command Line Interface
        url: https://docs.aws.amazon.com/cli/latest/reference/rbin/index.html
    overlays:
      - type: APIs.io Search
        url: overlays/rbin-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/rbin-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:rbin
  - name: Amazon Redshift
    description: >-
      Utilize the Amazon Redshift Data API to execute queries on Amazon Redshift
      tables by running SQL statements. Successful statements will be committed.
      Refer to the Amazon Redshift Management Guide for further details on the
      Amazon Redshift Data API and CLI usage examples.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/redshift/
    baseURL: https://example.com
    tags:
      - Tables
      - Data
    properties:
      - type: Documentation
        url: https://aws.amazon.com/redshift/
      - type: OpenAPI
        url: properties/redshift-data-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/redshift/features/
      - type: Pricing
        url: https://aws.amazon.com/redshift/pricing/
      - type: Customer Success
        url: https://aws.amazon.com/redshift/customer-success/
      - type: Solutions
        url: https://aws.amazon.com/redshift/solutions/
    overlays:
      - type: APIs.io Search
        url: overlays/redshift-data-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/redshift-data-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:redshift-data
  - name: Amazon Rekognition
    description: >-
      The Amazon Rekognition API provides endpoints for Amazon Rekognition
      Image, Amazon Rekognition Custom Labels, Amazon Rekognition Stored Video,
      and Amazon Rekognition Streaming Video. The API includes actions such as
      detecting faces, labels, text, and celebrities, as well as functionalities
      for creating collections, comparing faces, analyzing video content, and
      managing datasets and projects. Common parameters and errors are also
      documented to assist developers in integrating this API into their
      applications.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/rekognition/
    baseURL: https://example.com
    tags:
      - Processor
      - Stream
      - Machine Learning
      - Videos
    properties:
      - type: Documentation
        url: https://aws.amazon.com/rekognition/
      - type: OpenAPI
        url: properties/rekognition-openapi-original.yml
      - type: Pricing
        url: https://aws.amazon.com/rekognition/pricing/
      - type: Resources
        url: https://aws.amazon.com/rekognition/resources/
      - type: FAQ
        url: https://aws.amazon.com/rekognition/faqs/
      - type: Customers
        url: https://aws.amazon.com/rekognition/customers/
    overlays:
      - type: APIs.io Search
        url: overlays/rekognition-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/rekognition-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:rekognition
  - name: Amazon Redshift Serverless
    description: >-
      This API reference provides documentation for an interface for managing
      Amazon Redshift Serverless. This service automatically adjusts data
      warehouse capacity and scales resources based on workload demands,
      delivering high performance and simplified operations. With Amazon
      Redshift Serverless, users can focus on utilizing their data to gain new
      insights for their business and customers.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/redshift/redshift-serverless/
    baseURL: https://example.com
    tags:
      - Workgroup
    properties:
      - type: Documentation
        url: https://aws.amazon.com/redshift/redshift-serverless/
      - type: OpenAPI
        url: properties/redshift-serverless-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/redshift/features/
      - type: Pricing
        url: https://aws.amazon.com/redshift/pricing/
      - type: Customer Success
        url: https://aws.amazon.com/redshift/customer-success/
      - type: Solutions
        url: https://aws.amazon.com/redshift/solutions/
    overlays:
      - type: APIs.io Search
        url: overlays/redshift-serverless-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/redshift-serverless-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:redshift-serverless
  - name: AWS Resource Explorer
    description: >-
      Amazon Web Services Resource Explorer is a search and discovery service
      that allows users to explore their resources using an internet search
      engine-like experience. Examples of resources that can be searched for
      include Amazon RDS instances, Amazon S3 buckets, and Amazon DynamoDB
      tables. Users can search for resources using metadata such as names, tags,
      and IDs. Resource Explorer can search across all AWS Regions in the user's
      account to simplify cross-Region workloads. By turning on Resource
      Explorer, users can scan and index resources in each Region, with the
      option to designate one Region as the aggregator index for the account.
      This aggregator index contains a copy of all resource information from all
      Regions where Resource Explorer is enabled. Users can access a
      comprehensive view of their resources across all indexed Regions in their
      account. For more information on enabling and configuring Resource
      Explorer, refer to the user guide provided by Amazon Web Services.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/resourceexplorer/
    baseURL: https://example.com
    tags:
      - ARN
      - Accounts
      - Associate
      - Batches
      - Configurations
      - Default
      - Disassociate
      - Index
      - Indexes
      - Levels
      - Members
      - Resources
      - Search
      - Services
      - Supported
      - Tags
      - Types
      - Untag
      - View
      - Views
    properties:
      - type: Documentation
        url: https://aws.amazon.com/resourceexplorer/
      - type: OpenAPI
        url: properties/resource-explorer-2-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/resourceexplorer/features/
      - type: Pricing
        url: https://aws.amazon.com/resourceexplorer/pricing/
      - type: FAQ
        url: https://aws.amazon.com/resourceexplorer/faqs/
    overlays:
      - type: APIs.io Search
        url: overlays/resource-explorer-2-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/resource-explorer-2-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:resource-explorer-2
  - name: AWS Resource Groups Tagging
    description: >-
      AWS supports tagging on all core infrastructure resources that incur
      charges. Most other AWS resources also support tagging. Some resources
      support tagging only through that service's native tagging operations, and
      don't yet support this API. See the documentation for an individual
      service for information about that service's native tagging operations.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: >-
      https://docs.aws.amazon.com/resourcegroupstagging/latest/APIReference/overview.html
    baseURL: https://example.com
    tags:
      - Resources
      - Untag
      - Tags
    properties:
      - type: Documentation
        url: >-
          https://docs.aws.amazon.com/resourcegroupstagging/latest/APIReference/overview.html
      - type: OpenAPI
        url: properties/resourcegroupstaggingapi-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/resourcegroupstaggingapi-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/resourcegroupstaggingapi-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:resourcegroupstaggingapi
  - name: AWS RoboMaker
    description: >-
      AWS RoboMaker is a cloud-based simulation service that enables robotics
      developers to run, scale, and automate simulation without managing any
      infrastructure.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/robomaker/
    baseURL: https://example.com
    tags:
      - ARN
      - Applications
      - Batches
      - Body
      - Cancel
      - Deployments
      - Deregister
      - Describe
      - Exports
      - Fleets
      - Generation
      - Jobs
      - Register
      - Resources
      - Restart
      - Robots
      - Simulations
      - Sync
      - Tags
      - Templates
      - Untag
      - Versions
      - Worlds
    properties:
      - type: Documentation
        url: https://aws.amazon.com/robomaker/
      - type: OpenAPI
        url: properties/robomaker-openapi-original.yml
      - type: Pricing
        url: https://aws.amazon.com/robomaker/pricing/
      - type: Resources
        url: https://aws.amazon.com/robomaker/resources/
      - type: FAQ
        url: https://aws.amazon.com/robomaker/faqs/
      - type: Customers
        url: https://aws.amazon.com/robomaker/customers/
    overlays:
      - type: APIs.io Search
        url: overlays/robomaker-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/robomaker-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:robomaker
  - name: AWS re:Post Private
    description: >-
      re:Post Private is a tailored version of AWS re:Post designed exclusively
      for enterprise customers with Enterprise Support or Enterprise On-Ramp
      Support plans. This platform grants access to a wealth of knowledge and
      expert guidance, enabling organizations to expedite their transition to
      the cloud and enhance developer productivity.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/repost-private/
    baseURL: https://example.com
    tags:
      - ARN
      - Administrative
      - Administrator
      - Invite
      - Invites
      - Register
      - Resources
      - Send
      - Space
      - Spaces
      - Tags
      - Untag
    properties:
      - type: Documentation
        url: https://aws.amazon.com/repost-private/
      - type: OpenAPI
        url: properties/repostspace-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/repost-private/features/
      - type: Pricing
        url: https://aws.amazon.com/repost-private/pricing/
      - type: FAQ
        url: https://aws.amazon.com/repost-private/faqs/
    overlays:
      - type: APIs.io Search
        url: overlays/repostspace-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/repostspace-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:repostspace
  - name: AWS Identity and Access Management Roles Anywhere
    description: >-
      The API for Identity and Access Management Roles Anywhere enables secure
      access for workloads running outside of Amazon Web Services to obtain
      temporary AWS credentials. By leveraging IAM policies and roles, workloads
      can access AWS resources without the need for long-term credentials
      management. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/iam/roles-anywhere/
    baseURL: https://example.com
    tags:
      - Anchor
      - Anchors
      - Disable
      - Enable
      - Notifications
      - Profiles
      - Reset
      - Resources
      - Settings
      - Subjects
      - Tags
      - Trust
      - Trust Anchors
      - Trustanchor
      - Untag
    properties:
      - type: Documentation
        url: https://aws.amazon.com/iam/roles-anywhere/
      - type: OpenAPI
        url: properties/rolesanywhere-openapi-original.yml
      - type: Resources
        url: https://aws.amazon.com/iam/roles-anywhere/resources/
    overlays:
      - type: APIs.io Search
        url: overlays/rolesanywhere-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/rolesanywhere-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:rolesanywhere
  - name: AWS Resource Groups
    description: >-
      The Resource Groups API allows users to effectively organize various
      Amazon Web Services resources, including instances from Amazon Elastic
      Compute Cloud, databases from Amazon Relational Database Service, and
      buckets from Amazon Simple Storage Service. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://docs.aws.amazon.com/ARG/latest/APIReference/Welcome.html
    baseURL: https://example.com
    tags:
      - ARN
      - Accounts
      - Configurations
      - Groups
      - Queries
      - Resources
      - Search
      - Settings
      - Tags
      - Ungroup
      - Untag
    properties:
      - type: Documentation
        url: https://docs.aws.amazon.com/ARG/latest/APIReference/Welcome.html
      - type: OpenAPI
        url: properties/resource-groups-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/resource-groups-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/resource-groups-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:resource-groups
  - name: AWS Routing Control
    description: >-
      Welcome to the API Reference Guide for the Routing Control (Recovery
      Cluster) feature in Amazon Route 53 Application Recovery Controller (ARC).
      With Route 53 ARC, you can utilize routing control to recover applications
      by redirecting traffic across different Availability Zones or Amazon Web
      Services Regions with high reliability. Routing controls act as simple
      on/off switches hosted on a highly available cluster within Route 53 ARC. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://docs.aws.amazon.com/r53recovery/latest/dg/routing-control.html
    baseURL: https://example.com
    tags:
      - Controls
      - Routing
      - States
    properties:
      - type: Documentation
        url: https://docs.aws.amazon.com/r53recovery/latest/dg/routing-control.html
      - type: OpenAPI
        url: properties/route53-recovery-cluster-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/route53-recovery-cluster-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/route53-recovery-cluster-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:route53-recovery-cluster
  - name: "Amazon Route\_53"
    description: >-
      Amazon Route 53, is a robust and reliable Domain Name System (DNS) web
      service that ensures high availability and scalability for connecting user
      requests to internet applications hosted on AWS or on-premises
      environments.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/route53/
    baseURL: https://example.com
    tags:
      - Accounts
      - Activate
      - Associate
      - Associate VPC
      - Authorization
      - Authorizers VPC Association
      - Blocks
      - CIDR
      - Change
      - Checker
      - Checker IP Ranges
      - Checks
      - Collections
      - Comments
      - Configurations
      - Count
      - DNS Security
      - DNSAnswer
      - DNSSEC
      - Deactivate
      - Deauthorize VPC Association
      - Delegation
      - Delegation Sets
      - Disable
      - Disassociate
      - Disassociate VPC
      - Enable
      - Failure
      - Geo
      - Geolocation
      - Health
      - Health Check
      - Hosted
      - Hosted Zone Count
      - Hosted Zones
      - Hostedzonelimit
      - IP
      - Instances
      - Key Signing
      - Keys
      - Last
      - Last Failure Reasons
      - Limits
      - Locations
      - Logging
      - Names
      - Policies
      - Queries
      - Query Logging Configurations
      - Ranges
      - Rblocks
      - Rcollection
      - Reasons
      - Record
      - Resources
      - Reusable
      - Sets
      - Signing
      - Status
      - Tags
      - Tests
      - Traffic
      - Traffic Policies
      - Traffic Policy Instance Count
      - Traffic Policy Instances
      - Types
      - VPC
      - VPCAssociation
      - VPCFrom
      - VPCWith
      - Versions
      - Zones
    properties:
      - type: Documentation
        url: https://aws.amazon.com/route53/
      - type: OpenAPI
        url: properties/route53-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/route53/features/
      - type: Pricing
        url: https://aws.amazon.com/route53/pricing/
      - type: Resources
        url: https://aws.amazon.com/route53/resources/
      - type: FAQ
        url: https://aws.amazon.com/route53/faqs/
    overlays:
      - type: APIs.io Search
        url: overlays/route53-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/route53-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:route53
  - name: Amazon Route 53 Application Recovery Controller
    description: >-
      The Amazon Route 53 Application Recovery Controller (Route 53 ARC) allows
      you to monitor the readiness of your applications and resources for
      recovery and facilitates traffic redirection between AWS Regions or away
      from Availability Zones to support application disaster recovery efforts.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://docs.aws.amazon.com/amazonarc/
    baseURL: https://example.com
    tags:
      - ARN
      - Accounts
      - Architecture
      - Authorization
      - Cell
      - Cellreadiness
      - Cells
      - Checks
      - Cross Account Authorizations
      - Groups
      - Names
      - Readiness
      - Readiness Checks
      - Recommendations
      - Recovery
      - Recovery Groups
      - Recoverygroupreadiness
      - Resource Sets
      - Resources
      - Rules
      - Sets
      - Status
      - Summaries
      - Tags
      - Untag
    properties:
      - type: Documentation
        url: https://docs.aws.amazon.com/amazonarc/
      - type: OpenAPI
        url: properties/route53-recovery-readiness-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/route53-recovery-readiness-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/route53-recovery-readiness-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:route53-recovery-readiness
  - name: AWS Resilience Hub
    description: >-
      Resilience Hub is an API designed to help you protect your Amazon Web
      Services applications by conducting continuous resiliency assessments and
      validations. Integrated into your software development pipeline, it
      proactively identifies and mitigates weaknesses in your applications,
      ensures RTO and RPO targets are met, and resolves potential issues before
      deployment to production.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/resilience-hub/
    baseURL: https://example.com
    tags:
      - ARN
      - Alarm
      - Applications
      - Assessments
      - Batches
      - Compliance
      - Components
      - Describe
      - Draft
      - Drifts
      - Import
      - Inputs
      - Mapping
      - Policies
      - Publish
      - Recommendations
      - Removes
      - Resiliency
      - Resolutions
      - Resolve
      - Resources
      - Sources
      - Status
      - Suggested
      - Tags
      - Templates
      - Tests
      - Unsupported
      - Untag
      - Versions
    properties:
      - type: Documentation
        url: https://aws.amazon.com/resilience-hub/
      - type: OpenAPI
        url: properties/resiliencehub-openapi-original.yml
      - type: Pricing
        url: https://aws.amazon.com/resilience-hub/pricing/
      - type: Resources
        url: https://aws.amazon.com/resilience-hub/resources/
    overlays:
      - type: APIs.io Search
        url: overlays/resiliencehub-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/resiliencehub-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:resiliencehub
  - name: Amazon Route 53 Domains
    description: >-
      The Amazon Route 53 API allows users to easily register domain names and
      carry out various related functions.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: >-
      https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/domain-register.html
    baseURL: https://example.com
    tags:
      - Billing
      - View
    properties:
      - type: Documentation
        url: >-
          https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/domain-register.html
      - type: OpenAPI
        url: properties/route53domains-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/route53domains-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/route53domains-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:route53domains
  - name: AWS route53 resolver
    description: >-
      Amazon Route 53 Resolver offers comprehensive functionalities for
      efficiently resolving DNS queries across AWS, the internet, and
      on-premises networks. It also enables secure management of DNS within your
      Amazon Virtual Private Cloud (VPC).
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/route53/resolver/
    baseURL: https://example.com
    tags:
      - Resolvers
      - Rules
    properties:
      - type: Documentation
        url: https://aws.amazon.com/route53/resolver/
      - type: OpenAPI
        url: properties/route53resolver-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/route53/features/
      - type: Pricing
        url: https://aws.amazon.com/route53/pricing/
      - type: Resources
        url: https://aws.amazon.com/route53/resources/
      - type: FAQ
        url: https://aws.amazon.com/route53/faqs/
    overlays:
      - type: APIs.io Search
        url: overlays/route53resolver-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/route53resolver-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:route53resolver
  - name: Amazon Lex
    description: >-
      Amazon Lex offers build and runtime endpoints, each with a specific set of
      operations. Your conversational bot utilizes the runtime API to interpret
      user input text or voice. For instance, if a user says "I want pizza," the
      bot sends this input to Amazon Lex via the runtime API. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/lex/
    baseURL: https://example.com
    tags:
      - Alias
      - Bots
      - Content
      - Conversational
      - Names
      - Posts
      - Sessions
      - Text
      - Users
    properties:
      - type: Documentation
        url: https://aws.amazon.com/lex/
      - type: OpenAPI
        url: properties/runtimelex-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/lex/features/
      - type: Pricing
        url: https://aws.amazon.com/lex/pricing/
      - type: FAQ
        url: https://aws.amazon.com/lex/faqs/
      - type: Getting Started
        url: https://aws.amazon.com/lex/getting-started/
      - type: Resources
        url: https://aws.amazon.com/lex/resources/
      - type: Customers
        url: https://aws.amazon.com/lex/customers/
    overlays:
      - type: APIs.io Search
        url: overlays/runtimelex-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/runtimelex-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:runtimelex
  - name: Amazon CloudWatch RUM
    description: >-
      With Amazon CloudWatch RUM, you can monitor real user activities to gather
      client-side information on your web application's performance from live
      user sessions. This data includes load times, errors, and user actions.
      View this data in aggregated form or broken down by browsers and devices
      used by customers. Use this data to quickly pinpoint and resolve
      client-side performance issues.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: >-
      https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/CloudWatch-RUM.html
    baseURL: https://example.com
    tags:
      - ARN
      - Application Monitors
      - Applications
      - Data
      - Definitions
      - Destinations
      - Events
      - Metric Destination
      - Metrics
      - Monitors
      - Names
      - Resources
      - Rummetrics
      - Tags
      - Untag
    properties:
      - type: Documentation
        url: >-
          https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/CloudWatch-RUM.html
      - type: OpenAPI
        url: properties/rum-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/rum-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/rum-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:rum
  - name: Amazon Route 53 Application Recovery Controller
    description: >-
      The Amazon Route 53 Application Recovery Controller provides monitoring
      and coordination for application recovery across AWS Regions and
      Availability Zones. By streamlining the recovery process and reducing
      manual steps, this tool helps ensure that applications and resources are
      prepared for recovery. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/route53/application-recovery-controller/
    baseURL: https://example.com
    tags:
      - ARN
      - Associated
      - Checks
      - Clusters
      - Control Panels
      - Controls
      - Describe
      - Panels
      - Policies
      - Resources
      - Routing
      - Routing Controls
      - Rules
      - Safety
      - Safety Rules
      - Tags
      - Untag
    properties:
      - type: Documentation
        url: https://aws.amazon.com/route53/application-recovery-controller/
      - type: OpenAPI
        url: properties/route53-recovery-control-config-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/route53-recovery-control-config-openapi-search.yml
      - type: API Evangelist Ratings
        url: >-
          overlays/route53-recovery-control-config-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:route53-recovery-control-config
  - name: 'AWS S3 Control '
    description: >-
      Amazon Web Services S3 Control, allows users to perform control plane
      actions on Amazon S3.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: >-
      https://docs.aws.amazon.com/AmazonS3/latest/API/API_Types_AWS_S3_Control.html
    baseURL: https://example.com
    tags:
      - ARN
      - Access
      - Access Grants Instances
      - Access Point
      - Async
      - Blocks
      - Buckets
      - Center
      - Configurations
      - Data
      - Data Access
      - Describe
      - Dissociate
      - Entitycenter
      - Grants
      - Grants""
      - Groups
      - Identity
      - Instances
      - Jobs
      - Lambda
      - Lens
      - Lifecycle
      - Lifecycle Configuration
      - Locations
      - Multi
      - Names
      - Objects
      - Operation
      - Points
      - Policies
      - Policy Status
      - Prefix
      - Priorities
      - Public
      - Regional
      - Regions
      - Replication
      - Resource Policies
      - Resources
      - Routes
      - Status
      - Storage
      - Storage Lens
      - Storage Lens Groups
      - Submit
      - Tagging
      - Tags
      - Tokens
      - Untag
      - Versioning
    properties:
      - type: Documentation
        url: >-
          https://docs.aws.amazon.com/AmazonS3/latest/API/API_Types_AWS_S3_Control.html
      - type: OpenAPI
        url: properties/s3control-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/s3control-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/s3control-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:s3control
  - name: Amazon Augmented AI
    description: >-
      Amazon Augmented AI (Amazon A2I) enhances machine learning applications by
      incorporating human judgment when necessary. Human reviewers can step in
      when an AI application is unable to assess data confidently, through a
      process known as a human review workflow. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/augmented-ai/
    baseURL: https://example.com
    tags:
      - Describe
      - Human
      - Loops
      - Names
      - Stop
    properties:
      - type: Documentation
        url: https://aws.amazon.com/augmented-ai/
      - type: OpenAPI
        url: properties/sagemaker-a2i-runtime-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/augmented-ai/features/
      - type: Pricing
        url: https://aws.amazon.com/augmented-ai/pricing/
      - type: Resources
        url: https://aws.amazon.com/augmented-ai/resources/
      - type: FAQ
        url: https://aws.amazon.com/augmented-ai/faqs/
      - type: Customers
        url: https://aws.amazon.com/augmented-ai/customers/
    overlays:
      - type: APIs.io Search
        url: overlays/sagemaker-a2i-runtime-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/sagemaker-a2i-runtime-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:sagemaker-a2i-runtime
  - name: AWS SageMaker
    description: >-
      Amazon SageMaker is a fully managed service that provides a comprehensive
      set of tools for high-performance, cost-effective machine learning (ML)
      for any scenario. With SageMaker, you can create, train, and deploy ML
      models at scale using various tools like notebooks, debuggers, profilers,
      pipelines, MLOps, and more within a single integrated development
      environment (IDE).
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/sagemaker/
    baseURL: https://example.com
    tags:
      - Workteam
    properties:
      - type: Documentation
        url: https://aws.amazon.com/sagemaker/
      - type: OpenAPI
        url: properties/sagemaker-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/sagemaker/features/
      - type: Pricing
        url: https://aws.amazon.com/sagemaker/pricing/
      - type: FAQ
        url: https://aws.amazon.com/sagemaker/faqs/
      - type: Getting Started
        url: https://aws.amazon.com/sagemaker/getting-started/
      - type: Resources
        url: https://aws.amazon.com/sagemaker/resources/
      - type: Partners
        url: https://aws.amazon.com/sagemaker/partners/
      - type: Customers
        url: https://aws.amazon.com/sagemaker/customers/
    overlays:
      - type: APIs.io Search
        url: overlays/sagemaker-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/sagemaker-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:sagemaker
  - name: AWS S3
    description: >-
      The API for Amazon Simple Storage Service (Amazon S3) provides an object
      storage solution with top-notch scalability, data availability, security,
      and performance. It caters to customers of varying sizes and industries,
      offering the ability to store and secure any volume of data for a wide
      range of purposes, including data lakes, cloud-native applications, and
      mobile apps. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/s3/
    baseURL: https://example.com
    tags:
      - ACL
      - Accelerate
      - Access
      - Analytics
      - Attributes
      - Blocks
      - Buckets
      - Buckets
      - CORS
      - Configurations
      - Content
      - Controls
      - Copy
      - Directory
      - Encryption
      - Hold
      - Intelligent
      - Inventory
      - Key&select
      - Key+?acl
      - Key+?attributes
      - Key+?legal
      - Key+?restore
      - Key+?retention
      - Key+?tagging
      - Key+?torrent
      - Keys
      - Legal
      - Lifecycle
      - Locations
      - Locks
      - Logging
      - Metrics
      - Multipart
      - Notifications
      - Objects
      - Ownership
      - Payments
      - Policies
      - Public
      - Replication
      - Responses
      - Restore
      - Retention
      - Sessions
      - Status
      - Tagging
      - Tiering
      - Torrent
      - Types
      - Uploads
      - Versioning
      - Versions
      - Websites
      - Write
    properties:
      - type: Documentation
        url: https://aws.amazon.com/s3/
      - type: OpenAPI
        url: properties/s3-openapi-original.yml
      - type: Pricing
        url: https://aws.amazon.com/s3/pricing/
      - type: Security
        url: https://aws.amazon.com/s3/security/
      - type: FAQ
        url: https://aws.amazon.com/s3/faqs/
      - type: Features
        url: https://aws.amazon.com/s3/features/
      - type: Getting-started
        url: https://aws.amazon.com/s3/getting-started/
      - type: Videos
        url: https://aws.amazon.com/s3/videos/
      - type: Customers
        url: https://aws.amazon.com/s3/customers/
      - type: Resources
        url: https://aws.amazon.com/s3/resources/
    overlays:
      - type: APIs.io Search
        url: overlays/s3-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/s3-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:s3
  - name: AWS SageMaker Edge
    description: >-
      The API for Amazon SageMaker Edge Manager
      (aws.greengrass.SageMakerEdgeManager) facilitates the installation of the
      SageMaker Edge Manager agent binary. This component enables edge device
      model management, allowing users to optimize, secure, monitor, and
      maintain machine learning models across fleets of edge devices. The
      SageMaker Edge Manager component takes care of installing and managing the
      SageMaker Edge Manager agent lifecycle on the core device. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: >-
      https://docs.aws.amazon.com/greengrass/v2/developerguide/sagemaker-edge-manager-component.html
    baseURL: https://example.com
    tags:
      - Deployments
      - Device
      - Registrations
      - Heart Beats
      - Send
    properties:
      - type: Documentation
        url: >-
          https://docs.aws.amazon.com/greengrass/v2/developerguide/sagemaker-edge-manager-component.html
      - type: OpenAPI
        url: properties/sagemaker-edge-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/sagemaker-edge-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/sagemaker-edge-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:sagemaker-edge
  - name: Amazon SageMaker Feature Store
    description: >-
      The Amazon SageMaker Feature Store is a fully managed repository
      specifically designed for storing, sharing, and managing features for
      machine learning (ML) models. Features are the inputs necessary for ML
      models during both training and inference. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/sagemaker/feature-store/
    baseURL: https://example.com
    tags:
      - Batches
      - Record
      - Feature
      - Groups
      - Names
      - Machine Learning
    properties:
      - type: Documentation
        url: https://aws.amazon.com/sagemaker/feature-store/
      - type: OpenAPI
        url: properties/sagemaker-featurestore-runtime-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/sagemaker-featurestore-runtime-openapi-search.yml
      - type: API Evangelist Ratings
        url: >-
          overlays/sagemaker-featurestore-runtime-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:sagemaker-featurestore-runtime
  - name: Amazon S3 on Outposts
    description: >-
      Amazon S3 on Outposts delivers object storage to your on-premises AWS
      Outposts environment to meet local data processing and data residency
      needs. Using the S3 APIs and features, S3 on Outposts makes it easy to
      store, secure, tag, retrieve, report on, and control access to the data on
      your Outpost. AWS Outposts is a fully managed service that extends AWS
      infrastructure, services, and tools to virtually any data center,
      co-location space, or on-premises facility for a truly consistent hybrid
      experience
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/s3/outposts/
    baseURL: https://example.com
    tags:
      - Endpoints
      - Outposts
      - Shared
      - Storage
    properties:
      - type: Documentation
        url: https://aws.amazon.com/s3/outposts/
      - type: OpenAPI
        url: properties/s3outposts-openapi-original.yml
      - type: Pricing
        url: https://aws.amazon.com/outposts/rack/pricing/
      - type: Resources
        url: https://aws.amazon.com/outposts/rack/resources/
      - type: Getting Started
        url: https://aws.amazon.com/outposts/rack/getting-started/
      - type: FAQ
        url: https://aws.amazon.com/outposts/rack/faqs/
      - type: Partners
        url: https://aws.amazon.com/outposts/partners/
    overlays:
      - type: APIs.io Search
        url: overlays/s3outposts-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/s3outposts-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:s3outposts
  - name: Amazon SageMaker Metrics
    description: >-
      Contains all data plane API operations and data types for Amazon SageMaker
      Metrics. Use these APIs to put and retrieve (get) features related to your
      training run.    BatchPutMetrics
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://docs.aws.amazon.com/sagemaker/latest/dg/monitoring-cloudwatch.html
    baseURL: https://example.com
    tags:
      - Batches
      - Metrics
      - Data
    properties:
      - type: Documentation
        url: >-
          https://docs.aws.amazon.com/sagemaker/latest/dg/monitoring-cloudwatch.html
      - type: OpenAPI
        url: properties/sagemaker-metrics-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/sagemaker-metrics-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/sagemaker-metrics-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:sagemaker-metrics
  - name: Geospatial ML with Amazon SageMaker
    description: >-
      Amazon SageMaker offers specialized machine learning features tailored for
      geospatial data analysis. With this API, users can easily create, train,
      and deploy ML models using geospatial data sources. Additionally, the API
      provides access to pre-built processing operations, pretrained ML models,
      and visualization tools, enabling users to run geospatial ML efficiently
      and on a large scale.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/sagemaker/geospatial/
    baseURL: https://example.com
    tags:
      - ARN
      - Collections
      - Data
      - Earth
      - Enrichment
      - Exports
      - Jobs
      - Machine Learning
      - Models
      - Observation
      - Raster
      - Resources
      - Search
      - Stop
      - Tags
      - Tiles
      - Untag
      - Vectors
    properties:
      - type: Documentation
        url: https://aws.amazon.com/sagemaker/geospatial/
      - type: OpenAPI
        url: properties/sagemaker-geospatial-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/sagemaker/geospatial/features/
      - type: Pricing
        url: https://aws.amazon.com/sagemaker/geospatial/pricing/
      - type: Resources
        url: https://aws.amazon.com/sagemaker/geospatial/resources/
      - type: FAQ
        url: https://aws.amazon.com/sagemaker/geospatial/faqs/
      - type: Customers
        url: https://aws.amazon.com/sagemaker/geospatial/customers/
    overlays:
      - type: APIs.io Search
        url: overlays/sagemaker-geospatial-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/sagemaker-geospatial-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:sagemaker-geospatial
  - name: AWS Savings Plans
    description: >-
      Savings Plans is a flexible pricing model that can help you reduce your
      bill by up to 72% compared to On-Demand prices, in exchange for a one- or
      three-year hourly spend commitment. AWS offers three types of Savings
      Plans: Compute Savings Plans, EC2 Instance Savings Plans, and Amazon
      SageMaker.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/savingsplans/
    baseURL: https://example.com
    tags:
      - Describe
      - Offerings
      - Plan
      - Plans
      - Queued
      - Rates
      - Resources
      - Savings
      - Tags
      - Untag
    properties:
      - type: Documentation
        url: https://aws.amazon.com/savingsplans/
      - type: OpenAPI
        url: properties/savingsplans-openapi-original.yml
      - type: FAQ
        url: https://aws.amazon.com/savingsplans/faq/
      - type: Compute-pricing
        url: https://aws.amazon.com/savingsplans/compute-pricing/
      - type: Ml-pricing
        url: https://aws.amazon.com/savingsplans/ml-pricing/
      - type: FAQ
        url: https://aws.amazon.com/savingsplans/faq/
    overlays:
      - type: APIs.io Search
        url: overlays/savingsplans-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/savingsplans-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:savingsplans
  - name: Amazon EventBridge Schema Registry
    description: >-
      EventBridge offers pre-defined schemas for events generated by AWS
      services, but you can also create custom schemas or infer them from events
      on an event bus. Once you have a schema, you can download code bindings
      for popular programming languages to accelerate development. You can
      manage schemas and work with code bindings from the EventBridge console,
      API, or directly in your IDE using AWS toolkits.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://docs.aws.amazon.com/eventbridge/latest/userguide/eb-schema.html
    baseURL: https://example.com
    tags:
      - ARN
      - Binding
      - Code
      - Discover
      - Discovered
      - Discoverers
      - Events
      - Exports
      - Languages
      - Names
      - Policies
      - Registries
      - Resources
      - Schemas
      - Search
      - Sources
      - Stop
      - Tags
      - Untag
      - Versions
    properties:
      - type: Documentation
        url: https://example.com
      - type: OpenAPI
        url: properties/schemas-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/schemas-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/schemas-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:schemas
  - name: Amazon EventBridge Scheduler
    description: >-
      The Amazon EventBridge Scheduler API is a serverless tool for scheduling
      and managing tasks in one centralized service. It reliably delivers tasks
      and adjusts schedules based on downstream target availability. This
      reference provides a list of available API actions and data types for
      EventBridge Scheduler.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://docs.aws.amazon.com/eventbridge/
    baseURL: https://example.com
    tags:
      - ARN
      - Events
      - Groups
      - Names
      - Resources
      - Schedules
      - Tags
      - Untag
    properties:
      - type: Documentation
        url: https://docs.aws.amazon.com/eventbridge/
      - type: OpenAPI
        url: properties/scheduler-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/scheduler-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/scheduler-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:scheduler
  - name: Amazon SimpleDB
    description: >-
      This API, Amazon SimpleDB, is a cloud-based web service that offers
      essential database functionalities such as data indexing and querying. By
      handling the complex tasks of managing a web-scale database, SimpleDB
      empowers developers to concentrate on developing applications without
      worrying about database operations. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/simpledb/
    baseURL: https://example.com
    tags:
      - Databases
      - SQL
      - Selects
    properties:
      - type: Documentation
        url: https://aws.amazon.com/simpledb/
      - type: OpenAPI
        url: properties/sdb-openapi-original.yml
      - type: Pricing
        url: https://aws.amazon.com/simpledb/pricing/
      - type: Getting-started
        url: https://aws.amazon.com/simpledb/getting-started/
      - type: Developer-resources
        url: https://aws.amazon.com/simpledb/developer-resources/
      - type: FAQ
        url: https://aws.amazon.com/simpledb/faqs/
    overlays:
      - type: APIs.io Search
        url: overlays/sdb-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/sdb-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:sdb
  - name: Amazon Web Services Secrets Manager
    description: >-
      The AWS Secrets Manager API allows users to securely manage, fetch, and
      update database credentials, API keys, and other sensitive information at
      various stages of their existence.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/secrets-manager/
    baseURL: https://example.com
    tags:
      - Policies
      - Resources
      - Validate
      - Secrets
    properties:
      - type: Documentation
        url: https://aws.amazon.com/secrets-manager/
      - type: OpenAPI
        url: properties/secretsmanager-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/secrets-manager/features/
      - type: Pricing
        url: https://aws.amazon.com/secrets-manager/pricing/
      - type: Getting-started
        url: https://aws.amazon.com/secrets-manager/getting-started/
      - type: Resources
        url: https://aws.amazon.com/secrets-manager/resources/
      - type: FAQ
        url: https://aws.amazon.com/secrets-manager/faqs/
      - type: Customers
        url: https://aws.amazon.com/secrets-manager/customers/
    overlays:
      - type: APIs.io Search
        url: overlays/secretsmanager-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/secretsmanager-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:secretsmanager
  - name: AWS Serverless Application Repository
    description: >-
      The AWS Serverless Application Repository simplifies the process for
      developers and businesses to discover and deploy serverless applications
      in the AWS Cloud. This integration with the AWS Lambda console allows
      developers of all skill levels to easily start with serverless computing. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/serverless/serverlessrepo/
    baseURL: https://example.com
    tags:
      - Applications
      - Change
      - Change Sets
      - Cloud
      - Dependencies
      - Formation
      - Policies
      - Semantic
      - Sets
      - Templates
      - Unshare
      - Versions
    properties:
      - type: Documentation
        url: https://aws.amazon.com/serverless/serverlessrepo/
      - type: OpenAPI
        url: properties/serverlessrepo-openapi-original.yml
      - type: Publishing
        url: https://aws.amazon.com/serverless/serverlessrepo/publishing/
      - type: Resources
        url: https://aws.amazon.com/serverless/serverlessrepo/resources/
      - type: FAQ
        url: https://aws.amazon.com/serverless/serverlessrepo/faqs/
    overlays:
      - type: APIs.io Search
        url: overlays/serverlessrepo-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/serverlessrepo-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:serverlessrepo
  - name: Amazon Security Lake
    description: >-
      Amazon Security Lake is a fully managed security data lake service. You
      can use Security Lake to automatically centralize security data from
      cloud, on-premises, and custom sources into a data lake that's stored in
      your Amazon Web Services account. Amazon Web Services Organizations is an
      account management service that lets you consolidate multiple Amazon Web
      Services accounts into an organization that you create and centrally
      manage. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/security-lake/
    baseURL: https://example.com
    tags:
      - ARN
      - Administrator
      - Configurations
      - Custom
      - Data
      - Data Lakes
      - Delegate
      - Delegated
      - Exceptions
      - Lakes
      - Log Sources
      - Logs
      - Names
      - Notifications
      - Organizations
      - Register
      - Resources
      - Sources
      - Subscribers
      - Subscriptions
      - Tags
      - Untag
    properties:
      - type: Documentation
        url: https://aws.amazon.com/security-lake/
      - type: OpenAPI
        url: properties/securitylake-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/security-lake/features/
      - type: Pricing
        url: https://aws.amazon.com/security-lake/pricing/
      - type: Getting-started
        url: https://aws.amazon.com/security-lake/getting-started/
      - type: FAQ
        url: https://aws.amazon.com/security-lake/faqs/
      - type: Customers
        url: https://aws.amazon.com/security-lake/customers/
      - type: Resources
        url: https://aws.amazon.com/security-lake/resources/
      - type: Partners
        url: https://aws.amazon.com/security-lake/partners/
    overlays:
      - type: APIs.io Search
        url: overlays/securitylake-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/securitylake-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:securitylake
  - name: AWS Service Quotas
    description: >-
      Easily monitor and control your quotas as your Amazon Web Services
      projects expand with Service Quotas. Limits, also known as quotas, define
      the maximum number of resources you can generate within your AWS account. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://docs.aws.amazon.com/servicequotas/latest/userguide/intro.html
    baseURL: https://example.com
    tags:
      - Resources
      - Untag
    properties:
      - type: Documentation
        url: https://docs.aws.amazon.com/servicequotas/latest/userguide/intro.html
      - type: OpenAPI
        url: properties/service-quotas-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/service-quotas-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/service-quotas-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:service-quotas
  - name: AWS Cloud Map
    description: >-
      Our Cloud Map API allows you to easily set up and manage public DNS,
      private DNS, or HTTP namespaces for your microservice applications. By
      registering instances with Cloud Map via the API, you can ensure seamless
      integration and availability. Cloud Map automatically creates DNS records
      and optional health checks for public or private DNS namespaces, providing
      clients with up to eight healthy records in response to queries or
      requests.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/cloud-map/
    baseURL: https://example.com
    tags:
      - Services
      - Clouds
      - Maps
      - DNS
      - Namespaces
    properties:
      - type: Documentation
        url: https://aws.amazon.com/cloud-map/
      - type: OpenAPI
        url: properties/servicediscovery-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/cloud-map/features/
      - type: Pricing
        url: https://aws.amazon.com/cloud-map/pricing/
      - type: FAQ
        url: https://aws.amazon.com/cloud-map/faqs/
    overlays:
      - type: APIs.io Search
        url: overlays/servicediscovery-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/servicediscovery-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:servicediscovery
  - name: AWS Service Catalog
    description: >-
      AWS Service Catalog enables IT administrators to create, manage, and
      distribute portfolios of approved products to end users, who can then
      access the products they need in a personalized portal. Typical products
      include servers, databases, websites, or applications that are deployed
      using AWS resources (for example, an Amazon EC2 instance or an Amazon RDS
      database). 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://docs.aws.amazon.com/servicecatalog/
    baseURL: https://example.com
    tags:
      - ARN
      - Applications
      - Associated
      - Attributes
      - Configurations
      - Details
      - Disassociate
      - Groups
      - Resources
      - Sync
      - Tags
      - Types
      - Untag
    properties:
      - type: Documentation
        url: https://docs.aws.amazon.com/servicecatalog/
      - type: OpenAPI
        url: properties/servicecatalog-appregistry-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/servicecatalog-appregistry-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/servicecatalog-appregistry-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:servicecatalog-appregistry
  - name: AWS Shield Advanced
    description: >-
      The Shield Advanced API Reference is a comprehensive guide for developers
      seeking detailed information on the Shield Advanced API actions, data
      types, and errors. To learn more about the WAF and Shield Advanced
      features and how to effectively utilize the APIs, refer to the WAF and
      Shield Developer Guide.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/shield/
    baseURL: https://example.com
    tags:
      - Subscriptions
    properties:
      - type: Documentation
        url: https://aws.amazon.com/shield/
      - type: OpenAPI
        url: properties/shield-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/shield/features/
      - type: Pricing
        url: https://aws.amazon.com/shield/pricing/
      - type: Getting-started
        url: https://aws.amazon.com/shield/getting-started/
      - type: Resources
        url: https://aws.amazon.com/shield/resources/
    overlays:
      - type: APIs.io Search
        url: overlays/shield-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/shield-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:shield
  - name: 'AWS SimSpace Weaver '
    description: >-
      SimSpace Weaver is a cloud-based service on Amazon Web Services that
      enables users to construct and deploy large spatial simulations. These
      simulations can include crowd scenarios, real-world environments, and
      immersive experiences. The SimSpace Weaver API allows direct interaction
      with the service, providing detailed descriptions of available operations
      and data structures. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/simspaceweaver/
    baseURL: https://example.com
    tags:
      - ARN
      - Applications
      - Clock
      - Describe
      - Resources
      - Simulations
      - Snapshots
      - Start Application
      - Start Clock
      - Start Simulation
      - Stop
      - Stop APplication
      - Stop Clock
      - Tags
      - Untag
    properties:
      - type: Documentation
        url: https://aws.amazon.com/simspaceweaver/
      - type: OpenAPI
        url: properties/simspaceweaver-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/simspaceweaver/features/
      - type: Pricing
        url: https://aws.amazon.com/simspaceweaver/pricing/
      - type: Resources
        url: https://aws.amazon.com/simspaceweaver/resources/
    overlays:
      - type: APIs.io Search
        url: overlays/simspaceweaver-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/simspaceweaver-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:simspaceweaver
  - name: AWS Application Migration Service
    description: >-
      The AWS Application Migration Service streamlines the migration process by
      automating the conversion of source servers to run on AWS, reducing manual
      errors and saving time. It also offers a range of built-in and custom
      optimization options to simplify application modernization.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/application-migration-service/
    baseURL: https://example.com
    tags:
      - Jobs
      - Replication
    properties:
      - type: Documentation
        url: https://aws.amazon.com/application-migration-service/
      - type: OpenAPI
        url: properties/sms-openapi-original.yml
      - type: Pricing
        url: https://aws.amazon.com/application-migration-service/pricing/
      - type: FAQ
        url: https://aws.amazon.com/application-migration-service/faqs/
      - type: Resources
        url: https://aws.amazon.com/application-migration-service/resources/
    overlays:
      - type: APIs.io Search
        url: overlays/sms-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/sms-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:sms
  - name: AWS Snow Family
    description: >-
      The AWS Snow Family helps customers who need to run operations in austere,
      non-data center environments, and in locations which lack consistent
      network connectivity. The Snow Family (comprised of AWS Snowcone,
      Snowball, and AWS Snowmobile) oﬀers a number of physical devices and
      capacity profiles, most with built-in computing capabilities.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/snow/
    baseURL: https://example.com
    tags:
      - ARN
      - Cancel
      - Describe
      - Device
      - Devices
      - EC2
      - Ec2Instances
      - Execution
      - Executions
      - Managed
      - Resources
      - Tags
      - Tasks
      - Untag
    properties:
      - type: Documentation
        url: https://aws.amazon.com/snow/
      - type: OpenAPI
        url: properties/snow-device-management-openapi-original.yml
      - type: FAQ
        url: https://aws.amazon.com/snow/faqs/
    overlays:
      - type: APIs.io Search
        url: overlays/snow-device-management-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/snow-device-management-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:snow-device-management
  - name: AWS Security Hub
    description: >-
      The Security Hub API offers a comprehensive view of your security state
      within Amazon Web Services, allowing you to assess your environment
      against industry standards and best practices. By collecting security data
      across AWS accounts and third-party products, Security Hub enables
      analysis of security trends and identification of high-priority issues.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/security-hub/
    baseURL: https://example.com
    tags:
      - ARN
      - Accounts
      - Actions
      - Administrative
      - Administrator
      - Aggregator
      - Aggregators
      - Associate
      - Associations
      - Automation
      - Automation Rules
      - Batches
      - Configurations
      - Controls
      - Count
      - Decline
      - Definitions
      - Deregister
      - Describe
      - Disable
      - Disassociate
      - Disassociation
      - Enable
      - Enabled
      - Findings
      - History
      - Hub
      - Import
      - Insights
      - Invitations
      - Invite
      - Master
      - Members
      - Organizations
      - Policies
      - Products
      - Register
      - Resources
      - Results
      - Rules
      - Security
      - Standards
      - Subscriptions
      - Tags
      - Targets
      - Untag
    properties:
      - type: Documentation
        url: https://aws.amazon.com/security-hub/
      - type: OpenAPI
        url: properties/securityhub-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/security-hub/features/
      - type: Pricing
        url: https://aws.amazon.com/security-hub/pricing/
      - type: Getting Started
        url: https://aws.amazon.com/security-hub/getting-started/
      - type: Resources
        url: https://aws.amazon.com/security-hub/resources/
      - type: FAQ
        url: https://aws.amazon.com/security-hub/faqs/
      - type: Customers
        url: https://aws.amazon.com/security-hub/customers/
      - type: Partners
        url: https://aws.amazon.com/security-hub/partners/
    overlays:
      - type: APIs.io Search
        url: overlays/securityhub-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/securityhub-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:securityhub
  - name: Amazon Simple Notification Service
    description: >-
      The Amazon Simple Notification Service (Amazon SNS) is a web service that
      allows developers to create distributed web-enabled applications. With
      Amazon SNS, applications can easily send real-time notification messages
      to subscribers using multiple delivery protocols. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/sns/
    baseURL: https://example.com
    tags:
      - Numbers
      - Phone
      - SMSSandbox
      - Verify
    properties:
      - type: Documentation
        url: https://aws.amazon.com/sns/
      - type: OpenAPI
        url: properties/sns-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/sns/features/
      - type: Pricing
        url: https://aws.amazon.com/sns/pricing/
      - type: Getting-started
        url: https://aws.amazon.com/sns/getting-started/
      - type: Resources
        url: https://aws.amazon.com/sns/resources/
    overlays:
      - type: APIs.io Search
        url: overlays/sns-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/sns-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:sns
  - name: Amazon Simple Queue Service
    description: >-
      Introducing the Amazon SQS API Reference, a reliable and highly-scalable
      hosted queue that facilitates the storage and transmission of messages
      between applications and microservices. Amazon SQS effectively moves data
      between distributed components, promoting decoupling. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/sqs/
    baseURL: https://example.com
    tags:
      - Queues
      - Untag
      - Tags
      - Microservices
    properties:
      - type: Documentation
        url: https://aws.amazon.com/sqs/
      - type: OpenAPI
        url: properties/sqs-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/sqs/features/
      - type: Pricing
        url: https://aws.amazon.com/sqs/pricing/
      - type: Getting Started
        url: https://aws.amazon.com/sqs/getting-started/
      - type: Resources
        url: https://aws.amazon.com/sqs/resources/
      - type: FAQ
        url: https://aws.amazon.com/sqs/faqs/
    overlays:
      - type: APIs.io Search
        url: overlays/sqs-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/sqs-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:sqs
  - name: AWS Service Catalog
    description: >-
      AWS Service Catalog is a tool that allows you to efficiently handle your
      cloud resources by overseeing your infrastructure as code (IaC) templates,
      which can be written in either CloudFormation or Terraform configurations.
      This service helps you maintain compliance standards while enabling your
      customers to easily deploy the necessary cloud resources.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/servicecatalog/
    baseURL: https://example.com
    tags:
      - Options
      - Tags
      - Catalogs
      - Services
    properties:
      - type: Documentation
        url: https://aws.amazon.com/servicecatalog/
      - type: OpenAPI
        url: properties/servicecatalog-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/servicecatalog/features/
      - type: Pricing
        url: https://aws.amazon.com/servicecatalog/pricing/
      - type: Getting-started
        url: https://aws.amazon.com/servicecatalog/getting-started/
      - type: Resources
        url: https://aws.amazon.com/servicecatalog/resources/
      - type: FAQ
        url: https://aws.amazon.com/servicecatalog/faqs/
      - type: Customers
        url: https://aws.amazon.com/servicecatalog/customers/
      - type: Partners
        url: https://aws.amazon.com/servicecatalog/partners/
    overlays:
      - type: APIs.io Search
        url: overlays/servicecatalog-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/servicecatalog-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:servicecatalog
  - name: AWS Systems Manager
    description: >-
      AWS Systems Manager provides a comprehensive and secure management
      solution for resources across AWS and in both multicloud and hybrid
      environments.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/systems-manager/
    baseURL: https://example.com
    tags:
      - Services
      - Settings
    properties:
      - type: Documentation
        url: https://aws.amazon.com/systems-manager/
      - type: OpenAPI
        url: properties/ssm-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/systems-manager/features/
      - type: Pricing
        url: https://aws.amazon.com/systems-manager/pricing/
      - type: Getting-started
        url: https://aws.amazon.com/systems-manager/getting-started/
      - type: FAQ
        url: https://aws.amazon.com/systems-manager/faq/
      - type: Customers
        url: https://aws.amazon.com/systems-manager/customers/
      - type: Partners
        url: https://aws.amazon.com/systems-manager/partners/
    overlays:
      - type: APIs.io Search
        url: overlays/ssm-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/ssm-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:ssm
  - name: AWS Signer
    description: >-
      AWS Signer is a managed code-signing service designed to ensure the trust
      and integrity of your code. This service supports code signing for various
      applications such as AWS Lambda, IoT devices supported by AWS, and
      container images stored in registries like Amazon Elastic Container
      Registry (ECR). With AWS Signer, you can create signing profiles and use
      them to sign Lambda deployment packages, IoT device code updates, and
      container images. Integrated support is provided for services like Amazon
      S3, Amazon CloudWatch, and AWS CloudTrail. For more details on how to use
      AWS Signer, refer to the AWS Signer Developer Guide.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://docs.aws.amazon.com/signer/
    baseURL: https://example.com
    tags:
      - ARN
      - Describe
      - Jobs
      - Names
      - Payload
      - Permission
      - Permissions
      - Platforms
      - Profiles
      - Removes
      - Resources
      - Revocations
      - Revoke
      - Sign
      - Signatures
      - Signing
      - Statements
      - Status
      - Tags
      - Untag
    properties:
      - type: Documentation
        url: https://docs.aws.amazon.com/signer/
      - type: OpenAPI
        url: properties/signer-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/signer-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/signer-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:signer
  - name: AWS Systems Manager Incident Manager
    description: >-
      This API, Systems Manager Incident Manager, is a comprehensive incident
      management tool specifically designed to assist users in dealing with
      unforeseen interruptions or service disruptions in their Amazon Web
      Services-hosted applications. The platform aims to enhance incident
      resolution by promptly alerting responders of the impact, presenting key
      troubleshooting information, and offering collaborative features to
      facilitate the swift restoration of services. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: >-
      https://docs.aws.amazon.com/incident-manager/latest/userguide/what-is-incident-manager.html
    baseURL: https://example.com
    tags:
      - ARN
      - Batches
      - Deletion
      - Events
      - Findings
      - Incident
      - Items
      - Plan
      - Plans
      - Policies
      - Protection
      - Record
      - Records
      - Related
      - Replication
      - Resources
      - Responses
      - Sets
      - Tags
      - Timeline
      - Untag
    properties:
      - type: Documentation
        url: >-
          https://docs.aws.amazon.com/incident-manager/latest/userguide/what-is-incident-manager.html
      - type: OpenAPI
        url: properties/ssm-incidents-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/ssm-incidents-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/ssm-incidents-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:ssm-incidents
  - name: AWS IAM Identity Center
    description: >-
      The AWS IAM Identity Center Portal is a web service that simplifies the
      assignment of user access to IAM Identity Center resources, such as the
      AWS access portal. Users can have AWS account applications and roles
      assigned to them and be federated into the application. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/iam/identity-center/
    baseURL: https://example.com
    tags:
      - Credentials
      - Federation
      - Roles
      - Accounts
      - Assignment
      - Logout
    properties:
      - type: Documentation
        url: https://aws.amazon.com/iam/identity-center/
      - type: OpenAPI
        url: properties/sso-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/iam/identity-center/features/
      - type: FAQ
        url: https://aws.amazon.com/iam/identity-center/faqs/
      - type: Resources
        url: https://aws.amazon.com/iam/identity-center/resources/
    overlays:
      - type: APIs.io Search
        url: overlays/sso-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/sso-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:sso
  - name: AWS Systems Manager for SAP
    description: >-
      AWS Systems Manager for SAP is a tool designed to automate the management
      and operation of SAP applications on AWS. This integration allows for
      seamless communication between AWS services and SAP applications running
      on AWS. Users can easily access and utilize AWS Systems Manager for SAP
      through AWS APIs.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: >-
      https://docs.aws.amazon.com/ssm-sap/latest/userguide/what-is-ssm-for-sap.html
    baseURL: https://example.com
    tags:
      - ARN
      - Applications
      - Components
      - Databases
      - Deregister
      - Operation
      - Operations
      - Permission
      - Refresh
      - Register
      - Resources
      - Settings
      - Tags
      - Untag
    properties:
      - type: Documentation
        url: >-
          https://docs.aws.amazon.com/ssm-sap/latest/userguide/what-is-ssm-for-sap.html
      - type: OpenAPI
        url: properties/ssm-sap-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/ssm-sap-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/ssm-sap-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:ssm-sap
  - name: AWS Step Functions
    description: >-
      This API, AWS Step Functions, is a tool that allows developers to easily
      create visual workflows for utilizing AWS services, building distributed
      applications, automating processes, orchestrating microservices, and
      setting up data and machine learning pipelines.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/step-functions/
    baseURL: https://example.com
    tags:
      - Alias
      - Machines
      - States
    properties:
      - type: Documentation
        url: https://aws.amazon.com/step-functions/
      - type: OpenAPI
        url: properties/states-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/step-functions/features/
      - type: Pricing
        url: https://aws.amazon.com/step-functions/pricing/
      - type: Use Cases
        url: https://aws.amazon.com/step-functions/use-cases/
      - type: Customers
        url: https://aws.amazon.com/step-functions/customers/
      - type: Getting Started
        url: https://aws.amazon.com/step-functions/getting-started/
      - type: FAQ
        url: https://aws.amazon.com/step-functions/faqs/
    overlays:
      - type: APIs.io Search
        url: overlays/states-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/states-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:states
  - name: AWS Storage Gateway Service
    description: >-
      The Storage Gateway Service API allows seamless and secure integration
      between on-premises software appliances and cloud-based storage within
      Amazon Web Services infrastructure. This service enables cost-effective
      backup and rapid disaster recovery by allowing secure data uploads to the
      AWS cloud. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/storagegateway/
    baseURL: https://example.com
    tags:
      - Types
      - VTLDevice
      - Storage
      - Gateway
    properties:
      - type: Documentation
        url: https://aws.amazon.com/storagegateway/
      - type: OpenAPI
        url: properties/storagegateway-openapi-original.yml
      - type: Pricing
        url: https://aws.amazon.com/storagegateway/pricing/
      - type: Getting-started
        url: https://aws.amazon.com/storagegateway/getting-started/
      - type: Developer-resources
        url: https://aws.amazon.com/storagegateway/developer-resources/
      - type: FAQ
        url: https://aws.amazon.com/storagegateway/faqs/
      - type: Customers
        url: https://aws.amazon.com/storagegateway/customers/
      - type: Features
        url: https://aws.amazon.com/storagegateway/features/
    overlays:
      - type: APIs.io Search
        url: overlays/storagegateway-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/storagegateway-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:storagegateway
  - name: AWS Supply Chain
    description: >-
      The AWS Supply Chain API is a cloud-based application designed to
      streamline supply chain management processes by connecting and extracting
      inventory, supply, and demand data from existing ERP and supply chain
      systems into a single data model. This API supports configuration data
      import for Supply Planning and all operations are authenticated and signed
      by Amazon certificates. The use of the AWS SDK is required, along with AWS
      Identity and Access Management users and roles to ensure secure access and
      permission policies.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/aws-supply-chain/
    baseURL: https://example.com
    tags:
      - Bill
      - Configurations
      - Import
      - Instances
      - Jobs
      - Materials
      - Supply Chain
    properties:
      - type: Documentation
        url: https://aws.amazon.com/aws-supply-chain/
      - type: OpenAPI
        url: properties/supplychain-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/aws-supply-chain/features/
      - type: Pricing
        url: https://aws.amazon.com/aws-supply-chain/pricing/
      - type: Partners
        url: https://aws.amazon.com/aws-supply-chain/partners/
      - type: Resources
        url: https://aws.amazon.com/aws-supply-chain/resources/
    overlays:
      - type: APIs.io Search
        url: overlays/supplychain-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/supplychain-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:supplychain
  - name: AWS Security Token Service
    description: >-
      Introducing the Security Token Service (STS) API, which allows you to
      conveniently request temporary, restricted-access credentials for your
      users. This documentation offers comprehensive explanations of the STS API
      functionality, with detailed instructions on how to utilize this service
      effectively. For further insights on using temporary security credentials,
      refer to the resources on Temporary Security Credentials.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://docs.aws.amazon.com/STS/latest/APIReference/welcome.html
    baseURL: https://example.com
    tags:
      - Sessions
      - Tokens
    properties:
      - type: Documentation
        url: https://docs.aws.amazon.com/STS/latest/APIReference/welcome.html
      - type: OpenAPI
        url: properties/sts-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/sts-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/sts-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:sts
  - name: Amazon Simple Workflow Service
    description: >-
      The Amazon Simple Workflow Service (Amazon SWF) simplifies the process of
      building cloud-based applications that require coordination between
      distributed components. Tasks in Amazon SWF represent individual units of
      work within a workflow, with the service handling the management of
      intertask dependencies, scheduling, and concurrency to maintain the
      logical flow of the application.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/swf/
    baseURL: https://example.com
    tags:
      - Resources
      - Untag
      - Tags
      - Workflows
    properties:
      - type: Documentation
        url: https://aws.amazon.com/swf/
      - type: OpenAPI
        url: properties/swf-openapi-original.yml
      - type: Pricing
        url: https://aws.amazon.com/swf/pricing/
      - type: Testimonials
        url: https://aws.amazon.com/swf/testimonials/
      - type: Developer-resources
        url: https://aws.amazon.com/swf/developer-resources/
      - type: FAQ
        url: https://aws.amazon.com/swf/faqs/
      - type: Getting-started
        url: https://aws.amazon.com/swf/getting-started/
    overlays:
      - type: APIs.io Search
        url: overlays/swf-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/swf-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:swf
  - name: Amazon CloudWatch Synthetics
    description: >-
      Amazon CloudWatch Synthetics provides a way to continuously monitor your
      services by creating and managing canaries. These canaries are lightweight
      scripts that monitor your endpoints and APIs externally, allowing you to
      set them up to run 24/7, once per minute.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://docs.aws.amazon.com/cloudwatch/
    baseURL: https://example.com
    tags:
      - ARN
      - Associate
      - Associated
      - Canaries
      - Canary
      - Describe
      - Disassociate
      - Groups
      - Last
      - Names
      - Resources
      - Runs
      - Runtime
      - Stop
      - Tags
      - Untag
      - Versions
    properties:
      - type: Documentation
        url: https://example.com
      - type: OpenAPI
        url: properties/synthetics-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/synthetics-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/synthetics-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:synthetics
  - name: Amazon Timestream Query
    description: >-
      Easily store and analyze sensor data for IoT applications, metrics for
      DevOps use cases, and telemetry for application monitoring scenarios like
      clickstream data analysis with Amazon Timestream for LiveAnalytics. This
      managed time-series database engine allows developers and DevOps teams to
      run InfluxDB databases on AWS using open-source APIs for real-time
      time-series applications. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://docs.aws.amazon.com/timestream/
    baseURL: https://example.com
    tags:
      - Queries
      - Scheduled
      - time Series
      - Analytics
    properties:
      - type: Documentation
        url: https://docs.aws.amazon.com/timestream/
      - type: OpenAPI
        url: properties/timestream-query-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/timestream-query-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/timestream-query-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:timestream-query
  - name: Amazon Textract
    description: >-
      Amazon Textract is an advanced machine learning service that effortlessly
      extracts text, handwriting, layout elements, and data from scanned
      documents. Unlike traditional OCR tools, Textract can intelligently
      identify and extract specific data from various types of documents,
      including PDFs, images, tables, and forms. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/textract/
    baseURL: https://example.com
    tags:
      - Adapter
      - Content
      - OCR
      - PDF
      - Tables
      - Forms
    properties:
      - type: Documentation
        url: https://aws.amazon.com/textract/
      - type: OpenAPI
        url: properties/textract-openapi-original.yml
      - type: Pricing
        url: https://aws.amazon.com/textract/pricing/
      - type: Resources
        url: https://aws.amazon.com/textract/resources/
      - type: FAQ
        url: https://aws.amazon.com/textract/faqs/
      - type: Customers
        url: https://aws.amazon.com/textract/customers/
      - type: Partners
        url: https://aws.amazon.com/textract/partners/
      - type: Features
        url: https://aws.amazon.com/textract/features/
    overlays:
      - type: APIs.io Search
        url: overlays/textract-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/textract-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:textract
  - name: Amazon Timestream Write
    description: >-
      Amazon Timestream is a powerful time-series database service designed for
      storing and analyzing large volumes of time-series data. It is fully
      managed and scalable, allowing you to easily store and analyze trillions
      of data points per day. Timestream is ideal for IoT sensor data analysis,
      industrial telemetry management, and log data and metric analysis for
      application performance improvement. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://docs.aws.amazon.com/timestream/
    baseURL: https://example.com
    tags:
      - Records
      - Write
      - Database
      - Time-Series
    properties:
      - type: Documentation
        url: https://docs.aws.amazon.com/timestream/
      - type: OpenAPI
        url: properties/timestream-write-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/timestream-write-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/timestream-write-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:timestream-write
  - name: AWS Transfer
    description: >-
      Transfer Family is a managed service that allows for the transfer of files
      via FTP, FTPS, SFTP, and AS2 directly to and from Amazon S3 or Amazon EFS.
      Amazon Web Services facilitates the seamless migration of file transfer
      workflows to Transfer Family by integrating with existing authentication
      systems and providing DNS routing via Amazon Route 53. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/aws-transfer-family/
    baseURL: https://example.com
    tags:
      - Users
      - Transfers
      - FTP
      - FTPS
      - SFTP
      - AS2
    properties:
      - type: Documentation
        url: https://aws.amazon.com/aws-transfer-family/
      - type: OpenAPI
        url: properties/transfer-openapi-original.yml
      - type: Pricing
        url: https://aws.amazon.com/aws-transfer-family/pricing/
      - type: Getting-started
        url: https://aws.amazon.com/aws-transfer-family/getting-started/
      - type: Resources
        url: https://aws.amazon.com/aws-transfer-family/resources/
      - type: FAQ
        url: https://aws.amazon.com/aws-transfer-family/faqs/
      - type: Customers
        url: https://aws.amazon.com/aws-transfer-family/customers/
      - type: Partners
        url: https://aws.amazon.com/aws-transfer-family/partners/
    overlays:
      - type: APIs.io Search
        url: overlays/transfer-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/transfer-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:transfer
  - name: Amazon Transcribe
    description: >-
      The Amazon Transcribe streaming API provides real-time transcription
      services in three main categories: Standard, Medical, and Call Analytics.
      Standard transcriptions are suitable for general use cases, while Medical
      transcriptions are specialized for medical professionals and incorporate
      medical terminology. The Call Analytics option is specifically designed
      for call center audio, providing insights into customer service
      interactions.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/transcribe/
    baseURL: https://example.com
    tags:
      - Analytics
      - Call
      - Stream
      - Transcriptions
      - Medical
      - Healthcare
    properties:
      - type: Documentation
        url: https://aws.amazon.com/transcribe/
      - type: OpenAPI
        url: properties/transcribe-streaming-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/transcribe/features/
      - type: Pricing
        url: https://aws.amazon.com/transcribe/pricing/
      - type: Getting-started
        url: https://aws.amazon.com/transcribe/getting-started/
      - type: Resources
        url: https://aws.amazon.com/transcribe/resources/
      - type: FAQ
        url: https://aws.amazon.com/transcribe/faqs/
      - type: Customers
        url: https://aws.amazon.com/transcribe/customers/
    overlays:
      - type: APIs.io Search
        url: overlays/transcribe-streaming-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/transcribe-streaming-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:transcribe-streaming
  - name: AWS Telco Network Builder
    description: >-
      The Amazon Web Services Telco Network Builder (TNB) is a network
      automation service designed to assist in the deployment and management of
      telecom networks. With AWS TNB, users can efficiently manage the lifecycle
      of their telecommunication network functions, from initial planning to
      deployment and ongoing maintenance.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/tnb/
    baseURL: https://example.com
    tags:
      - ARN
      - Ate
      - Cancel
      - Content
      - Descriptions
      - Descriptors
      - Functions
      - Info
      - Instances
      - Instantiate
      - Networks
      - Occs
      - Operation
      - Operations
      - Packages
      - Resources
      - Tags
      - Terminate
      - Untag
      - Validate
      - Tags
    properties:
      - type: Documentation
        url: https://aws.amazon.com/tnb/
      - type: OpenAPI
        url: properties/tnb-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/tnb/features/
      - type: Pricing
        url: https://aws.amazon.com/tnb/pricing/
      - type: FAQ
        url: https://aws.amazon.com/tnb/faqs/
    overlays:
      - type: APIs.io Search
        url: overlays/tnb-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/tnb-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:tnb
  - name: AWS Translate
    description: >-
      Amazon Translate enables users to adapt content for a global audience and
      efficiently translate and analyze a large amount of text to facilitate
      communication across different languages.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/translate/
    baseURL: https://example.com
    tags:
      - Data
      - Parallel
    properties:
      - type: Documentation
        url: https://aws.amazon.com/translate/
      - type: OpenAPI
        url: properties/translate-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/translate/details/
      - type: Pricing
        url: https://aws.amazon.com/translate/pricing/
      - type: Getting Started
        url: https://aws.amazon.com/translate/getting-started/
      - type: Resources
        url: https://aws.amazon.com/translate/resources/
      - type: FAQ
        url: https://aws.amazon.com/translate/faqs/
      - type: Customers
        url: https://aws.amazon.com/translate/customers/
    overlays:
      - type: APIs.io Search
        url: overlays/translate-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/translate-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:translate
  - name: Amazon Verified Permissions
    description: >-
      Amazon Web Services offers Amazon Verified Permissions, a comprehensive
      permissions management service for applications. By utilizing Verified
      Permissions, developers can control user access through authorization
      based on various factors such as user information, resource attributes,
      and requested actions. This service allows for the creation and storage of
      authorization policies using the Cedar policy language, supporting both
      role-based access control (RBAC) and attribute-based access control (ABAC)
      models. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/verified-permissions/
    baseURL: https://example.com
    tags:
      - Policies
      - Templates
    properties:
      - type: Documentation
        url: https://aws.amazon.com/verified-permissions/
      - type: OpenAPI
        url: properties/verifiedpermissions-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/verified-permissions/features/
      - type: Getting Started
        url: https://aws.amazon.com/verified-permissions/getting-started/
      - type: Pricing
        url: https://aws.amazon.com/verified-permissions/pricing/
      - type: Resources
        url: https://aws.amazon.com/verified-permissions/resources/
      - type: FAQ
        url: https://aws.amazon.com/verified-permissions/faqs/
      - type: Partners
        url: https://aws.amazon.com/verified-permissions/partners/
    overlays:
      - type: APIs.io Search
        url: overlays/verifiedpermissions-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/verifiedpermissions-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:verifiedpermissions
  - name: AWS TrustedAdvisor
    description: >-
      The AWS Trusted Advisor API offers a comprehensive solution to help users
      optimize costs, enhance performance, bolster security and resilience, and
      effectively operate in the cloud at scale. By continuously assessing your
      AWS environment against industry best practices in categories like cost
      optimization, performance, resilience, security, operational excellence,
      and service limits, Trusted Advisor provides actionable recommendations to
      address any areas of concern.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/premiumsupport/technology/trusted-advisor/
    baseURL: https://example.com
    tags:
      - Organizations
      - Recommendations
      - Checks
      - Accounts
      - Resources
      - Lifecycle
    properties:
      - type: Documentation
        url: https://aws.amazon.com/premiumsupport/technology/trusted-advisor/
      - type: OpenAPI
        url: properties/trustedadvisor-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/trustedadvisor-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/trustedadvisor-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:trustedadvisor
  - name: Amazon VPC Lattice
    description: >-
      The Amazon VPC Lattice API is a comprehensive managed application
      networking service designed to seamlessly connect, secure, and monitor all
      services within your organization's various accounts and virtual private
      clouds. By providing a logical boundary for interconnecting microservices
      and legacy services, Amazon VPC Lattice enhances the efficiency of
      discovery and management. Consult the Amazon VPC Lattice User Guide for
      further details.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/vpc/lattice/
    baseURL: https://example.com
    tags:
      - ARN
      - Access
      - Access Log Subscriptions
      - Associations
      - Authentication
      - Authpolicy
      - Deregister
      - Deregister Targets
      - Groups
      - Listeners
      - Logs
      - Networks
      - Policies
      - Register
      - Registertargets
      - Resource Policies
      - Resources
      - Rules
      - Service Network Service Associations
      - Service Network VPC Associations
      - Service Networks
      - Services
      - Subscriptions
      - Tags
      - Target Groups
      - Targets
      - Untag
      - VPC
    properties:
      - type: Documentation
        url: https://aws.amazon.com/vpc/lattice/
      - type: OpenAPI
        url: properties/vpc-lattice-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/vpc/lattice/features/
      - type: Pricing
        url: https://aws.amazon.com/vpc/lattice/pricing/
      - type: FAQ
        url: https://aws.amazon.com/vpc/lattice/faqs/
    overlays:
      - type: APIs.io Search
        url: overlays/vpc-lattice-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/vpc-lattice-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:vpc-lattice
  - name: AWS WAF Classic
    description: >-
      AWS WAF Classic is a web application firewall that allows you to monitor
      HTTP and HTTPS requests directed towards Amazon API Gateway API, Amazon
      CloudFront, or an Application Load Balancer. Additionally, AWS WAF Classic
      enables you to manage access to your content by setting conditions such as
      originating IP addresses or query string values. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: >-
      https://docs.aws.amazon.com/waf/latest/developerguide/classic-waf-chapter.html
    baseURL: https://example.com
    tags:
      - Match
      - Sets
      - Firewalls
    properties:
      - type: Documentation
        url: >-
          https://docs.aws.amazon.com/waf/latest/developerguide/classic-waf-chapter.html
      - type: OpenAPI
        url: properties/waf-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/waf-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/waf-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:waf
  - name: Amazon Connect Voice ID
    description: >-
      Amazon Connect Voice ID is a cutting-edge feature within Amazon Connect
      that leverages machine learning technology to revolutionize caller
      authentication and fraud prevention in voice interactions. While
      traditional contact centers rely on time-consuming knowledge-based
      authentication methods, Voice ID uses the caller's unique voice
      characteristics to provide instant and accurate caller verification at a
      minimal cost. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/connect/voice-id/
    baseURL: https://example.com
    tags:
      - Watchlist
      - Voice
      - Machine Learning
    properties:
      - type: Documentation
        url: https://aws.amazon.com/connect/voice-id/
      - type: OpenAPI
        url: properties/voice-id-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/connect/features/
    overlays:
      - type: APIs.io Search
        url: overlays/voice-id-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/voice-id-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:voice-id
  - name: AWS WAF Classic Regional
    description: >-
      AWS WAF Classic Regional is intended for developers who are implementing
      AWS WAF Classic with AWS resources such as Elastic Load Balancing (ELB)
      Application Load Balancers and API Gateway APIs. For the most up-to-date
      version of AWS WAF, refer to the AWS WAFV2 API and Developer Guide, which
      now offers a unified set of endpoints for both regional and global use.
      The AWS WAF Regional Classic API Reference provides detailed information
      on AWS WAF Classic actions and data types for protecting ELB Application
      Load Balancers and API Gateway APIs. Developers can access these actions
      and data types through the listed endpoints in AWS Regions and Endpoints.
      This guide is designed to offer comprehensive information on API actions,
      data types, and errors for developers using AWS WAF Classic. Additional
      resources and detailed instructions on utilizing AWS WAF Classic can be
      found in the AWS WAF Classic developer guide.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: >-
      https://docs.aws.amazon.com/waf/latest/APIReference/API_Operations_AWS_WAF_Regional.html
    baseURL: https://example.com
    tags:
      - Match
      - Sets
      - Firewalls
    properties:
      - type: Documentation
        url: >-
          https://docs.aws.amazon.com/waf/latest/APIReference/API_Operations_AWS_WAF_Regional.html
      - type: OpenAPI
        url: properties/waf-regional-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/waf-regional-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/waf-regional-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:waf-regional
  - name: AWS Well-Architected Tool
    description: >-
      The API offered by the AWS Well Architected Tool serves as a reliable
      framework to assess your cloud architecture, enabling you to develop
      scalable designs that can adapt and grow over time.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/well-architected-tool/
    baseURL: https://example.com
    tags:
      - ARN
      - Alias
      - Answers
      - Associate
      - Ated
      - Checks
      - Consol
      - Consolidated
      - Details
      - Difference
      - Disassociate
      - Exports
      - Global
      - Import
      - Improvements
      - Invitation
      - Invitations
      - Lens
      - Lenses
      - Milestones
      - Notifications
      - Numbers
      - Profiles
      - Questions
      - Reports
      - Resources
      - Reviews
      - Settings
      - Share
      - Shares
      - Summaries
      - Tags
      - Templates
      - Untag
      - Upgrade
      - Versions
      - Workloads
    properties:
      - type: Documentation
        url: https://aws.amazon.com/well-architected-tool/
      - type: OpenAPI
        url: properties/wellarchitected-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/well-architected-tool/features/
      - type: Pricing
        url: https://aws.amazon.com/well-architected-tool/pricing/
      - type: Partners
        url: https://aws.amazon.com/well-architected-tool/partners/
      - type: Customers
        url: https://aws.amazon.com/well-architected-tool/customers/
      - type: FAQ
        url: https://aws.amazon.com/well-architected-tool/faqs/
      - type: Resources
        url: https://aws.amazon.com/well-architected-tool/resources/
    overlays:
      - type: APIs.io Search
        url: overlays/wellarchitected-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/wellarchitected-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:wellarchitected
  - name: AWS WAF
    description: >-
      AWS WAF is a powerful web application firewall designed to safeguard your
      AWS resources by monitoring and managing incoming web requests. It offers
      protection for various resources like Amazon CloudFront distributions,
      Amazon API Gateway REST APIs, Application Load Balancers, and AWS AppSync
      GraphQL APIs.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://docs.aws.amazon.com/waf/
    baseURL: https://example.com
    tags:
      - ACL
      - Web
      - Firewalls
      - Security
    properties:
      - type: Documentation
        url: https://docs.aws.amazon.com/waf/
      - type: OpenAPI
        url: properties/wafv2-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/wafv2-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/wafv2-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:wafv2
  - name: Amazon WorkMail
    description: >-
      Amazon WorkMail is a secure and managed business email and calendar
      service that allows users to access their email, contacts, and calendars
      through various client applications such as Microsoft Outlook, native iOS
      and Android email apps, and web browsers. It supports integration with
      corporate directories, email journaling for compliance, encryption key
      control, and data storage location control. Additionally, Amazon WorkMail
      offers interoperability with Microsoft Exchange Server and programmable
      management of users, groups, and resources through the Amazon WorkMail
      SDK.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/workmail/
    baseURL: https://example.com
    tags:
      - Users
    properties:
      - type: Documentation
        url: https://aws.amazon.com/workmail/
      - type: OpenAPI
        url: properties/workmail-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/workmail/features/
      - type: Pricing
        url: https://aws.amazon.com/workmail/pricing/
      - type: Resources
        url: https://aws.amazon.com/workmail/resources/
      - type: FAQ
        url: https://aws.amazon.com/workmail/faqs/
      - type: Features
        url: https://aws.amazon.com/workmail/features/
    overlays:
      - type: APIs.io Search
        url: overlays/workmail-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/workmail-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:workmail
  - name: Amazon WorkSpaces
    description: >-
      Amazon WorkSpaces Service is a cloud-based platform that allows you to
      easily provision virtual desktops for your users, eliminating the need for
      hardware procurement and complex software installation. With WorkSpaces,
      you can quickly add or remove users as needed and provide access to
      virtual desktops from various devices and web browsers. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/workspaces/
    baseURL: https://example.com
    tags:
      - Images
      - Permission
      - Workspaces
    properties:
      - type: Documentation
        url: https://aws.amazon.com/workspaces/
      - type: OpenAPI
        url: properties/workspaces-openapi-original.yml
      - type: Pricing
        url: https://aws.amazon.com/workspaces/pricing/
      - type: Web
        url: https://aws.amazon.com/workspaces/web/
      - type: Thin-client
        url: https://aws.amazon.com/workspaces/thin-client/
      - type: All-inclusive
        url: https://aws.amazon.com/workspaces/all-inclusive/
      - type: Core
        url: https://aws.amazon.com/workspaces/core/
    overlays:
      - type: APIs.io Search
        url: overlays/workspaces-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/workspaces-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:workspaces
  - name: Amazon WorkSpaces Thin Client
    description: >-
      The Amazon WorkSpaces Thin Client API is designed for use with Amazon Web
      Services End User Computing (EUC) virtual desktops, providing users with a
      cost-effective cloud desktop solution. The compact WorkSpaces Thin Client
      device supports up to two monitors and various peripherals, such as
      keyboards, mice, headsets, and webcams.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/workspaces/thin-client/
    baseURL: https://example.com
    tags:
      - ARN
      - Deregister
      - Device
      - Devices
      - Environments
      - Resources
      - Sets
      - Software
      - Software Sets
      - Tags
      - Untag
    properties:
      - type: Documentation
        url: https://aws.amazon.com/workspaces/thin-client/
      - type: OpenAPI
        url: properties/workspaces-thin-client-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/workspaces/thin-client/features/
      - type: Pricing
        url: https://aws.amazon.com/workspaces/thin-client/pricing/
      - type: Getting Started
        url: https://aws.amazon.com/workspaces/thin-client/getting-started/
      - type: Resources
        url: https://aws.amazon.com/workspaces/thin-client/resources/
      - type: FAQ
        url: https://aws.amazon.com/workspaces/thin-client/faqs/
    overlays:
      - type: APIs.io Search
        url: overlays/workspaces-thin-client-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/workspaces-thin-client-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:workspaces-thin-client
  - name: Amazon WorkDocs
    description: >-
      The Amazon WorkDocs API is tailored for a variety of use cases, including
      file migration, security applications, and eDiscovery/analytics. The API
      supports file migration applications for users looking to transfer files
      from different systems, while also allowing for basic metadata changes.
      Security applications can utilize the API actions to detect changes in
      WorkDocs and take necessary actions to ensure data security. General
      administrative applications, such as eDiscovery and analytics, can record
      and replicate data from WorkDocs for backup and analysis purposes. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/workdocs/
    baseURL: https://example.com
    tags:
      - Activation
      - Activities
      - Comments
      - Contents
      - Current
      - Custom
      - Deactivate
      - Describe
      - Documents
      - Folders
      - Groups
      - Initiate
      - Labels
      - Me
      - Metadata
      - Notifications
      - Organizations
      - Paths
      - Permission
      - Permissions
      - Principals
      - Removes
      - Resources
      - Restore
      - Root
      - Search
      - Subscriptions
      - Uploads
      - Users
      - Versions
    properties:
      - type: Documentation
        url: https://aws.amazon.com/workdocs/
      - type: OpenAPI
        url: properties/workdocs-openapi-original.yml
      - type: SDK
        url: https://aws.amazon.com/workdocs/sdk/
      - type: Pricing
        url: https://aws.amazon.com/workdocs/pricing/
      - type: Resources
        url: https://aws.amazon.com/workdocs/resources/
      - type: FAQ
        url: https://aws.amazon.com/workdocs/faq/
    overlays:
      - type: APIs.io Search
        url: overlays/workdocs-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/workdocs-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:workdocs
  - name: AWS WorkMail Message Flow
    description: >-
      The WorkMail Message Flow API provides access to email messages as they
      are being sent and received by a WorkMail organization.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://docs.aws.amazon.com/workmail/
    baseURL: https://example.com
    tags:
      - Content
      - Messages
      - Raw
    properties:
      - type: Documentation
        url: https://docs.aws.amazon.com/workmail/
      - type: OpenAPI
        url: properties/workmailmessageflow-openapi-original.yml
    overlays:
      - type: APIs.io Search
        url: overlays/workmailmessageflow-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/workmailmessageflow-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:workmailmessageflow
  - name: WorkSpaces Web
    description: >-
      The WorkSpaces Web API is a cost-effective, fully managed solution
      designed to support secure web-based workloads. It streamlines the process
      of granting employees access to internal websites and SaaS web
      applications without the need for complex appliances or specialized client
      software. 
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/workspaces/web/
    baseURL: https://example.com
    tags:
      - ARN
      - Access
      - Browser
      - Certificates
      - Disassociate
      - Entities
      - Er
      - Ers
      - IP
      - Identity
      - Logging
      - Metadata
      - Networks
      - Portals
      - Prov
      - Providers
      - Resources
      - Services
      - Settings
      - Store
      - Stores
      - Tags
      - Trust
      - Untag
      - Users
    properties:
      - type: Documentation
        url: https://aws.amazon.com/workspaces/web/
      - type: OpenAPI
        url: properties/workspaces-web-openapi-original.yml
      - type: Pricing
        url: https://aws.amazon.com/workspaces/web/pricing/
      - type: FAQ
        url: https://aws.amazon.com/workspaces/web/faqs/
      - type: Resources
        url: https://aws.amazon.com/workspaces/web/resources/
    overlays:
      - type: APIs.io Search
        url: overlays/workspaces-web-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/workspaces-web-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:workspaces-web
  - name: AWS X-Ray
    description: >-
      AWS X-Ray offers comprehensive visibility into the flow of requests within
      your application, allowing you to analyze and filter visual data
      pertaining to payloads, functions, traces, services, APIs, and other
      components. Utilizing both no-code and low-code actions, AWS X-Ray
      provides a seamless way to track and manage requests throughout your
      application.
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://aws.amazon.com/xray/
    baseURL: https://example.com
    tags:
      - Batches
      - Configurations
      - Encryption
      - Events
      - Graphs
      - Groups
      - Impact
      - Insights
      - Policies
      - Records
      - Resources
      - Rules
      - Sampling
      - Segments
      - Series
      - Services
      - Statistics
      - Summaries
      - Tags
      - Targets
      - Telemetry
      - Time
      - Traces
      - Untag
    properties:
      - type: Documentation
        url: https://aws.amazon.com/xray/
      - type: OpenAPI
        url: properties/xray-openapi-original.yml
      - type: Features
        url: https://aws.amazon.com/xray/features/
      - type: Pricing
        url: https://aws.amazon.com/xray/pricing/
      - type: Getting Started
        url: https://aws.amazon.com/xray/getting-started/
      - type: Resources
        url: https://aws.amazon.com/xray/resources/
      - type: FAQ
        url: https://aws.amazon.com/xray/faqs/
    overlays:
      - type: APIs.io Search
        url: overlays/xray-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/xray-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:xray
common:
  - type: Portal
    url: https://aws.amazon.com/
  - type: Developer
    url: https://aws.amazon.com/developer/
  - type: About
    url: https://aws.amazon.com/about-aws/
  - type: Documentation
    url: https://docs.aws.amazon.com/
  - type: Getting Started
    url: https://aws.amazon.com/getting-started/
  - type: Tools
    url: https://aws.amazon.com/developer/tools/
  - type: SDKs
    url: https://aws.amazon.com/developer/tools/
  - type: C++
    url: https://aws.amazon.com/developer/language/cpp/
  - type: .NET
    url: https://aws.amazon.com/developer/language/net/
  - type: Go
    url: https://aws.amazon.com/developer/language/go/
  - type: JavaScript
    url: https://aws.amazon.com/developer/language/javascript/
  - type: Java
    url: https://aws.amazon.com/developer/language/java/
  - type: Kotlin
    url: https://aws.amazon.com/developer/language/kotlin/
  - type: PHP
    url: https://aws.amazon.com/developer/language/php/
  - type: Python
    url: https://aws.amazon.com/developer/language/python/
  - type: Ruby
    url: https://aws.amazon.com/developer/language/ruby/
  - type: Rust
    url: https://aws.amazon.com/developer/language/rust/
  - type: Swift
    url: https://aws.amazon.com/developer/language/swift/
  - type: Command Line Interface
    url: https://docs.aws.amazon.com/cli/
  - type: Open Source
    url: https://aws.amazon.com/opensource/
  - type: Blog
    url: https://aws.amazon.com/blogs/
  - type: Press
    url: https://press.aboutamazon.com/press-release-archive
  - type: Investors
    url: https://ir.aboutamazon.com/overview/default.aspx
  - type: Analysts
    url: https://aws.amazon.com/resources/analyst-reports/
  - type: Support
    url: https://aws.amazon.com/premiumsupport/
  - type: Support Plans
    url: https://aws.amazon.com/premiumsupport/plans/
  - type: Support FAQs
    url: https://aws.amazon.com/premiumsupport/faqs/
  - type: Professional Services
    url: https://aws.amazon.com/professional-services/
  - type: Managed Services
    url: https://aws.amazon.com/managed-services/
  - type: Contact
    url: https://aws.amazon.com/contact-us/
  - type: Events
    url: https://aws.amazon.com/events/
  - type: Webinars
    url: https://aws.amazon.com/events/innovation-webinars/
  - type: Forum
    url: https://repost.aws/
  - type: Whats New
    url: https://aws.amazon.com/new/
  - type: Pricing
    url: https://aws.amazon.com/pricing/
  - type: Free Tier
    url: https://aws.amazon.com/free/
  - type: Pricing Calculator
    url: https://calculator.aws/
  - type: Cost Management
    url: https://aws.amazon.com/aws-cost-management/
  - type: Legal
    url: https://aws.amazon.com/legal/    
  - type: Terms of Service
    url: https://aws.amazon.com/serviceterms/
  - type: Privacy Policy
    url: https://aws.amazon.com/privacy/
  - type: Customer Agreement
    url: https://aws.amazon.com/agreement/
  - type: Service Level Agreements
    url: https://aws.amazon.com/legal/service-level-agreements/
  - type: Acceptable Use Policy
    url: https://aws.amazon.com/aup/
  - type: Trademark
    url: https://aws.amazon.com/trademark-guidelines/
  - type: LinkedIn
    url: https://www.linkedin.com/company/amazon-web-services/
  - type: Twitter
    url: https://twitter.com/awscloud
  - type: Facebook
    url: https://www.facebook.com/amazonwebservices
  - type: Instagram
    url: https://www.instagram.com/amazonwebservices/
  - type: Twitch
    url: https://www.twitch.tv/aws
  - type: YouTube
    url: https://www.youtube.com/user/AmazonWebServices/Cloud/
  - type: Knowledge Center
    url: https://repost.aws/knowledge-center
  - type: Podcast
    url: https://aws.amazon.com/podcasts/
  - type: Case Studies
    url: https://aws.amazon.com/solutions/case-studies/
  - type: Industries
    url: https://aws.amazon.com/industries/
  - type: Solutions
    url: https://aws.amazon.com/solutions/
  - type: White Papers
    url: https://aws.amazon.com/whitepapers/
  - type: Architecture
    url: https://aws.amazon.com/architecture/
  - type: Executive Insights
    url: https://aws.amazon.com/executive-insights/
  - type: Partners
    url: https://aws.amazon.com/partners/
  - type: Marketplace
    url: https://aws.amazon.com/marketplace
  - type: Training
    url: https://aws.amazon.com/training/
  - type: Careers
    url: https://aws.amazon.com/careers/
  - type: Students
    url: https://community.aws/students
  - type: Education
    url: https://aws.amazon.com/education/
  - type: Security
    url: https://aws.amazon.com/security/
  - type: Accessibility
    url: https://aws.amazon.com/accessibility/
  - type: SignUp
    url: https://portal.aws.amazon.com/billing/signup
  - type: Login
    url: https://signin.aws.amazon.com/signin
  - type: Console
    url: https://console.aws.amazon.com
  - type: Billing
    url: https://console.aws.amazon.com/billing/home
  - type: Credentials
    url: https://console.aws.amazon.com/iam/home
  - type: Health Dashboard
    url: https://phd.aws.amazon.com/
maintainers:
  - FN: API Evangelist
    url: https://apievangelist.com
    email: info@apievangelist.com
overlays:
  - type: APIs.io Search
    url: overlays/apis-io-search.yml
```
That bad boy is 13,341 lines long, and has just shy of 300 individual APIs indexed, complete with individual properties for each API, but also an impressive list of common properties--something I will turn into a blueprint shortly. 

This [APIs.json is the search overlay](https://github.com/api-search/cloud/blob/main/_apis/amazon-web-services/overlays/apis-io-search.yml) I am applying to the [AWS APIs.json index](https://github.com/api-search/cloud/blob/main/_apis/amazon-web-services/apis.md?plain=1) that I generate from their SDK manifest. Then I map out all of the other individual API properties, including the OpenAPI, and many other common properties. You can see it all in action in the APis.io cloud node, where I am doing the same to Azure, Google, and other cloud providers. 

There is a lot of learnings in that APIs.json file. It isn't complete, but it is the most complete we have. I am going to move onto Azure and some other adjacent APIs to change things up. But after a while, I will come back and group tags, generate an APIs.json blueprint, and see what other goodness I can squeeze out of this machine-readable landscape map for AWS.