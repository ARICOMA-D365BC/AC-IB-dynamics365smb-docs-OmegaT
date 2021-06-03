---
title: AUTOCONT SOLUTIONS - Parcels | Microsoft Docs
description: This section describes parcel functionality - Balikobot Integration
author: ac-kunes
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Czech, shipment, parcels, Shipping
ms.date: 06/24/2020
ms.author: v-makune
---

# Zásilky

Addon zásilek slouží k vytvořání zásilek a přímému tisku štítků vybraných dopravců, odesílání dat o zásilkách přepravci a objednání samotného svozu balíků. Pomocí totoho rozšíření je zrychlen proces zpracování a vytváření zásilek posílaných zákazníkům. Tento Addon využívá API služby Balíkobot.

Tento addon je stavěn na základu načítání čárového kódu (čísel) účtovaných dokladů. Zásilky je možno vytvářet z účtovaných prodejních dodávek a faktur. Pokud uživatel bude vytvářet zásilku z účt. prodejní dodávky, zásilka se vytváří bez dobírky a z faktur s dobírkou.

Seznam přepravců:
 - Česká pošta s.p.
 - DHL
 - Direct Parcel Distribution CZ s.r.o.
 - Geis CZ s.r.o.
 - Gebrüder Weiss
 - General Logistics Systems Czech Republic s.r.o.
 - IN TIME SPEDICE s. r.o.
 - Messenger
 - Pošta bez hranic (Frogman s.r.o.)
 - PPL CZ s.r.o. 
 - Slovenská pošta a.s.
 - TNT
 - TOPTRANS EU a.s.
 - Uloženka s.r.o.
 - UPS
 - Zásilkovna s.r.o.


## Vytvoření prodejní objednávky
Základním krokem procesu vytváření zásilek je prodejní objednávka. Data z prodejní objednávky se přenášejí do dalších dokladů, z kterých se vytváří zásilky, proto je nezbytné zadat bezchybně data již na počátku procesu. (Stejně tak se zásilky dají vytvářet z prodejních faktur.)
### Nutná pole k zadání před vydáním dokladu
- Adresa zákazníka
- Kód přepravce, kód služby přepravce případně kód pobočky přepravce
- Zákazníkovo telefonní číslo, e-mail nebo jeden z těchto údajů
- Kód způsobu platby (pokud se jedná o dobírku), variabilní symbol
- Vaše reference (v případě, že Váš zákazník vyžaduje na štítek např.: své číslo objednávky)

Systém nevydá doklad pokud není vyplněno telefonní číslo a/nebo e-mail! (viz. nastavení kontroly).
Pokud na objednávce není vybraný žádný přepravce, kontrola na vydání dokladu (telefonní číslo a e-mail je vypnutá).
### Volitné pole k zadání před vydáním dokladu
Uživatel již v prodejní objednávce může zadat volitené parametry zásilky. K zadání slouží infomrační panel **Parametry zásilky** na kartě prodejní objednávky. Pomocí tlačítka vložit se otevře okno s parametry z nastavení, které je možno doplnit dle potřeby. Může se jednat například o:
- Kontrola věku adresáta.
- Kontakt na řidiče.
- Donáška do patra.
- Dopolední doručenní.
- A mnohé další.

## Karta zásilky
Karta zásilky se skládá celkem z pěti částí.


### Hlavička zásilky
V hlavičce dokladu jsou pouze povinné údaje potřebné k založení zásilky, pro zadání dalších údajů jako jsou rozměry nebo vzkaz řidiči je nutné využít podokno Parametry zásilky. Každý přepravce a služba přepravce má své specifické parametry, které v případně neplnosti dat nahlásí zpráva, co zásilce chybí za údaj.
### Řádky zásilky
Pro definici počtu balíků v rámci jedné zásilky existuje pole „Počet balíků“. Pokud se bude jednat o balíkovou přepravu (NE PALETOVOU), po zadání počtu balíků se vytvoří řádky zásilky, ke kterým budou přiřazeny jednotlivé štítky od dopravce. V případě paletové přepravy bude toto pole určovat množství jedné manipulační jednotky (nevytvoří se několik řádků, ale vznikne jeden řádek a vyplní se množství; např.: 3 palety).
### Parametry zásilky
Volitelné parametry zásilky.
### Připojené doklady
V podookně připojené doklady je možné vidět všechny dodací listy nebo faktury, které byly vloženy do jedné zásilky (funkční pouze, když se zásilka posílá na jednu adresu) 
### Obsah zásilky
Obsah zásilky je především pro odesílání mimo EU, kdy je nutné udávat informace o tom co je v zásilce.
## Vytvoření nové zásilky z účtovaného dokladu

Po zaúčtování dodání nastává proces vytvoření zásilky pro zákazníka. Jedním ze způsobů je vytvoření zásilky s dodacího listu nebo účtované faktury. Pomocí načítání čísla dokladu se automaticky předvyplní formulář **Vytvořit zásilku**. Tímto krokem uživatel nemusí ručně vypisovat údaje o zásilce.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Vytvořit zásilku** a poté vyberte související odkaz.
1. Vložte číslo účtovaného dokladu (účtovaná prodejní dodávka, účtovananá prodejní faktura) do pole **Číslo dokladu**. Nebo využijte funkci Skenovat kódy (v případě kdy máte čárový kód s číslem dokladu).
1. Uživatel má možnost zadat počet balíků v rámci jedné zásilky.
1. Vyberte funkci **Vytvořit zásilku a vytisknout štítek**.
1. Zásilka je nyní vytvořena a zároveň je ve stavu **Ke svozu**, tzn. má již od dopravce přidělené číslo, štítek a data jsou na straně Balíkobotu).

## Ruční vytvoření zásilky

Zásilky lze vytvářet i ručně bez účtovaných dokladů, např.: pro odeslání dopisů, nebo dodatečného balíčku. Na přehledu zásilek se nachází funkce „Nový“, který otevře prázdnou kartu zásilky. Karta Zásilky a karta Vytvořit zásilku jsou skoro stejné. Při ručním vytváření zásilky, se nedá skenovat číslo účtovaného dokladu a údaje se musí vyplnit ručně. Při tomto vytváření je nutné zadat Stav na Nová a přídat jeden řádek. Po nachystání dat pro zásilku funkce „Přidat ke svozu“ zaeviduje zásilku v systému Balíkobotu. Poté je nutné ručně nechat vytisknout štítek.

Pro ruční vytvoření zásilky jsou kroky následující:
1. Na přehledu zásilek zvolit funkci **Nový**
2. Naplnit potřebná pole pro daného přepavce a jeho službu
3. Funkce **Přidat ke svozu** (zásilka je ve stavu **Ke svozu** a je možné tisknout štítek)
4. Funkce **Tisk štítku**
5. Zásilka je připravena k objednání svozu.

## Úprava zásilky
Upravovat zásilky lze pouze pokud jsou ve stavu **Nová**. Pokud je zásilka ve stavu **Svozeno** nelze ji již editovat. Pro úpravu/smazání informací zásilky, musí být ve stavu **Ke svozu**. Pomocí funkce Odebrat ze svozu se změní stav z **ke svozu** na **Nová**.

 Po tomto kroku je třeba uvědomit přepravce, že zásilku mažete nebo upravujete. V tento okamžik je zásilce odebráno číslo od přepravce a je smazán štítek. Po upravení dat uživatel použije funkci **Přidat ke svozu** a pro vytištění nového štítků použít funkci **Tisk štítků**.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Zásilky** a poté vyberte související odkaz.
2. Postavit se na řádek ze zásilkou a použít funkci **Odebrat ze svozu**
3. Otevřít danou zásilku (nyní má stav **nová**)
4. Doplnit údaje/hodnoty o zásilce (Změna přepravce, počet balíků, hmotnost, rozměry...)
5. Použít funkce **Přidat ke svozu** (zásilka je ve stavu **Ke svozu** a je možné tisknout štítek)
6. Dále je nutné použít funkci **Tisk štítku**
7. Zásilka je připravena k **objednání svozu**.

## Objednání svozu
Objednání svozu slouží k předání informace o Vašich zásilkách dopravci. Samotný proces objednání svozu je jednoduchý, slouží k tomu funkce „Objednat svoz“ na přehledu zásilek. 

Funkce zobrazí seznam přepravců s počtem zásilek, které ještě nebyly objednány ke svozu. Uživatel může objednat svoz pouze pro vybraného přepravce nebo pro všechny najednou.

Pro objednání svozu je nutné udělat tyto kroky:
1. Na přehledu zásilek vybrat funkci **Objednat svoz**
2. Na kartě objednat svozu zvolit, zda se bude objednávat svoz jednoho přepravce (**Objenad svoz**) nebo všech (**Objednat všechny svozy**).
3.  Po spuštění funkce se vytiskne **Předávací protokol svozu**.

## Tisk předávacího protokolu svozu
Předávací protokol je generován ze strany přepravců.
Tato sestava se může nastavit, aby se tiskla automaticky po objednání svozu. Nastavení automatického tisku je v okně **Nastavení Balíkobotu**. Pro dodatečný tisk předávacího protokolu vybraného přepravce slouží funkce se stejným názvem na přehledu zásilek, kdy stačí stát na jedné ze zásilek daného přepravce v daný den svozu. Poté se vytiskne soupiska všech zásilek od vybraného přepravce za určený den.

Pro dodatečný tisk předávacího protokolu svozu:
1. Stoupnout si na zásilky z daného svozu a použít funkci **Tisk předávacího protokolu svozu**.
2. Otevře se PDF soubor, který se následně vytiskne z okna prohližeče.

## Sledování zásilek
Na přehledu zásilek lze na první pohled zahlédnout stav přepravy zásilky. Tento stav není strukturován a je pouze informativní bez detailu. Pro aktualizaco toho stavu na řádku zásilky slouží tlačítko **Aktualizovat stav přepravy**. 

Pokud chcete zobrazit jednotlivé stavy od přepravce využijte funkci na přehledu zásilek **Sledování zásilky**, která otevře stránku s jednotlivými stavy přepravy.


## Kontroly a omezení

 - Pokud jsou na prodejní objednávce vyplněny pole Kód přepravce a Kód služby přepravce, je nutné zadat telefonní číslo a e-mail příjemce. POkud pole nebudou vyplěny nelze doklad vydat.
 - Při zadávání dat na kartě zásilky (automaticky pomocí načtení kódů, nebo ručně) je na kartě zásilky funkce **Ověřit data zásilky**. PO spuštění dostanete informaci, zda jsou předávané informace v pořádku.
 - Jedno expediční místo může být přiřazeno jedné lokaci. Vzniká vazba 1:1.

## Viz také
[Nastavení zásilek](ac-parcels-setup.md)  
[AC Productivity Pack](ac-productivity-pack.md)  
[AUTOCONT řešení](../index.md)
