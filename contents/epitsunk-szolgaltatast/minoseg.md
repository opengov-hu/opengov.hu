---
title: Minőség
desc: A szoftver minőség mérése és értékelése
preface: Minden szoftver minősége döntően befolyásolja a felhasználó elégedettségét, ezért különösen fontos, hogy törekedjünk a kiváló és hibátlan termék elkészítésére.
author: Pató István <istvan.pato@gmail.com>
date: 2013-05-12 19:44
template: layout.pug
---

### Minőség
A minőség a legfontosabb a szolgáltatások építésénél. Az emberek csak akkor fogják használni a szolgáltatást, ha azt egyszerűen, és könnyen tudják igénybe venni. Minden hiba, vagy csiszolatlan megoldás nehezíti a használatot.

A minőségért nem a minőség ügyi részleg felel. Ma már sok haladó vállalatnál egész egyszerűen megszüntették az ilyen részlegeket. Hogy miért? Azért mert a minőségért mindenki felel. A minőség a folyamatba van ágyazva, ha nem jó a minőség a folyamat szakad meg. A megszakadt folyamatot elemezni kell ki kell javítani (nem a terméket kell javítani!), és újra indítani a "termelést".

### Minőség definíciója
A minőség minden csapattagnak mást jelenthet, de alapvetően a felhasználó által tapasztalt élményt jelenti a tranzakció megkezdésétől a befejezéséig. Egy jól megírt , hibátlanul működő program is lehet rossz minőségű!

A felhasználó a szolgáltatást pozitívan értékeli, ha:
1. a szolgáltatás elérhető könnyen, többféle eszközről
2. nagyon egyszerűen kezelhető a program
3. biztonságban tudja az adatait a használat közben
4. különböző körülmények között is jól látja a tartalmat (napfény, gyengénlátó, sötét szoba, mobil telefon kijelző)
5. csak azt a tartalmat látja amire szüksége van
6. ha folyamat van, akkor tudja mit csinált eddig, hol tart, és mi van még hátra
7. az alkalmazást reszponzívnak érzi
8. úgy érzi hogy megoldotta a problémáját amiért használta a szolgáltatást

### Technikai adósság (Technical Debt)
A technikai adósság fogalmát talán úgy lehetne definiálni, hogy **kompromisszumokat kötünk az alkalmazás fejlesztés közben az alkalmazás minőségére és karbantarthatóságára vonatkozóan:** sebesség, folyamatos szállíthatóság, módosíthatóság, megjelenés, stb.

Szoftvert fejleszteni lehetetlen ilyen kompromisszumok nélkül, de nagyon fontos, hogy a csapat minden tagja tisztában legyen a problémával, és törekedjen annak megoldására.

**Sok kompromisszum esetén a fejlesztés lelassul, a minőség radikálisan csökken, a szállítás lehetetlenné válik.** Ekkor szoktak projekteket leállítani, átstruktúrálni és újraindítani, ezt mindenképpen el kell kerülni.

### Tesztelés
Mindent tesztelni kell, amit lehet. A szoftvert, a telepítést, még a specifikációt is. A 2000-es évek elején a tesztelések nagy részét kézzel végezték, kézzel összeállított teszttervek alapján. **Mára azonban a tesztelők feladata megváltozott: egy modern tesztelő automatikusan futtatható teszteket ír, módosít.** Felállítja az automatikus tesztrendszert és tesztek eredménye alapján értékeli a rendszer elemeket. Míg régen egy tesztelő hetente többször ugyanazokat a teszteket végezte kézzel, gyakran órákon keresztül, ma már ezt az időt arra fordítja, hogy megírja a tesztet, amit bármikor, akár naponta többször az automatikus tesztrendszer lefuttat és kiértékel. Így minden pillanatban, minden változás után ismerjük a rendszer minőségét. Természetesen a felhasználói élmény tesztelése megmaradt az ember számára.

A teszteléssel kapcsolatban olvasd el a következő fejezeteket is:

* [Tesztelés agilis környezetben](http://www.opengov.hu/epitsunk-szolgaltatast/agilis/teszteles-agilis-kornyezetben.html)
* [Alkalmazás tesztelés](http://www.opengov.hu/epitsunk-szolgaltatast/szoftver-fejlesztes/alkalmazas-teszteles.html)
* [Átadás - átvételi teszt](http://www.opengov.hu/epitsunk-szolgaltatast/szoftver-fejlesztes/atadas-atveteli.html)
