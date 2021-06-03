---
title: "AC Promis - Objednávky"
author: Autocont
ms.custom: na
ms.date: 07/18/2018
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.prod: dynamics-nav-2018
ms.translationtype: Human Translation
ms.sourcegitcommit: 
ms.openlocfilehash: 
ms.contentlocale: cs-cz
ms.lasthandoff: 

---


# <a name="ac-pm-shipment-invoice"></a>Objednávky

Obchodní případ začíná poptávkou odběratele na realizaci přepravy. Poptávka může vznikat na základě dlouhodobého ujednání mezi objednatelem a dodavatelem služby podloženého smlouvou, nebo také na základě aktuální potřeby libovolného odběratele bez předem domluvených smluvních podmínek. 

Odběratel je v systému zaevidován v rámci evidence nazvané Zákazníci, kde jsou evidovány, mimo jiné, údaje jako způsob příjmu objednávek na realizaci přepravy, ceník služeb, termín a způsob realizace, způsob fakturace, apod. Karta zákazníka musí být do systému zaevidována před samotnou realizací příjmu objednávek. 

Při evidenci objednávky dochází k výběru nebo pořízení dat, které s evidencí objednávky přímo souvisí. Jedná se např. o místa nakládek, místa vykládek, ale také o specifikaci samotného předmětu přepravy. Dle způsobu komunikace mohou být data zakládána automaticky dle domluvených pravidel, jsou však data související s objednávkou vyhledána a založena ručně. Systém obsahuje podpůrné funkce, které umožňují disponentovi využít již jednou evidovaná data a předcházet tak duplicitám v jednotlivých číselnících. Rovněž může být využito údajů z předešlých obchodních případů daného odběratele.

Součástí procesu příjmu objednávky (tzv. Zásilka) je stanovení ceny za realizaci služby. Může být buď smluvní nebo dohodou. Ke stanovení prodejní ceny systém pomáhá výpočtem předpokládaných nákladů nebo porovnáním nákladů a výnosů z podobných objednávek stejného nebo jiného odběratele. Variabilita ceníků umožňuje definovat ceny dle typu přepravovaného zboží, dle objemu či hmotnosti přepravovaného zboží, dle počtu přepravovaných palet zboží, nebo za celý náklad v rámci zásilky a to vše ve vazbě na místo nakládky nebo vykládky.

V neposlední řadě je úkolem disponenta zaplánování objednávky do realizace dle požadovaného termínu a místa přepravy a možností firmy. Je možné zásilku připojit k již existující naplánované přepravě nebo vytvořit zcela nový požadavek, to vše obvykle po konzultaci s dispečerem. Předáním zásilky k realizaci dispečerovi končí proces příjmu a zaplánování objednávky zákazníka.


## PŘÍJEM ZÁSILKY
Objednávka od zákazníka na realizaci přepravy je v systému evidovaná Zásilkou. Zásilka kromě standardních náležitostí jako jsou kdo a kdy si převoz komodit objednal, obsahuje také specifické požadavky související s objednávkou převozu zboží. 

### Obecné informace o zásilce

Prvním krokem zaevidování zásilky je doplnění informace o odběrateli. V případě, že požadovaný odběratel ještě není v číselníku zákazníků, dojde k jeho založení přes evidenci kontaktů. Dalšími údaji můžou být reference na číslo objednávky zákazníka, požadovaný typ vozidla, identifikace disponenta, který má zásilku na starosti, typ zásilky, datum objednávky a typ výpočtu ceny, od kterých se odvíjí ceníková cena… 

K vytvoření zásilky lze využít funkce pro kopii existující zásilky, průvodce pro vyhledání podobné zásilky a její kopie zásilky nebo vytvoření opakovaného závozu.

### Nakládka a Vykládka
Pro zadání místa nakládky/vykládky a požadovaných časů pro realizaci slouží řádky zásilky. Každá zásilka musí obsahovat minimálně jedno místo nakládky a jedno místo vykládky. Při stanovení místa nakládky a vykládky si disponent může vybírat z evidence distribučních míst, které již jsou v systému evidované nebo přímo z řádku zásilky založit pomocí průvodce nové. 

### Komodity zásilky
Zásilka musí také obsahovat alespoň jednu komoditu (zboží, které je předmětem přepravy) s nenulovým množstvím. Každá komodita musí obsahovat vazbu na řádek nakládky a řádek vykládky dané Zásilky. Volitelně může obsahovat doplňující údaje jako hmotnost, objem, počet palet, externí kód pro nakládku nebo vykládku apod.

### Cena realizace
Pro dokončení příjmu zásilky je stanovení ceny za realizaci přepravy požadovaných komodit. Ceny zásilky jsou evidované formou fakturačních řádků. K ocenění zásilky může dojít na základě definovaných zákaznických ceníků, ručním vložením ceny, nebo na základě výpočtu očekávaných nákladů na základě komunikace s mapovými podklady M&G. Zásilka obsahuje také funkci pro porovnání s realizovanými zásilkami z historických dat.

Informační panely zásilky poskytují nejenom velké množství informací pro operativní rozhodování, ale také provozní informace s možností rychlého přesunu k dokladům o realizaci a fakturaci zásilky. V rámci těchto panelů může uživatel také sledovat vyčíslení provize zásilky.
### Související služby
Pokud je součástí realizace zásilky potřebná služba spojená s dopravou, ale dopravní společnost tuto službu nezajišťuje, lze objednávku služby zaevidovat jako součást zásilky. Jedná se o služby jako např. přeskladnění, proclení apod.

### Stavové řízení
Zásilka obsahuje víceúrovňové stavové řízení z různých pohledů, které zachycují její stav plánování, realizace (z pohledu přepravy) a fakturace zásilky. Tyto stavy jsou na sobě nezávislé.

### Doplňkové funkcionality
Zásilka obsahuje nástroje obecných a průvodních textů pro evidenci specifických požadavků na zásilku z různých zdrojů (zákazník/distribuční místo, komodita…) např. dodací podmínky. 

### Příjem objednávky integrací
Součástí standardní funkcionality modulu nejsou zakomponované nástroje pro import objednávek. Integrace je realizována individuálně na základě zákaznických požadavků a dodaných struktur. 

## PLÁNOVÁNÍ A OPTIMALIZACE
Pro plánování realizace zásilek bez využití metod plánování je v NAV řada podpůrných funkcí pro usnadnění práce při sestavování plánu přepravy s velkou škálou uživatelských možností přístupů ke způsobu realizace:
- Vytvoření objednávky přepravy ze zásilky ve vazbě 1:1, tedy jedna přeprava realizuje pouze jednu objednávku zákazníka.
- Vytvoření objednávky přepravy zahrnutím více zásilek do jedné přepravy (N:1), tedy jedna přeprava realizuje více objednávek. Do přepravy mohou být zahrnuty zásilky různých zákazníků, ale také zásilky s různými body nakládky a vykládky, které je potřeba v rámci objednávky obsloužit. Seznam zásilek takto vkládaných do přepravy je plně v režii dispečera přepravy.
- Vložení jedné zásilky nebo více zásilek najednou do již existující přepravy.
- Rozložení jedné zásilky do více přeprav (1:N), ať už z důvodu potřeby rozložení nákladu do časově souběžných přeprav, nebo také realizaci přepravy nákladu formou postupného plnění realizace zásilky.
- Rozdělení zásilky na dílčí podzásilky pro potřeby přeložení v depu a umístění jednotlivých podzásilek na různé přepravy. Tento model umožňuje realizaci zásilek formou tzv. sběrné služby, nebo využití plánování Linehaul mezi depy…. 

V procesu plánování přeprav v NAV jsou dispečerovi dostupné informace týkající se vytížení vozidla, využití jeho ložní plochy, plánovaných časů a kilometrů přepravy, nákladů na realizaci a vyčíslení ziskovosti přepravy.

Optimalizační metody podporující minimalizaci ujetých kilometrů, časů a nákladů pro dosažení obsluhy požadované lokality při plánování trasy nejsou přímou součástí NAV.

### Integrace s Plantour
Pro oblast distribuce obsahuje systém funkcionalitu integrace s externím software pro plánování a optimalizaci tras PLANTOUR od společnosti DIGITECH ČR, spol. s r.o. Díky tomuto spojení je možné na základě každodenního zpracování objednávek navrhovat optimální trasy pro závoz dodacích míst včetně zohlednění zpětných svozů. Trasy jsou navrhovány na základě aktuálních objednávek a vozového parku dynamicky tak, aby byly optimální z hlediska nákladů a zároveň splňovaly všechny zadané restrikce (doba závozu, limit vytížení vozidla, požadavky na vybavenost vozidla aj.).


## <a name="see-also"></a>Viz také  
[AC ProMIS](ac-pm-promis.md)