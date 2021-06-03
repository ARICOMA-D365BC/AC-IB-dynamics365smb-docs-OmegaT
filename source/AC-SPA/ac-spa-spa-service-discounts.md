---
    title: "Slevy lázeňských služeb"
    author: AutoCont
    ms.date: 04/30/2018
    ms.topic: article
    ms.prod: dynamics-nav-2017
    ms.contentlocale: cs-cz
    ms.lasthandoff: 04/30/2018
---

# Slevy lázeňských služeb

Pro podporu marketingu lázeňské řešení nabízí systém slev. V rámci slevového systému lze uplatnit 3 typy slev. Všechny typy slev se mohou sejít na jednom pobytu, pokud odpovídají nastavení slev. Pobytové a řádkové slevy se na pobytu zadávají ručně, u volné osoby se ručně označuje pobyt, který by měl dostat vyhodnocenou slevu volné osoby.
Všechny slevy se propojí v tabulce **Položky slevy klientského účtu**, která je zdrojem pro výpočet výsledné slevy na klientský účet. 

## POBYTOVÉ SLEVY
Pobytové slevy se přiřazují na Kartě pobytu klienta a platí pro všechy služby, které vyhovují nastavení pobytové slevy.
**Nastavení slev** 

Pobytové slevy je možno nastavit buď %, nebo pevnou částkou a zároveň je možno řídit povolení změny výše a rozsahu uplatnění slev.
Pole Priorita umožňuje definovat nastavení s prázdnými hodnotami a pomocí priority určit prioritu různých kombinací. V případě, že pro klienta bude vyhovovat více pobytových slev, zobrazí se uživateli slevy pro výběr v pořadí dle priority (nejnižší číslo = nejvyšší priorita). 
**Slevy pobytu klienta** 
Na Kartě pobytu / skupiny se pobytové slevy zadávají v záložce Cenotvorba přes tlačítko AssistButton vedle pole „Pobytové slevy“. Do výběru se nabízí pouze pobytové slevy, které je možno pro daný pobyt či skupinu použít. Uživatel může vybrat i více pobytových slev, každé vybrané slevě se automaticky přiřadí pořadí a dle něho se pak jednotlivé pobytové slevy na pobytu uplatňují. Pořadí pobytových slev může uživatel měnit. Nadále však platí, že první se uplatňují pobytové slevy (dle jejich pořadí, pokud jich bude více), poté řádkové slevy (dle jejich pořadí, pokud jich bude více) a nakonec provize.
 
## ŘÁDKOVÉ SLEVY
Řádkové slevy se přiřazují k příslušnému řádku pobytu na Kartě pobytu klienta a platí pro služby, které souvisí s daným řádkem pobytu, ke kterému je sleva definovaná.
**Nastavení slev** 
Řádkové slevy je možno nastavit buď %, nebo pevnou částkou a zároveň je možno řídit povolení změny výše slevy.
Pole Priorita umožňuje definovat nastavení s prázdnými hodnotami a pomocí priority určit prioritu různých kombinací. V případě, že pro klienta bude vyhovovat více řádkových slev, zobrazí se uživateli slevy pro výběr v pořadí dle priority (nejnižší číslo = nejvyšší priorita). 

**Slevy pobytu klienta** 
Na Kartě pobytu se řádkové slevy zadávají v řádku pobytu přes tlačítko AssistButton vedle pole „Slevy služby“. Do výběru se nabízí pouze řádkové slevy, které je možno pro daný pobyt použít. Uživatel může vybrat i více řádkových slev, každé vybrané slevě se automaticky přiřadí pořadí a dle něho se pak jednotlivé řádkové slevy na pobytu uplatňují. Pořadí řádkových slev může uživatel měnit. Nadále však platí, že první se uplatňují pobytové slevy (dle jejich pořadí, pokud jich bude více), poté řádkové slevy (dle jejich pořadí, pokud jich bude více) a nakonec provize. 

## SLEVA VOLNÉ OSOBY
Sleva volné osoby umožňuje postihnout obchodní případy typu „každá 21. osoba zdarma“. Zadávají se na kartě pobytu skupiny klientů. Systém umožňuje měnit základ pro výpočet volných osob. Při aplikaci této slevy na skupinu je nutné označit osoby, které se při vyúčtování budou chápat jako volné. Jejich položky se na konci prodejního dokladu odečtou jako sleva. 



## <a name="see-also"></a>Viz také
[AC Lázeňské řešení](ac-spa-solution.md)