---
title: AC - Financial pack -  Factoring | Microsoft Docs
description: Jednoduchy popis tematu
author: ACMartinKunes

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.search.keywords: Factoring, finance 
ms.date: 01/31/2021
ms.author: AC MartinKunes
---
# Factoring - Nastavení

Základní nastavení add-onu fakoringu.
## Nastavení add-onu Faktoring
### Potřebné nastavní Business Central

Pro správnou funkci add-onu je potřeba nastavit a založit i jiné nastavení v Business Central.

|Nastavení|Popis|
|-|-|
|**Účty v účtové osnově**|V účtové osnově je nutné založit finanční účty pro sledování podstoupených pohledávek, nákladové a výnosové účty pro přeúčtování faktoringu; pokud již neexistují.|
|**Účto skupiny pro faktoring**|Přes Účto skupiny zákazníků je nutné založit nové účto skupiny pro faktoring, které se budou používat pro účtování faktoringu. ![Účtoskupiny pro faktoring](media/faktoring_setup_groupes.png)|
|**Náhradní účto skupiny zákazníka**|Je nutné založit nové kombinace náhrad účto skupin zákazníka (dostupné ze stránky Náhr. Účto skupiny zákazníka).![Náhradní účtoskupiny pro faktoring](media/faktoring_setup_groupes_alt.png)|

### Nastavení faktoringu

Na stránce Nastavení faktoringu je třeba provést základní nastavení pro modul faktoring: 
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nastavení faktoringu** a poté vyberte související odkaz.
2. Na kartě faktoringu vyplňte následující pole:
    - **Účto skupina faktoringu** – účto skupina, která je použita pro účtování faktoringové pohledávky 
    - **Protiúčet nákladů** – účet, na který se zaúčtuje pohledávka za zákazníkem 
    - **Protiúčet výnosů** – účet, na který se zaúčtuje výnos z faktoringu 
    - **DPH účto skupina zboží** – zde je třeba nastavit DPH účto skupinu zboží, která v kombinaci s DPH obchodní účto skupinou ze zákazníka-faktora reprezentuje účtování bez DPH 
    - **Přeúčtovat původní položku** – volba ANO umožňuje dále sledovat pohledávku za původním zákazníkem na podrozvahových účtech 
    - **Účto skupina přeúčtování** a **Protiúčet přeúčtování** – podrozvahové účty, na kterých se bude dále sledovat pohledávka k původnímu zákazníkovi 
    - **Čísla faktoringů** – číselná řada, kterou budou faktoringy číslovány   
![Nastavení faktoringu](media/faktoring_setup.png)
3. Po vyplnění polí můžete kartu zavřít.

### Šablony faktoringu 
Je možné definovat šablony pro převod faktoringových smluv do dokumentů Microsoft Word. Dokument je možné vytvořit na kartě faktoringu pomocí funkce **Vytvořit dokument faktoringu**.


**Viz také**

[Faktoring](ac-factoring.md)  
[Financial Pack](ac-finance-pack.md)  
