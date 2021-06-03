---
title: "AC Promis - Import objednávek a zasílání zpráv"
author: Autocont
ms.custom: na
ms.date: 07/18/2018
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.prod: dynamics-nav-2018
ms.translationtype: Human Translation
ms.sourcegitcommit: 
ms.openlocfilehash: 
ms.contentlocale: cs-cz
ms.lasthandoff: 

---


# <a name="ac-pm-lds-request"></a>Import objednávek a zasílání zpráv

Převážná část úloh dopravy a skladových operací je tvořena na základě dat poskytnutých od obchodních partnerů. Z důvodu, že každý partner má komunikaci specifickou a zároveň počet partnerů není omezen, byl zvolen následující princip:
 
1. Funkce pro komunikaci se systémy zákazníků.
2. Samostatná výměnná databáze pro výměnu zpráv. 
3. MS Dynamics NAV přebírá data z výměnné databáze a dále je zpracovává a ukládá v interních strukturách.Zároveň vytváří nové záznamy ve výměnné databázi jako podklad pro odchozí komunikaci směrem k obchodním partnerům.

V rámci komunikace s partnery může dojít k následujícím interakcím:

#### Příchozí zprávy od partnerů
- Skladové karty
- Příkaz k naskladnění
- Příkaz k vyskladnění - s dopravou
- Příkaz k vyskladnění - osobní odběr
- Plánovaný svoz
- Změna statusu
- Odblokování zásilek
- Jen doprava (bez skladové operace)
#### Odchozí zprávy k partnerům
- Stav skladu
- Změna statusu (vyvolaná námi)
- Inventurní výdej
- Inventurní příjem
- Neplánovaný svoz
- Track and Trace

## <a name="see-also"></a>Viz také  
[AC ProMIS](ac-pm-promis.md)
