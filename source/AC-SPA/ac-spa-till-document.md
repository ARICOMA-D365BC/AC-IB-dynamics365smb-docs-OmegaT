---
    title: "Prodejní pokladní doklady"
    author: AutoCont
    ms.date: 04/30/2018
    ms.topic: article
    ms.prod: dynamics-nav-2017
    ms.contentlocale: cs-cz
    ms.lasthandoff: 04/30/2018
---

# Prodejní pokladní doklady

Fakturace lázeňských služeb probíhá na standardních prodejních dokladech (Prodejní faktura, Prodejní dobropis) a také na prodejních pokladních dokladech (Pokladní doklad, Pokladní dobropis), které byly vytvořeny v rámci lázeňského řešení. Pro tyto doklady jsou vytvářeny i sestavy na míru zákazníka. Pro rychlé vyřízení a co největší komfort uživatelů se využívá funkčnosti, která umožňuje některé informace přednastavit. 

## NASTAVENÍ
### Kódy standardního prodeje
Pro fakturaci lázeňských služeb na prodejních dokladech je třeba založit Kódy standardního prodeje. Jedná se o standardní funkčnost, která byla v rámci lázeňského řešení rozšířena o možnost práce s lázeňskými službami. 
Pro využití prodeje lázeňských služeb je třeba v řádcích standardního prodeje vyplnit pole:
-	Typ = Účet
-	Typ lázeňské služby = výběr z následujících hodnot
	- 	Doplňková služba
	- 	Léčebný pobyt
	- 	Ubytování
	- 	Stravování
	- 	Služba v restauraci
	- 	Procedura
	- 	Laboratoř
	- 	Ošetřovatelská péče
	- 	Poplatek
	- 	Telefon
	- 	Wellnes služba
-	Prodejní kód – toto pole může být vyplněno dvěma způsoby:
	- 	Konkrétní hodnotou v závislosti na typu služby – tato hodnota se pak dostane do prodejního dokladu. Výběrem konkrétní služby se zároveň doplní i Číslo, Popis a účto skupiny zboží.
	- 	Prázdnou hodnotou – konkrétní služba se bude vybírat až na pokladním dokladu v závislosti na typu lázeňské služby

### Prodejní pokladní doklady
**Pokladna**  
V závislosti na používaných měnách je nutno založit standardní pokladny ve Správě financí – Pokladna.

**Pokladny pro prodejní doklady**  
Tento číselník slouží k propojení číselné řady s prodejní pokladnou v různých měnách. Číselná řada by měla mít nastaveno výchozí číslování a vyplněnou příslušnou skupinu dokladů, aby se pro prodejní pokladní doklady a prodejní pokladní dobropisy daly přednastavit některé hodnoty (viz. Výchozí hodnoty dokladů). Zároveň musí mít číselná řada definované návaznosti a vztahy.

**Kódy dle počítače**  
Tento číselník slouží k propojení číselné řady pro prodejní pokladní doklady a prodejní pokladní dobropisy s konkrétním počítačem, který je reprezentován jménem počítače. To umožní uživateli založit prodejní pokladní doklad v definované číselné řadě na základě jeho počítače a nemusí vybírat číselnou řadu ručně.

**Práva na data, Nastavení práv na data**  
Příslušnému uživateli či skupině uživatelů, který bude zodpovědný za danou pokladnu, je třeba přiřa-dit práva na data, která jsou definována v Nastavení práv na data:
-	Číselná řada – založení nové položky
-	Bank.účet/pokladna – čtení
-	Bank.účet/pokladna - účtování
-	List deníku – účtování deníku zboží
-	Lokace – účtování deníku zboží

**Výchozí hodnoty dokladů**  
Tato funkčnost umožňuje pro prodejní doklady reprezentované číselnou řadou nebo skupinou dokladů předdefinovat některé hodnoty, takže je uživatel nemusí při každém vytváření prodejního pokladního dokladu vypisovat ručně.
Na základě číselné řady se zpravidla umožňuje předdefinovat dimenze hlavičky dokladu a lokace, na základě skupiny dokladů pak výchozí zákazník, zúčtovací datum (workdate), datum dokladu (workdate), datum DPH (workdate), výchozí kód platební podmínky, výchozí kód způsobu dodávky, výchozí kód měny, výchozí kód cenové hladiny apod.
Tyto hodnoty se nastaví při vytvoření hlavičky prodejního pokladního dokladu, kde je uživatel může v případě potřeby změnit.

## POUŽITÍ
Prodej lázeňských služeb probíhá prostřednictvím **Prodejního pokladního dokladu**. Uživatel založí nový prodejní pokladní doklad. Pokud má nastavenou číselnou řadu dle počítače, výchozí hodnoty dokladů  a pokladnu pro prodejní doklady, pak se pro nový pokladní doklad automaticky přiřadí číslo z číselné řady, pokladna na základě výchozí měny, výchozí zákazník a lokace, dimenze, datumy.
Lázeňskou službu uživatel vybere pomocí funkce „Kopie std.řádků prodeje“ v řádcích pokladního dokladu. Ve formuláři Řádky standardního prodeje uživatel může vybrat jeden či více přednastavených řádků. Vybrané řádky se zkopírují do pokladního dokladu, kde uživatel případně změní množství či vybere konkrétní službu v poli „Prodejní kód“, pokud byl přednastaven pouze „Typ lázeňské služby“, bez konkrétního „Prodejního kódu“.
Další práce s pokladním dokladem probíhá standardně, zaúčtováním pokladního dokladu vzniká zápis do věcných položek, položek zákazníka, detailních položek zákazníka, DPH položek, položky bankovního účtu apod. v závislosti na skladbě pokladního dokladu. 


## <a name="see-also"></a>Viz také
[AC Lázeňské řešení](ac-spa-solution.md)