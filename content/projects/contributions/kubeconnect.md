---
title: "KubeConnect"
link: "https://github.com/tocsoft/KubeConnect"
description: "A cli for exposing exposing the services and ingresses of a Kubernetes cluster to the users local machine."
featured: true
tags: ["csharp","dotnet","kubernetes"]
weight: 90
sitemap: 
    priority : 0.8
---
KubeConnect is a cli tool that will exposes all the services and ingresses in a namespace of a local or remote Kubernetes cluster.

It exposes all the services and updates local DNS so that services can be accessed in the same as they would be accessible from inside the cluster.

Additionally it acts as a ingress endpoint for exposing the namespaces ingresses on the local machine. Ingress hosting also includes generating trusted local ssl certificates for accessing via https.