---
title: Centrální databáze | Microsoft Docs
description: Modul Centrální databáze umožňuje pomocí modulu Spooler synchronizovat číselníky mezi různými Business Cental databázemi a společnostmi. Způsob synchronizace (jaké tabulky, pole odkud a kam) je v Business Central parametrizovatelný.
author: ACMartinKunes
ms.service: dynamics365-business-central
ms.topic: Central database setup
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: klicova slova, 
ms.date: 05/05/2021
ms.author: AC MartinKunes
---
# Centrální číselníky

Modul **Centrální databáze** umožňuje pomocí modulu Spooler synchronizovat číselníky mezi různými Business Central databázemi a společnostmi. Způsob synchronizace (jaké tabulky, pole,odkud a kam) je parametrizovatelný.

Modul je určen k synchronizaci dat mezi různými datovými zdroji – může se jednat o dvě firmy v jedné databázi stejně jako o 2 firmy v databázích od sebe vzdálených. Nastavení je vždy master-klient mezi dvěma datovými firmami.

Aplikaci umožňuje synchronizovat všemi směry a selektivně (viz nastavení). Aplikace nekontroluje možné datové kolize (speciální případ je validace synchronizovaných dat) ani případnou cyklickou synchronizaci (nastavení je vždy pouze mezi dvěma datovými zdroji). 

Aplikaci lze použít k synchronizaci nejen mezi jednotlivými systémy Miscrosoft Business Solution – Business Central, ale též k synchronizaci dat s externími systémy (např. B2B aplikace, zákaznické aplikace, specializovaný výrobní software atd.).

Proces synchronizace může probíhat online v okamžiku změny dat (je generován změnový dokument pro daný záznam), dle volby uživatele jako komplexní balík synchronizovaných dat nebo automaticky jako balík dat v periodických intervalech (pomocí modulu Shareplan).

Datová komunikace o změnách nebo synchronizaci probíhá pomocí strukturovaných XML dokumentů.

Upozornění: V rámci synchronizovaných dat nelze provádět operaci přejmenování (změnu hodnoty
polí primárního klíče).

## Použití Celntrálních číselníků - Synchronizace 

Samotné použití spočívá ve správném nastavení a spuštění synchronizace tabulek. Více o nastavení Centrálních čísleníků naleznete v tématu **[Nastavení Centrálních číselníků](ac-centraldatabase-setup.md)**.

Synchronizace probíhá buď automaticky při změnách v definovaných datových tabulkách nebo ji můžete spustit ručně.

Pro ruční spuštění postupujte dle následujícího postupu:
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nastavení centrální databáze** a klikněte na související odkaz.
1. Otevře se stránka **Nastavení centrální databáze**, kde můžete zvolit **Akce** a funkci **Synchronizovat**.

Při ruční synchronizaci lze pomocí filtrů přesně specifikovat, jaké tabulky, odkud a kam se mají aktuálně synchronizovat. Tato volba se uplatňuje hlavně při synchronizaci již existujících dat do nových systémů (migrace a parametrizace).

## Viz také
[Nastavení Centrálních číselníků](ac-centraldatabase-setup.md)
[AC Productivity Pack](ac-productivity-pack.md)  
[AUTOCONT řešení](../index.md)