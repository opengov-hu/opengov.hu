---
title: Wintersmith
template: layout.jade
---

A legegyszerűbb alkalmazás esetén is szükség van valamiféle konfigurációs adatokra, pl. adatbáziskapcsolatok, külső szolgáltatások URL-je stb... Egy kormányzati szoftverrendszer nagy valószínűséggel több alkalmazásból fog állni, ezenkívül több külső rendszerkapcsolata is lesz, így a konfigurációmenedzsment az egyik legfontosabb alappillére a fejlesztésnek. Jól működő konfigurációmenedzsment nélkül nem lehet robusztus, jól skálázható és hordozható rendszereket építeni.

## Eszközök

A konfigurációmenedzsment eszközök (tool-ok) segítségével tudjuk egy rendszer konfigurációját és függőségeit karbantartani. Ezeket a feladatokat házon belül készített szoftvereszközökkel is meg lehet oldani, de a gyakorlatban célszerűbb valamilyen létező, elterjedt eszközt hazsnálni.

Három példa a létező, elterjedt konfigurációmenedzsment eszközökre: [CFEngine](http://cfengine.com/), [Chef](http://www.opscode.com/chef/) and [Puppet](https://puppetlabs.com/).

### Kezeld programkódként az infrastruktúra és konfiguráció leírását

A konfiguráció menedzselésének egyik megközelítési módja, hogy a konfigurációt és a szoftver függőségeit programkódként írjuk le. Ez a megközelítés a konfigurációmenedzsment számára is elhozza a programozásnál már megszokott pozitívumokat, mint pl.:

* tesztelhetőség
* újrahasznosíthatóság
* futtatható dokumentáció
* közös és egyértelmű nyelv a terület problémáinak megfogalmazásához
 
Amint az infrastruktúra konfigurációja le van írva programkódként, úgy az egyszerűen futtatható a szervereken, hálózatokon és szoftvereken.

### Készíts hordozható build-eket

A szoftverrendszerek migrálása különböző szolgáltatók, operációs rendszerek és környezetek között nem egyszerű és igen időigényes feladat. Még kompatibilis szolgáltatók, környezetek esetén is könnyen függőség tud kialakulni egy-egy irányába, csupán a technológiai tehetetlenség miatt. 

A konfigurációmenedzsment ösztönzi, elősegíti a rendszer felépítésének és konfigurációjának mélyebb megértését, így ez megkönnyíti a szolgáltatók, operációs rendszerek és környezetek közötti migrációt. 

### A fejleszésre használt eszközök, környezetek egyezzenek meg az éles környezettel

Gyakori probléma, hogy a fejelsztői- vagy tesztkörnyezetben tökéletesen működő kód nem, vagy nem jól működik az éles környezetben. Ennek a leggyakoribb oka, hogy a fejlesztésre használt környezet konfigurációja eltér az éles környezettől. Ez lehet például eltérő verziójú vagy típusú adatbáziskezelő, alkalmazásszerver vagy egyéb szoftverkomponens. Ennek a problémának a legegyszerűbb megoldása az, ha a fejlesztői és éles környezetek konfigurációja teljesen megegyezik. 

## Miért csináljuk így

Az konfiguráció kezelésére leginkább alkalmazott megoldások gyakran manuálisak, nehézkesek, lassúak és sok a hibalehetőség bennük. Az emberek nem igazán jók sok a lépésből álló monoton feladatok megoldásában és szoftverek kézzel történő telepítése többtíz vagy többszáz szerverre meglehetősen monoton feladat.

Ha az rendszer indulásakor még kézzel is korrekt módon elvégezhető a feladat, idővel a konfiguráció és szétcsúszhat ha nincsen rendesen kézben tartva. A probléma egyik hagyományos megoldása az, hogy a konfigurációváltoztatásokat megnehezítik így korlátozva azok számát. Ha azonban agilis és rugalmas szoftverrendszert akarunk építeni, a gyors változtatás lehetősége nagyon fontos, a kézi megoldás határait nagyon hamar elérjük.

## További olvasmányok

* [Infrastructure as Code](https://speakerdeck.com/garethr/infrastructure-as-code)
* [CFEngine](http://cfengine.com/)
* [Chef](http://www.opscode.com/chef/)
* [Puppet](http://puppetlabs.com/solutions/configuration-management/)
