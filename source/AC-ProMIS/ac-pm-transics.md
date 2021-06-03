---
title: "AC Promis - transics"
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


# <a name="ac-pm-transics"></a>Integrace Transics

## TRANSICS
Výměna dat s Transics probíhá na bázi webových služeb (web services). Z dostupných webových služeb jsou implementovány:
- Get_Vehicles
- Get_VehicleInfo_On_Date
- Insert_Planning
- Update_Planning
- Get_Planning_Modifications
- Cancel_Planning
- Get_Positions
- Get_ActivityList
- Get_ActivityReportDetail
- Get_RefuelReport
- Get_BorderCrossingReport
- Get_EcoMonitor_Report

Z výše uvedených služeb jsou získávány následující informace:
- Položky pozic vozidel	- jedná se informativní údaj pro dispečera, je protokolována historie
- Denní pozice		- viz předchozí, ale za celý den, aby se doplnily případné chybějící informace (např. byla služba nějakou dobu nedostupná)
- Položky přechodů hranic	- tyto informace slouží jako pomocný údaj pro vyúčtování cestovních příkazů
- Položky tankování	 	- jedná se o informativní údaje, jak řidič zaznamenal informace o tom, že natankoval
- Položka Ecomonitorgu 	- informace o způsobu jízdy řidiče; slouží jako podklad pro reporting či zákaznické řešení pro hodnocení řidičů
- Položky aktivit Transics	- v kombinaci s Přechody hranic se tvoří data v tabulce Žurnál aktivit řidiče, což je primární výsledek celé integrace. 
    Jedná se o následující typy aktivit:
    - Konzultace	- v závislosti na konkrétní instrukční, např. že začal vykládat, nakládat, …
    - Extra Informace - lze evidovat doplňující informace, které bude řidič zadávat (dle konkrétní instrukční sady, musí být upraveno jako zákaznická úprava
    - Anomálie
    - Chyby

## <a name="see-also"></a>Viz také  
[AC ProMIS](ac-pm-promis.md)