---
title: Minőség
desc: Hogyan definiáld, hogyan mérd, és hogyan tartsd fenn?
preface: Ha olyan jó minőségű szolgáltatást akarunk építeni, amit az emberek szívesen használnak, a fejlesztőcsapat minden tagjának felelősséget kell éreznie a minőség iránt. A rendszer minőségét azok határozzák meg, akik létrehozzák azt.
author: Szalai Gyula <gyszalai@gmail.com>
date: 2013-05-15 21:50
state: BETA
template: layout.jade
---

Ha a szoftvertermék minősége nem megfelelő, az minden résztvevőnek nyilvánvaló kell, hogy legyen és a projektben dolgozó minden embernek meg kell tennie a megfelelő lépéseket, hogy a minőség javuljon és a problémák megoldódjanak. 

## A minőség meghatározása

A minőség minden csapattag számára mást és mást jelent. A minőség alapvetően a szolgáltatás felhasználójának felhasználói élményét jelenti. 

Ez lehetnek például:

* \* a szolgáltatás elérhetősége a lehető legszélesebb felhasználói tábor számára a megfelelő eszközökön keresztül
* \* a felhasználói műveletek egyszerűsége
* \* a szolgáltató képessége, hogy szükség esetén minél gyorsabban segítséget nyújtson a felhasználónak
* \* a tárolt és kezelt adatok mennyisége arányban áll-e a nyújtott szolgáltatással és biztonságban vannak-e az adatok
* \* az infrastruktúra és a szoftverrendszer robusztussága
* \* a programkód megfelelően tesztelt és hibamentes-e
* \* mennyire gyorsan válaszol a rendszer nagy terhelés esetén
* \* mennyire gyorsan lehet skálázni a rendszert, hogy az előre nem tervezett mértékű forgalmat is kiszolgálja
* \* a fejlesztőcsapat képessége, hogy rövid idő alatt alkalmazkodjon a megváltozott követelményekhez és módosítson, vagy új funkciókat adjon a rendszerhez

### A technológiai adósságról

A szoftverfejlesztés kapcsán gyakran hallunk a 'technológiai adósságról' (technical debt). Sokféle definíció létezik erre a fogalomra, de általában azokat a kompromisszumos megoldásokat értjük alatta, amiket egy alkalmazás vagy rendszer fejlesztése közben alkalmazunk a szép, tiszta, bővíthető megoldások helyett azért, hogy a termék minél előbb a piacra kerüljön, vagy eljusson a felhasználóhoz.

Lehetetlen úgy szoftvert fejleszteni, hogy közben ne gyűlne össze némi technológiai adósság, de nagyon fontos, hogy a fejlesztőcsapat tisztában legyen a kompromisszumos megoldásokkal és a tagok megosszák a velük kapcsolatos információkat. A nagy mennyiségű technológiai adósság lelassítja a jövőbeni fejlesztést, viszont ha a csapatnak tiszta képe van a helyzetről, akkor az adósság ledolgozásához szükséges feladatokat a csapat folyamatosan be tudja a iktatni a fejlesztési feladatok közé, így biztosítva, hogy a jövőben is gyorsan tud menni a fejlesztés.

## Tesztelés

A megfelelő minőség eléréséhez egy sor különböző típusú tesztelést kell alkalmaznunk. Csak akkor tudod megmondani, hogy a szolgáltatás megfelel-e a fenti kritériumoknak vagy bármilyen más minőségi definíciónak, ha tesztelted a rendszert normál és extrém körülmények között.

A teszteléssel kapcsolatban olvasd el a következő fejezeteket is:

* [Tesztelés agilis környezetben](http://www.opengov.hu/epitsunk-szolgaltatast/agilis/teszteles-agilis-kornyezetben.html)
* [Alkalmazás tesztelés](http://www.opengov.hu/epitsunk-szolgaltatast/szoftver-fejlesztes/alkalmazas-teszteles.html)
* [Átadás - átvételi teszt](http://www.opengov.hu/epitsunk-szolgaltatast/szoftver-fejlesztes/atadas-atveteli.html)


## A csapaton belüli szerepek és minőségbiztosítási (QA) szakértők

Egy elektronikus szolgáltatás megfelelő minősége az egész csapat felelőssége, de a végső felelősség a **Service Manager**é. Nagyon fontos, hogy a **Service Manager** a csapattal együtt dolgozzon és megértse, hogy a megfelelő minőség biztosításához milyen lépések és teendők szükségesek.
Az ő feladatai közé tartozik az is, hogy biztosítsa, hogy a csapat már a funkciók tervezésekor szem előtt tartsa a minőséget és hogy legyen megfelelő idő és erőforrás a tesztek megírásához...

**That will include making sure that the team are considering quality when writing development stories and allowing time and resources to test what they're building, doing the groundwork to ensure that assumptions about the accessibility of a service are regularly tested, taking the time to consider failure scenarios and how they will respond, and so on.**

Ha valóban mindent lefedő tesztelést szeretnénk, időnként be kell vonni specialistákat vagy adott témakörre specifikus eszközöket, szolgáltatásokat. Például a penetrációs tesztek elvégzéséhez mindenképpen érdemes külső feleket bevonni, mert külső szemlélőként olyan hibákat és gyengeségeket is fel tudnak fedezni a rendszerben, amit a belső 
szemlélő nem vesz észre vagy nem is gondol rá.

Néhány csapat külön minőségbiztosítási szakértőt is alkalmaz. Ez azért lehet nagyon hasznos, mert így a minőségbiztosítással kapcsolatos dolgok irányítás alá kerülnek és a csapattagok is megkapják a megfelelő oktatást és erőforrásokat, hogy jobb minőségű legyen az elkészült szolgáltatás.

A minőségbiztosítási szakértő hatásköre tiszta kell hogy legyen és együtt kell dolgoznia a fejlesztőcsapattal, hogy a minőség a fejlesztés minden lépésébe beépüljön és ne csak utólag a folyamat végén legyen egy ellenőrzés. 

**We encourage teams employing a QA specialist to consider such a role a short-term responsibility with the intention that they quickly leave the team able to manage quality as part of their standard development and iteration of the service.**
