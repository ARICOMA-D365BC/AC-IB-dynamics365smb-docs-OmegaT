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

# Export účetní zavěrky - SK - nastavení

Pro definování statutárních výkazů slovenské legislativy (Rozvahy a Výkazu zisků a ztrát) je v systému D365 BC využívána standartní funkčnost účetních schémat doplněná o úpravy, které umožňují import účetní závěrky na portál Finanční správy SR prostřednictvím .xml souboru.

Pro zajištění exportu účetní závěrky je potřeba nastavit několik níže uvedených oblastí.

## Rozlišení schémat pro vybranou zemi

Pole **Přiřazeno legislativě** v přehledu účetních schémat slouží pro rozlišení českých a slovenských statutárních výkazů.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Účetní schémata** a poté vyberte související odkaz.
2. Ve sloupci **Přiřazeno legislativě** vyberte **SK** pro slovenské statutární výkazy.

## Mapování souborů účetních schémat

Pro jednotlivé buňky účetního schématu je potřeba nastavit příslušné hodnoty elementů xml souboru dle pokynů technické dokumentace. Pro každý řádek výkazu je nutné nastavit mapování běžného i minulého období.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Účetní schémata** a poté vyberte související odkaz.
2. Na kartě **Účetní schémata** zvolte akci **Proces** a funkci **Upravit účetní schéma**.
3. Na kartě vybraného **Účetního schématu** zvolte tlačítko **Akce** a poté v sekci **Další** vyberte funkci **Mapování souborů**.
4. Na kartě **Mapování souborů účetního schématu** v poli **Typ mapování** vyberte hodnotu Xml. Do polí účetního schématu zadejte odpovídající hodnoty elementů podle technických požadavků šablony xml.
5. Po úpravách kartu zavřete.

## [přibližně]<g1>See also</g1>

[AUTOCONT Řešení](../index.md)  
[SK Legislativní balíček](ac-sk-legislative-pack.md)  
[Export účetní závěrky - SK](ac-sk-balance-sheet-income-statement.md)
