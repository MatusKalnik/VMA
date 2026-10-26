# ACCEPTANCE.md

## 1. Výber šampiónov

### AC-1.1 Vyhľadanie vlastného šampióna
- Používateľ môže vyhľadať šampióna podľa jeho mena.
- Po zadaní názvu sa zobrazia zodpovedajúce výsledky.
- Po výbere šampióna sa jeho meno a ikona zobrazia v sekcii vlastného šampióna.
- Ak vyhľadávaniu nezodpovedá žiadny šampión, aplikácia zobrazí informáciu, že sa nenašli žiadne výsledky.

### AC-1.2 Výber nepriateľských šampiónov
- Používateľ môže vybrať minimálne jedného a maximálne päť nepriateľských šampiónov.
- Každý vybraný nepriateľský šampión sa zobrazí v zozname s menom a ikonou.
- Ten istý nepriateľský šampión nemožno pridať do zoznamu viackrát.
- Po dosiahnutí limitu piatich nepriateľov aplikácia neumožní pridať ďalšieho.
- Používateľ môže jednotlivého nepriateľa odstrániť zo zoznamu.
- Používateľ môže odstrániť všetkých vybraných nepriateľov naraz.

## 2. Analýza nepriateľského tímu

### AC-2.1 Fyzické a magické poškodenie
- Po výbere nepriateľských šampiónov aplikácia zobrazí odhad zastúpenia fyzického a magického poškodenia.
- Zobrazené percentá fyzického a magického poškodenia spolu dávajú 100 %, ak sú dostupné všetky potrebné údaje.
- Ak údaje potrebné na analýzu chýbajú, aplikácia na to používateľa upozorní a nebude chýbajúce údaje automaticky považovať za nulové poškodenie.

### AC-2.2 Hrozby nepriateľského tímu
- Aplikácia zobrazí indikátory relevantných hrozieb, ako sú kontrola davu (CC), liečenie a odolnosť alebo tankovosť.
- Každý indikátor vychádza z definovaných údajov o vybraných nepriateľských šampiónoch.
- Ak pre určitú hrozbu nie sú dostupné dostatočné údaje, aplikácia označí výsledok ako neznámy namiesto toho, aby tvrdila, že hrozba neexistuje.

## 3. Odporúčanie predmetov

### AC-3.1 Generovanie odporúčaní
- Po výbere vlastného šampióna a aspoň jedného nepriateľa aplikácia zobrazí odporúčané predmety, ak existujú zodpovedajúce pravidlá.
- Odporúčania zohľadňujú vybraného vlastného šampióna aj zloženie nepriateľského tímu.
- Každý odporúčaný predmet obsahuje názov, ikonu, cenu a vysvetlenie, prečo bol odporučený.
- Každý odporúčaný predmet je zaradený do kategórie začiatočných, základných alebo situačných predmetov.
- Ak neexistuje žiadny vhodný predmet, aplikácia zobrazí zrozumiteľnú správu namiesto prázdnej alebo chybovej obrazovky.
- Aplikácia nezobrazí predmet, ktorý nemá platný identifikátor v načítaných údajoch o predmetoch.

### AC-3.2 Zmena odporúčaní
- Po zmene vlastného šampióna alebo zoznamu nepriateľov aplikácia aktualizuje analýzu aj odporúčané predmety.
- Odporúčania zodpovedajú aktuálnemu výberu šampiónov a nezobrazujú výsledky predchádzajúceho výberu.

## 4. Odporúčanie counterpickov

### AC-4.1 Návrhy šampiónov
- Aplikácia zobrazí najviac päť odporúčaných counterpickov na základe vybraných nepriateľov a dostupných pravidiel.
- Každý odporúčaný šampión má názov a vysvetlenie, prečo môže byť vhodný proti vybranému tímu.
- Aplikácia zobrazí iba šampiónov, ktorí existujú v načítaných údajoch.
- Ak nie je možné nájsť žiadny vhodný counterpick, aplikácia zobrazí informáciu, že nie sú dostupné žiadne odporúčania.

## 5. Ukladanie a zdieľanie buildov

### AC-5.1 Ukladanie buildov
- Používateľ môže uložiť aktuálny výber šampiónov a súvisiace údaje buildu pod zvoleným názvom.
- Po uložení sa build zobrazí v zozname uložených buildov.
- Uložený build zostane dostupný po obnovení stránky v tom istom prehliadači a používateľskom profile, pokiaľ nebol vymazaný alebo vymazané údaje prehliadača.
- Používateľ môže uložený build premenovať.
- Používateľ môže uložený build odstrániť.
- Po odstránení sa build už nezobrazí v zozname uložených buildov.

### AC-5.2 Zdieľanie buildov
- Používateľ môže vytvoriť URL adresu, ktorá obsahuje údaje potrebné na obnovenie zdieľaného výberu.
- Po otvorení platnej zdieľanej URL aplikácia obnoví vlastného šampióna a nepriateľských šampiónov.
- Po obnovení výberu aplikácia vypočíta odporúčania podľa aktuálne dostupných pravidiel a údajov.
- Ak URL obsahuje neplatné alebo neznáme identifikátory, aplikácia ich bezpečne odmietne a zobrazí zrozumiteľnú správu.
- Zdieľaný build možno otvoriť aj v inom prehliadači bez prístupu k lokálne uloženým buildom pôvodného používateľa.

## 6. Mobilné a desktopové zobrazenie

### AC-6.1 Responzívne rozhranie
- Aplikácia je použiteľná na mobilnom zariadení aj na počítači.
- Pri šírke obrazovky 320 CSS pixelov možno používať výber šampiónov, analýzu aj odporúčania bez horizontálneho posúvania celej stránky.
- Texty, ikony a ovládacie prvky zostávajú čitateľné a navzájom sa neprekrývajú.
- Všetky hlavné funkcie možno ovládať pomocou dotykovej obrazovky aj myši.

## 7. Offline režim a načítavanie údajov

### AC-7.1 Načítanie údajov
- Ak sú údaje zo služby Data Dragon dostupné, aplikácia načíta potrebné údaje o šampiónoch a predmetoch.
- Ak sa údaje nepodarí načítať, aplikácia zobrazí zrozumiteľnú chybovú správu.
- Chyba pri načítaní externých údajov nespôsobí neošetrené zlyhanie celej aplikácie.

### AC-7.2 Offline použitie
- Po predchádzajúcom úspešnom načítaní aplikácie sa jej uložená aplikačná časť sprístupní aj bez internetového pripojenia, ak je implementovaný a funkčný servisný worker.
- Ak sú potrebné údaje uložené v cache, aplikácia ich môže použiť aj bez internetového pripojenia.
- Ak potrebné údaje v cache nie sú, aplikácia používateľa upozorní, že daná funkcia momentálne nie je dostupná.

## 8. Všeobecné požiadavky

- Aplikáciu možno používať bez vytvorenia účtu a bez prihlásenia.
- Uložené buildy sa ukladajú lokálne v prehliadači a neodosielajú sa na vlastný backend.
- Neplatné vstupy a chýbajúce údaje nespôsobia neošetrené zlyhanie aplikácie.
- Text získaný z externých údajov sa zobrazuje bezpečne a nevykonáva sa ako HTML alebo JavaScript.
- Hlavné funkcie možno otestovať bez pripojenia k databáze alebo vlastnému backendu.

## Kedy je funkcia hotová?

Funkcia sa považuje za hotovú, keď sú splnené všetky jej príslušné akceptačné kritériá a každý z nich bol overený testom.

Kritérium sa označí ako splnené až po úspešnom overení. Akceptačné kritériá opisujú očakávané správanie aplikácie; samy osebe nepotvrdzujú, že je funkcia už implementovaná.
