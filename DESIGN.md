# Rolling Life – tervjegyzet

## Alapötlet
- A telefon egy kézben, vízszintesen, mint egy tálca. A szem végig a nagy képernyőn van (laptop vagy tévé).
- A játékos nem a golyót irányítja, hanem a pályát billenti. A golyó a fizika szerint gurul.
- Nem ügyességi akadálypálya, hanem **döntéseken alapuló útvesztő**: változatos, de van kiút.
- A játék semmit nem árul el előre. A játékos csak a következményekből tanul.
- Napi legfeljebb 3 élet.

## Útvesztő – szerkezet
- Csomópontok (elágazások), és köztük utak. Minden út egy próbatétel (keskenyedés, kanyar, lejtő, emelkedő stb.).
- Vannak jobb és rosszabb utak, és **csalik**: az út eleje mást ígér, mint a vége.
  - pl. széles, kényelmes kezdet zsákutcába visz, egy ijesztően keskeny út rövidítés.
- **A rossz döntés ára később derül ki**, nem azonnal.
- Vannak **zsákutcák** és **lehetetlen szakaszok**, ahonnan vissza kell fordulni.

## Visszafordulás
- Nincs gomb. Visszafordulni úgy lehet, hogy a golyót visszagurítod. Semmi nem lép ki a játék világából.
- **A lehetetlen résznek mindig van visszaútja**, és az könnyebb, mint az odaút.
- **Csendes lezárás:** néhol az út mögötted lezárul. Ez nem látványos, csak a visszaúton derül ki.
  - Indok: a látványos lezárás elárulná, hogy előre van út, vagyis hogy az akadály nem lehetetlen.
- A lezárás és a lehetetlenség **nem függ össze** (mind a négy eset létezik):
  - lezárul mögötted, és előre járható
  - lezárul mögötted, és előre lehetetlen: lásd "A rossz döntés útja" (van belőle kiút, nem csapda)
  - nyitva marad, és előre lehetetlen (aki visszafordul, jól döntött)
  - nyitva marad, és előre járható

## A rossz döntés útja (eldöntve)
- **Jó döntés:** hosszabb, de jóval könnyebb út.
- **Rossz döntés:** nehéz akadálypálya, a végén egy **lehetetlen rész**. A pálya mögötte titokban lezárul.
- A kihívás itt a **lehetetlenség elfogadása**: aki visszafordul, az nyer.
- Visszafelé: egy rövid, **közepes** akadályszakasz (nem sok).
- Közben titokban kinyílt egy **könnyű egérút** (kordonos leágazás). Ebben is vannak akadályok, de nem túl nehezek.
- Az egérút oda vezet, ahová a helyes út vezetett volna. A rossz döntés ára tehát a nehezebb út és az elvesztett életek kockázata, nem az, hogy végleg eltévedsz.

## Zsákutca (eldöntve)
- Közepesen nehéz akadályok, a végén **semmi**.
- Visszafelé ugyanazokon az akadályokon kell végigmenni, ezért a zsákutca kétszer kerül.
- Utána a játékos elindulhat a másik, helyes úton.
- Megjegyzés: visszafelé ugyanaz az akadály más próba (a lejtőből emelkedő lesz, a kanyar a másik irányba fordul). Érdemes aszimmetrikus akadályokat tenni a zsákutcákba, hogy a visszaút ne csak ismétlés legyen.

## Lezárt leágazások (kordonok)
- A pálya néhol leágazik, mint egy autópálya-kijárat, de a leágazást egy **kordon** zárja le.
- Minden kordon egyforma, ránézésre nem derül ki, melyik ér valamit.
- A kordon megállítja a golyót, nekigurulva visszapattan róla.
- A kordon mögött az út egy darabig látszik, aztán **köd**be vész.
- Fajtái:
  - **Visszafelé nyíló:** a lehetetlen rész felől visszajövet kinyílik, könnyítő visszaútként. Ez a visszafordulás rejtett jutalma. Nyitáskor a kordon leereszkedik, ez már látszhat.
  - **Csali:** nem nyílik ki.
  - Javaslat: a csalik egy része máskor, máshonnan nyíljon ki (pl. egy másik út végéről, a túloldalról). Így a zárt kordon egy kérdés, amire a pályán valahol megvan a válasz.

## Jutalmak
- Nem pont, hanem valami, ami az útra hat.
- **Plusz élet:** a jó visszafordulásért (aki időben feladja a lehetetlent).
  - Legyen felső határa (pl. legfeljebb 5), és ne vigye át a következő napra, különben a napi 3 élet elveszti a tétjét.
- **Ideiglenes minitérkép:** jó döntésért egy elágazásnál.
  - Csak a következő elágazásig mutat, és néhány másodperc után eltűnik.
  - Az ott hozott jó döntés már nem ad újabb minitérképet (nem lehet láncban végiglátni a pályát).

## Technikai teendők az útvesztőhöz
- **Forgó kamera:** a kamera most mindig "előre" (+y) néz. Visszafelé haladáskor a haladási irányba kell fordulnia. Ez az első, amit meg kell építeni.
- Elágazások a pályamotorban (a darabok már bármilyen irányba futhatnak).
- Kordon: ütközés, csendes nyitás bizonyos feltételre (pl. visszafelé érkezés).
- Csendes lezárás a golyó mögött.
- Köd a kordonok mögött.
- Élet- és jutalomrendszer, minitérkép.

## Első próba-útvesztő (javaslat)
- 1 bejárat, 3 elágazás, 1 csali, 1 zsákutca, 1 lehetetlen szakasz rejtett, kordonos visszaúttal, és a kijárat.

## Korábbi döntések (tegnap este)
- A pálya elején ajtók, kb. 10 (ennyi személyiségtípus körül van), különböző színek: lila, fekete, pasztellkék, zöld, fehér, átlátszó stb.
- Minden ajtó nyitott, a "zárt" csak látszat. Az ajtó a játékosnak fontos, nem a játéknak.
- Anyagok: fa (alap, jól irányítható), vas (nehezebb szint, nagy tehetetlenség), papír (könnyű, a szél elfújja).
  - pl. a fagolyó nekimegy egy csapdának, és vassá válik.
- Gyakorlómód: nagy tálca akadályok nélkül, korlátlanul.
- Nincs reklám. Vagy van, vagy nincs.
- A golyó mindig a képernyő közepén, a pálya mozog körülötte.

## Irányítás – a tesztek alapján beállítva
- A kéz dőlése görbe szerint megy át a tálcára: kis mozdulat finom, nagy mozdulat erős.
- Érzékenység 1–5, alap: 3 (60° kézdöntésnél 60° tálcadőlés).
- Kormányzássegéd: 0–5 a játékba (kedvcsinálónak), 6 csak pályateszthez.
- Késés: kb. 60–80 ms a mozdulat és a golyó között (30 ms simítás, 60 csomag/s).
