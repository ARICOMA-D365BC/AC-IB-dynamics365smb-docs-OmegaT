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
# Opravné doklady
> Aktualizace: 13.05.2022

Zadání opravných dokladů s použitím nastaveného kódu původu a případným vyplněním původního čísla dokladu umožňuje správně přiřadit nebo vyloučit tyto transakce do Výkazu DPH. Podmínkou je nastavení polí Filtr kódu původu, Typ dokladu a Filtr typu dokladu na řádku Výkazu DPH.

## Interní oprava prodejní faktury

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Prodejní dobropis** a poté vyberte související odkaz.
2. Vyplňte hlavičku a řádky obvyklým způsobem.
3. V poli **Typ dobropisu** vyberte Interní oprava.
4. Do pole **Původní číslo prodejní faktury** vložte nebo vyberte číslo opravované faktury.

 

## Interní oprava nákupní faktury

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nákupní dobropis** a poté vyberte související odkaz.
2. Vyplňte hlavičku a řádky obvyklým způsobem.
3. V poli **Typ dobropisu** vyberte hodnotu Interní oprava.
4. Do pole **Původní číslo faktury dodavatele** vložte nebo vyberte číslo opravované faktury.

> [!NOTE]
> Transakce se zaúčtuje s nastaveným Kódem původu pro interní dobropis. Zároveň se v Položce DPH přepíše tento Kód původu i u opravované faktury.
>V případě, že položky DPH původního dokladu jsou Uzavřené, Kód původu pro interní dobropis se nedoplní do položek DPH původního dokladu ani do položek DPH dobropisu.

> [!WARNING]
> Nutné nastavení: Nastavení kódů původu, pole Nákupní interní dobropis = INTCREDIT, pole Prodejní interní dobropis = INTCREDIT  

## Prodejní vrubopis
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Prodejní faktura** a poté vyberte související odkaz.
2. Vyplňte hlavičku a řádky obvyklým způsobem.
3. V poli **Vrubopis** nastavte na ANO.
4. Do pole **Původní číslo prodejní faktury** vložte nebo vyberte číslo opravované faktury.

## Nákupní vrubopis
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nákupní faktura** a poté vyberte související odkaz.
2. Vyplňte hlavičku a řádky obvyklým způsobem.
3. V poli **Vrubopis** nastavte na ANO.
4. Do pole **Původní číslo faktury dodavatele** vložte nebo vyberte číslo opravované faktury.

> [!NOTE]
> Transakce se zaúčtuje s nastaveným Kódem původu pro vrubopis, Kód původu Položkách DPH původního dokladu se nemění.

> [!WARNING]
> Nutné nastavení: Nastavení kódů původu, pole Nákupní vrubopis = DEBITNOTE, pole Prodejní vrubopis = DEBITNOTE .

## Viz také

[AUTOCONT Řešení](../index.md)  
[SK Legislativní balíček](ac-sk-legislative-pack.md)  
[Výkaz DPH - nastavení](ac-sk-vat-statement-setup.md)
