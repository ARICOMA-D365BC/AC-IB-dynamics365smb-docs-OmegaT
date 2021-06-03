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

# Export účetní závěrky - SK

Slovenské statutární výkazy, Rozvaha a Výkaz zisků a ztrát, se dle požadavku Finanční správy SR importují sloučené, v jednom .xml souboru.

Pro zajištění tohoto požadavku je v D365 BC použita standardní funkčnost účetních schémat rozšířena o dodatečné úpravy. Samotný export pracuje s uloženými výsledky účetních schémat.

## Uložení výsledků účetních schémat pro export

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Účetní schémata** a poté vyberte související odkaz.
2. Na kartě **Účetní schémata** zvolte akci **Proces** a funkci **Náhled**.
3. Zadejte požadované filtry jako Filtr data, případně další filtry, vyberte tlačítko **Akce** a poté vyberte funkci **Výsledky** a **Uložit výsledky**.
4. V okně **Uložit výsledek úč. schématu** vyplňte pole dle potřeby.
5. Potvrďte pomocí tlačítka **OK**.

Výsledky účetních schémat se ukládají do seznamu v chronologickém sledu jejich vzniku. Na označení výsledků výkazů je vytvořena číselná řada nastavená v Nastavení financí.

## Export  do formátu .xml

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Export slouč.účt.schémat do XML** a poté vyberte související odkaz.
2. Na kartě **Export slouč.účt.schémat do XML** vyplňte požadovaná pole. Vyberte Kód výsledku v sekci pro Rozvahu a Výkaz zisků a ztrát.
3. Potvrďte pomocí tlačítka **OK**.

Pak již stačí výsledný soubor naimportovat do elektronického formuláře finanční správy.

## Viz také

[AUTOCONT Řešení](../index.md)  
[SK Legislativní balíček](ac-sk-legislative-pack.md)   
[Export účetní zavěrky - SK - nastavení](ac-sk-balance-sheet-income-statement-setup.md)
