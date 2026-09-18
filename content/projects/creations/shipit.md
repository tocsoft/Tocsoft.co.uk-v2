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

ShipIt is a tool and application for creating composable packages that can be centrally configured and combined into a complete Kubernetes-based application.

ShipIt has four distinct parts:

1. Package management: this allows for creating `shipit` packages that can be published to a container registry and later referenced during deployment.
2. Configuration management: this enables cluster-wide settings to be configured and then consumed and exposed by packages as part of deployment.
3. Deployment lifecycle management: this allows applications to be deployed in a strict sequence, with each component validated before the next is released. This supports blue-green deployments and helps achieve zero application downtime.
4. Application management UI: the application also runs a web UI that can be deployed into the cluster, enabling teams to manage component versions and update system-specific target versions.