---
title: AUTOCONT SOLUTIONS - SK Legistaltive Pack| Microsoft Docs
description: This section describes AUTOCONT Solutions - Slovak legislation
author: ac-kunes
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Slovak, , additional functions, sale, VAT
ms.author: v-makune
---

# Summary Report (VIES)

Standard functionality is used to create the Summary Report.

The difference compared to the standard functionality is in the structure of the XML file generated for the purposes of Slovak reporting.

## General Ledger Setup

To activate Slovak functionality, follow these steps:

1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do"), icon, enter **General Ledger Setup** and then choose the related link.
2. On the **General Ledger Setup** page you must select**SK** in **Legislation**field.
3. Confirm with the **OK** button.

## Setting up XML schemas

Import the current XML schema template into the XML schemas by following these steps:

1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do"), icon, enter **XML Schemas** and then choose the related link.
2. On the **XML Schemas** page, in the **Actions** section, select the **Load Schema**action.
3. An import window will open where you select the appropriate XML file.
4. After import, a new line appears on the **XML Schemas**.
5. In the appropriate row for each XML, select the correct number in the SML portID column.
   The Summary Report is **52068870**.
6. In the **Assigned to legislation** field, select **SK**.
7. Confirm with the **OK** button.

## See also

[AUTOCONT Solution](../index.md)  
[SK Legislative Pack](ac-sk-legislative-pack.md)
