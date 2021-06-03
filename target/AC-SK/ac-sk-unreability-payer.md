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

# Institut nespolehlivosti plátce

Funkcionalita zahrnuje systémové kontroly, které upozorňují uživatele na nespolehlivého plátce DPH při zpracování dokladů.

Seznam subjektů, u kterých nastaly důvody pro zrušení registrace platitele daně z přidané hodnoty, je dostupný na webových stránkách Finanční správy:

https://www.financnasprava.sk/sk/elektronicke-sluzby/verejne-sluzby/zoznamy/exporty-z-online-informacnych

Soubor "Zoznam platiteľov dane z pridanej hodnoty, u kterých nastali dôvody na zrušenie registrácie pre DPH.zip (csv)" je potřeba uložit a naimportovat do systému.

## Import souboru

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Položky nespolehlivosti plátce** a poté vyberte související odkaz.
2. Na stránce **Položky nespolehlivosti plátce** vyberte akci **Hromadné načtení nespolehlivosti dod.**
3. Otevře se okno **Volba importu podle legislativy**, kde je nutné vybrat **SK** a potvrdit pomocí tlačítka **OK**.
4. Dále se otevře okno **Import nespolehlivosti plátců DPH z aplikace Excel**, kde uživatel zvolí zda se mají smazat extistující položky pomcí zakšrtávacího tlačítka **Smazat existující položky**.

Po vytvoření **položek nespolehlivosti plátce** systém zkontroluje údaje na kartách zákazníků (Datum kontroly nespolehlivosti, Nespolehlivý plátce DPH) / dodavatelů a dohledá a vepíše na karty zákazníků nebo dodavatelů nacházejících se v uvedeném seznamu do pole **Nespolehlivý plátce** – ANO.

V případě, že se zákazník / dodavatel v uvedeném v seznamu nenachází, zůstane údaj Nespolehlivý plátce prázdný. Do pole **Datum kontroly nespolehlivosti** se přenáší datum importu údajů ze souboru.

## Aktualizace nespolehlivosti plátce

Při vytvoření nové karty Zákazníka / Dodavatele je potřebné tabulku Položky nespolehlivosti aktualizovat.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Položky nespolehlivosti plátce** a poté vyberte související odkaz.
2. Na stránce **Položky nespolehlivosti plátce** vyberte akci **Kontroluj všechny položky.**

## See also

[AUTOCONT Řešení](../index.md)  
[SK Legislativní balíček](ac-sk-legislative-pack.md)
