---
title: AUTOCONT SOLUTIONS - SK Legistaltive Pack | Microsoft Docs
description: This section describes AUTOCONT Solutions - Slovak legislation - 
author: ac-kunes
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Slovak, , additional functions, sale, VAT
ms.author: v-makune
---

# Export of financial statements - SK

According to the requirements of the Financial Administration of the Slovak Republic, the Slovak Statutory Statements, Balance Sheet and Profit and Loss Statement are imported merged, in one .xml file.

To ensure this requirement, the standard functionality of accounting schemes is used in D365 BC and extended by additional adjustments. The export itself works with the saved results of account schedules.

## Saving the results of accounting schemes for export

1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do"), icon, enter **Account Schedule** and then choose the related link.
2. On the **Account Schedules page**, choose the **Process** action and **Overview** feature.
3. Enter the filters you want as the Date Filter or other filters, select the **Action** button, and then select the **Results** and **Save Results** feature.
4. In the **Save Acc. Schedule Result** fill in the fields as needed.
5. Confirm with the **OK** button.

The results of accounting schemes are stored in a list in the chronological sequence of their formation. The number series set in General Ledger Setup is used to mark the results of the reports.

## Export to .xml format

1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do"), icon, enter **Export Merged Acc. schedule to XML** and then choose the related link.
2. On the **Exp.Merged Acc.Schedule to XML** page, fill in the required fields. Select Result Code in the Section for Balance Sheet and Profit and Loss.
3. Confirm with the **OK** button.

Then it is enough to import the resulting file into the electronic form of the financial administration.

## See also

[AUTOCONT Solutions](../index.md)  
[SK Legislative Pack](ac-sk-legislative-pack.md)   
[Export of financial statements - SK - Setup](ac-sk-balance-sheet-income-statement-setup.md)
