---
title: "AC Promis - Integrace Plantour"
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


# <a name="ac-pm-plantour"></a>Integrace Plantour

Integrace s aplikací Plantour probíhá na bázi výměnných tabulek v MS SQL.

Z NAV jsou exportovány následující 4 tabulky: 

- **Vozidla** – evidují se i parametry vozidel (kód s 12 pozicemi) pro porovnání s omezeními na dodacích místech (viz násl.bod)
- **Dodací místa** – z  NAV je tento seznam průběžně aktualizován, jak jsou průběžně na dokladech vytvářena. Evidují se až 2 časová okna pro 7 dní v týdnu, dále se pak evidují omezení pro vozidla (max. hmotnost, sklopná rampa, nakládací ruka,… to je zákaznická implementace)
- **Zásilky** – zde se evidují toky na/z dodacích míst (komodity, ale i např. palety); Plantour zohledňuje, aby šlo v každý okamžik na auto vše naložit.
- **Řidiči** – jen základní číselník vlastních řidičů Kód, jméno, telefon, Aktivní

Do NAV jsou importovány následující 2 tabulky:

- T_TRS_O	- vypočtené trasy
- T_ZAST_O	- zastávky na trase

Stávající způsob výběru zásilek pro odeslání do Plantour se provádí pomocí filtrů, kde lze využít pole jako číslo prvního nebo posledního distr. místa, požadovaný čas nakládky/vykládky, stav plánování, stav Plantour..  Pomocí těchto filtrů lze vybrat zásilky pro rozvoz nakládané v místě, pro které je využíváno plánování pomocí Plantour, zásilky pro zapracování s ohledem na datum, zásilky nezaplánované, zásilky neodeslané do Plantour…

## <a name="see-also"></a>Viz také  
[AC ProMIS](ac-pm-promis.md)