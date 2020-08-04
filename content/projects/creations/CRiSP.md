---
title: CRiSP
description: This suite of interdependent systems that together manage the Policy management system for an insurance company.
featured: true
tags:
  - REST
  - csharp
  - GraphQL
  - SQL Server
  - RabbitMQ
  - MassTransit
  - .Net Core
  - TypeScript
  - TeamCity
  - Octopus Deploy
  - Azure DevOps
  - Jira
  - Aurelia
  - Entity Framework
---

_This is a piece developed internally for an insurance company to replace their old/externally developed and maintained policy management system._

CRiSP is made up of a core Web API which acts as the gateway to the (Entity Framework based) DB layer and business logic layers from the UI applications. We expose 2 separate APIs, a standard REST based aspnet.net WebAPI based solution and a newer GraphQL API (which we are in the progress of migrating to). 

The Web API layer also has a service bus and windows server layer to offload longer runner or asynchronous workloads, such as email delivery, document rendering etc. This is also the layer that runs all our scheduled jobs, with a separate Quartz.net based service that just enqueues work to be done where we use our robust distributed locking system to ensure that schedule tasks aren't running concurrently without having to add complicated de duplication logic to our message queue server.

The API is secured using an custom Identity Server solution that provides JWTs verified by multiple authentication sources, be it bcrypt hashed local passwords, for external users, or offloading to Active Directory to authenticate passwords of internal staff, or even providing true windows authentication endpoints to allow our desktop based solutions to work with no authentication prompts.

Main back office interface is an Aurelia based SPA application written using TypeScript which integrates directly with the ID server and the API servers to provide secured and limited access to Policy data.

We have a client facing extranet primarily developed using a mixture of Razor Pages and vanilla JavaScript.

We also have a dedicated portal targeting our field surveying staff where they provide updates and reports on an ongoing bases regarding the properties being built and signing them off as fit for warranty cover also primarily developed using a mixture of Razor Pages and vanilla JavaScript.

My role in this project is acting as Lead developer, where I manage the overall architectural vision for the solution making final design decisions on language an technology choices as well as initiating and prototyping out new components/systems being included into the over design and also mentor and guide the rest of the development team of 10 on the project.


