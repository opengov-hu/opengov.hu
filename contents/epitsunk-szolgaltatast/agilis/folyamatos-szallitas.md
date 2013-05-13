---
title: Folyamatos szállítás
desc: Folyamatos termék szállítás bármikor
preface: A folyamatos szállítás (Continuous Delivery) célja hogy minél előbb, minőségi szolgáltatást adjon a felhasználónak.
author: Pató István <istvan.pato@gmail.com>
date: 2013-05-13 08:53
state: BETA
template: layout.jade
---

A [LEAN elmélet](http://en.wikipedia.org/wiki/Lean_software_development) szerint az a szoftver ami nincs használva, nem közvetít értéket, és csak veszteséget termel a karbantartása és kezelése. A folyamatos szállítás feladata az, hogy egy elkészült funkció, a megfelelő minőségben azonnal kikerülhessen használatra. Az agilis szemlélet szerint minden iteráció végén a szoftvernek olyan állapotban kell lennie, hogy az átadható legyen a felhasználók számára. Ez nem jelenti persze azt, hogy le is kell szállítani, de a képességnek meg kell lennie.

Ahhoz, hogy a folyamatos szállítás megvalósuljon szükséges, hogy a csapat rendelkezzen egy megfelelő fejlesztési lánccal, amely az igény begyűjtéstől kezdve az összes fejlesztési technológián és módszeren keresztül, az átadásig, és azon túl, a visszajelzés gyűjtését is lefedje. Ezt csak automatizálással lehet megoldani, amelynek a kulcsa konfiguráció menedzsment és fejlesztési folyamat. Ha automatizálva van a tesztelés, és a szoftver telepítése teszt és éles környezetbe, akkor a verziók kiadása, váltása unalamas eseménnyé válik. Emiatt gyakran (akár naponta többször) lehet új verziókat kiadni.

Minél előrébb tervezünk a jövőbe, annál bizonytalanabb a tervünk. Például, ha egy szoftvert 6 havonta adunk ki, akkor az első hónapban kifejlesztett funkció könnyen elavultá válhat az átadásra. Például közigazgatási alkalmazásoknál 6 hónap alatt akár jogszabályi változások is érvényteleníthetik az addigi fejlesztéseinket, ezért a szállító alapvető érdeke, hogy minél előbb átadja a terméket.

A technológia változása szintén kikényszeríti azt, hogy gyorsan és folyamatosan szállítsunk. Jelenleg a böngészők gyakran frissülnek (3 - 6 hónapos kiadások vannak), így például egy 2 éves fejlesztés esetén akár 13-14 féle böngészővel is tesztelni kell az alkalmazást. Ennyi tesztkörnyezet, ennyi féle hibajelzés: pénz és idő pocsékolás. Ha 6 hónap alatt kész a projekt, akkor 3-4 böngészővel megoldható a feladat.

### Telepítési folyamat
Mi történik a programmal onnantól kezdve, hogy a programozó megírta, addig hogy kikerül az éles rendszerbe? Erre a folyamatra úgy hivatkozunk, hogy **telepítési folyamat** (deployment pipeline).

#### A commit szakasz
Bármikor amikor a programozó elhelyezi a kódját (commit, push) a verzió követő rendszerben, automatikusan lefutnak a teszt esetek rajta. Ha itt hiba történik, akkor **gyorsan hibáztunk**, és így mód van az azonnali javításra. A programozó külső tesztelő ember nélkül, automatikusan, akár többször is tudta ellenőrizni saját munkáját, és azonnal javítani tudja azt.

#### Integrációs környezet
Mivel több programozó, vagy akár több csapat is dolgozhat egy szoftveren, ezért munkájuk integritásáról gondoskodni kell. Erre való az integrációs környezet. Ez a környezet az éles rendszerrel megegyező, így az itt jelentkező hibák ugyanúgy jelentkeznek az éles rendszeren is. Ebben a környezetben jól definiált módon, előkészített tesztadatok mentén, automatikusan futnak le az integrációs tesztek. Amennyiben itt hiba történik, akkor egy vagy több fejlesztő munkája segítségével a probléma megoldása után (Commit szakasz), a környezetben ismét lefut az integrációs teszt automatikusan. Az integrációs környezetet automatikusan, a konfiguráció menedzsment segítésgévél elkészített szoftverekkel állítjuk elő. A szoftver telepítése és a tesztelés szintén automatizált legyen. Ezzel akár minden commit szakasz után futtatható egy integrációs teszt. (Gyakorlatban nem minden kommit után célszerű, hanem csak adott időközönként.)

#### Egyéb, speciális környezetek
Más környezetben történik például a teljesítmény teszt, behatolási teszt, vagy a kézi tesztelés. Ezeknek a létéről a szoftver követelmények döntenek. Ha egy szoftverben mindig kötelező ellenőrizni a megfelelő teljesítményt, mert kritikus az alkalmazás szempontjából, akkor célszerű az intgerációs környezet mellett egy küldön, éles rendszerrel megegyező teljesítmény teszt környezetet fenntartani, amin automatikusan lefutnak a teljesítmény tesztek, ha az integrációs tesztek megfelelőek. Ugyanígy egy webes alkalmazásnál, ahol fontos a felhasználói élmény célszerű egy környezetet fenntartani a nem automatikus - kézi - teszteknek, ahol ember végzi a felhasználói élmény ellenőrzését.

#### Éles (production) környezet
Ha egy kód átment a Commit szakaszon, majd kikerült az Integrációs környezetbe és ott is megfelelt minden tesztnek, akkor potenciálisan kikerülhet az éles környezetbe. (Potenciálisan telepíthető, mert gazdasági, jogi, projekt technikai és egyéb okok megakadályozhatják a telepítést.) A telepítés az éles környezebe ugyanolyan feladat mint az integrációs környezetbe telepítés: scriptek, konfigurációk futtatása ugyanazokon az eszközökön, ugyanazzal a szoftver verzióval. Így az integrációs környezetbe telepítés és az éles környezetbe telepítés között ugyanazokat az eszközöket használjuk, ugyanazon a módon.
