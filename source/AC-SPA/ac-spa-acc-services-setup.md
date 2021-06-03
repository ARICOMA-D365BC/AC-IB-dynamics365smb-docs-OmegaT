---
    title: "Nastavení služeb ubytování"
    author: AutoCont
    ms.date: 04/30/2018
    ms.topic: article
    ms.prod: dynamics-nav-2017
    ms.contentlocale: cs-cz
    ms.lasthandoff: 04/30/2018
---

# Nastavení služeb ubytování

Tento číselník slouží pro automatické vyhledání a přiřazení služeb ubytování pro lůžko, přistýlku a neobsazené lůžko, které jsou závislé na kategorii ubytování, typu pobytu a věkové kategorii. 
Vazba mezi čerpanou a účtovanou službou nemusí vždy znamenat vazbu jedna ku jedné. Např. po-skytnutí lepší kategorie ubytování znamená jednu službu z hlediska operativy, ale může se dělit na dvě služby účtované (základ + příplatek). Každou službu pak může hradit stejný nebo i jiný plátce.
Z těchto důvodů je třeba pro ubytování definovat a mít možnost pro různé účely přiřadit několik slu-žeb:
-	Lůžko – umožňuje definovat základní službu pro lůžko
-	Příplatek – lůžko – umožňuje definovat službu příplatku pro lůžko
-	Neobsazené lůžko – umožňuje definovat základní službu za neobsazené lůžko v případě, kdy klient žádá obsazení celého pokoje
-	Příplatek – Neobsazené lůžko – umožňuje definovat službu příplatku za neobsazené lůžko v případě, kdy klient žádá obsazení celého pokoje
-	Klientem blokované lůžko – umožňuje definovat základní službu za blokování pokoje v případě, kdy je klient mimo lázeňské zařízení, např. z důvodu hospitalizace
-	Příplatek – Klientem blokované lůžko – umožňuje definovat službu příplatku za blokování pokoje v případě, kdy je klient mimo lázeňské zařízení, např. z důvodu hospitalizace
-	Příplatek – předčasný příjezd (umožňuje definovat službu příplatku pro předčasný příjezd, který neobsazuje ubytovací kapacitu)
-	Příplatek – rezervovaný předčasný příjezd (umožňuje definovat službu příplatku pro předčasný příjezd, který obsazuje ubytovací kapacitu)
-	Příplatek – pozdní odjezd (umožňuje definovat službu příplatku pro pozdní odjezd, který neobsazuje ubytovací kapacitu)
-	Příplatek – rezervovaný pozdní odjezd (umožňuje definovat službu příplatku pro pozdní odjezd, který obsazuje ubytovací kapacitu do standardního počátku následujícího dne)
-	Celý pokoj (toto pole umožňuje zadat službu pro vyúčtování celého pokoje jednomu klientovi, ostatní klienti na stejném pokoji jej budou mít zdarma)
-	Příplatek – celý pokoj (toto pole umožňuje zadat službu pro vyúčtování příplatku ze lepší kategorii v případě ceny za celý pokoj)
-	Číselník dále umožňuje definovat služby na stejném principu také pro přistýlky a průvodce 



## <a name="see-also"></a>Viz také
[AC Lázeňské řešení](ac-spa-solution.md)