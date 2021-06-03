---
    title: "Evidence návrhů na lázeňskou péči"
    author: AutoCont
    ms.date: 04/30/2018
    ms.topic: article
    ms.prod: dynamics-nav-2017
    ms.contentlocale: cs-cz
    ms.lasthandoff: 04/30/2018
---

# Evidence návrhů na lázeňskou péči

Návrhy od pojišťovny mají samostatnou evidenci v podobě **Karty návrhu na lázeňskou péči**. Hlavním důvodem tohoto oddělení je, že v případě odmítnutí návrhu se tyto požadavky nedostanou do evidence pobytů. Každému návrhu pojišťovny systém přiřazuje identifikační číslo, které představuje jednoznačnou identifikaci daného návrhu v systému. Ve chvíli, kdy uživatel zadá toto číslo kdekoli v systému, použije systém automaticky informace z této evidence a zároveň si uživatel může tuto evidenci z daného místa zobrazit. 
 Pro lepší přehlednost je evidence návrhů rozdělena do několika záložek:
-	Obecné – obsahuje informace o čísle klienta a stavu návrhu
-	Vlastnosti pobytu – obsahuje informace o pobytu, pro který je návrh vystaven, jako např. kód typu klienta, kód typu pobytu, standardní a maximální počet dní léčení
-	Návrh pojišťovny – obsahuje identifikační údaje daného návrhu od pojišťovny, jako např. číslo zdravotní pojišťovny a její pobočky, identifikace externího lékaře, datum vystavení a platnosti návrhu, indikace, apod. Systém zde provádí kontrolu na povolené indikace. V případě, že se uživatel pokusí zadat indikaci, která nevyhovuje naplnění číselníku povolených indikací, tzn., že nebude splňovat podmínku správné kombinace IČLZ, typu klienta a typu pobytu, systém zobrazí chybové hlášení. Tuto záložku je třeba vyplnit vždy. Hodnota v poli Typ péče je důležitá pro dávku, která se vytváří pro zdravotní pojišťovnu. Tuto hodnotu je možno změnit i po ukončení pobytu.
-	Klient – obsahuje základní informace o klientovi
-	Rezervace - obsahuje informace nezbytné pro rezervaci ubytovacích kapacit, jako např. plánované datum příjmu a konce pobytu, kategorii ubytování, číslo pokoje
-	Pobyt – obsahuje číslo pobytu klienta, pokud je z návrhu vytvořen pobyt a výchozí kód stravovací diety
-	Odmítnutí – tato záložka se vyplňuje pouze v případě odmítnutí návrhu. Po zadání konkrétního důvodu odmítnutí se automaticky změní stav Karty návrhu pojišťovny ze stavu Požadavek na Odmítnuto. Ke zrušení odmítnutí návrhu dojde smazáním hodnoty v poli Kód důvodu odmítnutí. Tím se zároveň změní stav Karty návrhu pojišťovny zpět z Odmítnuto na Požadavek. Na této záložce je možné vybrat z číselníku Lázně lázeňské zařízení, kam bude odmítnutý návrh předán a vytisknout odmítací dopis pro klienta, ZP a cílové lázně a to buď individuálně, nebo hromadně.
-	Změna pojišťovny – tato záložka se vyplňuje pouze v případě změny pojišťovny klienta během jeho pobytu. Pokud k tomu u daného klienta dojde, na této záložce se vyplní Číslo a pobočka nové (doplňkové) pojišťovny, Počáteční datum léčení u nové pojišťovny a Typ péče doplňkové zdrav. pojišťovny.
Na Kartě pobytu klienta je třeba změnit doplňkového plátce na novou (doplňkovou) pojišťovnu a v řádcích pobytu je třeba upravit hodnoty v poli Výběr plátce. Tzn. změnit hlavního plátce na doplňkového (aby se při účtování spotřeby vytvořily položky kl. účtu už na novou pojišťovnu, tj. doplňkového plátce). V případě, že původní plátce služby nebyl hlavní, ale doplňkový, je třeba jej změnit na Klient (to se týká hlavně příspěvkové péče).
Pro klienta se pak vytiskne Individuální vyúčtování lázeňské péče pro hlavní i doplňkovou (novou) pojišťovnu pomocí funkcí Klientský účet - Vytvoř data pro ind.vyúčt.lázeňské péče – hl.poj., Vytvoř data pro ind.vyúčt.lázeňské péče – doplň.poj. Návrh souhrnného vyúčtování pro pojišťovny bude tvořen pro hlavní i doplňkovou pojišťovnu. Uživatelsky se to neliší.

Přímo z karty návrhu lze vytvořit předběžnou rezervaci ubytovacích kapacit (bez existence pobytu) pro klienta, případně i jeho průvodce pomocí funkce **„Vytvoř předběžnou rezervaci“**. 
Pro vytvoření rezervace je třeba vyplnit: 
-	číslo klienta (na kartě klienta je třeba mít vyplněno pohlaví)
-	kód LD
-	kód typu klienta
-	kód typu pobytu
-	zaškrtnout pole S ubytováním (popř. S průvodcem)
-	kód kategorie ubytování
-	plánovaný termín pobytu

Předběžnou rezervaci z návrhu pojišťovny je možné vytvářet pouze ve stavu Požadavek, pokud ještě neexistuje pobyt nebo není zaškrtnuto pole „Předběžná rezervace“. 
Předběžnou rezervaci je možné  zrušit funkcí Zruš předběžnou rezervaci.
Pokud je návrh pojišťovnou potvrzen, stačí vytvořit pobyt pomocí funkce **„Vytvoř pobyt“**. Rezervaci z návrhu není třeba rušit (zruší se rezervací pobytu nebo příjmem z Karty pobytu klienta).
Pokud k návrhu již existuje pobyt, je možné použít funkce v pásu karet:
-	**„Otevři kartu pobytu“** – otevře kartu pobytu klienta z jeho návrhu na lázeňskou péči
-	**„Rezervuj pobyt“** – zarezervuje ubytovací kapacity pobytu klienta a změní stav pobytu klienta z „Požadavek“ na „Rezervace“
-	**„Zruš rezervaci pobytu“** – uvolní ubytovací kapacity pobytu klienta a změní stav pobytu klienta z  „Rezervace“ na „Požadavek“ 



## <a name="see-also"></a>Viz také
[AC Lázeňské řešení](ac-spa-solution.md)