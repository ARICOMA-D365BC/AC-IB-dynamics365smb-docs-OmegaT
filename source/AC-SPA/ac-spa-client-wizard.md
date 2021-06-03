---
    title: "Průvodce pro výběr nebo založení klienta"
    author: AutoCont
    ms.date: 04/30/2018
    ms.topic: article
    ms.prod: dynamics-nav-2017
    ms.contentlocale: cs-cz
    ms.lasthandoff: 04/30/2018
---

# Průvodce pro výběr nebo založení klienta

## ZALOŽENÍ NOVÉHO KLIENTA
Pro založení nového klienta se používá funkce **„Najdi nebo založ klienta“**, která nahrazuje tlačítko Nový. Funkce spustí „Průvodce pro výběr nebo založení klienta“. V horní části formuláře uživatel zadá informace o klientovi, které zná. Podle zadaných informací se filtrují existující klienti v databázi, kteří jsou zobrazeni v dolní části formuláře. Pokud zadaným informacím neodpovídá žádný záznam (v dolní části průvodce založením klienta se nezobrazí data), znamená to, že zadávaný klient v systému není a uživatel jej může založit pomocí tlačítka **„Založ nového klienta“**.
Nový klient je uložen do tabulky Klient s automaticky přiděleným jednoznačným číslem z číselné řady, která je nastavena pro klienty.

Tento způsob zakládání klientů umožňuje již při pořizování nových údajů o klientovi hlídat duplicitu. Systémová kontrola duplicity pak probíhá, pokud je zaškrtnuta její kontrola v **Základním nastavení** – pole **„Kontrolovat možné duplicity klienta“**. V případě zaškrtnutí kontroly systém hlídá duplicitu na základě příjmení, jména a data narození. Tato kontrola má formu varování, tzn., že při nalezení shody upozorní uživatele na existenci možné duplicity s uvedením čísel klientů, kterých se tato shoda týká.
Stejná kontrola probíhá i při změně jména, příjmení či data narození u již existujícího klienta.

## VYHLEDÁNÍ EXISTUJÍCÍHO KLIENTA
Pro vyhledání klienta se používá funkce „Najdi nebo založ klienta“. Funkce spustí „Průvodce pro výběr nebo založení klienta“. V horní části formuláře uživatel zadá informace o klientovi, které zná. Podle zadaných informací se filtrují existující klienti v databázi, kteří jsou zobrazeni v dolní části for-muláře. Čím více informací o klientovi uživatel zadá, tím více se zúžuje seznam klientů, kteří vyhovují zadávaným parametrům. Pokud se v dolní části formuláře objeví více než 1 klient, uživatel vybere toho odpovídajícího a pomocí tlačítka **„Vyber klienta“** se dostane na jeho kartu. 



## <a name="see-also"></a>Viz také
[AC Lázeňské řešení](ac-spa-solution.md)