---
title: Workflow status management | Microsoft Docs
description: Workflow status management
author: ac-kunes
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Czech, Workflow status management, additional functions
ms.author: v-makune
---
# WorkFlow - State Management

The **State Management** add-on adds status management tools to Microsoft Dynamics 365 Business Central as one or more users process jobs sequentially. Allows you to configure the processing states in which the task (document, record) can be located. It also allows you to monitor the current status and progress of processing and then automatically fill in forms and records with defined values or run any program actions when the status of the task (document, record) changes. It is mainly used for controlled approval and circulation of documents.

The Status Management add-on is all about the correct settings. If you want to use this add-on, the main functionality is the status change.

## Status change
To move to the next stage of solving a task (document, record), click on the **Process** function and then on the **Change Status** option (you can also find this function in the information panel for the task, document or record for which state control is set)

![State Management - Status Management Templates](media/WF_change_status.png)

When you click on this function, additional state control states are offered, which according to the definition of the next state filter are considered.

When the operation is complete, the **Status Management Status Code** on the Job, Document, or Record tab is updated.

## Checked Tables

The function of the checked table extends the functionality of the State Management add-on by the ability to check records or fields in tables bound to a table that is controlled by Status management.

The Status Management status is then allowed to be changed only if all checks within the scanned tables match. Practical uses may include the following:

- If Status Management is used on a voucher with headers and lines, such as a Sales Order, you can check whether there are any lines or lines of any type or content for the header. For example, that the order contains at least one line with the item, or that it has a price or location or global dimension filled in on all lines.
- It is possible to check whether the source record for any field in the table with the used Status Management contains the necessary data in other fields - eg if the Vendor code field is filled in the document header, then it checks whether this seller has filled in the email.

![WorkFlow - Checked Tables](media/workflow_tables.png " WorkFlow - Checked Tables")

## See also

[WorkFlow - State Management - Setup](ac-workflow-status-management-setup.md)  
[Productivity Pack](ac-productivity-pack.md)
