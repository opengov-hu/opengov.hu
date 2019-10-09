---
title: Tesztelés agilis környeztben
desc: Amit tesztelsz, az lesz a szolgáltatás
preface: Elsősorban a legfontosabb dolog, hogy felismerjük, hogy miért tesztelünk. Leggyakoribb hiba, ha arra fókuszálunk, hogy ellenőrizzük a terméket.
author: Pató István <istvan.pato@gmail.com>
date: 2013-05-20 17:11
template: layout.pug
---

Az agilis fejlesztés legfontosabb része a minőség. A tesztelést ehhez kell igazítani. Leggyakoribb hiba, hogy ha fókuszálunk, hogy ellenőrizzük a terméket. A minőség ettől több, annak a termék fejlesztés folyamatába kell épülnie.

### Építsd be a minőséget

Nem lehet a minőséget a végén tesztelni. Az erőnket arra kell fordítani, hogy a minőséget minden munkafolyamatban biztosítsuk. Például a specifikációk készítésénél gyakran látjuk, hogy semmilyen minőségellenőrzés nincs beépítve. A specifikációk nagy része leírja, hogy hogyan néz ki a rendszer, és mit kell tudni. **Akár több száz oldal specifikáció is születik anélkül, hogy egy mondat is elhangzana arról, hogy az adott funckió esetén mit is jelent a 'kész' szó.** A specifikációk nem tartalmaznak **átvételi feltétel listát és a tételekhez tartozó elfogadási feltételeket** sem. Pedig, mint tudjuk, a termék validálásának egyik módja, hogy a specifikációnak megfelel-e.

### Mindenki felelős a minőségért

A szolgáltatás minősége nem csak tesztelési kérdés. **A szoftver minősége a fejlesztő csapattól függ, minden egyes embertől.** Ha egy hiba felmerül, akkor nem csak a hibát (tünet), hanem az azt okozó problémát is meg kell oldalni, ebben viszont mindenki érdekelt.

### Gyors visszajelzés

Az agilis fejlesztés a gyors információ cserére épül. A tesztelésnek a gyors visszajelzést kell támogatnia. Az agilis tesztelési módszerek használatok, különösen kell erre ügyelni.

### A tesztelés módja a termékfejlesztés egyik eredménye

Mindig lesz újabb funkció, és újabb termék. Minden egyes termék tesztelése hozzá kell járuljon ahhoz, hogy a tesztelési módszerünk fejlődjön. Ügyelni kell arra, hogy a tesztelést automatizáljuk. A megírt tesztkódokat a lehető legjobb minőségben készítsük, hiszen ezektől függ az alkalmazásunk minősége.

### A gyors szállíthatóság a termékkel szembeni egyik követelmény

Minél később szállítunk, annál nagyobb lehet a veszteség. Gondoljunk bele, ha a szoftver konkrét bevételt termel, akkor minden egyes hónap amíg ez nem történik meg, veszteséget jelent: pénzben, értékben kifejezhető veszteség. Ezért nagyon fontos, hogy a terméket minél előbb szállítsuk. A tesztelés és annak automatizálása biztosítja azt, hogy bármikor tudjuk ellenőrizni a terméket, akár naponta többször is, így megfelelő eredmény esetén bármikor tudjuk a terméket szállítani. **A tesztelésnek olyan eszköznek kell lennie, amely biztosítja a lehető leggyorsabb, reprodukálható ellenőrzését a terméknek, a gyors szállítás céljából.**

### Tiszta és átlátható tesztelés

Mindenkinek értenie kell a minőségi folyamatokat, így a tesztelést is. Tudnia kell, hogy mit várhat tőle, illetve mit kell beleadnia saját részéről.

### Értékteremtés

A jól végzett tesztelés megerősíti a fejlesztési irányt: eredménye segít átgondolt döntést hozni, és segít elkerülni a kritikus helyzeteket (tűzoltás). Segít megérteni a rendszer komplexitását és összefüggéseit, így könnyebbé teszi a döntések meghozatalát.

### Tesztelés típusok

A legfontosabb jellemzője az agilis tesztelésnek a **tesztek automatizálása.** Ezek a tesztek egy automatizált integrációs tesztkörnyezetben (_Continuous Integration CI_) futnak le, és **ugyanúgy részei a tesztprogramok a szállítandó szoftvernek, mint maga a program.** Az automatizált tesztelés lényege, hogy bármikor reprodukálható, és elindítható, így **minden egyes programkód változtatáskor lefut a komplett tesztelés automatikusan**, így azonnal megtörténik a fejlesztő felé a visszajelzés. Ezért a hiba azonnal javítható, nem telnek el napok a fejlesztés és a hiba felismerése között. Ennek köszönhetően a fejlesztés felgyorsul, és **a hiba a lehető legkisebb veszteséget okozza.**

#### Programkód tesztelés

Részletes leírás a [Programkód tesztelés](/epitsunk-szolgaltatast/szoftver-fejlesztes/programkod-teszteles.html) részben.

#### Kézi tesztelés (Exploratory Testing)

Ezt a fogalmat az előre megírt tesztelés eset nélkül végzett, a felhasználó intuíciójára és képességeire alapozott tesztelésre szokták használni. Ennek a tesztelésnek mindig van célja, és nem jelenti azt hogy a tesztelő nem készül fel rá. Értenie kell az üzleti logikát, a tesztelés célját, és ki kell találnia, hogy hogyan végzi el azt, és hogyan értékel. A megfelelő tesztadatok előkészítésével egy adott állapotba hozza a rendszert, amelyen aztán elvégzi a tesztelést, és az eredményét elemzi és értékeli. Az ilyen teszteket a tesztelők végzik.

**Amennyiben hiba van és az reprodukálható, akkor a hibát automatizáljuk: megírjuk az automatikus tesztet hozzá, és azzal is reprodukáljuk a hibát. Így az automatikus teszt rendszerünkben minden egyes teszteléskor jelezve lesz ez a hiba mindaddig, amíg a fejlesztők ki nem javítják.**

#### Teljesítmény és terhelés tesztek

Részletes leírás a [Teljesítmény és terhelés tesztek](/epitsunk-szolgaltatast/uzemeltetes/teljesitmeny-es-terheles-tesztek.md)

#### Behatolási tesztek

Részletes leírás a [Teljesítmény és terhelés tesztek](/epitsunk-szolgaltatast/uzemeltetes/behatolasi-tesztek.md)

#### Felhasználhatósági teszt

A felhasználói felülettel rendelkező szoftver esetén fontos tesztelni, hogy különböző felhasználási körülmények és változatos felhasználói körök esetén mennyire használható a szoftver. Ilyen esetek: gyengénlátóknak, vagy vakok esetén is működjön a felület, vagy különböző méretű kijelzők esetén is használható legyen az alkalmazás, vagy megváltozott fényviszonyok mellett is látható legyen (pl: tablet napfényben) a tartalom.

#### Tömegekre bízott tesztelés

Gyakran a felhasználás közben derülnek ki a hibák, például XY böngészőben a tartalom nem jelenik meg jól. Mint fejlesztők, korlátozott erőforrásokkal rendelkezünk, így nem tudunk minden platformon, mindent letesztelni. Ezért fontos, hogy a tömegek által végzett felhasználás közben tapasztalt hibákról visszajelzést kapjunk. Ezeket a visszajelzéseket gyorsan kapjuk meg és lehetőleg szűrt, osztályozott formában, így gyorsan fel tudjuk használni és beépíteni a termékbe. Ezt a tesztelést általában a cégen belül, vagy a megrendelő oldali felhasználók egy szűkebb körével érdemes elvégeztetni. Ilyenkor szokták a szoftver jelzés mellé a BETA jelzést feltüntetni, jelezve, hogy még fejlesztés alatt áll a szoftver és nem a végleges kiadást használja a felhasználó.
