---
    title: "Řádky standardního prodeje"
    author: AutoCont
    ms.date: 04/30/2018
    ms.topic: article
    ms.prod: dynamics-nav-2017
    ms.contentlocale: cs-cz
    ms.lasthandoff: 04/30/2018
---

# Řádky standardního prodeje

Funkčnost vychází ze standardní funkčnosti Kódy standardního prodeje. V rámci lázeňského řešení byla rozšířena o možnost přímého vkládání předdefinovaných řádků do prodejních dokladů. 
Řádky standardního prodeje jsou rozšířeny o možnost práce s lázeňskými službami. 
Pro využití prodeje lázeňských služeb je třeba v řádcích standardního prodeje vyplnit pole:
-	Typ = Účet
-	Typ lázeňské služby = výběr z následujících hodnot:
	-	Doplňková služba
	-	Léčebný pobyt
	-	Ubytování
	-	Stravování
	-	Služba v restauraci
	-	Procedura
	-	Laboratoř
	-	Ošetřovatelská péče
	-	Poplatek
	-	Telefon
	-	Wellnes služba
-	Prodejní kód – toto pole může být vyplněno dvěma způsoby:
	-	Konkrétní hodnotou v závislosti na typu služby – tato hodnota se pak dostane do prodejního dokladu. Výběrem konkrétní služby se zároveň doplní i Číslo, Popis a účto skupiny zboží.
	-	Prázdnou hodnotou – konkrétní služba se bude vybírat až na pokladním dokladu v závislosti na typu lázeňské služby 

## <a name="see-also"></a>Viz také
[AC Lázeňské řešení](ac-spa-solution.md)