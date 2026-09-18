---
title: "KubeConnect"
link: "https://github.com/tocsoft/KubeConnect"
description: "A cli for exposing the services and ingresses of a Kubernetes cluster to be accessible from the users local machine."
featured: true
tags: ["csharp","dotnet","kubernetes"]
weight: 90
sitemap: 
    priority : 0.8
---
KubeConnect is a CLI tool that port-forwards all services and ingresses in a namespace of a local or remote Kubernetes cluster to the user’s local machine.

It exposes all services and updates local DNS so they can be accessed the same way they would be from inside the cluster.

In addition to exposing services, it also acts as an ingress endpoint for exposing ingresses to the local machine, including forcing local DNS entries. Ingress hosting also includes generating trusted local SSL certificates for HTTPS access.