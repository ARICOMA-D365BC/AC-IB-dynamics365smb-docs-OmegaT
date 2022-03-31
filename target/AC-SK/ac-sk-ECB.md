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

# Import směnných kurzů z ECB

Při importu směnných kurzů z ECB je zajištěn datumový posun platnosti směnného kurzu.
Do tabulky směnných kurzů se naimportuje kurz s datumem platnosti posunutým o 1 den dopředu oproti datumu vyhlášení na webových stránkách ECB.

## Nastavení pro datumový posun

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Služba směnného kurzu** a poté vyberte související odkaz.
2. Na kartě **Služba směnného kurzu** pro *ECB-EXCHANGE-RATES* otevřete **Definice výměny dat**.
3. Na stránce **Definice výměny dat** zvolte **Mapování pole**.
4. Do pole **Vzorec data SK** zadejte hodnotu *1D* pro zajištění funkčnosti posunu datumu při importu.
5. Potvrďte pomocí **OK**.

## See also

[AUTOCONT Solution](../index.md)  
[SK Legislative Pack](ac-sk-legislative-pack.md)
