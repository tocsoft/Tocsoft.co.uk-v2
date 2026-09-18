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

_This system was developed internally for an insurance company to replace an older externally maintained policy management platform._

CRiSP was composed of a core Web API that acted as the gateway between the UI applications and the Entity Framework-based database and business logic layers. It exposed two separate APIs: a standard REST-based ASP.NET Web API solution and a newer GraphQL API that was being progressively adopted during the migration phase.

The Web API layer also included a service bus and Windows Service worker layer to offload longer-running or asynchronous workloads, such as email delivery and document rendering. This was also the layer responsible for scheduled jobs, with a separate Quartz.NET-based service that simply enqueued work to be processed. A robust distributed locking system was used to ensure scheduled tasks did not run concurrently without adding complex deduplication logic to the message queue infrastructure.

The API was secured using a custom Identity Server solution that provided JWTs verified by multiple authentication sources. This included bcrypt-hashed local passwords for external users, Active Directory authentication for internal staff, and true Windows authentication endpoints to support desktop-based solutions without repeated authentication prompts.

The main back-office interface was an Aurelia-based SPA written in TypeScript, which integrated directly with the identity server and the API layer to provide secure, limited access to policy data.

The project also included a client-facing extranet, primarily developed using a mix of Razor Pages and vanilla JavaScript, as well as a dedicated portal for field survey staff to update and report on properties under construction and sign them off as fit for warranty cover.

My role in this project was that of Lead Developer, where I was responsible for the overall architectural vision of the solution, made final technology and language choices, initiated and prototyped new components and systems, and mentored the wider development team during the project’s delivery phase.


