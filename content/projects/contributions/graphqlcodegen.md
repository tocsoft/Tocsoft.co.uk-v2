---
title: "GraphQL CodeGen"
link: "https://github.com/tocsoft/GraphQLCodeGen"
description: "A template driven code generator for converting graphql queries into a strongly typed classes for both TypeScript and C#."
featured: true
tags: ["csharp","dotnet","Appveyor", "GraphQL", "TypeScript", "MSBuild", "npm"]
weight: 110
sitemap: 
    priority : 0.8
---

A template driven code generator for converting GraphQL queries into a strongly typed classes for both TypeScript and C#.

This library is released as an both a NuGet and npm package to enable integrating with various build pipelines for build time code generation.

MSBuild integration even allows for design time and and error output integrations so you just have to design your Queries and away you go nothing to install just the NuGet package.

This was primarily developed due to may work on [CRiSP](/projects/creations/crisp/) as I wanted a way for my team to have a very quick and intuitive development experience when we added GraphQL APIs into our stack.