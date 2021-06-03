---
title: AUTOCONT SOLUTIONS - SK Legistaltive Pack| Microsoft Docs
description: This section describes AUTOCONT Solutions - Slovak legislation
author: ac-kunes
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Slovak, , additional functions, sale, VAT
ms.author: v-makune
---
# Kontrolní výkaz DPH

Funkcionalita umožňuje zpracování Kontrolního výkazu DPH a jeho export do souboru formátu xml, který je možné importovat na portál Finanční správy SR nebo do aplikace eDane.

## Generování Kontrolního výkazu DPH

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Přehled kontrolních výkazů DPH** a poté vyberte související odkaz.
2. Pro založení nového Kontrolního výkazu zvolte funkci **Nový**.
3. Na Kartě kontrolního výkazu DPH vyplňte příslušná pole na hlavičce. Na záložce Ostatní je potřeba správně vyplnit pole **XML schéma**.
4. Pro vyplnění řádků výkazu spusťte funkci  **Naplň řádky výkazu**.
5. Pro jednoduchou kontrolu zvolte funkci **Náhled**.

> [!NOTE]
> Pole **Detailní položka** v řádcích KV slouží pro systémové označení řádku. Pokud má hodnotu ANO  položku do kontrolního výkazu nevybere (nepřenese se do xml a nereportuje se na Finanční správu). Při uzavření KV se uzavřou i položky, které budou mít v tomto poli hodnotu ANO.

> [!NOTE]
> Pole **Upozornění** v řádcích KV je informativní pole, které upozorňuje na chybějící údaje u jednotlivých dokladů načítaných do KV.

## Úpravy Kontrolního výkazu DPH

Uživatelsky je možné otevřít jednotlivé řádky kontrolního výkazu k editaci. Po ukončení úprav je potřebné položky v KV přepočítat.

1. Na Kartě kontrolního výkazu DPH zvolte funkci **Úpravy** pro editaci.
2. Po dokončení úprav zavřete okno. Systém se automaticky zeptá, zda požadujete Přepočítat součtové řádky. Potvrďte **Ano**.

## Export Kontrolního výkazu DPH do XML

1. Na Kartě kontrolního výkazu DPH zvolte funkci **Náhled**.
2. Poté zvolte **Export do XML** a dotaz systému potvrďte **Ano**.

## Uzavření Kontrolního výkazu DPH

Kontrolní výkaz je nutné uzavřít až po kontrole údajů. Po uzavření kontrolního výkazu systém zablokuje opětovné načítání dat do formuláře. Údaje vygenerované před jeho uzavřením už není možno změnit ani doplnit. Uzavřený formulář není možné vymazat ze seznamu vygenerovaných KV. Po uzavření formuláře položky v tabulce Položka DPH mají zaškrtnuté pole Uzavřeno pro kontrolní výkaz.

1. Na Kartě kontrolního výkazu DPH zvolte funkci **Uzavřít** pro jeho uzavření.

## [přibližně]<g1>See also</g1>

[AUTOCONT Řešení](../index.md)  
[SK Legislativní balíček](ac-sk-legislative-pack.md)  
[Kontrolní výkaz DPH - nastavení](ac-sk-vat-check-report-setup.md)
