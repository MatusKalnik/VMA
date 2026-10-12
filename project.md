# Project: LoL Item Advisor

## 1. Aký problém riešim?

Hráči League of Legends často nevedia, ktoré itemy sú najvhodnejšie proti konkrétnemu zloženiu súperovho tímu, a preto robia menej efektívne rozhodnutia počas zápasu.

## 2. Kto sú moji používatelia?

- **Casual a začínajúci hráči:** hráči, ktorí ešte nepoznajú všetky itemy, ich efekty a vhodné situácie na ich nákup.
- **Hráči na úrovni Bronze až Platinum:** hráči, ktorí chcú zlepšiť svoje rozhodovanie pri nákupe itemov.
- **Hráči používajúci mobil počas hry na PC:** hráči, ktorí chcú rýchlo získať odporúčanie bez zdĺhavého hľadania na internete.

## 3. Ako chcem problém vyriešiť (MVP)?

Vytvorím jednoduchú iPhone aplikáciu, ktorá hráčovi odporučí vhodné itemy na základe jeho championa a zloženia súperovho tímu.

MVP bude obsahovať:

- Výber vlastného championa pomocou vyhľadávania a obrázkov.
- Výber 1 až 5 súperových championov.
- Zobrazenie základných charakteristík súperov, napríklad fyzického a magického poškodenia, crowd controlu, liečenia a odolnosti.
- Odporúčanie relevantných itemov podľa zvoleného zloženia tímu.
- Krátke vysvetlenie, prečo je každý item vhodný.
- Zobrazenie názvov, ikon a základných informácií o championoch a itemoch.
- Jednoduché a rýchle používateľské rozhranie vhodné na používanie počas hry.

Odporúčania budú vychádzať z vlastných pravidiel uložených v JSON súbore. Informácie o championoch a itemoch budú získavané z Riot Data Dragon.

## 4. Čo v MVP nebude (Non-goals) a prečo?

- **Rozpoznávanie championov z obrázka alebo screenshotu:** vyžaduje ďalšiu technickú implementáciu. Ručný výber postačuje na overenie základnej myšlienky.
- **Hlasové ovládanie a Siri Shortcuts:** nie sú potrebné na fungovanie hlavnej funkcie.
- **Widgety a Live Activities:** predstavujú dodatočnú prácu a nie sú nevyhnutné pre prvú verziu.
- **Push notifikácie o patchoch:** vyžadujú ďalšiu infraštruktúru a nie sú súčasťou hlavného účelu aplikácie.
- **Live dáta zo zápasu a štatistiky win rate:** vyžadujú samostatný dátový zdroj alebo integráciu a rozširujú rozsah projektu.
- **Používateľské účty a cloud synchronizácia:** aplikácia bude fungovať bez registrácie a backendu.
- **Android verzia:** prvá verzia bude určená iba pre iPhone.
- **Automatické generovanie buildov pomocou AI:** odporúčania budú založené na definovaných pravidlách, nie na generatívnej AI.

## 5. Aké technológie potrebujem?

### Vývoj aplikácie
- **Swift:** programovací jazyk pre logiku aplikácie.
- **SwiftUI:** tvorba natívneho používateľského rozhrania pre iPhone.

### Dáta
- **Riot Data Dragon:** zdroj informácií a obrázkov championov a itemov.
- **JSON:** formát na uloženie vlastných pravidiel a odporúčaní pre jednotlivé situácie.

### Lokálne úložisko
- **UserDefaults:** na jednoduché používateľské nastavenia, napríklad obľúbené voľby.
- **SwiftData:** až v prípade, že bude potrebné ukladať a spravovať väčšie množstvo lokálnych údajov, napríklad vlastné buildy.

### Ďalšie nástroje
- **Xcode:** vývoj, testovanie a zostavenie iPhone aplikácie.
- **Git:** verzovanie zdrojového kódu.

### Architektúra
Aplikácia bude v MVP fungovať bez vlastného backendu. Dáta o championoch a itemoch sa načítajú z Riot Data Dragon a odporúčacie pravidlá budú uložené lokálne v aplikácii.

## 6. Cieľ MVP

Cieľom MVP je overiť, či hráči dokážu pomocou jednoduchej mobilnej aplikácie rýchlejšie nájsť vhodné itemy proti konkrétnemu zloženiu súperovho tímu a či im vysvetlenie odporúčaní pomáha pri rozhodovaní.

Úspech MVP bude znamenať, že používateľ dokáže vybrať svojho championa, zadať súperov tím a získať zrozumiteľné odporúčania bez zbytočných krokov.