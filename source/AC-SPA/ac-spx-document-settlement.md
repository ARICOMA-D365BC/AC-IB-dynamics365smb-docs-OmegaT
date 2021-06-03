---
    title: "Schvalování dokladů"
    author: AutoCont
    ms.date: 04/30/2018
    ms.topic: article
    ms.prod: dynamics-nav-2017
    ms.contentlocale: cs-cz
    ms.lasthandoff: 04/30/2018
---

# Schvalování dokladů
Schvalování dokladů v lázeňském řešení částečně využívá standardní funkčnost evidence pošty a rozšiřuje ji o věcnou a finanční likvidaci. Rovněž v procesu schvalování využívá vlastní workflow, které je více uživatelsky nastavitelné, co se týče kontroly a nastavování hodnot polí.
Schvalování dokladů probíhá ve třech úrovních, a to na nákupních objednávkách, nákupních fakturách a interních dokladech.
### Schvalování nákupních objednávek
Schvalování nákupních objednávek probíhá přímo na nákupních objednávkách s využitím šablon workflow.  

**Šablony workflow**
-	číslo tabulky = 38 – Nákupní hlavička
-	Stavy workflow	
	-	Nastavovaná pole (Datum schválení, Tisk zakázán, Odeslání zakázáno, Účtování zakázáno, …) – zohlednění v sestavách
	-	Kontrolovaná pole (Stav, Číslo věřitele…)
	-	Akce (Write, RELEA/REOP, …)
-	Nastavení šablony na číselnou řadu NO

**Schvalování nákupní objednávky** probíhá změnou stavu v info panelu nákupní objednávky. 

### Schvalování nákupních faktur
Schvalování nákupních faktur probíhá přes evidenci došlé pošty (Oblasti – ProProduktivitu-Evidence pošty)  
**Šablony evidence pošty**  
-	Typ pošty = Došlá
-	Číselná řada
-	Číselná řada dokladu
-	Kód šablony workflow
-	Typ kontaktu = Dodavatel
-	Typ dokladu = Faktura
-	Kód typu události žádosti k věcné likvidaci faktur
-	Kód typu události žádosti k finanční likvidaci faktur
-	Skupiny pro likvidaci dokladů – povolené skupiny pro věcnou likvidaci.  
-	Nastavení finanční likvidace – nastavení limitů v měně pro typy uživatelů likvidace dle hodnot dimenzí  

**Nastavení kódů původu**  
-	Záložka PRAMEN - Věcná likvidace nákupních faktur – zde definovaný kód původu se pak kontroluje s Kódem původu v právech na data (dimenze), pokud jsou tato práva aktivována a nastavena.

**Práva na data**  
-	INVENTORY-LOCATION – toto právo se kontroluje při věcné likvidaci zboží, které přišlo rovnou s fakturou a nepředchází mu nákupní příjemka. U zboží, které se objednává dopředu se věcná likvidace provádí u nákupních objednávek.

**Šablony workflow** (Oblasti – ProProduktivitu- WorkFlow – Nastavení)  
-	číslo tabulky = 52067961 – Evidence pošty
-	Stavy workflow	
	-	Nastavovaná pole (Stav,  …) 
	-	Kontrolovaná pole (Stav, Číslo dodavatele, Čas věcné likvidace, Čas finanční likvidace…)
	-	Akce (Write, Logování, …)


Schvalování nákupní faktury probíhá přes **Kartu evidence pošty**.

-	Založení nové evidence pošty výběrem šablony – řada polí se předvyplní ze šablony
-	Doplnění informací z došlého dokladu (Datum DPH původního dokladu, Číslo externího dokladu, Částka bez DPH, Číslo dodavatele, …) – Povinnost vyplnění polí lze kontrolovat pomocí stavů workflow
-	Workflow probíhá dle nastavení šablony workflow pomocí změn stavů v info panelu evidence pošty. V záložce Stav je možno vyplnit odpovědnou osobu za další stav, do kterého se evidence pošle. Souslednost stavů a jejich odpovědných osob je pak zobrazena v záložce Protokol stavu.
-	 **Věcná likvidace**
		- 	probíhá v záložce Věcná likvidace Karty evidence pošty
		-	Je třeba rozdělit řádky dle dimenzí a vybrat Kódy skupin pro likvidaci. Nabízí se pouze skupiny definované pro danou šablonu evidence pošty. Pokud je definována pouze 1 skupina, rovnou se propíše do věcné likvidace při zakládání evidence pošty ze šablony.
		-	Pomocí nastavení událostí a akcí workflow se rozešlou požadavky na schválení, nebo je může uživatel odeslat pomocí akce Odeslat požadavek věcné likvidace
		-	**Schválení**  
			- Schválení uživatel provede tlačítkem Schválit
			- Automaticky se zaškrtne pole Schváleno, vyplní se ID Schválil, Datum a čas schválení v řádku věcné likvidace a Čas věcné likvidace a Schválená částka likvidace v info panelu.
			- Pokud je nastavena finanční likvidace, při schválení posledního řádku věcné likvidace se založí řádek či řádky finanční likvidace dle limitů a v infopanelu se naplní pole Počet neschválených pol.fin.likvidace
		-	**Zrušení schválení**  
			- Uživatel provede tlačítkem Zrušit schválení
			- Automaticky se vyprázdní schvalovací pole
			- Zruší se finanční likvidace
-	**Finanční likvidace**  
	-	probíhá v záložce Finanční likvidace Karty evidence pošty
	-	vzniká automaticky po schválení posledního řádku věcné likvidace
	-	počítá se vždy z cen bez DPH a kontroluje se, zda je uživatel členem schvalovací skupiny
	-	Pomocí nastavení událostí a zaškrtnutého pole „Automatický požadavek finanční likvidace“ v šabloně evidence pošty, se rozešlou požadavky na finanční likvidaci, nebo je může uživatel odeslat pomocí akce Odeslat požadavek finanční likvidace 
	-	**Schválení**  
		- Uživatel provede tlačítkem Schválit
		- Automaticky se vyplní ID uživatele likvidace, Čas likvidace v řádku finanční likvidace a Čas finanční likvidace v infopanelu. V infopanelu se zároveň změní hodnota v poli Počet neschválených pol. fin. likvidace
-	**Vytvoření dokladu**  
	-	Provede uživatel pomocí akce „Vytvořit doklad“ z karty evidence pošty
	-	Funkce se řídí hodnotou v poli „Povol vytvoření dokladu“, kterou je možno nastavovat a kontrolovat pomocí nastavovaných a kontrolovaných polí jednotlivých stavů workflow
	-	Do dokladu se přenáší jen řádky, které mají vyplněno Typ + Číslo
	-	Vytvořený doklad je spojený s evidencí pošty přes Související doklady pošty (Navigace). 

-	**Zaúčtování dokladu**  
	-	Probíhá standardně nad nákupní fakturou
	-	Zaúčtováním nákupní faktury se změní i link v Souvisejících dokladech pošty na zaúčtovaný doklad.

### Schvalování interních dokladů
Schvalování interních dokladů probíhá přes evidenci došlé pošty (Oblasti – ProProduktivitu-Evidence pošty)  

**Šablony evidence pošty**  
-	Typ pošty = Došlá
-	Číselná řada
-	Číselná řada dokladu
-	Kód šablony workflow
-	Typ dokladu = Interní doklad
-	Název šablony deníku – slouží pro automatické vytvoření interního dokladu do finančního deníku pomocí akce „Vytvořit doklad“ v kartě evidence pošty
-	Název listu deníku
-	Kód typu události žádosti k věcné likvidaci faktur
-	Kód typu události žádosti k finanční likvidaci faktur
-	Skupiny pro likvidaci dokladů – povolené skupiny pro věcnou likvidaci. 
-	Nastavení finanční likvidace – nastavení limitů v měně pro typy uživatelů likvidace dle hodnot dimenzí 

**Nastavení kódů původu**  
-	Záložka PRAMEN - Věcná likvidace interních dokladů – zde definovaný kód původu se pak kontroluje s Kódem původu v právech na data (dimenze), pokud jsou tato práva aktivována a nastavena.

**Práva na data**  
-	INVENTORY-LOCATION – toto právo se kontroluje při věcné likvidaci zboží, které přišlo rovnou s fakturou a nepředchází mu nákupní příjemka. U zboží, které se objednává dopředu se věcná likvidace provádí u nákupních objednávek.

**Šablony workflow** (Oblasti – ProProduktivitu- WorkFlow – Nastavení)  
-	číslo tabulky = 52067961 – Evidence pošty
-	Stavy workflow	
	-	Nastavovaná pole (Stav,  …) 
	-	Kontrolovaná pole (Stav, Číslo dodavatele, Čas věcné likvidace, Čas finanční likvidace…)
	-	Akce (Write, Logování, …) 

Schvalování interních dokladů probíhá přes **Kartu evidence pošty**.  
-	Založení nové evidence pošty výběrem šablony pro typ dokladu = Interní doklady – řada polí se předvyplní ze šablony
-	Doplnění informací z došlého dokladu (Datum DPH původního dokladu, Číslo externího dokladu, Částka bez DPH, …) – Povinnost vyplnění polí lze kontrolovat pomocí stavů workflow a kontrolovaných polí.
-	Workflow probíhá dle nastavení šablony workflow pomocí změn stavů v info panelu evidence pošty. V záložce Stav je možno vyplnit odpovědnou osobu za další stav, do kterého se evidence pošle. Souslednost stavů a jejich odpovědných osob je pak zobrazena v záložce Protokol stavu.
-	**Věcná likvidace**  
	-	probíhá v záložce Věcná likvidace Karty evidence pošty
	-	Je třeba rozdělit řádky dle dimenzí a vybrat Kódy skupin pro likvidaci. Nabízí se pouze skupiny definované pro danou šablonu evidence pošty. Pokud je definována pouze 1 skupina, rovnou se propíše do věcné likvidace při zakládání evidence pošty ze šablony.
	-	Pomocí nastavení událostí se rozešlou požadavky na schválení, nebo je může uživatel odeslat pomocí akce Odeslat požadavek věcné likvidace
	-	**Schválení**  
		- Schválení uživatel provede tlačítkem Schválit
		- Automaticky se zaškrtne pole Schváleno, vyplní se ID Schválil, Datum a čas schválení v řádku věcné likvidace a Čas věcné likvidace a Schválená částka likvidace v info panelu.
		- Pokud je nastavena finanční likvidace, při schválení posledního řádku věcné likvidace se založí řádek či řádky finanční likvidace dle limitů a v infopanelu se naplní pole Počet neschválených pol.fin.likvidace
	-	**Zrušení schválení**  
		- Uživatel provede tlačítkem Zrušit schválení
		- Automaticky se vyprázdní schvalovací pole
		- Zruší se finanční likvidace
-	**Finanční likvidace**  
	-	probíhá v záložce Finanční likvidace Karty evidence pošty
	-	vzniká automaticky po schválení posledního řádku věcné likvidace
	-	počítá se vždy z cen bez DPH a kontroluje se, zda je uživatel členem schvalovací skupiny
	-	Pomocí nastavení událostí se rozešlou požadavky na schválení, nebo je může uživatel odeslat pomocí akce Odeslat požadavek finanční likvidace
	-	**Schválení**  
		- Uživatel provede tlačítkem Schválit
		- Automaticky se vyplní ID uživatele likvidace, Čas likvidace v řádku finanční likvidace a Čas finanční likvidace v infopanelu. V infopanelu se zároveň změní hodnota v poli Počet neschválených pol. fin. likvidace
-	**Vytvoření dokladu**  
	-	Provede uživatel pomocí akce „Vytvořit doklad“ z karty evidence pošty
	-	Tím se vytvoří řádky v definované šabloně a listu finančního deníku
	-	Do dokladu se přenáší jen řádky, které mají vyplněno Typ + Číslo
	-	Vytvořený doklad je spojený s evidencí pošty přes Související doklady pošty (Navigace). 

-	**Zaúčtování dokladu**  
	-	Probíhá standardně nad finančním deníkem
Zaúčtováním finančního deníku se změní i link v Souvisejících dokladech pošty na věcné položky 

## <a name="see-also"></a>Viz také
[AC Lázeňské řešení](ac-spa-solution.md)