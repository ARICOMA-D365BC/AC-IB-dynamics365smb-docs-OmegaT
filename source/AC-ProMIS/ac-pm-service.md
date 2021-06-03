---
title: "AC Promis - Servis"
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


# <a name="ac-pm-service"></a>Servis

Tato kapitola popisuje proces zpracování servisní zakázky zaměřené na specifika dopravních prostředků. Nejsou popisovány standardní funkcionality modulu Servis.

## KMENOVÁ DATA MODULU SERVIS
### SPRÁVA SERVISNÍHO MODULU
#### Nastavení servisu
##### Obecné

- Bezpečná průb. doba hlášení – v poli se nastaví výchozí období předstihu před vypršením časového termínu pro provedení servisní činnosti. S tímto předstihem pak budou servisní činnosti avizovány k provedení; jedná se tedy o omezení období časovou hranicí v budoucnosti, ve kterém systém testuje servisní činnosti k provedení. 
- Bezpečná průb. doba zakázky – v poli se nastaví časová rezerva pro  plánování zpožděných servisních činností. Pak datum zahájení servisní zakázky pro zpožděné servisní činnosti se navrhne jako Pracovní datum + Bezpečná průb. doba zakázky.
- Výchozí jednotka výkonu – v poli se nastaví měrná jednotka, pro kterou je testován předstih vypršení výkonu předepsaného pro provedení servisní činnosti
- Stav pro aut. založení PS z vozidel – v poli se nastaví stav karty vozu /nákladního vozu, při jehož dosažení se automaticky založí synchronizovaný předmět servisu

##### Povinná pole

Dále jsou zmíněna některá speciální pole ovlivňující chování systému v oblasti servisu

Parametr 

- Povinný prodejce – vynucuje kontrolu použití prodejce v servisních dokumentech (je rovněž nositelem dimenze střediska)
- Nutný kód příjemce – vynucuje zadání Kódu příjemce v hlavičkách servisních dokladů, existuje-li ve vazbě na zákazníka alespoň jeden záznam v tabulce Adresa příjemce. Tímto nastavením se kontroluje použití správné poštovní adresy na servisních dokladech.

### SPRÁVA ZDROJŮ SERVISU
#### Zdroj pro odvádění servisních činností

- Povinná servisní činnost – pole aktivuje při účtování řádku servisu i účtování položky servisní činnosti; se zdrojem musí být v řádku servisu zadán i kód servisní činnosti.

### SPRÁVA VOZOVÉHO PARKU
#### Šablony deníků servisních činností

Deníkové uspořádání plánování servisních činností umožňuje paralelní práci více uživatelů. Je zapotřebí pro uživatele definovat potřebné šablony deníků servisních činností. Prostřednictvím šablon je pak umožněn přístup do deníků.

#### Nastavení deníku servisních činností
- Centrum odpovědnosti – ke každému deníku by mělo být přiřazeno centrum odpovědnosti. Tento parametr se pak přenáší do servisních hlaviček a ovlivňuje zobrazování servisních dokladů pro uživatele, u kterých je nějaký filtr servisních center odpovědnosti nastaven.

#### Servisní činnosti
Tabulka je určena k nastavení servisních činností, které se mají sledovat a vykazovat u vozidel / nákladních vozů. 

- Je možné nastavit servisní činnost i pro jinou měrnou jednotku výkonu než km (např. motohodiny). 
- Dále je možné nastavit Systém provádění servisu – je-li nastavena volba Servis, pak servisní činnosti jsou primárně odváděny prostřednictvím servisních zakázek; je-li nastavena volba Nákup, pak je daná servisní činnost zajišťována externě nákupem servisní služby. Je možné nastavit i dodavatele externě zajišťované servisní služby.
- Typ sledovaného výkonu – je-li zvolena Pozice, pak pro výkonovou servisní činnost systém automaticky nabízí k evidenci stav km získaný z tabulky 4056891 Vehicle Position Entry, tzn. stav km získaný z vnějších telematických systémů. V případě ostatních servisních činností závislých na výkonu jiném, než ujetá vzdálenost (Pozice) – např. motohodiny, se musí pole ponechat prázdné.
- Číslo zdroje – v poli je uvedeno číslo zdroje, se kterým bude servisní činnost účtována prostřednictvím servisní zakázky.

####Skupiny servisních činností
Číselník skupiny servisních činností umožňuje seskupovat servisní činnosti do skupin. Smyslem je snížit administrativu a umožni přiřazování více servisních činností k vozidlům / nákladním vozům prostřednictvím skupiny servisních činností.
#### Přiřazení servisních činností
Jednotlivé servisní činnosti se mohou přiřadit ke skupině servisních činností pomoci nastavení v Přiřazení servisních činností
####  Vztah skupiny předmětu servisu a skupiny dopravních zařízení
Nastavení slouží k řízení automatizace vytváření evidence předmětů servisu z evidencí vozidlo a nákladní vůz.

- Automaticky vytvořit předmět servisu – volba v poli aktivuje automatické založení předmětu servisu dle karty vozidla /nákladní vůz. Okamžik aktivace založení je definován staven karty vozidla / nákladního vozu (vizte Nastavení servisu). 
    * <prázdný> - autom. zakládání je vypnuto.
    * Interní – předmět servisu se vytváří pouze, pokud karta vozu / nákladního vozu je interní.
    * Vše – předmět servisu se vytváří pro kartu vozu / nákladního vozu interní i externí. 

- Komponenta předmětu servisu – volba zakládá nákladní vůz také jako komponentu k nadřazenému předmětu servisu (vůz). Nemá smysl nastavovat pro návěsy / přívěsy, zapnutí parametru přichází do úvahy prakticky pouze pro pevně připojení nákladní vozy. 

#### Nastavení bezpečného výkonu
Nastavení v tabulce je využíváno pro plánování výkonových servisních činností. Umožňuje definovat zbývající výkon do stanoveného limitu pro provedení servisní činnosti. Je-li aktuální zbývající výkon menší než bezpečný, odpovídající servisní činnost je navržena do sešitu servisních činností.
#### Synchronizace evidencí Vozidlo / Nákladní vůz <-> Předmět servisu
Po vytvoření vazby jsou synchronizovány změny provedené v jedné evidenci do druhé evidence:
- Název <-> Popis
- Název 2 <-> Popis 2
- Vyhledávací název <-> Vyhledávací název
- Registrační značka (SPZ) <-> Registrační značka (SPZ)
- Číslo provozovatele <-> Číslo zákazníka

## EVIDENCE PŘEDMĚTU SERVISU
### AUTOMATICKÉ ZALOŽENÍ NOVÉHO PŘEDMĚTU SERVISU
Proces probíhá na kartě Vozu res. Nákladního vozu. Po nastavení evidenčních parametrů se přepne stav na Příprava (resp. dle nastavení servisu):
### DODATEČNÉ ZALOŽENÍ PŘEDMĚTU SERVISU
Proces je zahájen na kartě Vozu resp. Nákladního vozidla. Typicky se týká externích vozů, pro které není nutné se založením karty vozidla automaticky zakládat i kartu předmětu servisu. Karta předmětu servisu se založí až při první servisní zakázce.
- Akce Vytvořit předmět servisu – akce založí novou kartu předmětu servisu nezávisle na stavu karty Vozidla / Nákladního vozu
### PŘIPOJENÍ / ODPOJENÍ PŘEDMĚTU SERVISU
Akce jsou připraveny spíše pro výjimečná použití, kdy z nějakých důvodů dojde k založení předmětu servisu nezávisle na evidenci Vozu / Nákladního vozu, nebo naopak je zapotřebí obě evidence oddělit a dále nesynchronizovat.
## PŘIŘAZENÍ SERVISNÍCH ČINNOSTÍ
### PŘIŘAZENÍ SKUPIN SERVISNÍCH ČINNOSTÍ
Přiřazením jedné nebo více skupin servisních činností se přiřadí k vozidlu / nákladnímu vozu servisní činnosti obsažené v těchto skupinách:
## PLÁNOVÁNÍ SERVISNÍCH ČINNOSTÍ
K podávání požadavků na servis a plánování servisních činností je určen deník servisních činností.
### WORKFLOW ODSOUHLASENÍ SERVISNÍCH POŽADAVKŮ
K tomu, aby z deníku servisních činností mohly být generovány výstupy nových dokumentů nebo přeplánování existujících dokumentů, je nutné pro daný řádek realizovat proceduru odsouhlasení požadavků. Při odsouhlasení figurují 3 role:
- Dispečer – definuje „okno“, ve kterém se má servis realizovat; okno je definováno datem a časem začátku servisu a analogicky je definován i konec servisu
- Správce vozového parku – definuje datum pro provedení servisu ze svého pohledu; ideálně by mělo být navrženo uvnitř časového období definovaného dispečerem, nicméně může být nastaveno libovolně
- Servis – definuje datum analogicky jako Správce vozového parku ovšem z pohledu servisu

Jestliže všechna data jsou uvnitř intervalu definovaného dispečerem a současně datum správce a servisu je stejné, je termín servisu odsouhlasen. Schematicky je odsouhlasení znázorněno na následujícím obrázku: 
- první řádek (zeleně) prošel procedurou odsouhlasení a může poustoupit do další fáze procesu
- druhý řádek (červeně) neprošel procedurou, neboť správce vozového parku nastavil termín provedení servisu mimo plánovací „okno“ . Konflikt nyní musí řešit dispečer a servis. Odsouhlasení může proběhnout v libovolném počtu opakování a potrvá do té doby, dokud nebude dosaženo shody jako v prvním řádku. Dosažení termínové shody je indikováno v poli Termín odsouhlasen.

Zástupci výše uvedených rolí získají řádky deníku servisních činností, které vyžadují jejich pozornost tak, že je vyfiltrují podle polí
- Termín dispečink = Ano (role dispečer)
- Termín spr. voz. parku = Ano (role správce)
- Termín servis = Ano (role servis)
### VYTVOŘENÍ POŽADAVKU NA SERVISNÍ ČINNOST
Požadavky na servis se zadávají do tzv. Deníku servisních činností. Proces se skládá z následující kroků:
- Vložení vozidla
- Nastavení metody servisu
    - Interní – servis prováděný ve vlastním servisním středisku musí mít nastaven Typ dokladu = Servis.
    - Externí – servis prováděný externě musí mít nastaven Typ dokladu = Nákup a vyplněné Číslo dodavatele.
- Zadání požadovaných servisních činností (číselník Servisní činnosti na pásu karet)

Servisní činnosti je možné generovat funkcí Aktualizovat řádek serv. činnosti, která dle zadaných parametrů založí jeden nebo více řádků servisních činností.
Parametry funkce jsou:
- Bezpečná průběžná doba hlášení – týká se časových servisních činností a jde o časový předstih návrhu před předepsaným termínem pro provedení
- Použít bezpečný výkon hlášení – parametrem se zapne použití parametrů bezp. výkonu. 
- Použít alt. bezp. výkon. hl – parametr umožní definovat pro výpočet jiný bezpečný výkon než jak je uveden v nastavení; je-li tento parametr zapnut, je zapotřebí ještě definovat
    - Bezpečný výkon
    - Kód m.j. výkonu
### HROMADNÉ GENEROVÁNÍ POŽADAVKŮ DLE PŘEDPISU SERVISNÍCH ČINNOSTÍ
Hromadné generování požadavků obsahuje pokročilejší plánovací funkce, které vyhodnocují: 

- stav servisních činností dopravních prostředků
- stav rozpracovanosti dokladů (prvky dynamického plánování)
- potřebu inicializace evidence pro nové dopravní prostředky

Výstupem je naplněný deník servisních činností včetně tzv. Hlášení akce, kdy systém informuje o typu akce, která má být s daným řádkem deníku servisních činností provedena.

Řádky deníku se naplní spuštěním akce Získat hlášení akce. Po spuštění akce se zobrazí formulář pro zadání parametrů výpočtu.

Výsledkem výpočtu jsou navržené řádky deníku servisních činností s hlášenou akcí a mnemotechnický popis servisních činností sestavený z dat detailního řádku servisních činností.

    Význam hlášení akce:

   - *Nová* – systém navrhuje vytvořit nový dokument, jehož typ je specifikován v poli Typ dokladu
    - *Přeplánovaná* – systém navrhuje přeplánovat existující dokument, jehož identifikace je uvedena v polích Typ dokladu  a Číslo dokladu
    - *Storno* – systém navrhuje zrušit existující dokument, neboť dle stavu plánovacích parametrů jej vyhodnotil jako nadbytečný
    - *Účtovat činností* – týká se zejména inicializace servisních cyklů u dopravních prostředků nově zavedených do evidence; také je možné využít pro evidenci nakupovaných servisních činností, k jejichž evidenci nelze využít servisních zakázek. Účtováním servisních činností se evidují pouze položky servisních činností, nikoliv položky servisu.

    Hlášené akce lze v určitých případech ručně změnit.

Samotné provedení hlášené akce lze provést funkcí Provést hlášené akce…, pokud jsou řádky deníku servisu korektně nastaveny.
Zejména jde o:

- Dosažení shody v termínu plánování - Termín odsouhlasen = Ano
 - Hlášení akce avizuje akci, která má být s řádkem deníku servisní činnosti provedena
 - Pole Přijmout hlášené akce = Ano
  - V závislosti na hlášené akci je nastaven odpovídající typ dokladu (Servisní zakázka, Nákup)

Výsledkem je provedení hlášené akce – nejčastěji nová Servisní zakázka a smazání řádku deníku servisních činností.
## PROVÁDĚNÍ SERVISU
Základním dokumentem pro evidenci servisních činností je servisní zakázka. Ty mohou být generovány z deníku servisních činností (viz kapitola 5.4 Plánování servisních činností) nebo mohou být založeny ručně.
### PŘÍJEM DO SERVISU
Pokud byla servisní zakázka vygenerována z deníku servisních činností, po vytvoření dokumentů zbývá zkontrolovat a doplnit další potřebné parametry.
#### Kontrola / modifikace servisních činností
Řádky servisních činností, které mají být pro daný předmět servisu provedeny, se zpřístupní ze záložky Řádky volbou Servisní činnosti. Seznam servisních činností je možné upravovat – přidávat resp. mazat servisní činnosti.
#### Přejímka
K přejímce předmětu servisu je určen formulář Sešit předmětu servisu. 
Výbava vozidla se zadá na záložce Výbava.

Obsah nádrže a stav km se zadá na záložce Stav. Stav km je předvyplněn dle telematických údajů. Neexistují-li (externí vozidlo) nebo jsou-li telematické údaje vadné, lze je upravit

### PROVÁDĚNÍ SERVISU
Zahájení servisní činnosti, ale i další průběh servisu, se zaznamenává v poli Kód stavu opravy.

Samotná evidence realizace servisních činností se do řádku sešitu předmětu servisu zadává ručně nebo pomoci akce Vložit servisní činnosti:
Dále se v Sešitu zadává veškerý spotřebovaný materiál a odvedená práce techniků. 

Uživatel může řádky rovnou účtovat nebo provede pověřená osoba před uzavřením a fakturací zakázky.

Po zadání budou označeny řádky k zaúčtování a bude spuštěno vlastní zaúčtování. Pro zaúčtování spotřeby **materiálu a zdrojů** (práce) bude zvolena možnost **Dodat**, případně **Dodat a fakturovat**. 

Pro zaevidování provedení servisních činností bude spuštěna volba Dodat a spotřebovat.

### KONTROLA STAVU SERVISNÍCH CYKLŮ
Po zaúčtování servisních činností lze zkontrolovat stav servisních cyklů vozidla. Z karty vozidla se zobrazí statistika servisních činností, ve které:
- je zaznamenáno datum provedení posledního serv. cyklu a výkonový stav,
- je kalkulován očekávaný výkonový stav pro provedení servisu,
- je kalkulován zbývající výkon do provedení servisu; tento údaj se s každým zobrazením statistiky kalkuluje dle položek telematických údajů,
- se navyšuje hodnota ve sloupci Počet realizovaných serv. cyklů (rozkliknutím lze rozbalit detaily v podobě položek servisní činnosti).

#### Žurnál servisních činností
Při účtování servisních činností (z deníku servisních činností nebo ze servisní zakázky) je zaznamenáno do žurnálu servisních činností.
Každý žurnál sdružuje položky z jednoho účtování. 
Tyto obsahují zejména:
- Stav výkonu při řádném servisu – při jakém výkonu měla být servisní činnost řádně provedena
- Stav výkonu při servisu – při jakém výkonu byla servisní činnost skutečně provedena
- Datum řádného servisu – kdy měla být servisní činnost řádně provedena
- Zúčtovací datum – kdy byla servisní činnost skutečně provedena
## SERVISNÍ SVOLÁVACÍ AKCE
Systém obsahuje podporu pro evidenci servisních svolávacích akcí a práci s nimi. Karta servisní svolávací akce má definován název a začátek a konec platnosti. V řádcích jsou pak evidována všechna vozidla, pro která je svolávací akce určena.
Řádky je možné zadat ručně popř. funkcí pro import.
#### Připojení servisní svolávací akce 

Servisní svolávací akce jsou v Deníku servisních činností kontrolovány a přiřazovány k vozidlům po spuštění funkce Získat hlášení akcí. Dojde-li k přiřazení servisní akce, řádek deníku servisních činností je označen příznakem Servisní akce existuje. Detaily přiřazení lze pak zobrazit prostřednictvím akce Svolávací akce z pásu karet.

Na servisní zakázce je kontrola výskytu servisní svolávací akce provedena po vložení předmětu servisu do řádku servisní zakázky. Uživateli se zobrazí informace o přiřazení spolu s výčtem max. 3 přiřazených akcí.

Upozorňování na servisní svolávací akce je deaktivováno po jejich přiřazení nebo zaúčtování. Zaúčtováním nositele servisní svolávací akce (servisní zakázky) se vytvoří položka servisní svolávací akce. V případě dobropisování se účtuje kompenzační položka servisní svolávací akce. Tím se daná servisní svolávací akce pro vozidlo stane znovu aktivní.
#### Položky svolávací akce

Zaúčtováním Dodávky servisu vznikají kromě jiných i položky servisní svolávací akce.
Hodnota v poli Realizováno indikuje pozitivní (dodávka) nebo negativní (dodávka vratky) odvedení servisní sv. akce. 

Součet těchto hodnot za položky serv. svolávací akce se stejným číslem akce, typem a číslem vozidla, pak dává stav provedení servisní svolávací akce (0 – neprovedeno, 1 – provedeno).

## <a name="see-also"></a>Viz také  
[AC ProMIS](ac-pm-promis.md)