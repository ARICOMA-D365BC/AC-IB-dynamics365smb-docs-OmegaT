---
    title: "Ceny lázeňských služeb"
    author: AutoCont
    ms.date: 04/30/2018
    ms.topic: article
    ms.prod: dynamics-nav-2017
    ms.contentlocale: cs-cz
    ms.lasthandoff: 04/30/2018
---

# Ceny lázeňských služeb

Standardní ceník lázeňských služeb je reprezentován tabulkou Cena lázeňské služby, která se člení dle typu služby. Ve standardním ceníku je možné zobrazit kromě aktuálně platných cen i ceny historické či plánované pomocí tlačítek Historie / Plán.
-	Typ ceny
	- 	Určuje, zda se jedná o Prodejní, Nákladovou nebo Základní cenu. Pomocí této volby v hlavičce číselníku je možno v ceníku zobrazit konkrétní typ ceny, případně všechny typy najednou
	- 	Všechny tyto typy cen se dostávají do klientského účtu. Nákladovou cenu je možno definovat pouze v lokální měně a bez DPH
-  	Priorita
	- 	Umožňuje určit prioritu uplatnění různých cen
-	Ode dne, Do dne v týdnu
	- 	Umožňuje zadat interval dnů v týdnu, pro které platí daná cena (tj. interval 1-7, přičemž 1=Pondělí, 2=Úterý, …, 7=Neděle). Od dne v týdnu se vždy počítá od pondělí, Do dne v týdnu platí vždy do neděle.
	- 	Pokud bude cena jiná pro každý den, je nutno zadat 7 řádků s příslušnými čísly dne.
	- 	Pokud se bude cena lišit jen pro víkend, je možno zadat pouze 2 ceny. Víkendovou s hodnotami Od dne v týdnu = 6, Do dne v týdnu = 7. A jinou cenu pro pracovní dny s hodnotami Od dne v týdnu = 1, Do dne v týdnu = 5. Místo hodnoty 1 v poli Ode dne v týdnu lze zadat i prázdnou hodnotu, protože interval vždy začíná od pondělí.
	- 	Cenu, která přesahuje týden, je třeba zadat dvěma řádky. Např. cenu, která platí od pátku do pondělí, je třeba zadat dvěma řádky. Jeden řádek s hodnotami Od dne v týdnu = 5, Do dne v týdnu = 7. A druhý řádek se stejnou cenou a hodnotami Od dne v týdnu = 1, Do dne v týdnu = 1.
	- 	Pokud je cena platná pro každý den, intervaly se vyplňovat nemusí

Ceník služeb umožňuje nastavit různé ceny pro jednu službu v závislosti na cenové hladině, kódu měny, lázeňském domě, dependenci, jednotce, datu použití, priority, dne v týdnu. Časová podmíněnost ceníku umožňuje sledovat historii cen i připravovat ceník na delší období předem. Ceny se uplatňují vždy ke dni služby, takže se cena za stejnou službu může v průběhu pobytu měnit (např. přelom sezóny). 



## <a name="see-also"></a>Viz také
[AC Lázeňské řešení](ac-spa-solution.md)