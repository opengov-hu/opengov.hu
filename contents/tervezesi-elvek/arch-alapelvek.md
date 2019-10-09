---
title: Architektúra tervezés
desc: Az architektúra tervezés alapkövetelményei
preface: Egy jól kitalált architektúra a megvalósítást olcsóbbá teszi, meggyorsítja a bevezetést és megbízhatóvá, karbantarthatóvá teszi a  szoftvert.
author: Pató István <istvan.pato@gmail.com>
date: 2013-05-13 08:53
template: layout.pug
---

### Szoftver architektúra

A jó szoftver architektúra egyik fő ismérve, hogy moduláris szerkezetű. A monolitikus szoftverek mindig problémát jelentenek, csökkentik a minőséget és a rendelkezésre állást. A szoftver architektúra több szinten valósítható meg:

* rendszerszinten: ekkor a különböző szoftverek egymáshoz kapcsolódását definiálja, ezt nevezzük **rendszerszintű szoftver architektúrának,**
* adott szoftver szinten: adott alkalmazás belső komponensei közötti kapcsolatot mutatja. Ennek jelentősége a monolitikus szoftverek eltűnésével jelentősen csökkent.

A továbbiakban a rendszerszintű szoftver architektúrával foglalkozunk.

### Jelentősége

Egy rosszul megírt program javítható. **Egy rosszul megtervezett szoftver architektúra alapján létrehozott rendszer javíthatatlan, mert maga a szoftver architektúra az amely hibás.** Ekkor csak a komplett architektúrális megújítás segít, amely az esetek többségében a kapcsolódó szoftverek teljes újraírásával valósítható csak meg. **Ezért a fejlesztési projektben a legfontosabb dolog a megbízható szoftver architektúra kialakítása.**

### Megbízható szoftver architektúra

A szoftver architektúra elsődleges követelménye, hogy rajta keresztül biztosítható legyen az igények kiszolgálása. Ehhez alapvetően az igényeket kell szem előtt tartani a szoftver architketúra tervezésekor. Nem szabad kompromisszumokat kötni! Minden kompromisszum, amely az igények kiszolgálásának minőségéből enged azt eredményezi, hogy a megvalósítási fázisban akár jelentősen is sérülhetnek ezek. **Általánoságban elmondható, hogy egy kicsit rossz architektúra, sokkal rosszabb szoftvert eredményez, amely automatikusan jelenti a felhasználói igények jelentős minőség romlását.** A szoftver architektúra minőségén a megvalósíthatóság, a felhasználói élmény, a használhatóság, a karbantarthatóság és az üzemeltethetőség múlik.

### Tényezők a tervezéskor

Az architektúra tervezésekor sok tényezőt figyelembe kell venni, de a legfontosabb az igények kiszolgálása. Ez nem jelenti azt, hogy a többi tényező rovására engedményeket lehet tenni. Az alábbiakat mindenképpen vegyük figyelembe:

* igények kiszolgálása
* teljesítmény
* megbízhatóság
* tranzakciós határok
* rendelkezésre állás
* üzemeltethetőség
* egyes komponensek leállásának következménye
* több példányos működés
* alapszoftverek licensz díja

### Tervezés követelményei

* **Moduláris architektúrát tervezz!** Az architekútrát mindenképpen úgy alakítsd, hogy az átalakítható legyen úgy, hogy a kapcsolódó szoftvereket ez minimálisan érintse. Az architktúrát ezért modulárisra kell tervezni.
* **Lekérdezéskor mindig szinkron műveleteket használjunk!** Ahol fontos a válaszidő, ott mindenképpen szinkron (http, websocket, socket) kapcsolatot használjunk, tipikusan ilyenek a lekérdezések. Sohase használjunk aszinkron működést, ezzel a rendszerünket védjük ugyan, de eredménye az alacsony teljesítmény, a kiszolgálás minőségének csökkenése és a jelentősen nagyobb és bonyolultabb szoftver.
* **Teljesítmény növeléshez használjunk keseket!** Gondoskodjunk a keselés tervezésekor a kes inicializálásáról és a kes invalidálásáról is.
* **Idempotens legyen a rendszer!** A rendszerünkben ismételhető legyen az üzenet úgy, hogy ha az többször is elküldésre kerül, akkor se okozzon problémát a rendszerünknek. Például egy külső fél akar karbantartó üzenetet küldeni felén, de épp nem tud, akkor később megismételhesse. Nagyon fontos, hogy nem lehetünk abban biztosak, hogy a küldő megkapta a feldolgozásunkról szóló visszajelzést, ezért fontos, hogy ugyanazt a kérést ismételve mindig ugyanazt a választ adjuk és a rendszrünkre ugyanazt a hatást gyakorolja. Természetesen ki lehet ezt váltani aszinkron működéssel, de ennek ára, hogy jelentősen csökken a teljesítmény magának az aszinkron működés elvéből fakadóan és bonyolultabb lesz a szoftver rendszerünk.
* **Pontosan állapítsuk meg a tranzakció határokat!** Például az email küldésben a tranzakció határ az SMTP szerver, nem pedig az email megérkezése a klienshez. Ugyanez igaz a nyomtatásra is: elküldtük a nyomtatónak az üzenetet, ez a tranzakciós határ.
* **Tervezzük meg a tranzakciókat!** A több szoftver komponenst érintő tranzakciót ne tekintsük egyszerűen megoldható szoftver szintű tranzakciónak (commit, 2 és 3 fázisú commit). Gondoljuk át például azt, hogy az ATM-ek esetében akár több bank is kapcsolatba kerül egymással, ahol esélytelen hogy egymás rendszerét írják. Gondolkozzunk _kompenzációs tranzakciókban is,_ ha ilyen, elosztott tranzakciót tervezünk!
* **'Immutable' (módosíthatatlan) adatkezelésben gondolkodjunk!** Tipikusan a bankok és kormányzatok használnak olyan rendszereket, ahol a rögzített adatot meg kell őrizni úgy ahogy beérkezett. Ennek régebben biztonsági okai voltak, mára azonban felismerték, hogy az ilyen adattárolással nagymértékben leegyszerűsíthető a rendszer és brutálisan növelhető a teljesítmény (például relációs adatbázisok esetén nincs update, csak insert). A karbantartás oldalon redikálisan egyszerűsödik a logika, amelynek a következménye a programhibák csökkenése (banki rendszereknél pénzben mérhető) és a karbantarthatóság növekedése. Lekérdezés oldalon a horizontális skálázás elterjedésével (például NoSQL rendszerek) a teljesítmény olcsón növelhető. A hétköznapi életben a legjobb példa a számla előállítás, amely 'módosíthatatlan' adattartalommal kell hogy rendelkezzen. Közigazgatásban a történeti adatok vagy okmányok kezelésekor használjuk ezt a megoldást.
* **Elosztott rendszert tervezz!** Még ha azt is gondolod, hogy a rendszered nem elosztott. Képzelj el egy georedundáns kialakítást, amely minden egyes helyen több példányban fut. Ha ilyen a rendszered, akkor elosztott rendszerre jellemző kérdések fognak felmerülni. Az elosztott rendszerekben a szerveren elhelyezett végpontok állapotmentesek (stateless), ez biztosítja a magas rendelkezésre állást és a dinamikus skálázhatóságot. Soha ne gondolkodj szerver oldali sessionben.
* **Ne csak asztali gépekben, de mobil rendszerekben is gondolkodj!** A mobil rendszerek sávszélessége olykor kicsi, ne legyen terjengős az adatszerkezet. Úgy tervezd meg a rendszert, hogy az natív mobil alkalmazásból, más gépi interfészről vagy akár böngészőből is ugyanazt az interfészt használja, tipikusan REST API-t szoktak ilyen céllal használni JSON adat formátummal.
* **Vedd figyelembe a terhelést!** Ha több ezer felhasználód van, akkor a régi technológiák (példul szinkron servlet hívás) olyan méretű teljesítmény igényt gerjesztenek, amely komoly beruházást igényelhetnek. Ezért néhány ezer felhasználó esetén (néhány száz kérés / másodperc) érdemes aszinkron rendszert fejleszteni (Jetty, Netty, VertX vagy NodeJS).
* **Az alapszoftvereket válaszd az architektúrához, ne fordítva!** Tipikus hiba amit el szoktak követni, hogy nem tartják be a tervezési folyamatot: igények alapján kell megtervezni az architektúrát, az architektúrához pedig ki kell választani az eszközöket. A valós életben több esetben megfigyelhető, hogy abszolút fordítva indultak el a rendszer felépítésében. Mivel a terméket kiválasztották és az igények is adottak voltak, ezért a megvalósítás lehetetlenné vált, mert a híd két oldala - az igény és eszköz - nem találkozott. Az ilyen döntések automatikusan és mindig a projekt kudarcát jelentik.
