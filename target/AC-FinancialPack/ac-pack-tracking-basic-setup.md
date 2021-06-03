---
title: Autocont - Pack Tracking Basic Setup | Microsoft Docs
description:  This section describes Autocont Pack Tracking Basic AddOn Setup
author: ACPJanousek
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Pack tracking, setup, rapidstart, item
ms.date: 01/31/2020 TODO
ms.author: v-pejano
---

# Evidence obalů základ (EKOKOM) - Nastavení
Pro zajištění fungování add-on modulu **Evidence obalů základ** je třeba provést nutné kroky nastavení.

## Založení Výkazu obalů
V systému lze založit potřebný počet různých Výkazů obalů. Pomocí ![Žárovka, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat") vyhledejte **Výkazy obalů**.

> [!NOTE]  
> Pokud se chystáte importovat poskytnuté soubory parametrizace EKO-KOM, je nutné založit Výkaz obalů s kódem **EKO-KOM**.

## Parametrizace Výkazu obalů EKO-KOM
Součástí dodávky add-on modulu Evidence obalů jsou excelové soubory *ekokom_def.xlsx* a *ekokom.xlsx* obsahující parametrizaci pro **Výkaz obalů EKO-KOM**.  
Soubory s parametrizací lze do systému nahrát pomocí služby **RapidStart**.

## Definice prvků Výkazu obalů (struktury výkazu)
Pro každý založený výkaz je nutno nadefinovat jeho prvky. Pomocí vyhledávací funkce ![Žárovka, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat") vyhledejte **Definice prvků výkazu obalů**.  
Prvky ve výkazu lze seskupovat do pozic na výkazu. Celkem lze definovat 10 pozic (seskupení prvků). Prvky v rámci jedné pozice mají dále přiřazený kód.

Pole formuláře Definice prvků výkazu obalů:

| Pole | Popis |
|---------------|---------------|  
| **Kód pro vykazování** | Kód výkazu založeného v předchozím kroku |
| **Pozice** | Uživatelem určená skupina prvků výkazu |
| **Kód** | Kód prvku v rámci pozice |
| **Popis** | Popis prvku výkazu |
| **Umístění ve výkazu** | Textová popisná informace |


Lze tak například vytvořit tabulku s těmito hodnotami:

| Kód pro vykazování | Pozice | Kód | Popis |
|----------|----------|----------|----------|
| EKO-KOM | P1 | 1 | Obaly pro jedno použití |
| EKO-KOM | P1 | 2 | Obaly pro opakované použití |
| EKO-KOM | P2 | 1 | zpoplatněné |
| EKO-KOM | P2 | 2 | předplacené |
| EKO-KOM | P2 | 3 | neplacené |

## Založení prvků ve Výkazu obalů (definice vlastního výkazu)

Definice vlastního výkazu se provádí založením prvků Výkazu obalů. Pomocí vyhledávací funkce ![Žárovka, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat") vyhledejte **Prvky výkazu obalů**. Ve formuláři se definují jednotlivé řádky výkazu tak, že se vybírají z dříve definovaných prvků pro jednotlivé pozice výkazu. Pole *Popis* je pak systémem doplněno v závislosti na plnění pole na stránce **Definice prvků vykazu obalů**.

Záznam stránky **Prvky výkazu obalů** tak může vypadat třeba takto:

| Kód pro vykazování | Kód | Popis |
|---------------|---------------|---------------|
| EKO-KOM | 13 | Obaly pro jedno použití neplacené |

## Založení výjimek ve výkazu obalů

V každém založeném **Výkazu obalů** lze definovat výjimky, specifikované stavem řádků v Deníku zboží, které nebudou do výkazu zahrnuty. Pomocí vyhledávací funkce ![Žárovka, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat") vyhledejte **Výjimky prvku výkazu obalů**.  Výjimka je definována údaji zadanými do polí **Typ pohybu**, **ID pole**, **Hodnota** a **Pozice** (ve výkazu). Pro vytvoření výjimky je nutné specifikovat také **Kód prvku**.

## [přibližně]<g1>See also</g1>
[Evidence obalů základ (EKOKOM)](ac-pack-tracking-basic.md)  
[Financial Pack](ac-finance-pack.md)
