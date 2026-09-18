---
title: Localdev
description: A tool developed to automate setup and development of our core product on both development machines using minikube and remote Kubernetes clusters alike 
featured: true
weight: 10
tags:
  - PowerShell
  - csharp
  - SQL Server
  - RabbitMQ
  - Kubernetes
  - AKS
  - Docker
  - MiniKube
---

_This tool was developed internally for a startup in the data visualization and analytics space._

Localdev is a tool created to automate the setup and development of our core product across both local developer machines or remote Kubernetes clusters. It normalizes the process of setting up a cluster, connecting to the environment, configuring the required services, and seeding databases.

The tool can also connect into either a local or remote cluster and expose all services as though they were running locally. It can bridge local services so they are visible to workloads running remotely. This significantly reduces the platform knowledge required to make changes. Instead of understanding and configuring a large set of services, SQL Server, and port mappings manually (a setup process that could take several days to get right), the process is reduced to a single command-line call.

In addition to setup, Localdev supports reset and snapshot workflows so that once work on one area is complete, teams can quickly revert to a known state and continue working on another change. This is especially useful for integration testing.

The tool is simple enough for non-developers, such as engineering leadership or sales stakeholders, to use as a demonstration aid for showcasing the product offline.
