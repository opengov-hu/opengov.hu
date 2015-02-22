---
title: REST API
desc: REST API a szoftver infrastruktúra nyelve
preface: Az információ technológia változásával a fejlődés felgyorsult, amely nem csak az eszközökre, hanem a megoldásokra is hatással volt. A korábban nehézkes, lassú és bonyolult kommunikációs módszereket egy könnyen érthető, egyszerű és a weben natív megoldásnak számító megoldás váltotta, a REST API.
author: Pató István <istvan.pato@gmail.com>
date: 2015-02-22 18:53
state: BETA
template: layout.jade
---

### Mi volt eddig?

A 2000-es évek elején kezdett el teret hódítani az XML. Addig nem volt elterjedt egységes adatszerkezet, amelyet ember és gép egyszerűen olvashatott volna. Az XML felett megjelentek olyan rétegek, például WSDL, WS-Addressing, WS-Policy, WS-Security, SOAP, stb, amelyek próbálták formalizálni a szoftverek egymás közötti kommunikációját. A megoldások is erre épültek, a vállalatok, kormányzatok belső rendszereikben használták. Az internet széleskörű elterjedése azonban változást hozott, az alkalmazásoknak meg kellett nyílniuk a külvilág felé (internet bank, elektrónikus kormányzati ügyintézés). A nyitás folyamán a belső, megszokott módszereket vitték át a webes platformra, amely gyorsan felszínre hozta a megoldás hátrányát. A korábbi tranzakció számok megnöttek, a nyomonkövetés fontos lett a minőségi szolgáltatások biztosításában.

### Miért kellett váltani?

Az XML technológiához kapcsolódó megoldások erőforrásigényesek, nehézkesek, helyigényesek voltak. A böngészőkön natív adatszerkezet a JSON, az XML idegen számára. A mobil eszközökön nem volt mindegy, hogy 50 kybte XML vagy 15 kbyte JSON adat közlekedik, mert ennek feldolgozása 2-3x több ideig tartott és több energiába került. A szervereken a bankok és kormányzatok naplózást végeznek, amelyek az XML esetén 2-3x több tárterületet igényelnek. A feldoglozáshoz 2x annyi szerver és energia kell.

Mivel a JSON a böngészőkön natív adatszerkezet és a mérete kisebb, ugyanakkor ugyanúgy jól olvasható, mint az xml, ezért kézenfekvő volt a megoldás, hogy ez legyen az az adatszerkezet, amelyet publikus szolgáltatásoknál felhasználnak. Később felismerték ennek az adatszerkezetnek az előnyeit, így a belső rendszerek kommunikációjában is elterjedt.

A JSON adatszerkezet mellett ugyanakkor szükség volt arra a kényelemre amelyet a SOAP/WSDL/WS-* világ biztosított. Ezt a JSON elterjedésével együtt a REST API megoldás hozta el.

### Mi a REST API?

Egy állapotmentes (stateless) szoftver architektúra megoldás, ahol a meglévő webes standardokat használjuk ki az alkalmazás-alkalmazás kommunikációban a szerveren vagy kliensen tárolt objektumok állapotának átvitelére.

### XML/SOAP/WSDL/WS-* és a JSON/REST API összevetése

Amit az XML világ biztosít, azt a REST-es világ is biztosítja. Alábbiakban összeszedjük, hogy mely XML technológia mely JSON/REST technológiának felel meg.

| Technika | XML | JSON/REST |
| -------- | --- | --------- |
| Adatszerkezet | XML | JSON |
| Útválasztás | WS-Addressing | Standard, HTTP URL alapú |
| Titkosítás | WS-Security | Standard, választható megoldások |
| Bináris adat kezelése | MTOM és SOAP with Attachemnt | Standard, HTTP upload |
| Aszinkronitás | Nincs | Standard, HTTP asszinkron |
| Fejléc adatok | SOAP Header | Standard, HTTP Header |
| Üzenet küldés | SOAP Fault boritékban | Standard, HTTP response code |
| Adatméret | 100% (SOAP XML) | 25% |
| Böngésző feldolgozás | kiegészítő szoftverrel | natívan |
| Elterjedtség | közepes | nagyon magas |
| Validálás | kiegészítő szoftverrel | kiegészítő szoftverrel |
| Üzenet előállítás | kiegészítő szoftverrel | kiegészítő szoftverrel (NodeJS esetén natív) |
| Használható-e közvetlenül böngészből? | Nem | Igen |
| RPC jellegű? | Igen | Nem |
