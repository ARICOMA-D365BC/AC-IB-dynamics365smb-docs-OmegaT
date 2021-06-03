---
title: "AC Promis - Realizace přepravy"
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


# <a name="ac-pm-transportation"></a>Realizace přepravy

## POPIS PROCESU
Proces začíná předáním objednávky na realizaci přepravy zboží nebo ručním založením dle operativních potřeb disponenta resp. dispečera.

Odpovědná osoba za dokončení objednávky přepravy zkontroluje nebo upraví pořadí realizace nakládek a vykládek i s možností korekce plánovaných časů jednotlivých bodů přepravy a přiřadí dopravce, který bude realizovat přepravu. V případě vlastní realizace přepravy přidělí potřebné zdroje. Před dokončením procesu přípravy objednávky přepravy jsou pomocí nástrojů M&G vytvořeny itineráře úseků mezi jednotlivými body přepravy, vypočteny časy a vzdálenosti potřebné pro realizaci dle plánu. V rámci přeprav realizovaných vlastními zdroji může dispečer provést úpravu trasy v mapových podkladech. Zaplánovanou objednávku přepravy dispečer odešle do komunikačního zařízení přiřazeného vozidla.

V případě chybějící kapacity vlastních zdrojů může být objednávka přepravy nabídnuta k realizaci subdopravci. Poptávku subdopravce řídí odpovědná osoba (disponent/dispečer), která dle smluvených podmínek se subdopravcem doplní cenu za realizaci, číslo vozidla, nákl. vozu, případně kontakt na řidiče. Podklady k realizaci přepravy subdopravcem jsou zaslány formou tiskové sestavy obsahující informace o bodech nakládek a vykládek s časy, ve kterých mají být jednotlivá místa obsloužena, smluvní cenu za realizaci přepravy a event. potřebné přepravní a dodací podmínky.

V průběhu realizace přepravy dispečer sleduje stav realizace jednotlivých nakládek/vykládek, provádí kontrolu elektronického sběru dat z vlastních vozidel a dle potřeby komunikuje s řidičem a zajišťuje mu backoffice pro realizaci. Řidič přihlášený do vozidla zadává pomocí komunikačního zařízení údaje o prováděných aktivitách. Tyto údaje jsou online přenášeny ke zpracování do software, který slouží dispečerům ke sledování vozidel (Transics nebo Webdispečink). NAV tyto data v pravidelných intervalech stahuje a zpracovává. Na jejich základě vyhodnocuje stav realizace jednotlivých bodů přepravy a tedy i stav realizace jednotlivých komodit, které jsou na tyto body přepravy navázané. V případě realizace přepravy subdodavatelem jsou data o průběhu realizace zadávána ručně dispečerem (např. skutečný čas příjezdu na nakládku).

Součástí realizace přepravy je tvorba a evidence průvodních dokladů, které jsou pro řidiče dokladem o provedení nakládky nebo vykládky (dodací listy, CMR, apod.). Průvodní doklady slouží jako podklad k fakturaci, proto je řidič realizující poslední etapu přepravy povinen odevzdat všechny potvrzené průvodní doklady zpět k zaevidování do NAV.

Po dokončení přepravy provádí odpovědná osoba kompletaci dat a kontrolu odevzdaných průvodních dokladů. Jsou-li doklady kompletní, může být zahájen proces fakturace.

### PŘIDĚLENÍ ZDROJŮ NA PŘEPRAVU
Zdroje na přepravu jsou zadávány s ohledem na dodavatele, který byl určen pro realizaci přepravy. V případě realizace vlastními zdroji, je při jejich přiřazení k přepravě kontrolována časová disponibilita daného zdroje. Součástí je kontrola, že vozidlo, nákl. vůz nebo řidič není v daném čase přidělen na jinou přepravu, nebo nemá plánovanou absenci v daném čase (dovolená, školení, lékař…). 

V rámci přepravy má možnost dispečer zkontrolovat plnění požadavků, restrikcí a vlastností plynoucích ze zásilek, distribučních míst použitých na přepravě, zemí distribučních míst přepravy vůči vlastnostem a restrikcím plynoucích z přiřazených vozidel, nákl. vozů a řidičů na přepravě.
Současně je dispečer při potvrzení přepravy upozorněn na blížící se STK kontrolu vozidla/nákl. vozu zadané na kartě příslušného zdroje. 

V případě realizace externími zdroji není při přiřazení zdroje na přepravu kontrolována jejich skutečná disponibilita, ale pouze disponibilita v rámci plánovaných přeprav v IS. Není cílem udržovat evidenci celého časového plánu externích zdrojů. Za poskytnutí volného externího zdroje odpovídá subdopravce. Při využívání externích dopravců lze provádět kontrolu na evidenci jejich pojištění.

#### Disponibilita vlastního vozového parku a řidičů
Odpovědná osoba (disponent/dispečer) má k dispozici vícero nástrojů, které mu umožní sledovat nejenom aktuální disponibilitu vlastních vozidel/nákl. vozů a řidičů, ale také dostat přehled o tom, ve kterém místě a čase končí poslední plánovaná přeprava jednotlivých vozidel. To umožňuje disponentům operativně reagovat při zajištění další potencionální zakázky s minimalizací nákladů na přesun vozidel mezi přepravami. Jedná se zejména o Časovou mapu vozidel.

Tento formulář umožňuje:
- Zobrazit rezervovaný čas jednotlivých zdrojů (vozidel, řidičů, nákladních vozů).
- Zobrazit barevně rozlišené rezervace dle typu Absence vs. Přeprava.
- Zobrazit pojmenování rezervace – pouze textově.
- Otevřít z konkrétní rezervace odkaz na odpovídající doklad přepravy či absence.
- Přepínat zobrazení časové osy v detailu Minuty/Hodiny/Dny/Týdny s tím, že vždy se zobrazí stejný počet časových úseků (cca 70).

Přehled vlastních volných vozidel s poslední plánovanou přepravou v požadované zemi/městě k aktuálnímu dni.

### VÝPOČET A ÚPRAVA TRASY
Součástí každé přepravy jsou minimálně dvě zeměpisná místa, mezi kterými je potřeba naplánovat trasu. Jedná se v podstatě o definici pořadí jednotlivých řádků přepravy, pro usnadnění systém obsahuje propojení s externím systémem.

Vytvořené itineráře tras lze v NAV upravovat doplněním průjezdných bodů a provést aktualizaci výpočtu kilometrů a časů dle provedených úprav. Díky této integraci je možné zobrazení itineráře v mapových podkladech.

Systém využívá při výpočtu plánování trasy evidenci již vytvořených itinerářů, které mohou být zakládány ručně bez aktuální potřeby využití v přepravách nebo generovány na základě plánovaných přeprav. Evidence itinerářů umožňuje zohlednit i zkušenost dispečerů, řidičů a další vlastnosti, které nelze exaktně spočítat. Informace zanesené do konkrétního itineráře jsou využity při jeho dalším použití na přepravách. Součástí evidence mohou být i alternativní trasy pro daný úsek (itinerář) a jedna z nich je definována jako výchozí pro plánování přeprav. Dispečer může na přepravě operativně vybrat jinou variantu trasy.

#### Integrace s Map & Guide
Pro usnadnění výpočtu trasy mezi jednotlivými body přepravy je systém integrován s mapovými podklady Map & Guide. Každý profil trasy může obsahovat vlastní nastavení podmínek pro výpočet optimální trasy zohledňující např. omezení výšky, šířky, délky, celkové hmotnosti a zatížení nápravy, zákazy a omezení průjezdů a další.

Jedná se o výpočet čistých kilometrů a času pro realizaci dopravy v již naplánovaném pořadí míst, které je potřeba obsloužit vozidlem s požadovaným profilem. Plánovaný výpočet trasy nezohledňuje predikce předepsané doby řízení a odpočinku, ani zbývající dobu jízdy a zbývající dobu směny řidiče nebo posádky.

Po stanovení profilu trasy přepravy (např. tahač s návěsem, dodávka, osobní vůz, tahač s nebezpečným nákladem…) je server s mapovými podklady dotázán o výpočet jednotlivých úseků trasy, na které je přeprava rozdělena. Pro úseky přepravy realizované vlastními zdroji je v NAV zakládán itinerář s počátečním a cílovým bodem v detailu položek průjezdných bodů, společně s informací o zpoplatněných a nezpoplatněných kilometrech po jednotlivých zemích a rozdělení poplatků v rámci itineráře. Pro přepravy realizované externími přepravci je pouze proveden výpočet kilometrů a časů potřebných na realizaci daného úseku a zaznamenán do přepravy. 

Do výpočtu plánované trasy je zařazen také nájezd přiřazeného vozidla, který je aktualizován na základě koncového místa jeho předchozí přepravy.

### KALKULOVANÉ NÁKLADY A ZISK PŘEPRAVY
Vyčíslené plánované kilometry a čas potřebný na realizaci přepravy jsou podkladem pro výpočet kalkulovaných nákladů přeprav. Pro realizaci přeprav vlastními zdroji je ke stanovení kalkulovaných nákladů využito možnosti parametrizace samostatně sazby za kilometr a za hodinu vozidla ve vazbě na profil výpočtu trasy (dodávka, tahač s návěsem…) a tranzit dané přepravy. 
Náklady přepravy realizované externími dopravci lze vyčíslit s použitím platného ceníku. Pro jednotlivé externí dopravce lze v ceníku stanovit ceny dle plánované vzdálenosti, jednotkové ceny za komoditu, nebo pomocí paušální částky za realizaci přepravy.

Interní kalkulované náklady i smluvní náklady přepravy realizované externím dopravcem jsou v přepravě evidované formou fakturačních řádků. Tato forma evidence nákladů umožňuje rozpuštění jejich částky na komodity jednotlivých zásilek zařazených do přepravy v algoritmu podílu ujetých kilometrů jednotlivých komodit. Výsledkem je okamžité vyčíslení zisku/ztráty přepravy porovnáním plánovaných nákladů stanovených na přepravě a prodejní ceny zásilek realizovaných přepravou. Rozpuštění nákladů přímo na jednotlivé komodity zásilky umožňuje také vyčíslení zisku/ztráty jednotlivých zásilek nebo jednotlivých podzásilek.

### ŘÍZENÍ A REALIZACE PŘEPRAVY
Potvrzením přepravy obsahující všechny potřebné informace pro realizaci jsou generovány položky kontrol, které jsou požadavkem pro monitorování akcí v průběhu realizace přepravy. Pravidla vytváření položek kontrol ve vazbě na jednotlivé typy řádků přepravy lze definovat dle potřeb společnosti. Standardně je pro nájezd vyžadováno pouze potvrzení jeho započetí, kdežto u nakládek nebo vykládek je požadováno potvrzení příjezdu a odjezdu z daného místa ve dvou samostatných akcích.

#### Integrace s Transics, Webdispečink
Pokud společnost používá ve svých automobilech palubní jednotky od firmy Transics nebo Webdispečink, Plán přepravy (položky kontrol pro jednotlivé řádky přepravy) odesílá dispečer do vozidel přímo z objednávky přepravy v NAV. Řidič dostává do palubní jednotky informaci o požadavku na realizaci přepravy a potvrdí jeho příjem. Samotné zahájení přepravy je realizováno buď potvrzením prvního bodu přepravy řidičem (obvykle zahájení nájezdu), nebo automaticky na základě ukončení posledního bodu předchozí realizované přepravy.

Řidič je v komunikačním zařízení vozidla při zastavení vyzván k potvrzení prováděné akce např. příjezdu na místo nakládky nebo vykládky. Po opětovném rozjetí vozidla a ujetí definované vzdálenosti od daného místa, ve kterém byla potvrzena akce příjezdu na požadované místo, může být automaticky provedeno potvrzení odjezdu, nebo řidič může sám v komunikačním zařízení vozidla akci odjezdu z daného místa potvrdit ručně. 

Monitorovací jednotka ve vozidle průběžně zaznamenává data o průběhu jízdy a realizaci bodů přepravy a zasílá do centrálního systému (Transics, Webdispečink..). Odtud jsou data v pravidelných intervalech stahována do NAV a na základě nich je v IS aktualizován stav realizace jednotlivých bodů přepravy a tedy i realizace jednotlivých komodit zásilek.

#### Pult sledování přepravy
Ke sledování stavu realizace jednotlivých bodů přepravy slouží v NAV tzv. Pult sledování přepravy. Dispečer zde může vidět, ve kterém bodě přepravy se vozidlo nachází, nebo zda je na cestě mezi dvěma body a zobrazit aktuální pozici vozidla v mapovém podkladu.
V Pultu je také možné provádět ruční doplnění chybějících dat, pokud řidič ve vozidle neprovádí požadované potvrzení akcí, nebo se jedná o chybu v komunikaci s monitorovacím zařízením. Dispečer má tak online přehled o realizaci a možnost event. úprav dat dle skutečné realizace.
Při realizaci přepravy subdodavatelem, kdy data z monitorovacích zařízení externích vozidel nejsou k dispozici, je pult sledování využíván k ručnímu doplnění dat o realizaci jednotlivých bodů přepravy. 

Dispečer má možnost filtrovat záznamy v Pultu sledování tak, aby mohl v časové souslednosti sledovat přepravy např. jemu přidělené nebo přepravy určitého typu, apod.

#### Sledování plnění plánu
V položkách kontrol jednotlivých bodů přepravy je doplnění skutečného času dané kontroly provedeno potvrzení realizace a vyhodnocení splnění časové rezervy skutečného času vůči plánovanému dle nastavených pravidel. Současně dochází ke kontrole dodržení časové posloupnosti bodů přepravy, jako např. že vykládka nemůže předcházet nakládce, nebo odjezd z místa přepravy nemůže předcházet příjezdu na daný bod a jiné.

#### Pult zpráv vozidel
Pro online komunikaci s vozidlem může být také využito pultu zpráv vozidel, který umožňuje dispečerovi zaslat zprávu do jednoho nebo více vozidel najednou. Pult zobrazuje příjmové i odchozí zprávy v komunikaci s vozidlem. Pult je využíván ke komunikaci přes Webdispečink.

### EVIDENCE DOKLADŮ PŘEPRAVY A PŘÍPRAVA FAKTURACE
Každá objednávka zákazníka (Zásilka) v sobě obsahuje seznam požadovaných dokladů souvisejících s realizací přepravy. Každá Zásilka teoreticky může obsahovat jiný typ průvodních dokladů. 
Po samotné realizaci je prováděn sběr a evidence těchto dokladů ve vazbě k původním objednávkám zákazníka. Fyzický sběr dokladů je prováděn dle možností řidičů a společnosti. 
Jiný odpovědný pracovník na základě identifikace objednávky zákazníka (zásilky) z odevzdaného dokladu provede jeho zaevidování do IS.

Po připojení požadovaných dokladů a kontrole správnosti cen zásilky může být doklad předán k fakturaci. Při kontrole cen zásilky před fakturací je potřeba zohlednit, zda fakturace probíhá na základě objednaného množství, skutečné realizace nebo také zda nerealizované množství nemá zůstat předmětem fakturace, protože příčinou jeho nedoručení není přeprava.

### VYHODNOCENÍ PRŮBĚHU PŘEPRAVY
Ze software, který zaznamenává pohyb vozidla a akce řidiče v průběhu přepravy, jsou průběžně stahována data do NAV a evidované v položkách vozidla a položkách aktivit.

Na základě dat položek kontrol může dispečer realizovat ruční vyhodnocení průběhu jednotlivých bodů přepravy, ale také provést vyhodnocení přepravy jako celku. Dispečer při tomto vyhodnocování může ověřit správnost zadání dat řidičem přímo v aktivitách evidovaných pro danou přepravu.

### ŽURNÁL AKTIVIT ŘIDIČE
Data o aktivitách řidiče nebo posádky jsou průběžně kompletována z monitorovacího sw a plněna do přehledu žurnálu aktivit řidiče. Žurnál může být ručně dle potřeby doplněn, pokud data z monitorovacího zařízení nejsou kompletní, nebo se jedná o vozidlo, které nemá monitorovací zařízení.

Záznamy v žurnálu mohou sloužit pro další vyhodnocení práce řidiče, jako jsou počty provedených nakládek nebo vykládek, času strávených jednotlivými aktivitami v průběhu realizace, práce o víkendech nebo svátcích, apod.
Záznamy v žurnálu slouží také jako podklad pro vyúčtování pracovních cest řidičů dle výkonů v jednotlivých zemích a stanovení nároku na stravné.

## <a name="see-also"></a>Viz také  
[AC ProMIS](ac-pm-promis.md)