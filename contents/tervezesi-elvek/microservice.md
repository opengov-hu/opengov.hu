---
title: Microservice
desc: Jobb architektúrák - microservice
preface: A kétezres évek közepére jellemző monolitikus rendszeket a microservice alapú architektúrák váltották (váltják) le.
author: Pató István <istvan.pato@gmail.com>
date: 2013-05-13 08:53
template: layout.pug
---

### Monolitikus rendszerek

Aki nagyvállalati vagy kormányzati rendszerekkel foglalkozott az elmúlt években, biztosan találkozott még olyan termékfüggő, monolitikus, egyedi szaktudást igénylő, licenc díjas rendszerekkel, amelyek karbantartása jelentős összegekbe kerül, ugyanakkor teljesítményük a mai szemmel nézve (néhány 10 vagy talán 100 kérés / másodperc) alacsony. Ezeknek a hagyományos, monolitikus rendszereknek - például ESB, vagy alkalmazás szerverek -, a térhódítása a 2000-es évek elején indult meg. A 2000-es évek közepére széles körben elterjedtek és ennek köszönhetően széles körben ismerté váltak a problémáik is. **Nyílvánvalóvá vált, hogy a monolitikus rendszerek képtelenek megoldani a nagy terhelésű és elosztott rendszerek problémáját.** Tömegesen elkezdtek terjedni a microservice alapú megoldások, amelyek nem igényeltek alkalmazás szervereket, nem függtek beszállítói termékektől. A microservice architktúrának nem volt nagy reklámja - hiszen az egy architektúrális megoldás, szemlélet - annál inkább az ezt támogató infrastruktúrának a Cloud-nak.

### Hol tartunk most

Jelenleg a közigazgatásban sok helyen találkozni még központosított, monolitikus architektúrákkal. Gyakran a központosítást egy termék jelentette, például egy ESB alapszoftver vagy egy alkalmazás szerver. Ahol a nagyobb teljesítmény szükséges volt, ott ezeket a rendszereket ki kellett váltani microservice alapú architektúrákkal. Tarthatatlanná vált az az állapot, hogy teljesítmény és rendelkezésre állási okokból, **egy alkalmazás - egy alkalmazás szerver licencdíj** 'architektúra' működjön. Ha az alkalmazás teljesítményét növelni akarták, akkor vagy a meglévő szervert cserélték nagyobb teljesítményűre, vagy újabb szervert állítottak be. Az alkalmazás szerverek processzormagonkénti licencdíja viszont jelentős kiadást jelent. **2015 óta jelentős fordulat állt be a magyar közigazgatási informatika rendszerek tervezési szemléletében: igényként jelent meg a microservice alapú rendszertervezés.**

### Hová tartunk

**Ahol lehet az alkalmazás szerverek és az ESB rendszerek régi, több mint 15 éves hegemóniáját a microservice architektúrák váltják ki.** A folyamat lassú, de tekintettel az ilyen régi rendszerek üzemeltetési költségére nem gazdasági okok állnak a háttérben, sokkal inkább erőforrás rendelkezésre állási gondok. A microservice architektúrák előnyei:

* egyszerű, áttekinthető üzemeltetés
* egyszerűbb, áttekinthető fejlesztés
* moduláris jellegű architektúra
* olcsó, horizontális skálázhatóság
* gyorsabb szoftver
* rövidebb bevezetési idő
* részletekben bevezethető rendszer
* több a képzett munkaerő
* beszállító független
* egyszerűbb és hibamentesebb szoftver (nincs alkalmazásszerver, vagy ESB szerver)
* ipari standardokra épül
* cloud támogatás azonnal biztosított
* önállóan verziózható szoftver komponensek
* párhuzamosítható fejlesztések
* áttekinthető projekt, kisebb költség: kisebb kockázat

### De mi is az a microservice?

A Google, Youtube, PayPal informatikai rendszerében nincsenek alkalmazás szerverek és ESB rendszerek, a cégek mégis prosperálnak és hatalmas tömegeket szolgálnak ki. Hogyan érték ezt el? Olyan architektúrát építettek, amely szem előtt tartotta az igényeket és ehhez választottak megoldást. Ez a megoldás versenyképessé tette őket, akik nem ezt választották, azoknak ma már nem tudjuk a nevét. A megoldás a microservice alapú architektúra volt. Elosztott rendszereket hoztak létre, amelyek megbízhatóan és nagy sebességgel működnek. **A microservice architektúrában sok szoftver vesz részt, ahol a szoftverek kliensként és szerverként is működnek, egymással kommunikálnak. A kommunikációt szabványosították, az ilyen rendszerek szinte mindegyike REST API-t használ, JSON adatformátummal, ezzel biztosítva azt, hogy nem csak cégen belül egységes a kommunikáció platform, de akár más cégekkel is könnyedén kommunikál a szoftver.** Példa erre, ha a Google regisztrációnkkal akarjuk igénybe venni egy másik cég alkalmazását, vagy ha PayPal segítségével akarunk fizetni egy webáruházban. Ma már nem működne az internet REST API + JSON nélkül.

### Microservice jellemzői

* a szoftver kicsi, néhány 100 sor
* specifikáció kisebb és egyszerűbb
* interfészt valósít meg REST API + JSON segítségével
* nem konténerben fut, hanem egy paranccsal elindítható
* telepítés gyors, egy parancs
* szoftver fordítás és tesztelés gyors, egy parancs
* folyamatos szállítás (_continuous delivery_)
* egyértelmű, hogy kik fejlesztik
* olcsó
* jellemzően 2-3 fő végzi a fejlesztést és tesztelést
* horizontálisan, dinamikusan skálázható
* idempotens működésű
* moduláris felépítésű
* jól kitesztelt, biztonsági követelményeket jól biztosítja: _code review_ néhány 100 sorra elvégezhető
* nagy teljesítményt biztosít
* gyorsan elindítható, vagy leállítható
* konténerekbe szervezhető, tipikusan _docker_ alapokon
* egyértelmű felelősség elhatárolás a komponensek között
* a az alkalmazás fejlesztés elkezdése és átadása között csupán hetek telnek el
* a lehető legalacsonyabb a fejlesztési kockázat
* automatizál üzemeltetési megoldásokat tartalmaz

### Hogyan használjuk?

**A microservice egy rendszer tervezési stílus.** Ne csak az alkalmazásban gondolkodjunk, hanem a megrendelőnk látens igényei szerint is: a megrendelőnek előny, ha más alkalmazásaival könnyedén össze tudja kötni az általunk szállított alkalmazást. Már a koncepció kialakításakor a microservice mentén gondolkodjunk. Az architektúránk minden pontján tükrözze ezt a megközelítést. Amikor a specifikációkat készítjük, kisebb anyagot kell írni, de mindig tartsuk szem előtt, hogy kommunikációk zajlanak a szoftver komponensek között. A tesztelés sokkal egyszerűbb és fókuszáltabb, emiatt jobb a program minősége. Az üzemeltetés átlátható és automatizálható.
