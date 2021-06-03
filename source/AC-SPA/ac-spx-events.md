---
    title: "Události"
    author: AutoCont
    ms.date: 04/30/2018
    ms.topic: article
    ms.prod: dynamics-nav-2017
    ms.contentlocale: cs-cz
    ms.lasthandoff: 04/30/2018
---

# Události
Modul Události umožňuje vytvoření a odeslání události při vybraných operacích v různých oblastech systému.
Příkladem využití událostí může být např. generování události při vzniku či přiřazení úkolu či činnosti, nebo při posunu termínu splnění úkolu, kontrole termínu vypršení smluv, generování a odeslání události při nedodání výsledků laboratoře, přihlášení a odhlášení uživatelů, změně pracovního data nebo změně záznamů v protokolu změn. 
Nástroj Události slouží k podání informace o nějakém procesu, který nastal a splňuje předem definované podmínky. Tato informace může v sobě mít odkaz na zdroj, ze kterého pochází.  

**Nastavení**  

**Obecné nastavení** – záložka Události
-	Zpracuj události po přihlášení
-	Čas pro znovuotevření dispečera událostí (pokud uživatel událost nezpracuje, ale jen zavře, znovu se mu připomene po tomto čase) – možno nastavit pro jednotlivé uživatele
-	Čas pro otevření pro nové události – možno nastavit pro jednotlivé uživatele
-	Přípona zástupce
-	Kód události přihlášení
-	Kód události odhlášení
-	Kód události změny prac. data
-	Kód události uživatelsky zadaného oznámení
-	Kód události notifikace standardního workflow
-	Kód události fronty úloh – Informace
-	Kód události fronty úloh – Chyba

**Nastavení poštovního protokolu SMTP**  
-	SMTP server pro odesílání e-mailů

**Prodejci**
-	Upozornění na události přes e-mail
-	E-mail

**Nastavení uživatelů** – záložka Události   
Záložka obsahuje jednak informace o nezpracovaných událostech uživatele, jednak umožňuje nastavit události, které se budou generovat a zobrazovat pro daného uživatele a upravit výchozí nastavení zpracování událostí z Obecného nastavení přímo na míru konkrétního uživatele
-	Zpracuj události po přihlášení
-	Zobraz události po přihlášení
-	Čas pro znovuotevření dispečera událostí (pokud uživatel událost nezpracuje, ale jen zavře, znovu se mu připomene po tomto čase) 
-	Čas pro otevření pro nové události 
-	Nepoužívat dispečera událostí
-	Generuj událost přihl./odhlášení
-	Zakázat změnu pracovního data
-	Generuj událost zm. Prac. data
-	Upozornění na události přes e-mail
-	Nezpracovaná událost
-	Nezpracované události chyb
-	Nezpracované události úkolů
-	Nezpracované informační události
-	Nezpracované události změny stavu
-	Nezpracované události varování

**Zaměstnanci**
-	Upozornění na události přes e-mail
-	E-mail

**Typy událostí**
Pro události je možné definovat několik typů, které je možno navázat na různá zdrojová data v systému, definovat způsob zpracování, upozornění, zobrazení a opakování příbuzné události. 

**Nastavení příjemců událostí**
Pro každý typ události je možno nastavit příjemce události, kterým může být:
-	Uživatel
-	Prodejce
-	Skupina uživatelů
-	Skupina příjemců – pro skupinu příjemců se definují členové skupiny příjemců události

**Skupiny příjemců události**  
Příjemcem události může být skupina příjemců, která je složena ze členů skupiny příjemců události. To umožňuje sestavit pro nějakou událost speciální tým. Členy skupiny příjemců mohou být:
-	Uživatel
-	Prodejce
-	Skupina uživatelů  


**Mé události**  
Z událostí uživatele je možné vytvořit pohled, který bude obsahovat pouze události daného uživatele a tento pohled se pak může zobrazovat v centru rolí, kde si jej uživatel může spravovat. Kromě seznamu událostí a základních informací o událostech se uživatel může prokliknout přímo ke zdrojovému záznamu a událost rychle vyřešit.

## <a name="see-also"></a>Viz také
[AC Lázeňské řešení](ac-spa-solution.md)