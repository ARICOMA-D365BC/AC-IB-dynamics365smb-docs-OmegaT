---
    title: "Pobytová akce"
    author: AutoCont
    ms.date: 04/30/2018
    ms.topic: article
    ms.prod: dynamics-nav-2017
    ms.contentlocale: cs-cz
    ms.lasthandoff: 04/30/2018
---

# Pobytová akce

Pobytové akce patří mezi marketingové nástroje lázeňského řešení. Je možno je nastavit ve formuláři Pobytové akce. Dle zadaných podmínek může jednomu pobytu vyhovovat i několik pobytových akcí najednou, systém pak vybere tu nejvýhodnější pro klienta.

Pobytová akce je založena na definovaném počtu pobytových dní zdarma (např. 7 za 5, 14 za 12 apod.), které se uplatní v případě, že dosažené množství služeb pro uplatnění akce je >= základu pro výpočet. Uplatnění se spojí se službou s největším počtem dní.
Dny zdarma se v položce klientského účtu projeví jako nové položky se záporným množstvím a číslem pobytové akce.

Význam polí:
-	Pole Kód typu klienta, Kód typu pobytu, Číslo plátce, Kód lázeňského domu, Kód dependen-ce a Den nástupu – slouží jako podmínka pro výběr dané akce pro pobyt. 
-	Den nástupu se vztahuje k počátečnímu datu pobytu.
-	Počáteční a koncové datum – ohraničuje platnost akce
-	Způsob kontroly
	- 	Kód služby – kontrola nezbytného počtu služeb pro uplatnění akce se provádí přes kódy služeb
	- 	Kategorie služby - kontrola nezbytného počtu služeb pro uplatnění akce se provádí přes kategorie služeb, které je možno definovat ke konkrétním službám v poli Kód kategorie (v číselníku Lázeňská služba). Pro výpočty se pak služby sčítají dle stejné kategorie.
-	Typ položek pro kontrolu – určuje, z jakých položek se bude kontrolovat jejich množství ve vztahu k poli Základ pro výpočet. Akce se uplatní pouze v případě, kdy kontrolní množství je >= Základu pro výpočet.  
	- 	Vše – pro uplatnění akce se bude brát v úvahu Kontrolní množství všech služeb zařazených do kontroly akcí, z nich se vybere minimální množství a to se zkontroluje na hodnotu základu pro výpočet. Jestliže bude větší nebo rovno, akce se uplatní.
	- 	Léčebný pobyt – pro uplatnění akce se bude brát v úvahu pouze Kontrolní množství služeb léčení zařazených do kontroly akcí, z nich se vybere minimální množství a to se zkontroluje na hodnotu základu pro výpočet. V případě, že bude shodné či větší, akce se uplatní. A to i v případě, že kontrolní množství služeb ubytování či stravování bude menší.
	- 	Ubytování – pro uplatnění akce se bude brát v úvahu pouze Kontrolní množství služeb ubytování zařazených do kontroly akcí, z nich se vybere minimální množství a to se zkontroluje na hodnotu základu pro výpočet. V případě, že bude shodné či větší, akce se uplatní.
	- 	Stravování – pro uplatnění akce se bude brát v úvahu pouze Kontrolní množství služeb stravování zařazených do kontroly akcí, z nich se vybere minimální množství a to se zkontroluje na hodnotu základu pro výpočet. V případě, že bude shodné či větší, akce se uplatní.
-	Základ pro výpočet – definuje množství, které musí být u kontrolovaných služeb dosaženo, aby došlo k uplatnění akce
-	Účtované množství – toto pole určuje počet účtovaných dnů. Rozdíl účtovaných dnů a základu pro výpočet pak tvoří dny zdarma.
-	Uplatni na ubytování, stravování, léčení – pomocí těchto polí se dá definovat, na jaké typy služeb bude akce uplatněna v případě splnění definovaných podmínek.

**Lázeňská služba**  
S pobytovými akcemi souvisí 3 pole:
-	Kód kategorie – umožňuje kontrolovat počet služeb pro uplatnění akce na základě nějaké společné vlastnosti a sloučit tak několik kódů služeb
-	Zařadit do kontroly pobytových akcí – umožňuje zařadit službu do kontrolního mechanismu pro zjištění, zda pobyt s danými službami vyhovuje podmínkám definované akce
-	Zařadit do uplatnění slev pobytových akcí – umožňuje na službu uplatnit slevu dle definova-ných podmínek pobytové akce

**Nastavení lázeňských financí**  
S pobytovými akcemi souvisí 3 pole:
-	Zpracuj pobytové akce k poslednímu dni – pokud je pole zaškrtnuto, akce se počítají až při účtování konce pobytu
-	Zahrň doplňkového plátce do pobytových akcí - pokud je pole zaškrtnuto, akce se budou po-čítat i pro doplňkového plátce (standardně je do pobytových akcí zahrnut hlavní plátce)
-	Zahrň klienta do pobytových akcí - pokud je pole zaškrtnuto, akce se budou počítat i pro po-ložky hrazené klientem

**Nastavení typu pobytu**   
S pobytovými akcemi souvisí 2 pole:
-	Povol pobytové akce – zaškrtnutí v tomto poli povoluje využití pobytových akcí pro danou kombinaci typu klienta a pobytu
-	Zpřístupnit povolení pobytových akcí – zaškrtnutí v tomto poli umožňuje nastavit povolení na pobytové akce na konkrétní kartě pobytu klienta, která vychází z dané kombinace typu klienta a pobytu 



## <a name="see-also"></a>Viz také
[AC Lázeňské řešení](ac-spa-solution.md)