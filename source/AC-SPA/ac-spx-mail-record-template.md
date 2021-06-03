---
    title: "Šablony evidence pošty"
    author: AutoCont
    ms.date: 04/30/2018
    ms.topic: article
    ms.prod: dynamics-nav-2017
    ms.contentlocale: cs-cz
    ms.lasthandoff: 04/30/2018
---

# Šablony evidence pošty
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

## <a name="see-also"></a>Viz také
[AC Lázeňské řešení](ac-spa-solution.md)