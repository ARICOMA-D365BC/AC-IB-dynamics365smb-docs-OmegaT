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

# VAT Control Report - Setup

To ensure proper functionality, you need to set up several areas below

## General Ledger Setup

To activate Slovak functionality, follow these steps:

1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do"), icon, enter **General Ledger Setup** and then choose the related link.
2. On the **General Ledger Setup** page you must select**SK** in **Legislation**field.
3. Confirm with the **OK** button.

## Setting up XML schemas

The XML schema for the VAT Control Report must be imported into the application into the XML schemas.

1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do"), icon, enter **XML Schemas** and then choose the related link.
2. On the **XML Schemas** page choose **Load Schema** action
3. An import window will open where you select the appropriate XML file.
4. After import, a new line appears on **XML Schemas** page.
5. In the SML portID field, select the value **52068871** -valid from 1.1.2020.
6. In the **Assing legislation** select **SK**.
7. Confirm with the **OK** button.


## VAT report line settings - extensions

To ensure the correct reporting of the VAT Control Report, it is necessary to set the fields in the lines of the VAT report:

1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do"), icon, enter **VAT Statements** and then choose the related link.
2. For each line in the sales tax statement, define the following fields:

- Source Code filter
- Document type
- Document type filter
- VAT Control Report Section
- VAT Check Report Section for individuals

![Import of unreliable VAT payers from xml format](media/VAT_check_report.png)

3. Confirm with the **OK** button.

## Setting the sections of the VAT Control Report

Use the following procedure to set up:

1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do"), icon, enter **VAT Check Report Section** and then choose the related link.
2. Set up section codes according to applicable reporting regulations.
3. To report received simplified invoices, you need to set the **Section Code Below Limit** and **Section Code Above Limit**. The fields **VAT Amount Limit** and **Limit Valid From** are filled in at the same time.

![Import of unreliable VAT payers from xml format](media/VAT_check_report_section.png)

## Set up VAT Control Report Section Columns

It is necessary to set columns for individual sections, which will be exported to an xml file.

1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do"), icon, enter **VAT Check Report Section** and then choose the related link.
2. Select the row for which you want to set columns, and then choose **Action** -> **Section** -> **Column Selection Setup**.
3. Enter the codes according to the valid reporting regulation. In the **Assigned Field field in the report line**, you can set from which system field the value will be populated into the Control Report.

## See also

[AUTOCONT Solutions](../index.md)  
[SK Legislative Pack](ac-sk-legislative-pack.md)  
[VAT Control Report](ac-sk-vat-check-report-export.md)
