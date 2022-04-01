---
title: AC - Financial pack -  Multiple payments | Microsoft Docs
description: Jednoduchy popis tematu
author: ACMartinKunes

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.search.keywords: Multiple payments, finance 
ms.date: 01/31/2021
ms.author: AC MartinKunes
---
# Více úhrad - nastavení
> Update 01.04.2022

Před tím, než budete moci používat funkcionality více způsobů plateb ve vašich obchodních procesech, musíte provést základní nastavení modulu. Jedná se o číselníky:

- Způsoby platby
- Platební místa
- Nastavení uživatelů

## Nastavení Způsobů platby

V seznamu Způsoby plateb vytvořte kódy reprezentující používané způsoby plateb (např. hotovost, karta, stravenky,… dle platné legislativy a dle očekávaného rozsahu použití ve firmě) tak, aby bylo možné následně definovat úhradu zákazníkem v požadované struktuře.

Existuje-li ve firmě více přepážek či poboček, je obvyklé evidovat operace na těchto místech odděleně. V takovém případě je třeba vydefinovat pro každý způsob úhrady i příslušný počet protiúčtů. Protiúčtem může být finanční účet či bankovní účet, nicméně nejčastěji se používá karta pokladny.

Dále je třeba definovat *Typ pokladní operace* pro další kontrolní mechanismy funkcionality. Vždy musí existovat řádek s typem „Hotovost“, který systém použije při zadání přijaté částky v hotovosti pro vytvoření řádku rozpisu plateb.

Při ručním vytváření řádků Rozpisu platby je Kód způsobu platby filtrován dle Kódu platebního místa přiřazeného uživateli (viz dále).

![Způsoby plateb](media/multiple_payment_methonds_overview.png)

## Nastavení platebních míst

Pokud si firma vydefinuje způsoby plateb s více pokladnami, může být pro ni výhodné pojmenovat si jednotlivá fyzická pokladní místa a definovat uživatele, které na nich pracují.

V seznamu Platební místa si vydefinujte všechna místa, kde mohou zákazníci hradit své závazky vůči vaší firmě.

V seznamu Nastavení uživatelů přiřaďte vybraným uživatelům obsluhujícím zákazníky příslušný kód platebního místa. Tímto přiřazením docílíte usměrňování chování uživatelů s cílem zamezit chybám z nepozornosti. **Viz: Přiřazení způsobů plateb k uživatelům.**

Přiřazením Kódu platebního místa na způsobu platby docílíte větší kontroly uživatelů, aby nebylo možné omylem provést úhradu vůči protiúčtu, který není uživateli přiřazen.


## Nastavení Více způsobů plateb

Popis jednotlivých parametrů:
- **Povolit více typů hotovosti** – dovolí definovat více způsobů plateb se stejným typem pokladní operace a pro stejné platební místo. Je nutné, pokud chcete např. umožnit přijímat i cizí měnu na pokladních místech.
- **Kontrola způsobu platby na prod.dokl.** – tímto lze nastavit, aby systém při akci Vydání na prodejním dokladu kontroloval, je-li použit odpovídající Způsob platby (tedy s přiřazeným Platebním místem stejným jako má nastaven uživatel, který akci Vydání spustil). Pokud je vše správně nastaveno, systém změní Způsob platby na dokladu, v opačném případě systém zobrazí chybové hlášení.
- **Kontrola způsobu platby na nák.dokl.** – dtto, ale pro nákupní doklady.
- **Povolit registraci EET** – zapíná kontrolu, že v řádcích Rozpisu platby lze použít pouze takové, které mají nastaven sloupec Kód platebního zařízení EET.
- **Kontrolovat fiskální tiskárnu** – tímto nastavením se zapíná vynucení použití funkcionality integrace s tzv. Fiskálními tiskárnami, jejich použití je povinné v legislativním prostředí Slovenské republiky (viz [Fiskální tiskárny](https://muj.autocont.cz/docs/cs-cz/dynamics365/business-central/AC-FinancialPack/ac-fiscal-printers.html)).

Na záložce Číslování lze nastavit číselnou řadu pro doklady platby. Tato se použije pouze v případě, že použijete způsob platby s jiným protiúčtem než Pokladna (pokladny mají vlastní číselné řady viz [Nastavení číselných řad pro příjmové a výdajové doklady](https://docs.microsoft.com/cs-cz/dynamics365/business-central/localfunctionality/czech/ui-extensions-cash-desk-localization-cz#nastaven%C3%AD-%C4%8D%C3%ADseln%C3%BDch-%C5%99ad-pro-p%C5%99%C3%ADjmov%C3%A9-a-v%C3%BDdajov%C3%A9-doklady)).

## Přiřazení způsobů plateb k uživatelům

Z důvodů lepší kontroly nakládání s hotovostí či ceninami je obvykle požadována samostatná evidence pro každého uživatele. Aby se omezila chybovost, je možné každému uživateli přiřadit jeho vlastní Kód platebního místa.
1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do"), icon, enter **User Setup** and then choose the related link.
2. Na stránce Nastavení uživatelů vyberte ve sloupci Kód platebního místa požadovanou hodnotu.


## See also

[Více úhad](ac-multiple-payment-methods.md)  
[Financial Pack](ac-finance-pack.md)
