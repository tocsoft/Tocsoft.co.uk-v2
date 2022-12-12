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

_This is a tool developed internally for a startup in the data visualization and analytics space._

Localdev is a tool developed to automate setup and development of our core product on both development machines using
minikube and remote Kubernetes clusters alike (to facilitate developers working on lower grade hardware). It works by
normalizing the process of setting up a cluster (or connecting to the remove cluster) configuring it to run all the
development pieces of the product, seeding databases etc.

It can also be used to connect into the cluster (local or remote) exposing all the services as though they were running
locally and also bridging in a local service so that it is exposed to service running remotely. This drastically reduces
platform knowledge required to make changes, instead of having to understand you need these 20 services running and SQL
server running, then reconfiguring all of those so the correct ports etc are used (a setup process that could take upwards
of a week at times get 100% right) got down to a single command line call. In addition to the setup, it also supports
resetting/snapshotting so that once you have completed work on an area you can simply reset back to a well-known state
and carry on working on a separate change. (Great for integration testing).

The tool is even simple enough for other people not actively developing the product (CTO etc) being able to use it as a
sales tool to demonstrate the product offline.
