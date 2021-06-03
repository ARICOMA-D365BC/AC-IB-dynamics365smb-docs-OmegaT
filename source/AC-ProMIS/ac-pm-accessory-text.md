---
title: "AC Promis - Průvodní texty"
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


# <a name="ac-pm-accessory-text"></a>Průvodní texty

**Průvodní texty** umožňují definovat a řídit poznámky jednotlivých entit. Vztahují se vždy k dané entitě, tzn., že se pořizují ke konkrétní entitě a s danou entitou se také smažou. Jedná se o relaci 1:N. 
Využívají se jako poznámky a také v reportech.

### Kódy užití textu

Kódy užití umožňují škálovat texty, které se pak připojují k různým entitám.

**Nastavení průvodních textů** – jedná se o uživatelsky definovaný číselník, který určuje, pro kterou entitu budou průvodní texty přístupné a s jakými kódy užití. Hodnota v poli „Pořadí pro výběr“ určuje, v jakém pořadí se budou kódy užití průvodních textů nabízet uživateli v rámci stejné entity.

V poli „Použij skupinu textů jako šablonu“ je možno vybrat skupinu obecných textů, která bude sloužit jako šablona pro dané užití průvodního textu. Uživatel pak tuto šablonu může využít při zadávání průvodního textu k dané entitě a případně ji jen upravit dle vlastností dané entity. 

Průvodní texty se zobrazují v informačním okně u dané entity, pokud je pro danou entitu definováno alespoň 1 užití průvodního textu v Nastavení průvodních textů. Rozkliknutím pole „Počet“ (a to i v případě prázdné hodnoty) se uživatel dostane do obsahu průvodního textu. Pomocí tlačítka „Upravit text“ může definovat obsah textu pro jednotlivé kódy jazyka.

Pokud je pro dané užití průvodního textu nastavena šablona obecného textu, může ji uživatel využít pomocí akce „Použij šablonu“. Tím se do obsahu průvodního textu zkopíruje text definovaný v obecných textech. Uživatel jej může dodatečně upravit. 


## <a name="see-also"></a>Viz také  
[AC ProMIS](ac-pm-promis.md)