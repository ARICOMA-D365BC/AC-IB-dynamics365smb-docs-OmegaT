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

# Kontrolní výkaz DPH - nastavení

Pro zajištění správné funkčnosti je potřeba nastavit několik níže uvedených oblastí.

## Nastavení financí

Pro aktivování slovenských funkčností využijte následující postup:

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nastavení financí** a poté vyberte související odkaz.
2. Na kartě **Nastavení financí** je nutné vybrat do pole **Legislativa** hodnotu **SK**.
3. Potvrďte pomocí tlačítka **OK**.

## Nastavení XML schémat

XML schéma ke Kontrolnímu výkazu DPH je potřebné do aplikace naimportovat do XML schémat.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **XML schémata** a poté vyberte související odkaz.
2. Na stránce **XML schémata** vyberte akci **Načíst schéma**.
3. Otevře se vám okno pro import, kde vyberete příslušný XML soubor.
4. Po import se na kartě **XML schémata** objeví nový řádek.
5. Do pole SML portID vyberte hodnotu **52068871** -platná od 1.1.2020.
6. do pole **Přiřazeno legislativě** vyberte hodnotu **SK**.
7. Potvrďte pomocí tlačítka **OK**.

## Nastavení řádků výkazu DPH - rozšíření

Pro zajištění správného vykazování Kontrolního výkazu DPH je potřeba nastavit pole v řádcích výkazu DPH:

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Výkazy DPH** a poté vyberte související odkaz.
2. Pro jednotlivé řádky výkazu DPH definujte pole:

- Filtr kódu původu
- Typ dokladu
- Filtr typu dokladu
- Sekce kontrolního výkazu DPH
- Sekce kontrolního výkazu DPH pro fyzické osoby

3. Potvrďte pomocí tlačítka **OK**.

## Nastavení sekcí kontrolního výkazu DPH

Pro nastavení využijte následující postup:

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Sekce kontrolního výkazu DPH** a poté vyberte související odkaz.
2. Nastavte kódy sekcí dle platných nařízení pro vykazování.
3. Pro vykazování přijatých zjednodušených faktur je potřeba nastavit **Kód sekce pod limit** a **Kód sekce nad limit**. Zároveň se vyplní i pole **Limit částky DPH** a **Platnost limitu od**.
4. Potvrďte pomocí tlačítka **OK**.

## Nastavení sloupců sekcí kontrolního výkazu DPH

Pro jednotlivé sekce je potřeba nastavit sloupce, které budou exportovány do xml souboru.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Sekce kontrolního výkazu DPH** a poté vyberte související odkaz.
2. Označte řádek, pro který chcete nastavovat a poté zvolte funkci **Akce** - **Sekce** - **Nastavení sloupců sekcí výkazu**.
3. Zadejte kódy dle plateného nařízení pro vykazování. V poli **Přiřazené pole v řádku výkazu** je nastavení z jakého systémového pole bude hodnota naplněna do Kontrolního výkazu.

## Viz také

[AUTOCONT Řešení](../index.md)  
[SK Legislativní balíček](ac-sk-legislative-pack.md)  
[Kontrolní výkaz DPH](ac-sk-vat-check-report-export.md)
