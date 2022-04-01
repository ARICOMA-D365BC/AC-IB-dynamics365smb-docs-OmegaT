---
title: AC - Financial pack -  Multiple payments | Microsoft Docs
description: Jednoduchy popis tematu
author: ACMartinKunes

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.search.keywords: Multiple payments, finance 
ms.date: 04/01/2022
ms.author: AC MartinKunes
---
# Multiple payment methods
> Update 01.04.2022

**The Multiple Payment Methods** module extends the standard of sales documents in the area of balancing the document directly during posting.
On sales invoice or sales credit note documents, instead of one payment method, it is now possible to define multiple payment methods, typically partly by credit card and partly in cash.

The functionality extends the possibilities of setting rules to users even if one payment method is used, both on sales and purchase documents. The aim is to reduce user errors by assigning users to specific "payment places".
In practice, however, it happens that a customer wants to pay on the spot in cash a receipt that should have been paid by bank transfer. Then it is also possible to use the functionality of the module and define the combination of payment on the posted invoice (credit memo) or on the issued advance.
It is possible to use all three counter-account options included in the localization (Financial Account, Bank Account, Cashier) to record the settlement counter-account. However, the most common is the use of **the Cashier as a counter-account**, which allows combining the use of Multiple Payment Methods and Cash Receipts and brings with it rounding advantages (it is automatically resolved only on the cash receipt).

> [!WARNING]
> The module forms the basis for supporting retail sales in the form of Cash&Carry. The functionality is not available on purchase orders (generally on sales/purchase documents where partial invoicing is possible). If you add it to these documents, then you must treat potentially conflicting states programmatically or methodically.
> The option to define multiple payment methods is not available by default on any purchase document, but can be added there as part of the customer extension functionality.


## Posting a sales invoice with multiple payment methods

1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do"), icon, enter **Sales Invoices** and then choose the related link.
2. Create a new sales invoice according to your conventions.
3. On the **Sales Invoice** page, choose **Release** and then run **Payment Schedule** function.
4. Enter the amount of cash you received from the customer.
5. In the next step, enter other methods of payment and the amount paid in that way in the lines.
6. In the Return Cash Amt. (LCY) field, determine the amount that you should return to the customer.
7. Choose **Close** to close the page.
8. On the Sales Invoice page, run the Post function.

> [!NOTE]
> Ff you do not enter a cash amount, you must enter amounts in the rows exactly up to the amount of the receipt (i.e., so that the Balance field is zero).

![Payment Schedule](media/multiple_payment_methods_payment.png)

## Additional payment of the posted sales invoice
1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do"), icon, enter **Posted Sales Invoices** and then choose the related link.
2. Find the relevant document and open its card.
3. On the Posted Sales Invoice page, choose the **Payment Schedule** function.
4. Enter the amount of cash you received from the customer.
5. In the next step, enter other methods of payment and the amount paid in that way in the lines.
6. In the Return Cash Amt. (LCY) field, determine the amount that you should return to the customer.
7. On the Payment Schedule page, run the Post function to post one or more balancing items (typically cash receipts).
8. Choose **Close** to close the page.

> [!NOTE]
> A similar procedure can be used on the Posted Sales Credit Memo page.
> If the receipt is unrounded, rounding of the cash to be refunded takes place only when posting the settlement through the rounding set in the Cash Receipts functionality.

## Records of payment – simplified regime

In case the customer wants to settle the document when charging by one method only, e.g. by bank card, the simplified mode can be used by entering the selected Payment Method Code directly in the document header.

1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do"), icon, enter **Sales Invoices** and then choose the related link.
2. Find the relevant document and open its card.
3. On the Sales Invoice page, select the appropriate value in the **Payment Method Code** field.
4. On the Sales Invoice page, run the Post function.

> [!NOTE]
> A similar procedure can be used on the Posted Sales Credit Memo page.

## Records of payment – simplified mode with substitution of payment method

It is a relatively common practice that the preferred or allowed payment method (typically cash payment) is defined on customer cards. However, when there are more than one such code (due to record keeping requirements), it is necessary to ensure that the document is posted with the code appropriate to the user posting the document. If "Check payment method on sales document" is enabled, the system will make the change automatically (see [Setting up Payment Methods](http://muj.autocont.cz/docs/cs-cz/d365businesscentral/AC-FinancialPack/ac-multiple-payment-methods-setup.html#nastaven%C3%AD-zp%C5%AFsob%C5%AF-platby)).


1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do"), icon, enter **Multiple Payment Methods Setup** and then choose the related link.
2. Verify that check **Check Payment Method On Sales Documents** is turned on.
3. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do"), icon, enter **User Setup** and then choose the related link.
4. Verify that **Payment Place Code** is set on the logged-in user login.
5. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do"), icon, enter **Customers** and then choose the related link.
6. Find the relevant customer and open their card.
7. In the **Payment Method Code** field, set the method that has the value Cash set in the Cashier Operation Type column, but that does not have a **Payment Location Code** defined (see "Cash" as shown in the **Payment Method Settings**)
7. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do"), icon, enter **Sales Invoices** and then choose the related link.
9. Run the New action to create a new document.
10. On the Sales Invoice page, enter the customer (see above)
11. Enter at least one invoice line.
12. On the Sales invoice page, start the release function.


## EET records directly from the Payment Schedule

In some cases, it is required to create a register of EET (legislation in the Czech Republic) already on the payment schedule, i.e. before the document is posted (e.g. for printing documents for the implementation of cash on delivery, etc.).

If Enable EET registration is enabled, the Register EET action is available on the payment schedule, resp. Cancel EET (see [Payment Methods Settings](http://muj.autocont.cz/docs/cs-cz/d365businesscentral/AC-FinancialPack/ac-multiple-payment-methods-setup.html#nastaven%C3%AD-zp%C5%AFsob%C5%AF-platby)).

1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do"), icon, enter **Multiple Payment Methods Setup** and then choose the related link.
2. Verify that the Enable EET registration option is enabled.
3. Create a new sales invoice according to your conventions.
4. On the Sales Invoice page, run the Release action and then run the Payment Schedule function.
5. Enter the amount of cash you received from the customer.
6. In the next step, enter other methods of payment and the amount paid in that way in the lines.
7. Start the Register EET action.
8. Choose **Close** to close the page.


## See also

[Multiple payment methods - Setup](ac-multiple-payment-methods-setup.md)  
[Financial Pack](ac-finance-pack.md)
