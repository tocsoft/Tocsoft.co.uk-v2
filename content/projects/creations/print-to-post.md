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

_This is a piece developed internally for a large solicitors replacing a previous system._

This is a complex enterprise application and framework to provide a simplified workflow for send out mail to clients and other third parties.

EDS is a suite of applications/systems that all integrate to produce a single combined letter pack that must be printed enveloped and posted out it does this at a few levels. Deeply integrating with Proclaim (the case management system) to extract recently generated documents and access any other documents associated with the case. Next is provides a normalisation document processing workflow to take the multitude of documents produce or imported into proclaim and convert them into a common format for later manipulation(PDFs). No it provides a UI to bundle multiple documents together into a single document pack for posting and in the same UI provide a workflow to allow managers to review the pack before they are sent on. Once packs are sent we have a second client application that can access the document packs and intelligently feeds them to a large printer for the final packing the enveloping in the most efficient way for the post-room team to envelope and post. Finally, once printed, the last step then imports the document packs back into Proclaim for tracking and accountability. Also providing a web interface for seeing the audit logs for all the modifications on the pack as it passed though the various stages.

_This new system had to fully inter-operate with the old system with two way syncing of printing data while it was rolled out across the company so we could minimize impact that most users experienced._