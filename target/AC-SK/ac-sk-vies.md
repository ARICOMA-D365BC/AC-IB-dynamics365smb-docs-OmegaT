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

# Souhrnný výkaz (VIES)

Na vytvoření Souhrnného výkazu je použita standartní funkcionalita.

Rozdíl oproti standardní funkčnosti je v struktuře souboru XML generovaném pro účely slovenského vykazování.

## Nastavení financí

Pro aktivování slovenských funkčností využijte následující postup:

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nastavení financí** a poté vyberte související odkaz.
2. Na kartě **Nastavení financí** je nutné vybrat do pole **Legislativa** hodnotu **SK**.
3. Potvrďte pomocí tlačítka **OK**.

## Nastavení XML schémat

Do XML schémat naimportujte aktuální šablonu XML schématu dle následujícího postupu:

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **XML schémata** a poté vyberte související odkaz.
2. Na stránce **XML schémata** v sekci **Proces** vyberte akci **Načíst schéma**.
3. Otevře se vám okno pro import, kde vyberete příslušný XML soubor.
4. Po importu se na kartě **XML schémata** objeví nový řádek.
5. V příslušném řádku pro každé XML vyberte správné číslo ve sloupci SML portID.
   Souhrnný Výkaz to je **52068870**.
6. V poli **Přiřazeno legislativě** vyberte hodnotu **SK**.
7. Potvrďte pomocí tlačítka **OK**.

## See also

[AUTOCONT Solution](../index.md)  
[SK Legislative Pack](ac-sk-legislative-pack.md)
