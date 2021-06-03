---
    title: "Obchodní rejstřík"
    author: AutoCont
    ms.date: 04/30/2018
    ms.topic: article
    ms.prod: dynamics-nav-2017
    ms.contentlocale: cs-cz
    ms.lasthandoff: 04/30/2018
---

# Obchodní rejstřík

Funkčnost obchodního rejstříku umožňuje sdružovat kontakty se stejným IČ. Využívá napojení na ARES, kontrolu DIČ a kontrolu nespolehlivosti plátce, které jsou součástí funkčnosti Lokalizace CZ. 
Obchodní rejstřík má samostatnou evidenci, která je vedena na Kartě obchodního rejstříku a také své nastavení. Již na úrovni obchodního rejstříku lze provádět řadu kontrol spojených s IČ a vytvářet kontakty, zákazníky a dodavatele.  

**Nastavení obchodního rejstříku**
-	Výchozí šablona zákazníka/dodavatele
-	Číslování kontaktů, zákazníků, dodavatelů
-	Odkaz na registr ARES
-	Nastavení synchronizace bankovních účtů
-	Nastavení synchronizace zákazníků a dodavatelů při mazání kontaktů

**Klasifikace obchodního rejstříku**
-	Pro zobrazení popisů klasifikací je nutno naplnit číselník kódů klasifikace OR, jinak z aktualizace ARES se naplňují pouze kódy (popis není součástí xml souboru).

**Karta obchodního rejstříku**
-	Aktualizace ARES
	-	probíhá přes Protokol ověření IČ. Lze ji spustit pomocí tlačítka Aktualizace ARES v pásu karet nebo přes tlačítko AssistButton vedle pole IČ
	-	Pokud systém nalezne pro dané IČ záznam v databázi registrace ek. subjektů, v protokolu se vytvoří záznam se stavem Platné a pokud jde o první ověřování, otevře se zároveň formulář pro aktualizaci údajů, jinak lze formulář otevřít přes tlačítko Aktualizovat kartu. Při otvírání formuláře se automaticky porovnávají údaje z Karty obchodního rejstříku oproti zjištěným údajům z databáze registru. V případě, že jsou údaje shodné, formulář pro aktualizaci se neotevře a uživateli se objeví hláška, že údaje jsou shodné a není co aktualizovat. V opačném případě se otevře formulář Aktualizace Ares s údaji, které se neshodují s automatickým zaškrtnutím aktualizace. Aktualizace se standardně automaticky nezaškrtne v případě, že záznam v Pramenu obsahuje údaj, který v registru není. Uživatel může rozhodnout, co se má z registru aktualizovat pomocí zaškrtnutí u příslušného pole. Aktualizace se provede tlačítkem OK.
	-	U neplatných záznamů se automaticky nastavuje důvod neplatnosti v poli Výsledek ověření
	-	Zobrazení ARES na webu je umožněno přes tlačítko v Protokolu ověření IČ 
	-	Při každém spuštění funkce Ověřit IČ se založí nový záznam do Protokolu ověření IČ

-	Kontrola DIČ
	-	Probíhá přes tlačítko Kontrola DIČ v pásu karet nebo přes tlačítko AssistButton vedle pole DIČ, které spustí Protokol ověření DIČ. V protokolu jsou uvedeny jednotlivé stavy ověřování a nové ověření se pak provede pomocí funkce Ověřit DIČ.

-	Kontrola nespolehlivosti plátce DPH
	-	Probíhá přes tlačítko Kontrola nespolehlivosti plátce DPH v pásu karet. Funkce kontroluje jak plátce, tak i jeho registrované bankovní účty. Po ukončení kontroly uživateli oznámí počet zkontrolovaných položek, které si uživatel může otevřít pod tlačítkem Stav nespolehlivosti z pásu karet.
	-	Výsledek a datum kontroly nespolehlivosti funkce zároveň zapíše do příslušných polí v záložce Detaily na kartě obchodního rejstříku
-	Vytvořit kontakt – tato funkce vytvoří nový kontakt s údaji z OR, ale bez adresy
-	Vytvořit kontakt s adresou – tato funkce vytvoří nový kontakt s údaji z OR
-	Vytvořit zákazníka – tato funkce vytvoří nového zákazníka přes šablonu zákazníka
-	Vytvořit dodavatele – tato funkce vytvoří nového dodavatele přes šablonu dodavatele 

## <a name="see-also"></a>Viz také
[AC Lázeňské řešení](ac-spa-solution.md)