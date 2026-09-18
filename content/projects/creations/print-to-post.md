---
title: EDS/Print to Post 
description: This is a complex enterprise application and framework to provide a simplified workflow for send out mail to clients and other third parties.
featured: true
tags:
  - SOAP
  - csharp
  - REST
  - Proclaim
  - ODBC
  - WPF
---

_This was developed internally for a large solicitor's firm to replace an older system._

EDS/Print to Post was a complex enterprise application and framework designed to simplify the workflow for sending outgoing mail to clients and other third parties.

EDS was a suite of integrated applications that worked together to produce a single combined letter pack for printing, enveloping, and posting. It operated at several stages: first, it integrated deeply with Proclaim, the case management system, to retrieve recently generated documents and any other associated case files. Next, it provided a normalization workflow that converted the wide variety of documents produced or imported into Proclaim into a common format for later processing, primarily PDF documents. It then provided a UI to bundle multiple documents into a single posting pack and included a review workflow for managers before the pack was sent.

Once packs were dispatched, a second client application accessed the document packs and fed them to a large printer for final packing and enveloping in the most efficient way for the post-room team. Finally, after printing, the system imported the packs back into Proclaim for tracking and accountability. It also included a web interface for reviewing audit logs covering each modification made to the pack throughout the process.

_The new system had to interoperate fully with the legacy system, synchronizing printing data in both directions during rollout to minimize disruption for end users._