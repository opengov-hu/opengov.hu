---
title: Rendszeres visszatekintés
desc: Hogyan és miért elemezzünk?
preface: Az agilis szoftverfejlesztés egyik központi elve a gyors visszacsatolás - amint lehet, bemutatjuk a készülő terméket a megrendelőnek, hogy lássuk, mennyire felel meg az igényeinek. A visszatekintés ugyanennek az elvnek az alkalmazása a fejlesztőcsapat munkájára, segítségével hamar ki tudjuk deríteni, hogy a fejlesztés során alkalmazott módszerek és megoldások közül mi működik és mi nem, így folyamatosan javítani tudjuk a munkamódszereinket.
author: Szalai Gyula <gyszalai@gmail.com>
date: 2013-06-01 13:10
template: layout.pug
---

## Mi a visszatekintő (retrospektív) megbeszélés

A visszatekintés egy minden [sprint](/epitsunk_szolgaltatast/agilis/agilis-fogalmak.html) végén tartott megbeszélés, ahol a csapat tagjai meg tudják beszélni, hogy mi ment jól és mi ment rosszul az adott sprintben és kitalálhatják, hogy a problémás dolgokon hogyan tudnak javítani. Nagyobb visszatekintések is lehetnek, pl. egy projekt végén a teljes projekt történéseit meg lehet beszélni.

A visszatekintés a következő lépésekből áll

* Adatok, információk összegyűjtése
* A problémák elemzése, kibontása
* A teendők eldöntése

A visszatekintés során minden csapattagnak meg kell adni a lehetőséget, hogy hozzájáruljon a fejlesztési folyamat és a termelékenység javításához.

## A visszatekintés vezetője

Minden visszatekintő megbeszélést egy vezetőnek kell felügyelnie. A vezető szerepe, hogy lehetőséget teremtsen minden résztvevőnek, hogy előadja a problémáit és a pozitív(!) hozzászólásait a többieknek. Neki kell továbbá biztosítania, hogy a megbeszélés egyben maradjon és produktív legyen, azaz ne legyen a beszélgetésből értelmetlen panaszáradat. A vezető ideális esetben egy az adott projekten kívüli személy, hogy a csapattagok közül mindenki egyformán tudjon szerepelni, de ez nem feltétlenül szükséges.

A vezető feladatai a következők:

* A visszatekintő megbeszélés megtervezése
* Az egyenlő részvétel biztosítása
* A megbeszélés egyben tartása, azaz hogy a téma ne térüljön el
* Annak biztosítása, hogy a szükséges lépésekről döntés születik és ezekhez a megfelelő csapattagok hozzá lesznek rendelve
* A megbeszélés időkeretének menedzselése, hogy a szükségesnél több idő ne menjen el

## Az alapszabályok rögzítése

Sokat segít, ha rögzítjük a megbeszélések alapszabályait, amik pl. a következők lehetnek:

* Mindenki aktívan részt vesz a megbeszélésben
* Senki nem vág a másik szavába (a vezetőt kivéve).
* Senki nem hozhat laptopot és egyéb figyelemelvonó eszközt, hogy az emberi beszélgetésen legyen a fókusz.

## A visszatekintések eredménye

A visszatekintő megbeszélések eredményeképpen ki kell derülnie, hogy mik azok a lépések, amiket meg kell tennünk ahhoz, hogy a munkamódszerünk javuljon. Ideálisan már a következő sprintben de ha lehet minél hamarabb.  

A megfogalmazott lépésekkel, teendőkkel kapcsolatos követelmények

* legyenek konkrétak, mérhetőek (pl. 'írjunk 10 unit tesztet az XY modulhoz' vagy 'állítsunk össze egy új tesztkörnyezetet az alkalmazáshoz'). Az 'írjunk több unit tesztet' vagy 'jobban figyeljünk a minőségre' nem elég konkrét.
* legyen konkrét határidejük
* legyen konkrét felelőse, az ne a 'csapat' legyen
* ne olyan személy legyen a felelős, aki nincsen jelen

A következő visszatekintő megbeszéléseken vissza kell ellenőrizni, hogy a feladatokat a felelősök elvégezték-e. Ha többször előfordul, hogy elvégzetlenül marad néhány, lehetséges, hogy túl sok a feladat.

## Visszatekintő megbeszélés vázlat

A következőkben egy 8-10 fős csapat lehetséges megbeszélésvázlatát nézzük meg, ami egy kéthetes sprintet fed le.

A megbeszélésen minden pont időkorlátos és a vezető felelőssége, hogy ez be is legyen tartva. Az adott csapatmérethez és sprinthosszhoz 90 perc egy elfogadható időtartam. Praktikus a megbeszélés tervébe beépíteni egy 10%-os csúszóidőt, amit az egyes pontok között lehet mozgatni így biztosítva, hogy nem futunk ki az időből.

### 00:00 – 00:05 (5 perc) Az alapok megteremtése

Ismertesd a megbeszélés témáját és ha szükséges célját. Ha a résztvevők nem ismerik egymást és/vagy szégyenlősek, a résztvevők rövid bemutatása nem árt.

### 00:05 - 00:10 (5 perc) Teendők, feladatok az előző visszatekintő megbeszélésről

Ellenőrizzétek, hogy a megbeszélt teendőket, feladatokat a felelősök elvégezték. Ha nem, derítsétek ki, hogy miért nem. Jelöljetek ki új határidőt, ha szükséges, bár a feladatok tologatása nem célszerű.

### 00:10 - 00:20 (10 perc) Ami jó volt

Adj a csapattagoknak 10 percet, hogy felírjanak minden olyan dolgot egy-egy cetlire, ami az elmúlt két hétben (az előző visszatekintő óta) jól működött, jól sikerült. Ha lényeges a névtelenség, ahhoz hogy mindenki bátran leírja a dolgokat, akkor a végén szedd össze a cetliket és tedd ki őket a falra. Ha nem lényeges a névtelenség, akkor a csapattagok is kitehetik őket, esetleg néhány szóban el is mondhatják, hogy mire gondoltak. Arra viszont figyelj, hogy most még ne alakuljon ki beszélgetés, vita – ezen a ponton egyelőre csak az információkat kell begyűjteni.

### 00:20 - 00:30 (10 perc) Megbeszélés

Csoportosítsátok a cetliket témák szerint és beszéljetek meg minden fő területet. Ha túl sok lenne, állítsatok fel fontossági sorrendet pl. szavazással.

Mi az ami jól ment és így kellene folytatnunk? Miért mentek ezek a dolgok jól és mit tanulhatunk belőle? Vannak olyan dolgok, amiket továbbra is tudunk alkalmazni?

### 00:30 - 00:45 (15 perc) Ami rossz volt

Adj a csapatnak kb. 15 percet, hogy felírhassanak egy-egy cetlire olyan dolgokat, amik nem mentek jól az elmúlt két hétben.

### 00:45 - 01:05 (20 perc) Megbeszélés

Ismét csoportosítsátok a cetliket témák szerint, szükség szerint állítsatok fel fontossági sorrendet és beszéljétek meg a fő területeket.

Ki tudjuk találni, hogy miért mentek ezek a dolgok rosszul? Ki tudjuk találni, hogy mit kell tennünk ahhoz, hogy a dolgok javuljanak? Meg tudjuk akadályozni, hogy bizonyos dolgok újra megtörténjenek? Ki tudunk jelölni teendőket, amit a jelenlevők közül valaki elvállal és ezzel javul a helyzet?

### 01:05 - 01:20 (15 perc) Teendők

Nézzétek át az előző pontokban azonosított teendőket, lépéseket, rendeljétek hozzá egy-egy jelenlevő csapattaghoz és adjatok ezeknek reális határidőt.

A visszatekintő megbeszélés teljes hossza 80 perc 10% csúszóidővel. A megbeszélést a tervezett idő előtt be lehet fejezni, ha mindenki elmondta, amit akart, viszont az időkeretet nem szabad túllépni. Ha túl sok a megbeszélnivaló, akkor a témákat fontossági sorrendbe kell állítani és esetleg a következő megbeszéléseken időt kell nekik szorítani.

##Miért csináljuk így?

Azzal, hogy rendszeresen visszatekintő megbeszéléseket tartunk, elérhetjük, hogy a munkamódszerünket folyamatosan, apró lépésekkel mindig jobbá tudjuk tenni. Ideális esetben a problémákat még az előtt észre tudjuk venni, hogy komoly gondot okoznának. Meg tudjuk találni azokat a munkamódszereket, amik hatékonyabbá, produktívabbá vagy legalábbis boldogabbá tesznek minket.
Az agilis munkamódszerek segítségével a munkánkat jobban tudjuk végezni, a visszatekintések pedig segítenek a folyamatok, módszerek finomhangolásában.

##További olvasmányok

Az 'Agile Retrospective Wiki' tartalmaz néhány nagyon hasznos bejegyzést, pl.
[különböző típusú visszatekintő megbeszélésekhez terveket](http://retrospectivewiki.org/index.php?title=Retrospective_Plans)

Egy nagyon hasznos könyv: [Agile Retrospectives: Making Good Teams Great](http://pragprog.com/book/dlret/agile-retrospectives).
