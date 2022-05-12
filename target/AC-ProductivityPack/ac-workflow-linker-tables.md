---
title: Workflow linker tables | Microsoft Docs
description: Workflow linker tables
author: ac-kunes
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Czech, Workflow linker tables, additional functions
ms.author: v-makune
---
# WorkFlow - Linker Tables

The Workflow – Linker Tables add-on extends the functionality of the Workflow add-on by the ability to check records or fields in tables bound to a table that is controlled by workflow.
The workflow status is then allowed to be changed only if all checks within the inspected tables are compliant. Practical uses may include the following:

- If a workflow is applied to a document with a header and lines, such as on a Sales order, you can check whether there are any lines or lines of any type or content for the header. For example, that the order contains at least one line with the goods, or that it has a price or location or glob filled in on all lines.
- It is possible to check whether the source record for any field in the table with the workflow used contains the necessary data in other fields – for example, if the Salesperson Code field is filled in on the document header, then it checks whether this salesperson has filled in the email.

![WorkFlow - Linker Tables](media/workflow_tables.png " WorkFlow - Linker Tables")

**See also**

[WorkFlow - Linker Tables - Setup](ac-workflow-linker-tables-setup.md)  
[Productivity Pack](ac-productivity-pack.md)

