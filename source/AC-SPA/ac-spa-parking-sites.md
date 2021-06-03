---
    title: "Parkoviště"
    author: AutoCont
    ms.date: 04/30/2018
    ms.topic: article
    ms.prod: dynamics-nav-2017
    ms.contentlocale: cs-cz
    ms.lasthandoff: 04/30/2018
---

# Parkoviště

Evidence parkování umožňuje evidovat v systému parkovací kapacity a do nich umisťovat osoby, které na pobyt přijely autem a tisknout jim parkovací lístek. Evidence probíhá nad Ručními položkami klientského účtu.

## NASTAVENÍ
**Lázeňská služba**  
-	Služba parkování
	- 	Toto pole slouží pro aktivaci nástrojů pro kontrolu kapacit parkovacích míst
	- 	Pro doplňkové služby, které se budou týkat parkování a budou vstupovat do eviden-ce parkovacích míst je třeba toto pole zaškrtnout
	- 	Pokud pole není standardně zobrazeno, je nutno jej zobrazit

**Parkoviště**  
Jedná se o číselník, kde je třeba definovat jednotlivá parkoviště a určit způsob kontroly jejich kapaci-ty. K tomu slouží pole Typ kontroly, které může nabývat hodnot:
-	Žádná
	- 	u tohoto typu žádná kontrola neprobíhá
-	Celková kapacita
	- 	u tohoto typu kontroly se kontroluje pouze celková kapacita, tzn., že se zde neevidují jednotlivá stání, pouze se hlídá nepřekročení celkové kapacity parkoviště. Při evidenci se nemusí vyplňovat číslo stání. 
-	Jednotlivá místa
	- 	u tohoto typu kontroly se kontroluje jak celková kapacita, tak i kapacita konkrétního místa (stání). Při evidenci se musí vyplňovat číslo stání. 
Pokud je zaškrtnuto pole Kontroluj SPZ vozidla, při účtování doplňkové služby typu Služba parkování se kontroluje vyplnění SPZ vozidla v evidenci.

**Blokace parkoviště**  
Přes tabulku Parkoviště je možno zablokovat příslušné parkovací místo či celé parkoviště na zvolené období pro případ oprav, parkování jiných vozidel než klientů apod.

## POUŽITÍ
Evidence parkovacích míst probíhá ve formuláři Ruční položky služeb, který je přístupný z Karty po-bytu klienta pomocí tlačítka „Doplňkové služby – ruční položky“ v pásu karet. Parkování se týkají sloupce: 
-	Služba parkování
-	Kód parkoviště
-	Číslo stání
-	Počet vozidel
-	SPZ vozidla 
Výběrem služby parkování se automaticky nastaví hodnota 1 do pole Počet vozidel, SPZ vozidla se doplní z osoby pobytu. Obě hodnoty je možné změnit. 
Zadáním Počátečního data a Koncového data se automaticky doplní hodnota do pole Množství. Množství služby se automaticky aktualizuje při změně období služy a počtu vozidel.
Pokud je na daném parkovišti nastavena kontrola kapacity, při jejím překročení systém ohlásí chybovou hlášku: „Pro vybrané parkoviště/stání není v požadovaném termínu volná kapacita.“ Jedná se pouze o varovné hlášení, tzn., že jej uživatel může vědomě překročit. Jakmile pak odskočí ze zadáva-ného záznamu, záznamy, které překračují kapacitu, zčervenají.
Pokud je počáteční a koncové datum služby v různém měsíci, je třeba spustit funkci Rozděl položku podle měsíců. To je důležité proto, že na klientský účet nelze zaúčtovat položku z různých měsíců. Funkce rozdělí záznam do tolika položek, do kolika měsíců zasahuje. 
Aby došlo k rozdělení položek, je třeba, aby korespondovalo Počáteční a Koncové datum s množstvím.

Do evidence je možno zadat i minusovou položku ve smyslu storna. Při kontrole parkovacích kapacit se pak tato položka odečítá. Storna je tedy třeba vytvářet v této evidenci, ne až v položkách klient-ského účtu, aby se tak uvolnila obsazená kapacita parkoviště.  



## <a name="see-also"></a>Viz také
[AC Lázeňské řešení](ac-spa-solution.md)