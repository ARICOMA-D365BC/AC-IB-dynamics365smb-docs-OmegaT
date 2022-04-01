---
title: AC - Financial pack -  Multiple payments | Microsoft Docs
description: Jednoduchy popis tematu
author: ACMartinKunes

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.search.keywords: Multiple payments, finance 
ms.date: 04/01/2022
ms.author: AC MartinKunes
---
# Více úhrad
> Aktualizace 01.04.2022

Addon **Více způsobů plateb** rozšiřuje standard prodejních dokladů v oblasti vyrovnání dokladu přímo při účtování.
Na dokladech prodejní faktura či prodejní dobropis je namísto jednoho způsobu platby je nově možné definovat více způsobů, typicky část úhrady platební kartou a část v hotovosti.

Funkcionalita rozšiřuje možnosti nastavení pravidel uživatelům i v případě použití jednoho způsobu platby, a to jak na prodejních tak i nákupních dokladech. Cílem je omezení chybovosti uživatelů prostřednictvím jejich přiřazení k určitým „pokladním místům“.
V praxi se ale stává, že zákazník chce uhradit na místě v hotovosti doklad, který měl být uhrazen bankovním převodem. Pak je možné využít i funkčnost modulu a definovat kombinaci úhrady na zaúčtované faktuře (dobropisu) či na vystavené záloze.
Pro evidenci protiúčtu vyrovnání je možné používat všechny tři možnosti protiúčtů, které obsahuje lokalizace (Finanční účet, Bankovní účet, Pokladna). Nejběžnější je však **použití Pokladny jako protiúčtu**, které umožňuje kombinovat použití Více způsobů plateb a Pokladních dokladů a přináší s sebou výhody v oblasti zaokrouhlování (je automaticky řešeno až na pokladním dokladu).

> [!WARNING]
> Modul tvoří základ pro podporu maloobchodního prodeje formou Cash&Carry. Funkcionalita není dostupná na objednávkách (obecně na prodejních/nákupních dokladech, kde je možná částečná fakturace). Pokud si ji na tyto doklady přidáte, pak si musíte ošetřit programově či metodicky potenciálně konfliktní stavy.
Možnost definice více způsobů plateb není standardně k dispozici na žádném nákupním dokladu, ale je možné je tam doplnit v rámci zákaznického rozšíření funkcionality.


## Účtování prodejní faktury s více způsoby úhrady

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Prodejní faktury** a poté vyberte související odkaz.
2.	Vytvořte novou prodejní fakturu dle vašich zvyklostí.
3.	Na stránce **Prodejní faktura** spusťte akci **Vydat** a poté spusťte funkci **Rozpis platby**.
4.	Zadejte částku v hotovosti, kterou jste obdrželi od zákazníka.
5.	V dalším kroku zadejte do řádků další způsoby úhrady a částku hrazenou daným způsobem.
6.	V poli Vrátit hotovost (LM) zjistěte částku, jakou máte zákazníkovi vrátit.
7.	Tlačítkem **OK** zavřete stránku.
8.	Na stránce Prodejní faktura spusťte funkci Účtovat.

> [!NOTE]
> Pokud nezadáte částku v hotovosti, musíte v řádcích zadat částky přesně do výše částky dokladu (tedy tak, aby v poli Zůstatek byla hodnota nula).

![Rozpis platby](media/multiple_payment_methods_payment.png)

## Dodatečná úhrada zaúčtované prodejní faktury
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Účtované prodejní faktury** a poté vyberte související odkaz.
2.	Najděte příslušný doklad a otevřete jeho kartu.
3.	Na stránce Účtovaná prodejní faktura spusťte funkci **Rozpis platby**.
4.	Zadejte částku v hotovosti, kterou jste obdrželi od zákazníka.
5.	V dalším kroku zadejte do řádků další způsoby úhrady a částku hrazenou daným způsobem.
6.	V poli Vrátit hotovost (LM) zjistěte částku, jakou máte zákazníkovi vrátit.
7.	Na stránce Rozpis platby spusťte funkci Účtovat pro zaúčtování jedné či více vyrovnávacích položek (typicky pokladních dokladů).
8.	Tlačítkem **OK** zavřete stránku.

> [!NOTE]
> Obdobný postup lze použít na stránce Účtovaný prodejní dobropis.
> Je-li doklad nezaokrouhlený, zaokrouhlení částky hotovosti k vrácení probíhá až při účtování vyrovnání prostřednictvím nastaveného zaokrouhlení ve funkcionalitě Pokladní doklady.

## Evidence úhrady – zjednodušený režim

V případě, že zákazník chce provést vyrovnání dokladu při účtování pouze jedním způsobem, např. bankovní kartou, lze použít zjednodušený režim zadáním vybraného Kódu způsobu platby přímo v hlavičce dokladu.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Prodejní faktury** a poté vyberte související odkaz.
2. Najděte příslušný doklad a otevřete jeho kartu.
3. Na stránce Prodejní faktura vyberte v poli **Kód způsobu platby** odpovídající hodnotu.
4. Na stránce Prodejní faktura spusťte funkci Účtovat.

> [!NOTE]
> Obdobný postup lze použít na stránce Účtovaný prodejní dobropis.

## Evidence úhrady – zjednodušený režim se záměnou Způsobu platby

Poměrně běžnou praxí je, že na kartách zákazníků je definován preferovaný či povolený způsob platby (typicky úhrada v hotovosti). Když je ale takových kódů (z důvodů požadavků na evidenci) více, je třeba zajistit zaúčtování dokladu s kódem příslušným uživateli, který doklad účtuje. V případě zapnutého Kontrola způsobu platby na prod.dokl. provede změnu systém automaticky (viz [Nastavení způsobů platby](http://muj.autocont.cz/docs/cs-cz/d365businesscentral/AC-FinancialPack/ac-multiple-payment-methods-setup.html#nastaven%C3%AD-zp%C5%AFsob%C5%AF-platby)).


1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nastavení více způsobů plateb** a poté vyberte související odkaz.
2.	Ověřte, že je zapnuta volba **Kontrola způsobu platby na prod.dokl**.
3. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nastavení uživatelů** a poté vyberte související odkaz.
4.	Ověřte, že je na přihlášeném uživateli nastaven **Kód platebního místa**.
5. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Zákazníci** a poté vyberte související odkaz.
6.	Najděte příslušného zákazníka a otevřete jeho kartu.
7.	V poli **Kód způsobu platby** nastavte způsob, který má nastavenu hodnotu Hotovost ve sloupci Typ operace pokladny, ale který nemá definovaný **Kód platebního místa** (viz „Hotově“ dle obrázku v **Nastavení způsobů platby**)
7. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Prodejní faktury** a poté vyberte související odkaz.
9.	Spuštěním akce Nový vytvořte nový doklad.
10.	Na stránce Prodejní faktura zadejte zákazníka (viz výše)
11.	Zadejte alespoň jeden řádek faktury.
12.	Na stránce Prodejní faktura spusťte funkci Vydat.


## Evidence EET přímo z rozpisu platby

V některých případech je požadováno vytvoření evidence EET (legislativa v ČR) již na rozpisu platby, tedy ještě před zaúčtováním dokladu (např. pro tisk podkladů pro realizaci dobírky, apod.).

V případě zapnutého Povolit registraci EET je na rozpisu platby dostupná akce Registrovat EET, resp. Storno EET (viz [Nastavení způsobů platby](http://muj.autocont.cz/docs/cs-cz/d365businesscentral/AC-FinancialPack/ac-multiple-payment-methods-setup.html#nastaven%C3%AD-zp%C5%AFsob%C5%AF-platby)).

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nastavení více způsobů plateb** a poté vyberte související odkaz.
2.	Ověřte, že je zapnuta volba Povolit registraci EET.
3.	Vytvořte novou prodejní fakturu dle vašich zvyklostí.
4.	Na stránce Prodejní faktura spusťte akci Vydat a poté spusťte funkci Rozpis platby.
5.	Zadejte částku v hotovosti, kterou jste obdrželi od zákazníka.
6.	V dalším kroku zadejte do řádků další způsoby úhrady a částku hrazenou daným způsobem.
7.	Spusťte akci Registrovat EET.
8.	Tlačítkem **OK** zavřete stránku.


## Viz také

[Nastavení - Více úhad](ac-multiple-payment-methods-setup.md)  
[Financial Pack](ac-finance-pack.md)  
