---
title: "AC Promis - Záznamy o provozu vozidel"
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


# <a name="ac-pm-traffic-records"></a>Záznamy o provozu vozidel

Součástí pomocné evidence pro nákladní dopravu jsou záznamy o provozu vozidla (stazka), ve kterých jsou zaznamenány skutečné jízdy a jejich průběh. Záznam obsahuje údaje jako manipulace s vozidlem během jeho provozu, identifikaci řidiče nebo posádky vykonávající jízdu, stav tachometru, počáteční a koncové stavy nádrže, místa a časy prováděných nakládek a vykládek, ujeté kilometry nebo čerpání pohonných hmot. Evidence na základě hodnot stavu nádrže, ujetých km a množství tankování, které byly v rámci jízdy zaznamenány, umožňuje vyčíslení spotřeby vozidla za jednotlivý záznam o provozu. 

Ke sběru dat o průběhu realizace jízdy může sloužit buď papírová evidence, nebo elektronický sběr dat z monitorovacího zařízení vozidla. K papírové evidenci jsou využívány standardní tiskopisy např. ET220 a tiskopis vyplňuje řidič v průběhu jízdy. Pokud je požadována elektronická evidence, jsou data ručně převedena do záznamů o provozu vozidel v NAV. Jednou z výhod tohoto způsobu evidence je přesné určení počátku a konce konkrétního záznamu vozidla, protože se odvíjí od údajů ve vyplněném tiskopisu. Druhou výhodou je možnost doplnění/korekce dat při jejich přepisu.

Naopak elektronické zpracování evidence na základě dat stažených z monitorovacího zařízení vozidla je ve velké míře závislé na kvalitě vkládaných dat o prováděných operacích řidičem v průběhu realizace přepravy. Pro elektronické vytvoření záznamu o provozu vozidla je využito vícero zdrojů informací, které jsou uchovány v terminálových položkách, položkách aktivit vozidla, položkách přechodu hranic a položkách tankování. Nevýhodou elektronického zpracování je přesné určení počátku a konce záznamu, pokud není součástí dat z monitorovacího zařízení.

Záznam o provozu vozidla není primárně určen pro výpočet nároku stravného pro řidiče. Tento výpočet je prováděn v samostatné evidenci Vyúčtování cest zaměstnanců viz kapitola níže.

Evidence záznamů o provozu vozidla v IS poskytuje kontrolní nástroje pro ověření správnosti dat mezi dvěma navazujícími záznamy vozidla např. chybějící záznamy o provozu, stav tachometru, spotřeby vozidla.

## <a name="see-also"></a>Viz také  
[AC ProMIS](ac-pm-promis.md)