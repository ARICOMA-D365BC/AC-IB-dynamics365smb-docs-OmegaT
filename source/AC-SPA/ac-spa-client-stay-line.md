---
    title: "Řádky pobytu klienta"
    author: AutoCont
    ms.date: 04/30/2018
    ms.topic: article
    ms.prod: dynamics-nav-2017
    ms.contentlocale: cs-cz
    ms.lasthandoff: 04/30/2018
---

# Řádky pobytu klienta

V různých stavech pobytu klienta lze přidávat nové řádky pobytu, s kterými lze pak samostatně manipulovat pomocí funkcí v pásu karet u řádků:
-	Navrhni standardní řádky
-	Proveď rezervaci vybraných řádků
-	Zruš rezervaci vybraných řádků
-	Zruš příjezd vybraných řádků

Aby mohl systém reflektovat na různorodé požadavky klientů na ubytování, využívá k tomu řadu polí z řádku ubytování:
-	Počáteční datum – představuje počáteční datum rezervace či obsazení ubytovací kapacity
-	Koncové datum - představuje koncové datum rezervace či obsazení ubytovací kapacity
-	Počáteční datum účt. ubytování – představuje počáteční datum ubytování, které je klientovi účtováno
-	Koncové datum účt. ubytování – představuje koncové datum ubytování, které je klientovi účtováno
-	Předčasný příjezd – toto pole má význam pro řádky typu ubytování. Může nabývat hodnot:
	- 	Ne – výchozí hodnota. 
	- 	Za příplatek – pro daný požadavek ubytování je požadován předčasný příjezd, který se bude plátci účtovat v hodnotě příplatku
	- 	Bez příplatku – pro daný požadavek ubytování je požadován předčasný příjezd, který nebude účtován
-	Obsaď kapacitu pro předčasný příjezd – zaškrtnutí provede obsazení ubytovací kapacity pro noc před příjezdem a zároveň nastaví hodnoty do polí: Počáteční datum účtování ubytování a Ubytovací kapacity rezervovány od data
-	Ubytovací kapacity rezervovány od data – hodnota v tomto poli určuje obsazení ubytovacích kapacit
-	Očekávaný čas příjezdu – zde může uživatel zadat očekávaný čas příjezdu klienta. Pole je nepovinné, jeho hodnota se zobrazuje v Obsazení ubytovacích kapacit.
-	Pozdní odjezd – toto pole má význam pro řádky typu ubytování. Může nabývat hodnot:
	- 	Ne – výchozí hodnota. 
	- 	Za příplatek – pro daný požadavek ubytování je požadován pozdní odjezd, který se bude plátci účtovat v hodnotě příplatku
	- 	Bez příplatku – pro daný požadavek ubytování je požadován pozdní odjezd, který nebude účtován
-	Obsaď kapacitu pro pozdní odjezd – zaškrtnutí provede obsazení ubytovací kapacity pro další noc po koncovém datu a zároveň nastaví hodnoty do polí: Koncové datum účtování ubytování a Ubytovací kapacity rezervovány do data
-	Ubytovací kapacity rezervovány do data – hodnota v tomto poli určuje obsazení ubytovacích kapacit
-	Očekávaný čas odjezdu – zde může uživatel zadat očekávaný čas odjezdu klienta. Pole je nepovinné, jeho hodnota se zobrazuje v Obsazení ubytovacích kapacit.
-	Typ vztahu dat ubytování – nově toto pole určuje vztah mezi účtovanými daty (Počáteční, Koncové datum účtování ubytování) a rezervovanými kapacitami (Ubytovací kapacity rezervovány od, do data). Může nabývat hodnot:
	- 	Shodné – účtovaná data jsou shodná s rezervovanými kapacitami
	- 	Posun počátečního data – umožňuje posun „Počátečního data účt. ubytování“ zpět oproti „Ubytovací kapacitě rezervované od“ o hodnotu v poli „Úprava počtu účtovaných dní ubytování“
	- 	Posun koncového data – umožňuje posun „Koncového data účt. ubytování“ dopředu oproti „Ubytovací kapacitě rezervované do“ o hodnotu v poli „Úprava počtu účtovaných dní ubytování“
	- 	Posun všech dat - umožňuje posun „Počátečního data účt. ubytování“ zpět oproti „Ubytovací kapacitě rezervované od“ a zároveň posun „Koncového data účt. ubytování“ dopředu oproti „Ubytovací kapacitě rezervované do“ o hodnotu v poli „Úprava počtu účtovaných dní ubytování“
	- 	Ruční vstup – umožňuje ručně zadat „Počáteční či Koncové datum účt. ubytování“. Zadané datumy však musí být vně původního intervalu.
-	Úprava počtu účtovaných dní ubytování – vždy se zadává kladná hodnota. Posun zpět či dopředu určuje hodnota v poli „Typ vztahu dat ubytování“. 



## <a name="see-also"></a>Viz také
[AC Lázeňské řešení](ac-spa-solution.md)