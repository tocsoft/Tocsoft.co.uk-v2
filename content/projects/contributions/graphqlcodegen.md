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

A template-driven code generator for converting GraphQL queries into strongly typed classes for both TypeScript and C#.

This library is published as both a NuGet package and an npm package to support integration with a range of build pipelines for build-time code generation.

The MSBuild integration also supports design-time feedback and error reporting, so once the queries are defined, there is no additional setup required beyond installing the NuGet package.

This was primarily developed from my work on [CRiSP](/projects/creations/crisp/), where I wanted to give my team a fast and intuitive development experience as we introduced GraphQL APIs into our stack.