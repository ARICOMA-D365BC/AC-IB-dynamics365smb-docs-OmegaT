---
    title: "Přehled dárkových poukázek"
    author: AutoCont
    ms.date: 04/30/2018
    ms.topic: article
    ms.prod: dynamics-nav-2017
    ms.contentlocale: cs-cz
    ms.lasthandoff: 04/30/2018
---

# Přehled dárkových poukázek

Dárkové poukázky jsou v systému evidovány na **Kartě dárkové poukázky**. Jednotlivé karty jsou číslovány automaticky na základě číselné řady definované v typu dárkové poukázky. Podle typu jsou také přístupné příslušné funkce, které lze s poukázkou daného typu provádět.
Důležitá pole:
-	Částka poukázky včetně DPH – jedná se o částku, na kterou se poukázka vztahuje a za kterou budou čerpány produkty
-	Prodejní částka poukázky včetně DPH – jedná se o částku, za kterou bude DP prodaná. Automaticky se dotahuje částka z pole Částka poukázky včetně DPH, ale lze ji v tomto poli změnit. Pokud bude definována nižší částka, rozdíl nominální a prodejní hodnoty se při prodeji poukázky zaúčtuje na nový řádek s kontem slevy definovaným v poli Finanční konto prodejní slevy. Konto slevy se definuje v typu dárkové poukázky a při vytvoření dárkové poukázky se přenáší do Karty dárkové poukázky a odtud do prodejního dokladu, pokud je částka poukázky různá od prodejní částky poukázky.
-	Použitý základ DPH a Základ DPH k použití – zobrazují částku bez DPH. Při uzavírání dárkové poukázky se kontroluje, zda je Základ DPH k použití nulový.
-	Částka služeb včetně DPH – toto pole se plní u poukázek s typem účtování = „Prodej služby“ jako součet cen služeb poukázky. Výsledná hodnota je závislá na hodnotě v poli Datum ocenění a na cenové hladině definované v typu dárkové poukázky.
-	Obchodní DPH účto skupina – doplňuje se automaticky při prodeji poukázky a na tuto hodnotu se pak kontroluje obchodní DPH účto skupina při užití poukázky.
-	Číslo zaměstnance – je třeba vyplnit pro poukázky s typem účtování = „Dar společnosti“
-	Záložka Klient/Plátce

Jednotlivé funkce na Kartě dárkové poukázky se v pásu karet zpřístupňují nebo znepřístupňují na základě typu účtování.

## Vytvoření dárkové poukázky
Dárkové poukázky je možno vytvořit několika způsoby, pomocí funkce:
-	Vytvoř novou poukázku – tato funkce založí novou dárkovou poukázku stejného typu, jako má DP, na které stojí kurzor při zakládání nové DP
-	Vytvoř novou poukázku s výběrem typu – umožňuje před založením nové DP vybrat typ nové DP
-	Automatické založení ze sady poukázek – jednotlivé DP se založí automaticky se založením sady

Vytvořením poukázky se nové poukázce přidělí číslo z číselné řady definované pro daný typ a doplní některé informace z typu poukázky. Další informace uživatel doplní v kartě DP.

## Vytvoření sady dárkové poukázky
Sadu dárkové poukázky lze vytvořit pomocí funkce „Vytvoř novou sadu“. Nové sadě se přidělí číslo z číselné řady definované pro daný typ sady a doplní se informace z typu sady. Zároveň se automaticky založí jednotlivé dárkové poukázky definované pro sadu. 

## VÝDEJ/VRÁCENÍ DP (DAR SPOLEČNOSTI)
Funkce Výdeje a vrácení je přístupná z karty DP pouze pro dárkové poukázky s typem účtování = „Dar společnosti“. Vyžaduje vyplněné Číslo zaměstnance na Kartě DP.
-	Výdej – založí položku DP typu prodej a umožní DP použít (vyplněná Částka k použití včetně DPH).
-	Vrácení – založí položku DP typu Vrácení a DP uzavře.

## PRODEJ
### Prodej dárkových poukázek
Prodej dárkových poukázek s typem účtování = Hodnota, Prodej služby se provádí na prodejním dokladu pomocí funkce „Navrhni prodej dárkových poukázek“. Na prodejní doklad se nabízí jen neuzavřené dárkové poukázky s typem účtování Hodnota a Prodej služby, které ještě nejsou prodané. Prodej se uskuteční za prodejní částku včetně DPH. Pokud je odlišná od nominální hodnoty poukázky, založí se další prodejní řádek na konto slevy definované v typu poukázky s rozdílovou částkou.
Zaúčtováním prodejního dokladu
-	vznikne položka DP typu Prodej na nominální částku poukázky, která se objeví i na kontě poukázky. Pokud při prodeji byla uplatněna sleva, částka slevy jde na konto slevy.  
-	Hodnota v poli Prodej na DP se změní na Ano
-	Naplní se Částka k použití včetně DPH a DP je možno použít na čerpání produktů

### Storno prodeje DP
Storno prodeje DP se provádí na prodejním dobropisu či na prodejním pokladním dobropisu pomocí funkce „Navrhni prodej dárkových poukázek“. Na prodejní dobropis se nabízí jen neuzavřené dárkové poukázky s typem účtování Hodnota a Prodej služby s nenulovou částkou k použití včetně DPH.
Zaúčtováním prodejního dobropisu
-	vznikne položka DP typu Vrácení na nominální částku poukázky, která se objeví i na kontě poukázky. Pokud při prodeji byla uplatněna sleva, částka slevy se vrátí na konto slevy.  
-	Částka k použití včetně DPH se vynuluje
-	DP se uzavře

### Prodej sad dárkových poukázek
Prodej sady dárkových poukázek se provádí na prodejním dokladu pomocí funkce „Navrhni prodej sad dárkových poukázek“. Je to jediné místo, kde se pracuje se sadou jako celkem. Na prodejní doklad se nabízí jen neuzavřené a neprodané sady dárkových poukázek. 
Zaúčtováním prodejního dokladu
-	vzniknou položky DP typu Prodej na nominální částky poukázek 
-	Hodnota v poli Prodej na jednotlivých DP i v sadě DP se změní na Ano
-	Naplní se Částky k použití včetně DPH a jednotlivé DP je možno použít na čerpání produktů

## UŽITÍ
### Použití DP na prodejním dokladu
Na prodejním dokladu lze použít otevřené platné DP s nenulovou částkou k použití včetně DPH. K použití slouží funkce:
-	Připoj dárkovou poukázku
	- 	Funkce připojí vybranou DP do prodejního dokladu max. do výše částky k použití včetně DPH
	- 	Použitá částka z DP je zobrazena v poli Čerpaná částka dárkových poukázek (záložka Obecné na kartě prodejního dokladu). Do detailu použitých částek z jednotlivých DP připojených k dokladu je možno se dostat rozkliknutím této částky, nebo pomocí page Přiřazené dárkové poukázky (záložka Navigace v pásu karet prodejního dokladu).

-	Zruš připojení dárk. poukázek
	- 	Tato funkce zruší přiřazení všech DP k prodejnímu dokladu, tudíž se vynuluje i pole Čerpaná částka dárkových poukázek

-	Test připojených dárk. poukázek
	- 	Tato funkce otestuje připojení dárkových poukázek na prodejním dokladu a výsledek testu oznámí uživateli. 

Zaúčtováním prodejního dokladu s připojenou DP:
-	vznikne položka DP typu Použití na částku, která byla použita na dokladu a o tuto částku se sníží konto DP 
-	Hodnota v poli Užití na DP se změní na Ano
-	Změní se Částka k použití včetně DPH
-	Pokud se použije celá částka, dárková poukázka se uzavře

## PROPADNUTÍ
Jakmile dárková poukázka pozbyde platnosti a vykazuje nenulový zůstatek, je možno účtovat propadnutí, které přeúčtuje zbylou částku z konta DP na konto výnosů propadnutí, které je definované v typu dárkové poukázky. Propadnutí je možné účtovat z karty či přehledu dárkových poukázek pomocí funkcí:
-	Účtuj propadnutí
	- 	funkce přeúčtuje zůstatek konkrétní propadlé DP z konta DP na konto výnosů propadnutí
	- 	vytvoří položku DP typu propadnutí
	- 	vynuluje Částku k použití včetně DPH
	- 	uzavře DP

-	Účtuj propadnutí všech prošlých poukázek – zaúčtuje propadnutí pro všechny prošlé DP
-	Účtuj storno propadnutí
	- 	funkce přeúčtuje zůstatek konkrétní propadlé DP z konta výnosů propadnutí na konto DP
	- 	vytvoří položku DP typu propadnutí s opačným znaménkem
	- 	naplní Částku k použití včetně DPH
	- 	otevře DP 




## <a name="see-also"></a>Viz také
[AC Lázeňské řešení](ac-spa-solution.md)