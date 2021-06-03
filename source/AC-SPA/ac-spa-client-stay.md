---
    title: "Evidence pobytů"
    author: AutoCont
    ms.date: 04/30/2018
    ms.topic: article
    ms.prod: dynamics-nav-2017
    ms.contentlocale: cs-cz
    ms.lasthandoff: 04/30/2018
---

# Evidence pobytů

Pobyty klientů jsou evidovány na **Kartě pobytu klienta**, která představuje klíčovou evidenci v systému. Informace, které jsou důležité pro evidenci pobytu, jsou rozčleněny do několika záložek dle obsahu. Klíčové informace jsou zobrazeny i při zavřené záložce.

**Karta pobytu klienta** prochází několika stavy v závislosti na průběhu klientova pobytu:
-	Požadavek
	- 	Jedná se o výchozí stav. Je automaticky přidělen při zadávání nového pobytu. 
	- Do tohoto stavu je možné pobyt dostat také ze stavu:
		- „Rezervace“ - pomocí funkce „Zruš rezervaci“
		-  „Příjezd“ - pomocí funkce „Zruš příjezd“
		- „Storno“ – pomocí funkce „Vrať storno pobytu“
	- 	 V tomto stavu lze u individuálních pobytů měnit většinu údajů, pokud to dovolí omezení definovaná v nastavení. Pobyt je pouze zaznamenán, nejsou rezervovány žádné ubytovací kapacity.
-	Rezervace
	- 	Stav Rezervace indikuje, že klient má v daném lázeňském domě zarezervovány ubytovací kapacity. Změnou počátečního nebo koncového data v řádku pobytu se automaticky mění i rezervace dané ubytovací kapacity.
	- 	Do tohoto stavu je možné pobyt dostat ze stavu:
		- „Požadavek“ - pomocí funkce „Rezervace“
		- „Příjezd“ - pomocí funkce „Vrať příjezd na rezervaci“
	- 	Rezervace může být:
		- Pevná – rezervuje se přímo konkrétní pokoj uvedený v řádku pobytu typu ubytování
		- Volná – rezervuje se kategorie ubytování uvedená v řádku pobytu typu ubytování. Systém interně pobytu přidělí pokoj v dané kategorii, ten se však může měnit, pokud daný pokoj bude vyžadovat jiný klient. Systém automaticky přesune tuto volnou rezervaci na jiný volný pokoj v dané kategorii.
-	Příjezd
	- 	Tento stav umožňuje všechny operace spojené s fyzickým příjezdem klienta
	- 	Bydlící klient obdrží klíče od pokoje, obsadí se mu ubytovací kapacity, může k lékaři a na rozpis procedur. 
	- 	Do tohoto stavu je možné pobyt dostat ze stavu:
		- „Požadavek“ - pomocí funkce „Příjezd“
		- „Rezervace“ - pomocí funkce „Příjezd“
		- „Příjem“ – pomocí funkce „Zruš příjem“
		- „Převedení“  - pomocí funkce „Zruš převod“
-	Příjem
	- 	Tento stav slouží k provedení administrativních úkonů, které jsou s příjmem spojené, jako např. kontrola osobních údajů klienta, zda odpovídají údajům zadaných v systému a případná jejich aktualizace, vyplnění víza, hlášení cizinecké policii. 
	- 	Do tohoto stavu je možné pobyt dostat ze stavu:
		- „Příjezd“ – pomocí funkce „Příjem“
		- „Převedení“  - pomocí funkce „Zruš převod“
		- „Odjezd“ – pomocí funkce „Zruš odjezd“
-	Přerušení
	- 	Stav Přerušení na Kartě pobytu klienta indikuje, že pobyt klienta je z nějakého důvodu přerušen. Do tohoto stavu se pobyt dostane pomocí wizardu, ve kterém se určí, které služby se přerušují, na jak dlouho a z jakého důvodu.
-	Převedení
	- 	Tento stav indikuje, že pobyt klienta byl během svého trvání převeden na jiný typ pobytu pomocí wizardu „Průvodce převodu pobytu“. 
	- 	Do tohoto stavu je možné pobyt dostat ze stavu:
		- „Příjezd“ – pomocí funkce „Převod na nový typ“
		- „Příjem“ – pomocí funkce „Převod na nový typ“
-	Odjezd
	-	Tento stav umožňuje operace spojené s fyzickým odjezdem klienta. 
	- 	Provádí se kontroly spojené s odjezdem, pokud jsou na plátci nastaveny.
	-	V tomto stavu již klient nemůže čerpat služby. Končí platnost telefonního účtu, nelze načasovat proceduru Nelze vkládat položky na klientský účet pocházející z jiných zdrojů (např. z restaurace, rozpisu procedur).
	-	Do tohoto stavu je možné pobyt dostat ze stavu:
		- „Příjem“ – pomocí funkce „Odjezd“
		- „Ukončení“ – pomocí funkce „Zruš ukončení“
-	Ukončení
	- 	Tento stav slouží k administrativním úkonům, které jsou spojené s ukončením pobytu, jako např. úprava položek klientského účtu, jejichž plátcem není klient.
	- 	Do tohoto stavu je možné pobyt dostat ze stavu:
		- „Odjezd“ – pomocí funkce „Ukončení“
-	Storno
	- 	Do totoho stavu je možno převézt pobyt pouze ze stavu „Požadavek“ (pomocí funkce „Stornuj pobyt“) v případě, že klient nepřijel. Jedině v tomto stavu je možno přidat na klientský účet storno poplatky.
Činnosti a funkce, které lze s pobytem provádět, jsou přístupné v pásu karet v závislosti na stavu pobytu. 



## <a name="see-also"></a>Viz také
[AC Lázeňské řešení](ac-spa-solution.md)