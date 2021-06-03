---
    title: "Obecné popisy"
    author: AutoCont
    ms.date: 04/30/2018
    ms.topic: article
    ms.prod: dynamics-nav-2017
    ms.contentlocale: cs-cz
    ms.lasthandoff: 04/30/2018
---

# Obecné popisy
**Obecné popisy** jednak rozšířují standardní texty, které se používají v systému např. do fakturačních řádků, jednak se zde dají definovat jakékoli obecné texty, které lze pak využít k různým účelům, jako např. text do předmětu e-mailu, text do těla e-mailu, oslovení. 
Obecné popisy se mohou a nemusí vztahovat ke konkrétní tabulce. Pole z tabulky je pak možno využít v syntaxi textu. Text si tak uživatel může vyskládat z:
-	vlastního textu
-	hodnoty pole
-	názvu pole (Titulek pole)
-	ze systémových hodnot (pracovní datum, aktuální datum, aktuální čas)
-	registrovaných funkcí, pokud jsou pro danou tabulku nějaké funkce zaregistrovány.
Vzorec textu pak může vypadat např. takto: Zákazník %1 %2 %3 (%4), kde procento a číslo zastupují definované parametry. Pro vzorec textu je možno definovat překlady v různých jazycích. Pokud je ve vzorci použit typ = Titulek pole, jeho překlad je závislý na implementovaných jazykových sadách objektů.
Pomocí akce Test je možno pro vybraný záznam zkontrolovat podobu nadefinovaného textu. 

**Kódy užití obecných popisů** – jedná se o uživatelsky definovaný číselník, který slouží pro definici použití obecných popisů. 

**Nastavení popisů** – tato struktura slouží k nastavení použití obecných popisů v různých částech lázeňského řešení.

## <a name="see-also"></a>Viz také
[AC Lázeňské řešení](ac-spa-solution.md)