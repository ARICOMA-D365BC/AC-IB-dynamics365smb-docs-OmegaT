---
title: Autocont - Pack Tracking Basic | Microsoft Docs
description:  This section describes Autocont Pack Tracking Basic AddOn
author: ACPJanousek
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Pack tracking, inventory, item, report,
ms.date: 01/31/2020 TODO
ms.author: v-pejano
---

# Pack Tracking Basic (EKOKOM)
Pack Tracking Basic module is an extension of the Inventory area.  
The module establishes a separate packaging record linked to the inventory area and standard goods movements (purchase, sale, receipt, issue, transfer, consumption and production).

Pack Tracking contains a classification of the types of packaging. t allows you to manage any number of documents for the needs of packaging reporting required internally by the company or legislation (the basic parameterization of the EKO-KOM report for the purposes of reporting by the relevant persons pursuant to the Packaging Act No. 477/2001 Coll. is part of it).

Packing entries are automatically leveled in the background during the movement of items, and therefore the processing of documents for the Pack Tracing does not burden the user in any way.
The output of the module is the print report **Packing Statement Basis**, which provides documents for filling in the required forms.

## Assigning Packing Statement Elements
After the correct setting of the add-on module **Pack Tracking Basic** it is possible to assign elements of the Packing Statement Elements on the Item card.  
The assignment is made on the relevant Item cars, choose Actions/Item/**Packing Elements Assignment**.

For each item and its unit of measure, you can assign any number of elements of packaging reports (include items in several statements). Packing Elements Assignment is bound to **Statement Code** and **Movement Type**. The combination of these values is complemented by **Code** that determines the position in the report. The **Base Unit Weight** field is related to the unit of measure on the report line.

## Report generating
Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do"), icon, enter **Packing Statement Basis** and then choose the related link.
It serves as a basis for the report on packaging production for EKO-KOM, a. s. This report displays the basis for completing the Packaging Statements.

If you want to mark items as reported, it is necessary to check the **Mark Entries** field for the option of unreported items and fill in the **Statement no.** field.  
The data used in the statement can be filtered, e.g. by Posting Date, Packing Stat. El. Name, etc.

## See also
[Pack Tracking Basic (EKOKOM) - Setup](ac-pack-tracking-basic-setup.md)  
[Financial Pack](ac-finance-pack.md)
