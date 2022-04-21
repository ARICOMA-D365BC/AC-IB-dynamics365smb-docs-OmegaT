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
# VAT Control Report

The functionality enables the processing of the VAT Control Report and its export to an xml file, which can be imported to the portal of the Financial Administration of the Slovak Republic or to the eDane application.

## Generate a VAT Control Report

1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do"), icon, enter **VAT Check Report List** and then choose the related link.
2. To create a new Control Report, choose the **New** function.
3. On the VAT Control Report Card, fill in the appropriate fields on the header. On the Other tab, it is necessary to fill in the **XML schema** field correctly.
4. To fill the statement lines, run the **Fill report lines** function.
5. For a simple check, choose the **Preview** function.

> [!NOTE]
> The **Detailed item** field in CHR rows is used for the system designation of the row. If YES, the item is not selected for the control report (it is not transferred to xml and is not reported to the Financial Administration) When you close the CHR, the items that will have a value of YES in this field are also closed.

> [!NOTE]
> The **Warning** field in CHR rows is an informative field that warns about missing data for individual documents loaded into CHR.

## Adjustments to the VAT control report

It is possible to open individual lines of the control report for editing. After the end of the modifications, it is necessary to recalculate the entris in the CHR.

1. On the VAT Control Report page, select the **Edit** feature for editing
2. When you are finished editing, close the window. The system will automatically ask if you want to recalculate the total rows. Confirm with **Yes**.

## Export the VAT Control Report to XML

1. On the VAT Control Statement card, choose the **Preview** feature.
2. Then choose **Export to XML** and confirm the system query with **Yes**.

## Closing the VAT Control Report

The control report must be closed only after the data have been checked. When the control report is closed, the system blocks the reloading of data into the form. The data generated before its closure can no longer be changed or added. Uzavřený formulář není možné vymazat ze seznamu vygenerovaných CHR. When the form is closed, the entries in the VAT entry table the Closed box selected for the control report.

1. Select the **Close** function on the VAT Control report Card to close it.

## See also

[AUTOCONT Solutions](../index.md)  
[SK Legislative pack](ac-sk-legislative-pack.md)  
[VAT Control Report - Settings](ac-sk-vat-check-report-setup.md)
