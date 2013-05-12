# OpenGov.hu nyilatkozat

**Valljuk, hogy nem a termék oldja meg a problémát, hanem a megfelelő szakemberek. Nem a licenszek vásárlása, hanem az elvégzett munka, a szolgáltatás az, amely működő megoldásokat eredményez.**

## OpenGov.hu
**Nyílt kormányzati informatikai szolgáltatások kézikönyve**

Ez a GitHub tároló az OpenGov.hu tartalmát kezeli.

## Cél
Az opengov.hu célja, hogy közösségi alapokon szerveződve létrejöjjön egy olyan nyílt, a legmodernebb informatikai megoldásokat bemutató tudásbázis, amely a kormányzati informatika döntéshozói, fejlesztői részére naprakész, minőségi információforrás.

A tartalom mindenre kiterjedhet ami információ, és információ technológia, néhány példa:

- hogyan szervezzük az informatikai projekteket?
- hogyan történjen a fejlesztés?
- milyen fejelsztőeszközök ajánlottak?
- milyen tesztelési eszközök és módszerek biztosítják a minőséget?
- emberi tényezők és a fejlesztés pszichológiája

**A létrehozott tartalom egységes nyelv a döntéshozók, végrehajtók, fejlesztők között, ezzel megkönnyítve és olcsóbbá téve az informatikai fejlesztéseket.**

## OpenGov.hu és nyílt tartalom
Az OpenGov.hu kezdeményezés csak nyílt eszközökre és módszerekre épül. Alapja a magyar szoftverfejelsztők együttes, önkéntes és nyílt munkája. Támogatja a nyílt forráskódot, a szabad szoftvereket, az ingyenes termékeket és módszereket.

## OpenGov.hu várt hatása
A fenti célok megvalósulása esetén számos hatása lehet az OpenGov.hu kezdeményezésnek:

- Az átláthatóság és modern módszerek segítenek a fejlesztőknek bekapcsolódni a kormányzati informatikai fejlesztésekbe, és ezen keresztül a magasan képzett munkaerőt sikerül itthon tartani.
- Növeli a sikeres kormányzati informatikai fejlesztések számát.
- Rövidíti a fejlesztések átfutási idejét.
- Jelentősen csökkenti a költségeket.
- Átláthatóvá teszi a költségeket.
- A magyar munkaerő felhasználásával Magyarországon történő adózással javítja a nemzetgazdaság helyzetét.
- A kormányzati informatikában résztvevő szakemberek az egyéb gazdasági szereplők részére végzett munkájukkal tovább növelhetik a magyar gazdaság erejét.
- Csökkenti az informatikai fejlesztések tervezési költségeit, jelentősen csökkentve a projekt kockázatokat.

## OpenGov.hu indítói és karbantartói

### Pató István
2000 óta foglalkozik kormányzati informatikai fejlesztésekkel: architektúrák tervezése, tervezés, programozás, automatikus tesztek fejlesztése, teljesítmény tesztek, UX tervezés. Ismert fejlesztési technológiák, eszközök: Agile, Lean, Kanban and Scrum, Wiki, Java platform HTML5, Google Maps, JavaScript, CSS, jQuery, Open Source Software and Open Standard, NoSQL - MongoDB, vert.x, Ubuntu Linux, Redis, JMeter, Git and BitBucket, Mustache template engine, Jade, NodeJS, Grunt, NetBeans, Apache Maven, Twitter Bootstrap, BDD - Cucumber, JUnit, WebDriver, Chrome, Firefox, Internet "OMG" Explorer, Jenkins, Cloud - Amazon Web Service EC2 and S3, SpringFramework, JMS, SOAP WebService, Objective-C, iOS, XCODE, ...

## OpenGov.hu készítése
Az OpenGov.hu fejlesztése nyílt alkalmazásokkal történik. Az oldal tartalmát CSS, MarkDown (.md), HTML5 és JavaScript segítségével fejlesztjük. Felhasználjuk a közösségi médiát (Twitter, GitHub) a fejlesztésre és kapcsolattartásra. A felhasznált nyílt szoftverek és módszerek:
- Wintersmith https://github.com/jnordberg/wintersmith : NodeJS alapú statikus tartalom generáló eszköz az OpenGov.hu web oldalának előállításához.
- Ubuntu Linux operációs rendszer
- GIMP képszerkesztő
- Kanban
- reText MarkDown fájl szerkesztő
- Jade: template eszköz

### A weboldal generálása
1. Telepítsd a NodeJS (npm) és a Wintersmith programot.
1. Klónozd a git tárolót!
1. A létrehozott könyvtárban add ki az alábbi parancsot:
**wintersmith build**
1. A ./build könyvtárban megtalálod a kész tartalmat.

### Fejlesztés és ellenőrzés
A fejlesztéshez nem szükséges mindig kigenerálni a build könyvtárat! Egyszerűen add ki a **wintersmith preview** parancsot az opengov.hu könyvtárban, és a böngészőben a **http://localhost:8080** címen eléred az oldalt.

### Oldalak metaadatai
Az oldalakhoz kötelező a minimális metaadatokat megadni az alábbi formában:

    ---
    title: OpenGov.hu tartalma
    desc: A tartalom létrehozásának kritériumai.
    preface: Ezen az oldalon összefoglaljuk az OpenGov.hu oldalon lévő tartalmak létrehozásának, és fejlesztésének alapvető követelményeit.
    author: Pató István <istvan.pato@gmail.com>
    date: 2013-05-12 15:40
    state: BETA
    template: layout.jade
    ---

A *state* BETA, vagy LIVE értékű lehet. Először minden tartalmat BETA jelzővel adj meg, ha az adott oldal már LIVE értékű, akkor ne változtasd.

### Az oldalak megfogalmazása
Az oldalakat közvetlen stílusban fogalmazzuk meg. Nem használunk egyesszám elsőszemélyt.


