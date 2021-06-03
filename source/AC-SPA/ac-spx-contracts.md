---
    title: "Evidence smluv"
    author: AutoCont
    ms.date: 04/30/2018
    ms.topic: article
    ms.prod: dynamics-nav-2017
    ms.contentlocale: cs-cz
    ms.lasthandoff: 04/30/2018
---

# Evidence smluv
Smlouvy jsou v systému evidovány na **Kartě smlouvy**. Jednotlivé karty jsou číslovány automaticky na základě číselné řady definované v Obecném nastavení. Papírové číslo smlouvy je možno zadat do pole Formální číslo smlouvy.
Důležitá pole v hlavičce Karty smlouvy:
-	Formální číslo smlouvy = číslo na smlouvě
-	Název = název smlouvy
-	Typ kontaktu = zdroj, pro který je smlouva určena. Možné volby jsou:
	- Dodavatel
	- Zákazník
	- Klient
	- Lékař
	- Zaměstnanec
-	Číslo kontaktu = číslo ze zdroje dle typu. Název kontaktu se doplňuje z tabulky Kontakt dle nastavení vytvoření názvu
-	Kód hlavního předmětu = hlavní předmět smlouvy
-	Kód zodpovědného org.úseku = organizační úsek, který zodpovídá za smlouvu.
-	Kód úložiště = umístění originálu smlouvy
-	Datum podpisu = datum podepsání smlouvy
-	Platná od data, do data = platnost smlouvy
-	Vzorec data upozornění – zde je možno definovat vzorec data, kdy má systém upozornit na nastavenou skutečnost, např. na datum vypršení smlouvy. 
	- Funkčnost upozornění řeší modul Upozorňovátko, který slouží např. k hlídání termínů na dokladech (datum dodání, splatnosti, datum platnosti, datum upozornění). Je možno informovat mailem zaměstnance o aktuálnosti termínu (kontroly, plnění, splnění, …). Pro každou tabulku v systému, která má být sledována Upozorňovátkem, je nastavena tzv. Karta šablony události. Na této kartě jsou specifikovány další omezující podmínky, tzn. Upozorňovátko nemusí pracovat se všemi záznamy z dané tabulky, ale pouze s vybranou podmnožinou.
	- Ke každé šabloně jsou dále definovány Fáze událostí, tj. stavy, ve kterých se v Upozorňovátku může konkrétní Položka události nacházet. U fází jsou uvedena i pravidla jejich použití odkazující se např. na vznik záznamu nebo určité datumové pole.
	- Vlastní hromadné vytvoření a aktualizace Položek upozornění je řešeno spuštěním reportu (ručně či plánovačem).

V **předmětech smlouvy** je možno evidovat další předměty smlouvy, což umožňuje její zařazení do více skupin dle předmětů, které řeší. 

Pokud ke zdrojové smlouvě náleží dodatky, které mají své číslo, je vhodné je evidovat jako další smlouvu a s touto hlavní smlouvou je spojit pomocí funkčnosti Připojení souvisejících smluv – funkce Připoj související smlouvu v záložce **Související smlouvy**. 

## <a name="see-also"></a>Viz také
[AC Lázeňské řešení](ac-spa-solution.md)