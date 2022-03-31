---
title: Spooler | Microsoft Docs
description: Spooler slouží pro komunikaci systému Business Central s externími systémy nebo datovými zdroji.
author: ACMartinKunes
ms.service: dynamics365-business-central
ms.topic: Spooler
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: klicova slova, 
ms.date: 05/05/2021
ms.author: AC MartinKunes
---
# Spooler

Spooler slouží pro komunikaci systému Microsoft Dynamics Business Central s externími systémy nebo datovými zdroji.

Má dvě základní funkce:
- Úložiště nezpracovaných úloh a jako archív komunikačních dokumentů.
- Nástroj pro různé typy komunikací a pro zpracování příchozích dokumentů.

Komunikace může probíhat jak z Bussiness Central do externího systému nebo naopak z externího systému do Bussiness Central. Spooler umožňuje aktuálně využívat celkem 5 komunikačních protokolů (tento počet se neustále rozrůstá).

Tento modul má mnohostranné využití – při synchronizaci dat mezi systémy (katalogy, nastavení systémů v rámci holdingů), v komunikaci dotazů s externími systémy (např. pro systémy B2B nebo B2C), pro archivaci a zpracování automatických elektronických dokladů (objednávkové systémy, elektronické dodávky, fakturace, potvrzení).

Kromě funkce obecného nástroje na komunikaci umožňuje ve spolupráci s modulem Elektronická fakturace poskytovat plně bezpapírovou fakturaci směrem k zákazníkům, která je uznávána i státními kontrolními orgány.

Tento modul je postaven samostatně a nezasahuje do ostatních modulů.

## In Buffer a Out Buffer

Hlavní částí spooleru jsou dvě tabulky, ve kterých jsou uchovány jednotlivé záznamy o komunikaci včetně souborů.

Rozhraní obou tabulek je téměř stejné. Každý záznam v tabulce IN Bufferu i OUT Bufferu má přiděleno jedinečné číslo **ID dokumentu**. Je zde také zobrazen **Typ procesu** a **Typ dokumentu**. Dále je v záznamu vidět jaká úloha se zpracovává – pole **ID úkolu** a jakým agentem je zpracovávána – pole **ID agenta**. Stav záznamu označuje pole **Zpracováno**. Nabývá hodnot Ne, Ano, Expirováno a Odloženo. **Pole ID zdrojového systému** nám v IN Bufferu ukazuje odkud (z jakého systému) daný záznam pochází.

### Neodeslání položky Out Bufferu

Na rozdíl od IN Buffer je na OUT Bufferu pole **Nenutit posloupnost odesílání** - tady je možno kódem vyjmout položku Bufferu z výpočtu o posloupnosti odesílání. Při odesílání dokladů z OUT Bufferu se snaží OUT Agent držet posloupnost odesílání následujícím způsobem:


- Pokud se nějakou položku nepodaří odeslat, tak se neodešlou ani žádné další položky směřující ke stejnému cíli (dle polí **ID cílového systému** a **Parametr komunikace** z nastavení příjemců, bez ohledu na úlohu).
- Funkcionalita posloupnosti odesílání pracuje tak, že pokud je v OUT Bufferu vyplněno pole **Parametr komunikace**, tak se zpracovává právě podle toho pole.

- Držení posloupnosti odesílání ve spooleru má 2 základní důvody:
   1. Dodrží posloupnost odesílaných dokumentů.
   2. Šetří čas aplikačnímu serveru v případě nefunkčnosti spojení - pokud je potřeba poslat větší množství dokumentů na jedno místo (například TCP adresa/port) a spojení není funkční, tak pokus o odeslání může trvat i několik vteřin a je nežádoucí aby se tento pokus opakoval s každou položkou - v krajním případě to může zastavit Aplikační server i na několik hodin. Je dobré používat pole **Nenutit posloupnost odesílání** po důkladné úvaze.

### Komunikace In a Out Bufferu
Pro zobrazení úloh komunikace mezi Out Bufferem a In Bufferem postupujte následujícím způsobem:

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **In Buffer** a klikněte na související odkaz.
1. Otevře se stránka **In Buffer**, kde funkci v sekci **Související** použijte funkci **Položka**, kde najdete následující funkce:
   - Položky elektronických dokladů
   - In Buffer - Odpověď
   - In Buffer - Odpověď (včetně archivu)
   - In Buffer - Dotaz
   - In Buffer - Dotaz (včetně archivu)

1. U Out Bufferu jsou volby obdobně.
1. V zobrazených řádcích se řadí vždy dle **ID dokumentu**.

### Export dokumentu komunikace

Na formulářích IN Bufferu i OUT Bufferu možno exportovat dokument, zobrazit dokument a zobrazit jako HTML – to v případě, že pro úlohu spooleru je nadefinovaná šablona XSL. Dále je zde možnost daný záznam expirovat, změnit poznámku nebo ručně odeslat do archívu.

Pro export dokumentu postupujte následujícím způsobem:

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Out Buffer** a klikněte na související odkaz.
1. Otevře se stránka **Out Buffer**, kde můžete použít funkci **Export Dokumentu**.

Další funkcí pod plačítkem **Export Dokumentu** je také volba Zkontrolovat elektronický podpis a zobrazit certifikát podpisu.

### Nezpracovaný záznam

Pokud je daný záznam ve stavu Zpracováno = Ne, tak je možno danou úlohu spustit z formuláře ručně. Tato funkce je dostupná pouze pro In Buffer.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **In Buffer** a klikněte na související odkaz.
1. Otevře se stránka **In Buffer**, kde můžete použít funkci **Spustit úlohu**.

Program pak umožňuje zobrazit chybu, kvůli které se úloha nezpracovala. Pokud se po ručním spuštění úloha nezpracovala, je zřejmě problém s aplikačním serverem (např. uživatelská práva). Na formuláři **IN Bufferu** je funkce **Odeslat úlohu**, která umožňuje danou úlohu odeslat z IN Bufferu.

### Ruční vložení úkolu do In nebo Out Bufferu

Pro vložení úkolu do In nebo Out Bufferu postupujte následujícím způsobem:

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **In Buffer** a klikněte na související odkaz.
1. Otevře se stránka **In Buffer**, kde vyberte sekci **Akce**, dále **Funkce** a nakonec funci **Vložit úlohu**.
1. Na stránce **Vložit In Buffer** vyplňte následující pole podle potřeby:
   - **Dokument**, kde se vybírá dokument úlohy. Pokud se dle hlavičky dokumentu najde úloha spooleru, tak se automaticky nastaví údaje ve formuláři např. ID agenta, Typ procesu, Typ dokumentu. Pokud ne, tak se musí ručně nastavit.
   - **Není XML** nás informuje, zda přiřazený dokument není nebo je XML.
   - **Elektronicky podepsáno** – pokud je toto pole zatrženo, dokument je elektronicky podepsán. To je možno zkontrolovat v sekci Funkce výběrem možnosti **Zobrazit certifikát podpisu**. Pod stejnou sekci je také možnost **Zobrazit datum podpisu**.
   - Pole **Priorita** má pouze evidenční charakter.

## Archiv - In a Out Buffer

Pro zobrazení položek archivu In nebo Out Bufferu posutpujte následujícím způsobem:

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Archivovaný In Buffer** nebo **Archivovaný Out Buffer** a klikněte na související odkaz.

Do archívu se položky dostanou automaticky při zpracování, pokud je to nastaveno v úloze spooleru (Nearchivovat při zpracování, Nearchivovat při expiraci) nebo v nastavení spooleru (Archivovat IN Buffer při zpracování a Archivovat IN Buffer při expiraci, Archivovat OUT Buffer při zpracování a Archivovat OUT Buffer při expiraci).

Do archivu se položky dostanou také ručně z formuláře IN Bufferu nebo OUT Bufferu pomocí funkce **Přesun do archívu**.

Další možností, jak dostat položky do archívu je pomocí **reportů R4002900 Move IN Buffer to Archive** a **R4002901 Move OUT Buffer to Archive**.

## See also
[Spooler - Nastavení](ac-spooler-setup.md)
[AC Productivity Pack](ac-productivity-pack.md)  
[AUTOCONT řešení](../index.md)