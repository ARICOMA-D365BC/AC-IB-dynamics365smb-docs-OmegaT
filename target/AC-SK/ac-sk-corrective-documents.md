---
title: AUTOCONT SOLUTIONS - SK Legistaltive Pack| Microsoft Docs
description: This section describes AUTOCONT Solutions - Slovak legislation
author: ac-kunes
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Slovak, , additional functions, internal correction, debit memo, credit memo
ms.author: v-makune
---
# Corrective documents
> Update: 13.05.2022

Entering corrective documents using the set origin code and possibly filling in the original document number allows you to correctly assign or exclude these transactions to the VAT statement. The condition is to set up the Origin Code Filter, Document Type, and Document Type Filter fields on the VAT Statement line.

## Internal correction of sales invoice

1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do"), icon, enter **Sales Credit Memos** and then choose the related link.
2. Fill in the header and rows as usual.
3. V poli **Typ dobropisu** vyberte Interní oprava.
4. Do pole **Původní číslo prodejní faktury** vložte nebo vyberte číslo opravované faktury.



## Interní oprava nákupní faktury

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nákupní dobropis** a poté vyberte související odkaz.
2. Fill in the header and rows as usual.
3. V poli **Typ dobropisu** vyberte hodnotu Interní oprava.
4. Do pole **Původní číslo faktury dodavatele** vložte nebo vyberte číslo opravované faktury.

> [!NOTE]
> Transakce se zaúčtuje s nastaveným Kódem původu pro interní dobropis. Zároveň se v Položce DPH přepíše tento Kód původu i u opravované faktury.
> V případě, že položky DPH původního dokladu jsou Uzavřené, Kód původu pro interní dobropis se nedoplní do položek DPH původního dokladu ani do položek DPH dobropisu.

> [!WARNING]
> Nutné nastavení: Nastavení kódů původu, pole Nákupní interní dobropis = INTCREDIT, pole Prodejní interní dobropis = INTCREDIT

## Prodejní vrubopis
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Prodejní faktura** a poté vyberte související odkaz.
2. Fill in the header and rows as usual.
3. V poli **Vrubopis** nastavte na ANO.
4. Do pole **Původní číslo prodejní faktury** vložte nebo vyberte číslo opravované faktury.

## Nákupní vrubopis
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nákupní faktura** a poté vyberte související odkaz.
2. Fill in the header and rows as usual.
3. V poli **Vrubopis** nastavte na ANO.
4. Do pole **Původní číslo faktury dodavatele** vložte nebo vyberte číslo opravované faktury.

> [!NOTE]
> Transakce se zaúčtuje s nastaveným Kódem původu pro vrubopis, Kód původu Položkách DPH původního dokladu se nemění.

> [!WARNING]
> Nutné nastavení: Nastavení kódů původu, pole Nákupní vrubopis = DEBITNOTE, pole Prodejní vrubopis = DEBITNOTE .

## See also

[AUTOCONT Řešení](../index.md)  
[SK Legislativní balíček](ac-sk-legislative-pack.md)  
[Výkaz DPH - nastavení](ac-sk-vat-statement-setup.md)
