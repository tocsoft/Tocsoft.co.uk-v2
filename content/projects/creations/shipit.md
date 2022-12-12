---
title: ShipIt
description: This is a cli/web package and configuration manager for Kubernetes applications made up of multiple distinct but interdependent services.
featured: false
tags:
  - csharp
  - Kubernetes
  - Docker
  - .Net Core
---

ShipIt is tool and application used to create composable packages that can be centrally configured and combined into a complete Kubernetes based application.

ShipIt has 4 distinct parts, 
1. package management, this allows for creating `shipit` packages that can be published to a container registry and then later referenced in a deployment.
2. configuration management, this allows for configuring a cluster for settings that then are consumed and exposed from the packages as part of a deployment. 
3. deployment lifetime management, this allows for deploying the packages with a very strict pattern, deploying each component  in turn, monitoring for success before deploying the next component, allowing for a blue green deployment model and thus zero application downtime.
The Web API layer also has a service bus and windows server layer to offload longer runner or asynchronous workloads, such as email delivery, document rendering etc. This is also the layer that runs all our scheduled jobs, with a separate Quartz.net based service that just enqueues work to be done where we use our robust distributed locking system to ensure that schedule tasks aren't running concurrently without having to add complicated de duplication logic to our message queue server.
4. application also runs a web UI, that can be deployed into the cluster, that can be used to manage component versions and update the system specific target versions.