---
title: Agilis fejlesztés jellemzői
desc: Ütemezett, átgondolt, átlátható fejlesztés.
preface: A fejlesztés időszakát részekre bontjuk (Sprint), és minden egyes részben jól meghatározott User Story-k kerülnek megvalósításra. Egyértelműen minden Sprint végén potenciálisan szállítható a termék.
author: Pató István <istvan.pato@gmail.com>
date: 2013-05-13 18:37
state: BETA
template: layout.jade
---

Új termék kifejlesztésére a <a href="http://en.wikipedia.org/wiki/Scrum_(development)">Scrum</a> az egyik legjobb módszer. Akkor alkalmazzuk, ha a fejlesztő csapat csak ezen új fejlesztésen dolgozik. Amennyiben a fejlesztő csapat más feladatot is ellát közben (más fejlesztés, vagy szupport tevékenység), úgy a Scrum csak korlátozottan alkalmazható. Ekkor célszerű a <a href="http://en.wikipedia.org/wiki/Kanban_(development)">Kanban</a> módszert alkalmazni.

Egy tipikus csapat 4-7 fő között mozog. Ha sok a feladat, akkor több 4-7 fős csapatot kell kialakítani! Az agilis fejlesztés nem működik önálló, önszervező csapat nélkül!

### Scrum

A Scrum esetén a fejlesztést a határidőig egyenlő időrészekre bontjuk, általában 1 és 4 hét között, ezeket Sprintnek hívjuk. Egy Sprintben végezzük el a feladatokat, amelyeket a Product Backlogból választunk. A Product Backlog tartalmazza a User Storykat. Minden egyes User Story egy jól megfogalmazott mondat, amely a felhasználó igényt definiálja. Naponta tart a csapat stand-up meetinget (állva történő, gyors egyeztetés) az elvégzett feladatról, az aznapi feladatokról és a felmerült akadályokról. Minden egyes Sprint a Sprint tervezésével kezdődik, és minden egyes Sprint egy élő szoftver bemutatóval végződik, ahol a csapat demonstrálja az elvégzett munkát, és bemutatja az eredményeket a megrendelőnek. Ekkor azonnali visszacsatolás jön létre a megrendelő és a szállító között 1 - 4 hetenként! A bemutató végén a megrendelővel együtt a következő Sprint előzetes tervezése megtörténik, ami alapján a csapat még egy részletesebb Sprint tervezést is végez (fejlesztési feladatok lebontása, egyeztetése). Részletes információ a [Scrum](http://www.agilelearninglabs.com/resources/scrum-introduction/) fejlesztésről.

#### Sprint
A Sprint adja a Scrum alapú fejlesztés ritmusát. A méretéről (1-4 hét) a termék fejlesztés elkezdése előtt kell dönteni, és később fixen tartani. Az első sprintben (szokták 0. sprintnek is hívni) kialakítják a fejlesztő, bemutató és tesztkörnyezeteket. Kialakítják a közös fejlesztési módszereket, és eszközöket. Előkészítik a Product Backlogot, átláthatóvá teszik a fejlesztést (táblák, hibakövető szoftver, automatikus mérő és tesztelő programok üzembe helyezése, stb).


#### Napi megbeszélés (stand-up meeting), maximum 15 perc
Csak a fejlesztők vesznek részt rajta, a Scrum Master (ő felel a Scrum szabályok betartásáért és javítja a hibákat) valamint a Product Owner (termék felelős). Ezen a találkozón 3 kérdést kell minden csapattagnak megválaszolnia: mit csináltak tegnap, mit fognak ma csinálni, és van-e őket akadályozó probléma. Az egyeztetésen csak az előbb felsorolt emberek szólalhatnak fel, de bárki megfigyelőként részt vehet (pl: megrendelő). A 15 perc nem alkalmas arra, hogy bármit megbeszéljünk. Arra alkalmas, hogy mindenkinek az ismeretét napi szinten szinkronizáljuk. Ha megbeszélendő dolog merül fel, akkor munkacsoportokba lehet egyeztetni, így megspóroljuk azon emberek idejét akik dolgoznak a projekten. [Stand-Up Meeting vagy Daily Scrum Meeting](http://www.mountaingoatsoftware.com/scrum/daily-scrum/)

#### Sprint tervezés, maximum 4 óra
A csapat ekkor dönti el, hogy mit vállalnak be a következő Sprintre. Mindig User Storykat vállalnak el, amelyeket egy mértékegység nélküli számmal jellemeznek, hogy mennyi munka szerintük. A User Storyk súlyozása relatív egymáshoz képest. A Sprint tervezés két részből áll, az egyik a súlyozás, a másik a User Storyk bevállogatása a Sprintbe.

#### Sprint bemutató, maximum 2 óra
Ekkor a csapat minden tagja jelenlétében a megrendelőnek bemutatják a futó szoftvert. Amit nem sikerült megcsinálni, azt egyeztetni kell a megrendelővel, hogy miért nem sikerült. Ezen kívül a megrendelő az észrevételeit, módosítási igényeit közölheti (újabb User Storyk születnek).

#### Retrospektív, maximum 2 óra
A Sprint bemutató után szokták tartani, a megrendelő részvétele nélkül. Ezen a fejlesztési folyamat minőségét kell növelni: megnézni mi ment jól és mi ment rosszul. Hogyan lehet a rossz dolgokat javítani, hogyan lehet a jó dolgokat fentartani, erősíteni.

#### Mérés
A Scrum előrehaladást diagramokon lehet ábrázolni, így napról napra látszik az előre haladás, illetve megbecsülhető a valós befejezési határidő. A Scrum úgynevezett Burn Down Chart megjelenítést használ, amely az összes User Story becsült pontjainak összegével indít, és minden nap a befejezett User Storyk pontjaival csökken. Ideális esetben a Sprint végére elérjük a grafikon X tengelyét. Néhány példa, amelyek különböző viselkedésű Scrum csapatokra jellemző: [Scrum Burn Down Charts](http://www.scrumdesk.com/is-it-your-burn-down-chart/)

### Kanban
A kanban használata egyszerűbb mint a Scrum, kevesebb előírást tartalmaz, ezért rugalmasabb. Alapvető követelményei: vízualizáld a folyamatot, limitád a folyamatban lévő munkát (WIP), menedzseld a folyamatodat, egyértelműek legyenek a szabályaid, legyen visszajelzésre mód, fejleszd a folyamatodat csapatban és kísérletezz. A kanban esetén a folyamatot egy kanban táblán szemléltetik. Az ezen átfolyó feladatokat mérik, és diagramon ábrázolják. Mind a tábla, mind a diagram mindenkinek azonnal és szabadon elérhető, így nem kell senkit megzavarnunk azzal hogy "Hol tartunk?", mert az egyértelmű és világos. Minden csapat magának alakítja ki a kanban táblát, csak a csapat dönthet arról nem szabad előírásba adni! A mérőszámokat a kanban definiálja, de azon kívül szabadon bevezethető egyéb is. Példa a [kanban táblára](http://en.wikipedia.org/wiki/Kanban_board)

