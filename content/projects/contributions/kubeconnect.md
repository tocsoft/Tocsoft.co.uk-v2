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
KubeConnect is a cli tool that will port forward all the services and ingresses in a namespace of a local or remote Kubernetes cluster to the users local machine.

It exposes all the services and updates local DNS so that services can be accessed in the same as they would be accessible from inside the cluster.

Along with exposing the services it also acts as a ingress endpoint for exposing the ingresses to the local machine (including forcing DNS entries in locally). Ingress hosting also includes generating trusted local SSL certificates for accessing via https.