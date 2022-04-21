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

# Import of exchange rates from the ECB

When importing exchange rates from the ECB, the date shift of the exchange rate validity is ensured.
The exchange rate table imports the exchange rate with the validity date moved forward by 1 day compared to the announcement date on the ECB website.

## Settings for the date offset

1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do"), icon, enter **Curr. Exch. Rate Service** and then choose the related link.
2. On the **Currency Exchange Rate Services** page for *ECB-EXCHANGE-RATES* open **Data Exchange Definitions**.
3. On the **Data Exchange Definition** page, choose **Field Mapping**.
4. In the **SK Date Formula** field enter *1D* o ensure that the date offset works for import.
5. Confirm with **OK**.

## See also

[AUTOCONT Solution](../index.md)  
[SK Legislative Pack](ac-sk-legislative-pack.md)
