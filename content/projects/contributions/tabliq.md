---
title: "Tabliq"
link: "https://github.com/FatedCreations/Tabliq"
description: "A custom SQL parser, query rewriting, and validation engine for schema-aware SQL transformation."
featured: true
tags: ["csharp","dotnet","sql"]
weight: 80
sitemap:
    priority: 0.8
---

Tabliq is a schema-aware SQL parsing, validation, and transformation engine built to help applications reason about SQL without depending on a live database.

At its core, Tabliq allows SQL to be inspected, validated, and rewritten in a controlled and deterministic way. It is designed for scenarios where a logical data model must be separated from the physical database implementation, while still allowing queries to be executed safely and consistently.

Key capabilities include:

1. Support for custom virtual schemas
2. Hooks and tooling to bind queries to a virtual schema
3. Validation of missing tables and columns without hitting a database
4. SQL rewriting across dialects, such as converting ANSI SQL to T-SQL
5. Rewriting tables as subqueries where required by downstream logic or compatibility constraints
6. Full schema-level transformation, enabling logical names to map to physical tables and columns while preserving the external shape of the result set

This means a query written against a logical schema can be translated to a different physical schema without altering the contract seen by consumers. For example, a virtual table named "people" with a column "id" can be mapped to a real database table such as "dbo.users" with a column such as "userid", while the result columns remain consistent and transparent to the consumer.

Tabliq is particularly useful for query abstraction, database portability, validation pipelines, SQL translation, and schema-driven data access layers. It helps bridge the gap between logical intent and physical execution, making complex SQL transformations easier to manage and reason about.