---
Title: "HelpDesk - Setup"
Description: 
Author: AUTOCONT
Date: 04/04/2019
Product: dynamics365-business-central
Contentlocale: cs-cz
---

# HelpDesk - Nastavení

Modul  Helpdesk slouží k centralizovanému zadávání, evidenci, zpracování a vyhodnocování různých požadavků uživatelů v systému Microsoft Dynamics NAV. Uživatelé zde mohou zadávat požadavky na servisní úkony, na poskytnutí podpory, úpravu nebo doplnění funkcionality, evidovat reklamace a podobně. Umožňuje také kategorizaci požadavků, nastavení priorit a řízené zpracování přiřazenými řešiteli. K dispozici je i historie uzavřených požadavků HelpDesku.


Aby bylo možné zadávat požadavky do HelpDesku, je nutné předem provést některá nastavení:
- Nastavit HelpDesk.
- Založit číselnou řadu pro požadavky HelpDesku.
- Založit kategorie uživatelů.
- Zadat oprávněné osoby a přiřadit je do kategorií.
- Naplnit tabulku priorit požadavků.
- Vytvořit kategorie požadavků (volitelně, pokud se sledují).
- Naplnit tabulku způsobů řešení.
- Vytvořit šablonu workflow pro Helpdesk.
- Nastavit workflow pro HelpDesk.


## Nastavení HelpDesku

Základní nastavení helpdesku slouží k nastavení kategorií požadavků a priorit, zda je nutné požadavky zadávat pomocí průvodce.

1. Pomocí vyhledávací funkce **Řekněte mi, co chcete udělat (Alt + Q)** vyhledejte **Nastavení helpdesku**.
2. Na kartě Nastavení v záložce Obecné je potřeba vybrat **Vynucení Kategorií** a **Výchozí prioritu**.
3. V záložce Číslování nastavit **Číselnou řadu** pro požadavky.
4. Potvrďte pomocí OK.


## Nastavení kategorie uživatelů

Kategorie uživatelů představují skupiny uživatelů. Skupinám uživatelů se přiřadí určitá váha (stupeň důležitosti), která je jedním z faktorů při automatickém výpočtu priority požadavku.

1. Pomocí vyhledávací funkce **Řekněte mi, co chcete udělat (Alt + Q)** vyhledejte **Kategorie uživatelů**.
2. Naplnit pole: **Kód**, **Popis** a **Váha**.
3. Potvrďte pomocí OK.


## Nastavení seznamu oprávněných osob

Pro každou oprávněnou osobu se zvolí příslušná Kategorie uživatele, podle které program automaticky předvyplní Váhu požadavku pro danou osobu. Předvyplněnou hodnotu pole Váha lze pro každou osobu individuálně upravit. Pro výpočet celkové priority požadavku, pak program použije tuto hodnotu

Pomocí vyhledávací funkce **Řekněte mi, co chcete udělat (Alt + Q)** vyhledejte **Oprávněné osoby**.
2. Zvolit volbu **Nový**.
3. Na kartě oprávněné osoby zadat obecné informace do záložky Obecné:
   - **Kód**, **Jméno**, **Kategorie**, **ID** **uživatele**, **Váha**, **Povolena** změna uživatele (opravňuje  ke změně Oprávněné osoby) a **Výchozí** **priorita**.
4. Na kartě oprávněné osoby lze zadat i **detailní informace** do záložky Spojení:
   - **Adresa**, **Telefon**, **Fax**, **Mobil**, **E-mail**.
5. Potvrďte pomocí OK.


## Nastavení priority požadavků

Aby bylo možné vyhodnocovat požadavky podle jejich naléhavosti, je nutné vyplnit **Priority požadavků**. V rámci nastavení je nutné zadat: **Kód**, **Popis** a **Váha**.

 - Váha – pro výpočet výsledné priority požadavku. Váhy lze stanovit libovolně, záleží na místních podmínkách a zvyklostech (zpravidla čím závažnější je požadavek, tím vyšší váha)
 - Výpočet data odezvy, Výpočet data řešení – vzorce pro výpočet. Do polí lze zadat celá čísla se zkratkou jednotky času (např. D = den, M = měsíc, K = kvartál, R = rok). Výsledné datum se vypočte z data, kdy byl požadavek zadán (datum lze následně upravit).

1. Pomocí vyhledávací funkce **Řekněte mi, co chcete udělat (Alt + Q)** vyhledejte **Priority požadavků**.
2. Do tabulky je nutné zadat:
   - **Kód**, **Popis**, **Váha**, **Výpočet data** odezvy a **Výpočet data řešení**.
3. Potvrďte pomocí OK.  


## Nastavení kategorie požadavků

Pro sledování požadavků z jiných hledisek než podle závažnosti je možné nadefinovat kategorie požadavků, a to až ve 3 úrovních, pro které platí stromový rozpad (tzn. jsou ve vztahu hierarchické podřízenosti, tj. volba Kategorie 1 určí, jaké se budou nabízet Kategorie 2, a ty zase ovlivní nabídku Kategorií 3).

1. Pomocí vyhledávací funkce **Řekněte mi, co chcete udělat (Alt + Q)** vyhledejte **Kategorie požadavků**.
2. Na kartě požadavku zadat **Kód** a **popis kategorie požadavku 1**.
3. Pro rozpad na další úroveň v ribbonu vybrat funkci **Kategorie požadavku 2**.
4. Stejný krok opakovat **pro třetí úroveň**.
5. Potvrďte pomocí OK.


## Nastavení řešení požadavků

V této tabulce je možné nadefinovat Kód (max. 10 znaků) a Popis (max. 30 znaků) jednotlivých způsobů řešení požadavků.

1. Pomocí vyhledávací funkce **Řekněte mi, co chcete udělat (Alt + Q)** vyhledejte **Řešení**.
2. Nadefinovat **Kód** a **Popis řešení požadavků**.
3. Potvrďtě pomocí OK.


## Založení šablony Workflow HelpDesku

Pro založení šabloby workflow je nutný **addon WorkFlow**. 

1. Pomocí vyhledávací funkce **Řekněte mi, co chcete udělat (Alt + Q)** vyhledejte **Šablony workflow**
2. Vyplnit na řádku **kód**, **popis** a **číslo tabulky (52068298)**.
3. V ribbonu nastavit stavy WF pomocí tlačítka **Stavy workflow**.
   - Pro stav workflow je třeba nadefinovat **Kód**, **Popis** a **Filtr dalšího stavu**, který určuje, do jakých dalších stavů je možné z daného stavu přejít. Jeden ze stavů musí být označen jako **Výchozí stav** – ten se vyplní při založení nového helpdesk požadavku. Některé stavy mohou být označeny jako **Konečný stav**, z něhož se už nepokračuje do dalšího stavu.
4. Pro konkrétní stav workflow lze definovat **Akci workflow**. Stačí stát na daném řádku stavu a v ribbonu kliknout na **Akce Workflow**.
   - Pro aktivní řádek lze specifikovat **Akce workflow**, **Kontrolovaná pole** a **Nastavovaná pole**. V Akcích se definují **Codeunity**, **Reporty** či **XMLporty**, které se automaticky spustí při přechodu do daného stavu (např. odeslání e-mailové zprávy). U kontrolovaných resp. nastavovaných polí se určí, co a kde se má kontrolovat nebo nastavit při přechodu do daného stavu.
5. Potvrďte pomocí OK.

## Nastavení WorklFlow pro HelpDesk

Po založení šablony je nutné nastavit tuto šablonu v Nastavení workflow.

1. Pomocí vyhledávací funkce **Řekněte mi, co chcete udělat (Alt + Q)** vyhledejte **Nastavení workflow**.
2. Do pole **Šablona workflow** helpdesku zvoli definovanou šablonu.
3. Potvrďte pomocí OK.

## Viz také
[HelpDesk](ac-helpdesk.md)  
[AC Productivity Pack](ac-productivity-pack.md)
