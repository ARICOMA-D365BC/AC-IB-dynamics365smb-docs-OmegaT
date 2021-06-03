---
title: Centrální databáze | Microsoft Docs
description: Modul Centrální databáze umožňuje pomocí modulu Spooler synchronizovat číselníky mezi různými Business Cental databázemi a společnostmi. Způsob synchronizace (jaké tabulky, pole odkud a kam) je v Business Central parametrizovatelný.
author: ACMartinKunes
ms.service: dynamics365-business-central
ms.topic: Central database
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: klicova slova, 
ms.date: 05/05/2021
ms.author: AC MartinKunes
---
# Nastavení Centrálních číselníků

## Nastavení Centrální databáze


Pro základní nastavení centrální databáze pokračujte podle následujícícho postupu:

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nastavení centrální databáze** a klikněte na související odkaz.
1. Otevře se stránka **Nastavení centrální databáze**, kde nastavíte následující pole:
   - **ID Systému** – slouží k identifikaci systému - název firmy, jak bude používán v oblasti komunikací (důležité je správné nastavení tohoto názvu i v ostatních kooperujících firmách)-
   - **ID systému centrální databáze** – název firmy, která slouží jako řídící pro komunikačně-synchronizační proces. Tato firma stanovuje nastavení pro “podřízené” firmy. Jedna firma může přijímat nastavení od centrální databáze a zároveň být sama centrální databází pro jiné firmy = v systému může být více centrálních databází.
   - **Centrální databáze** – interně používané pole určující, zda je firma sama centrální databází. Nastaveníje zásadní pro rozhodování o zasílání synchronizovaných dat a o kontrolách.
   - **Typ procesu** – nastavení kódu, který odpovídá kódu uvedenému v nastavení úloh spooleru v poli Process Type (viz nastavení spooleru). Tento kód je součástí XML dokumentu a na jeho základě se rozeznává, zda dokument může počkat se zpracováním.
   - **Typ procesu – okamžitá odpověď** – nastavení kódu, který odpovídá kódu uvedenému v nastavení úloh spooleru v poli Process Type (viz nastavení spooleru). Tento kód je součástí XML dokumentu a na jeho základě se rozeznává, zda se dokument musí ihned zpracovat a odeslat odpověď.
1. Po vyplnění polí stránku zavřete.


## Nastavení Cílových systémů

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Cílové systémy** a klikněte na související odkaz.
1. Otevře se stránka **Cílové systémy**, kde vyplníte následující pole:
   - **ID** – kód firmy pro komunikaci (musí být shodný v celém komunikačním řetězci
   - **Popis** – orientační popis k dané firmě
   - **Název databáze** – název databáze, ve které se firma nachází
   - **Název firmy** – správný název firmy uvedený jako jméno firmy v její databázi (může být odlišné od kódového označení)
1. Po vyplnění polí stránku zavřete.

## Nastavení tabulky centrální databáze

Aplikace umožňuje synchronizovat jednotlivé tabulky a jejich vybraná pole, lze  synchronizovat i pouze data spadající do určitého filtru. Synchronizace může být nezávislá a různá pro několik firem.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nastavení tabulky centrální databáze** a klikněte na související odkaz.
1. Otevře se stránka **Nastavení tabulky centrální databáze**, kde vyplníte následující pole:
   - **Vypnuto** – toto pole umožňuje dočasně vypnout synchronizaci při ponechání nastavení. Používá se hlavně při řešení kolizí nebo hromadném zpracování centralizovaných dat (importy, přejmenování atd.).
   - **Priorita** – je možno nastavit pořadí pro odesílání k synchronizaci.
   - **ID centrální databáze** – ID systému, který řídí synchronizaci dané tabulky. Pokud se toto ID nerovná ID systému firmy, ve které se nacházíme, nelze záznam měnit.
   - **Číslo tabulky** – číslo objektu datové tabulky v systému. Tabulku lze vybrat z číselníku všech tabulek. Synchronizace některých tabulek je z hlediska systému nesmyslná nebo může způsobit kolizi.
   - **Název tabulky** – toto pole se vyplní automaticky dle nastavení pole Číslo tabulky.
   - **ID** – nezávislý kód, který je součástí primárního klíče a umožňuje nastavit rozdílné synchronizace pro jednu tabulku (např. pokud chci mít rozdíl v nastavení pro 2 firmy, kde u jedné chci povolit změnu určitých dat a u druhé nikoliv). Tento kód nemá další vazbu v systému a uživatel si ho může nastavit, jak chce (jméno firmy, skupina firem, typ synchronizace atd.).
   - **Typ synchronizace** – tato volba nabývá dvou hodnot – Push a Pull. Význam této volby je při zakládání nových dat do systému (změna dat a mazání dat jsou posílány vždy automaticky).
   - **Push** – volba znamená, že v případě změny dat jsou tato data ihned zaslána do podřízených systému a tam updatována (data jsou “tlačena”).
   - **Pull** – tato volba znamená, že nově vytvořená data nejsou zasílána ihned do podřízených systémů, ale uživatel si sám může “sáhnout” do centrální databáze a vybrat si, která dat z centrály chce ve svém systému (data jsou “tahána”)
   - **Pole** – tato volba určuje, zda se synchronizují některá nebo všechna pole (toto pole má návaznost na funkcionalitu nastavení synchronizovaných polí, viz níže)
   - **Povol změnu** – pole určuje, zda uživatel v podřízené databázi může změnit hodnotu polí v daném záznamu (kontrola na synchronizovaných polích)
   - **Povol vložit** – pole určuje, zda uživatel v podřízené databázi může založit nový záznam v synchronizované tabulce
   - **Synchronizovat po** – pole je využíváno pro optimalizaci přenosu dat a vytížení systému; lze vybrat z hodnot Limitovaný počet záznamů a Všechny záznamy
   - **Limit záznamů** – pole je využíváno pro optimalizaci přenosu dat a vytížení systému
   - **Maximální počet záznamů v odpovědi** – pole je využíváno pro optimalizaci přenosu dat a vytížení systému; systém omezuje počet záznamů zasílaných jako odpověď z centrální databáze při dotazech na synchronizovaná data
1. Po vyplnění polí stránku zavřete.

## Ostatní nastavení
Po základním nastavení addonu Centrální databáze je potřeba nastavit další oblasti. Jedná se o konkrétní nastavení polí tabulek centrální databáze.

### Nastavení polí centrální databáze

Nastavení slouží k definici, která konkrétní pole dané tabulky a jakým způsobem chceme synchronizovat.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nastavení tabulky centrální databáze** a klikněte na související odkaz.
1. Otevře se stránka **Nastavení tabulky centrální databáze**, kde vybere řádek s odpovídající tabulkou.
1. Vyberete možnost **Související**, dále **Nastavení** a vyberete funkci **Pole**, kde vyplňte náledující pole dle potřeby:
   - **Číslo pole** – číslo je vybíráno z objektu dané tabulky a je jednoznačnou identifikací pole v celém systému (spolu s číslem tabulky). Při změnách v systému se čísla polí nemění.
   - **Titulek pole** – toto pole se vyplní automaticky dle nastavení pole Číslo pole.
   - **Povol změnu** – pole určuje, zda uživatel v podřízené firmě může měnit hodnotu tohoto konkrétního pole.
   - **Pole primárního klíče** – pole je používáno interně, systém hodnotu nastavuje  sám. Pole s tímto označením je povinně synchronizováno vždy
   - **Nevalidovat** – pole určuje, zda po synchronizace tohoto pole nastane tzv. validační proces (spuštění funkcí souvisejících se změnou hodnoty pole). Toto pole musí nastavovat velmi zkušený uživatel systému, špatné nastavení způsobí kolizní situace.
1. Po vyplění polí stránku zavřete.

### Nastavení příjemců centrální databáze

Nastavení slouží v definování komunikace pro konkrétní záznam z nastavení synchronizace tabulek (jak bylo popsáno výše, jedna tabulka může být synchronizována pro různé firmy různým způsobem).

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nastavení tabulky centrální databáze** a klikněte na související odkaz.
1. Otevře se stránka **Nastavení tabulky centrální databáze**, kde vybere řádek s odpovídající tabulkou.
1. Vyberete možnost **Související**, dále **Nastavení** a vyberete funkci **Příjemci**, kde vyplňte náledující pole dle potřeby:

   - **Vypnuto** – toto pole umožňuje dočasně vypnout synchronizaci při ponechání nastavení. Používá se hlavně při řešení kolizí nebo hromadném zpracování centralizovaných dat (importy, přejmenování atd.).
   - **ID cílového systému** – vazba do nastavení cílových systémů, kód určuje, která firma bude příjemcem synchronizovaných dat při události.
   - **Filtr synchronizace tabulky** – v poli (a pomocném podřízeném formuláři) lze nastavit obecný filtr, který určuje, která data se budou synchronizovat (pouze data spadající do filtru).
   - **Filtr oprávnění tabulky** – v poli (a pomocném podřízeném formuláři) lze nastavit obecný filtr, který určuje, která data bude moci uživatel v podřízené firmě modifikovat či zakládat.
1. Po vyplění polí stránku zavřete.

### Nastavení Relací

Nastavení slouží k určení relačních vazeb, které zajišťují, aby při synchronizace záznamů z určité tabulky proběhla synchronizace souvisejících záznamů (např. zboží + měrná jednotka zboží).

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nastavení tabulky centrální databáze** a klikněte na související odkaz.
1. Otevře se stránka **Nastavení tabulky centrální databáze**, kde vybere řádek s odpovídající tabulkou.
1. Vyberete možnost **Související**, dále **Nastavení** a vyberete funkci **Relace**, kde vyplňte náledující pole dle potřeby:

   - **Vypnuto** – toto pole umožňuje dočasně vypnout synchronizaci při ponechání nastavení. Používá se hlavně při řešení kolizí nebo hromadném zpracování centralizovaných dat (importy, přejmenování atd.)
   - **Číslo tabulky relace** – číslo objektu datové tabulky v systému. Tabulku lze vybrat z číselníku již synchronizovaných tabulek. Tato tabulka je relačně nebo logicky podřízena a její data mají vazbu k nadřízené tabulce
   - **Název tabulky relace** – toto pole se vyplní automaticky dle nastavení pole Číslo tabulky relace
   - **Filtr tabulky** – v poli (a pomocném podřízeném formuláři) lze nastavit obecný filtr, který určuje, která data budou synchronizována v rámci relační synchronizace
   - **Relace existuje** – pole, které určuje, zda je již definována relační vazba
   - **Relace** – pouze zobrazované formulářové pole, v jehož podřízeném formuláři lze definovat relační vazbu

**See also**

[Centrální číselníky](ac-centraldatabase.md)`  
[AC Productivity Pack](ac-productivity-pack.md)  
[AUTOCONT řešení](../index.md)