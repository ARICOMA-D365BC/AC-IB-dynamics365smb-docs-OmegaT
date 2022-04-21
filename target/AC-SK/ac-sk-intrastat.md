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

# Intrastat statement

For the purpose of generating the Intrastat report, standard functionality is used.

The difference from the standard functionality is in the structure of the file with the extension .xml generated for the purposes of Slovak reporting.

To activate Slovak functionality, these settings are needed, use the following procedure:

## General Ledger Setup

1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do"), icon, enter **General Ledger Setup** and then choose the related link.
2. On the **General Ledger Setup** page you must select**SK** in **Legislation**field.
3. Confirm with the **OK** button.

## Intrastat file mapping

The settings are used to map fields in the application to nodes .xml. This table is part of the supplied configuration package.

1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do"), icon, enter **Intrastat File Mapping** and then choose the related link.
2. On the **Intrastat File Mapping** review or complete the settings.
3. Confirm with the **OK** button.

![File Mapping](media/ac-sk-intrastat.png)

## Export a file for Intrastat

1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do"), icon, enter **Intrastat Journals** and then choose the related link.
2. Insert journal lines with the **Suggest Lines...** feature.
3. Export using the function **Export**, it is necessary to fill in *Contact person*, *Type*, *Serial number of the statement*
4. Confirm with the **OK** button.

## See also




[AUTOCONT Solution](../index.md)  
[SK Legislative Pack](ac-sk-legislative-pack.md)
