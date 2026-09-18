---
title: PEX Suite - system extension suite
description: This is a suite of applications that can be centrally deployed and expand the native capabilities of Proclaim (Case management software).
tags:
  - SOAP
  - csharp
  - Proclaim
  - ODBC
---

_This was developed internally for a large solicitor's firm to extend their case management system._

PEX was a suite of centrally deployed applications that expanded the native capabilities of Proclaim, the case management platform used by the business.

The core of the system was an application host that ran the other applications in a coordinated, synchronous manner and fed results back into Proclaim.

Several tools were built on top of the PEX framework. One example was an automatic translator that allowed Polish call handlers to capture information in Polish and then translate it into English with guided assistance for downstream processing. Another module was a custom history picker UI for selecting arbitrary items from case history; this used a custom REST API that read directly from the Proclaim database via ODBC.

The most feature-rich module was a PDF and document manipulator. It accepted a document code from either the history picker or an embedded field and allowed users to select arbitrary pages from a source document, returning the extracted pages as a new PDF for later use. It could also split a document exactly in two, with all pages placed into one or the other output file, which was particularly useful for separating invoices from third-party reports.