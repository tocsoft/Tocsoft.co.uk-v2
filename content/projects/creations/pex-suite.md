---
title: PEX Suite - system extension suite
description: This is a suite of applications that can be centrally deployed and expand the native capabilities of Proclaim (Case management software).
featured: true
tags:
  - SOAP
  - csharp
  - Proclaim
  - ODBC
---

_This is a piece developed internally for a large solicitors to extend their case management system._

This is a suite of applications that can be centrally deployed and expand the native capabilities of Proclaim (Case management software).

PEX is made up of multiple applications the core being an application host that runs the other application in a synchronous manor allowing for a results to be fed back into Proclaim.

A few of the tools that have been written on top the PEX Framework include, automatic translators allowing Polish call handlers to collect data in Polish and then automatically(with guidance) translate the text to English for further use.

Another PEX module/application is a custom history picker UI which can be used to choose arbitrary items from the history, this uses a custom REST API that in-turn talks direct to the Proclaim DB via ODBC.

The most feature full module was a PDF/document manipulator that can be fed a document code(taken from history picker or embedded field) and will allow the end user select arbitrary pages out of the source document and return the extracted parts as a new PDF for later use, or it can be used for splitting a document exactly in 2 pieces with all the pages in one of the other (useful for splitting invoices off third party reports).