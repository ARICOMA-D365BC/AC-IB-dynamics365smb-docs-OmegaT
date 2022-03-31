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
> Aktualizace: 03.03.2022

Funkcionalita zahrnuje systémové kontroly, které upozorňují uživatele na nespolehlivého plátce DPH při zpracování dokladů. Dále obsahuje kontroly, zda je použitý bankovní účet partnera registrovaný pro podnikání v SR dle zákona 222/2004 Z.z.

Seznam subjektů, u kterých nastaly důvody pro zrušení registrace platitele daně z přidané hodnoty, je dostupný na webových stránkách Finanční správy. Pro automatizaci stahování je třeba, aby se zákazník registroval na portále [OpenData FS API](https://opendata.financnasprava.sk/page/openapi).

V záznamech Finanční správy SR pak automatická úloha hledá dodavatele či zákazníky evidovanév systému, vytváří vlastní záznamy (tzv. Položky nespolehlivosti plátce) a vůči těmto pak provádí kontroly při zpracování dokladů.

Jako spolehlivá je označena společnost, která není uvedena v seznamu a která má zveřejněný alespoň 
jeden bankovní účet pro podnikání na Slovensku.

> [!NOTE]
> Kontrola nespolehlivosti plátce DPH v případě zákazníků je omezena pouze na kontrolu na 
Platebním příkazu.

## Ověření nového dodavatele
Mohou existovat scénáře, kdy je třeba provést okamžitou kontrolu nespolehlivosti plátce. Pro tyto případy použijte na stránce Karta dodavatele akci Kontrola nespolehlivosti plátce DPH.

## Nákupní doklad
Kontrola nespolehlivost plátce DPH se provádí při vložení či změně dodavatele (resp. Čísla věřitele) na nákupním dokladu. Uživateli se pak zobrazí na dokladu notifikace.

Při spuštění akce Vydání dochází ke kontrole bankovního účtu na záložce Detaily platby, zda-li je v seznamu dodavatelem zveřejněných účtů pro podnikání na Slovensku.

## Platební příkaz
> [!WARNING]
> Dostupné od verze 2022 Wave 1

Před odesláním požadavku na schválení Platebního příkazu spusťte funkci Kontrola nespolehlivosti plátce DPH, která na řádcích nastaví příznak Zveřejněný bankovní účet (a také příznak Nespolehlivý plátce DPH).

Tato kontrola se provede automaticky při akci Vydání, které není povoleno, pokud některý z řádků nevyhovuje kontrole.

## Nastavení aktualizace nespolehlivosti plátce

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nastavení služby nespolehlivého plátce** a poté vyberte související odkaz. 
2. Spusťte funkci **Nastavit výchozí webovou službu SK**, která naplní URL služby.
3. V poli API klíč služby OpenDataFS zadejte hodnotu klíče vygenerovaného na portále **[OpenData FS API](https://opendata.financnasprava.sk/page/openapi)**.
4. Zapněte **Automaticky aktualizovat pro vytvoření položky fronty úloh**. Systém nabídne otevření Karty položky fronty úloh, kde je možné změnit parametry spouštění. Výchozím nastavení je aktualizace jednou denně ve 20:00 hod.
## Viz také

[AUTOCONT Řešení](../index.md)  
[SK Legislativní balíček](ac-sk-legislative-pack.md)
