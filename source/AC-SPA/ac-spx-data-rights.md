---
    title: "Práva na data"
    author: AutoCont
    ms.date: 04/30/2018
    ms.topic: article
    ms.prod: dynamics-nav-2017
    ms.contentlocale: cs-cz
    ms.lasthandoff: 04/30/2018
---

# Práva na data
Práva na data slouží k vymezení přístupu ke konkrétním hodnotám dat (např. ke konkrétním lokacím, pokladnám, střediskům apod.). Mohou být přidělována uživatelům či skupinám uživatelů s povolením přiřazení práv na data.
Mohou být definována dvěma způsoby. Definovaná hodnota se do vyhodnocení práv buď zahrne, nebo se naopak vyloučí. To usnadní uživateli definici, může tak zvolit způsob podle menšího výčtu hodnot. Způsob vyhodnocení určuje pole “Typ přidělení”, které může nabývat hodnot:
-	Zahrnout
-	Vyloučit

Pole „Způsob vyhodnocení“ určuje, co se vyhodnocuje. Může nabývat hodnot:
-	Bez hodnoty – použití pro případy, kde se nevyžadují konkrétní hodnoty, ale jen existence daného práva, např. admin práva a spuštění nějaké funkčnosti či sestavy. Při přidělení práva uživateli či skupině uživatelů se automaticky zaškrtne pole „Platí pro všechny hodnoty“.
-	Hodnota pole – vyhodnocuje se hodnota definovaného pole tabulky.
-	Hodnota dimenze – vyhodnocuje se definovaný „Kód dimenze“ pro definovaný Kód původu. Definice se provede prostřednictvím akce „Založ práva na dimenze“ v pásu karet.
-	Číslo referenční tabulky -  tato hodnota se používá pro podřízené tabulky (např. pro Průvodní texty). Definice se provede prostřednictvím akce „Založ práva na referenční data“ v pásu karet.
-	Skupina hodnot – tento způsob vyhodnocení se používá pro kombinace hodnot.

Identifikaci jednotlivých práv na data si může určit zákazník. Jaký „Kód“ se použije pro jakou funkčnost, se nastavuje v tabulce **Nastavení práv na data**. Tato tabulka slouží k přiřazení konkrétních kódů práv na data k jednotlivým účelům použití, podobně jako se nastavují Kódy původu.

## <a name="see-also"></a>Viz také
[AC Lázeňské řešení](ac-spa-solution.md)