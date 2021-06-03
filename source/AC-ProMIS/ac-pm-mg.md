---
title: "AC Promis - Map&Guide"
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


# <a name="ac-pm-MG"></a>Map&Guide

Tato komunikace je možná pouze s Map&Guide licencovaným jako Server (Desktop edice není pro integraci použitelná). Komunikace je pak realizována pomocí následujících tří webových služeb:
- o	**xLocate** – z NAV se odešlou souřadnice a server M&G vrátí, co se v daném místě nachází; a naopak
- o	**xMap** - z NAV se odešlou požadované body zájmu a server M&G vrací mapu (jako obrázek) s vyznačenými body)
-  o	**xRoute** - z NAV se odešle požadavek na trasu s počátkem a koncem, server M&G vrací trasu reprezentovanou průjezdnými body

Pozn. V případě komunikace s externím serverem není možné definovat vlastní ikony pro vyznačení bodů zájmu, lze využít pouze předdefinované.

## <a name="see-also"></a>Viz také  
[AC ProMIS](ac-pm-promis.md)