---
title: Autocont - Pack Tracking Basic | Microsoft Docs
description:  This section describes Autocont Pack Tracking Basic AddOn
author: ACPJanousek
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Pack tracking, inventory, item, report,
ms.date: 01/31/2020 TODO
ms.author: v-pejano
---

# Pack Tracking Basic (EKOKOM)
Modul Evidence obalů je rozšířením oblasti Zásoby.  
Modul zakládá samostatnou evidenci obalů svázanou s oblastí zásob a standardními pohyby zboží (nákup, prodej, příjem, výdej, transfer, spotřeba a výroba).

Evidence obalů obsahuje klasifikaci druhů obalů. Umožňuje spravovat libovolný počet podkladů pro potřeby obalového výkaznictví požadovaného interně firmou nebo legislativou (základní parametrizace výkazu EKO-KOM pro potřeby výkaznictví příslušnými osobami dle Zákona o obalech č. 477/2001 Sb. je součástí).

Položky obalů se vyrovnávají automaticky na pozadí při pohybech zboží, a proto zpracování podkladů pro Evidenci obalů uživatele nijak nezatěžuje.
Výstupem modulu je tisková sestava **Podklad pro výkaz obalů**, která poskytuje podklady pro vyplnění vyžadovaných tiskopisů.

## Přiřazování prvků Výkazu obalů
Po korektním nastavení add-on modulu **Evidence obalů základ** je možné na kartách Zboží přiřazovat prvky Výkazu obalů.  
Přiřazení se provede na příslušných kartách Zboží, v nabídce zvolte Akce/Zboží/**Prvky výkazu obalů**.

Pro každé zboží a jeho měrnou jednotku lze přiřadit libovolný počet prvků výkazů obalů (zařadit zboží do několika výkazů). Přiřazení prvku je vázáno na **Kód pro vykazování** a **Typ pohybu**. Kombinaci těchto hodnot doplňuje **Kód** určující pozici ve výkazu. Pole **Hmotnost** je vztaženo k měrné jednotce na řádku výkazu.

## Vytváření sestav
Pomocí vyhledávací funkce ![Žárovka, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat") vyhledejte **Podklad pro výkaz obalů**.
Slouží jako podklad pro výkaz o produkci obalů pro společnost EKO-KOM, a. s. Uvedená sestava zobrazí podklady pro vyplnění Výkazu obalů.

Pokud chceme označit položky jako vykázané, je nutno pro možnost nevykázaných položek zatrhnout pole **Označit položky** a vyplnit pole **Číslo výpisu**.  
Data použitá do výkazu lze filtrovat, např. podle Zúčtovacího data, Kódu pro vykazování jednotlivých položek apod.

## See also
[Nastavení - Evidence obalů základ (EKOKOM)](ac-pack-tracking-basic-setup.md)  
[Financial Pack](ac-finance-pack.md)
