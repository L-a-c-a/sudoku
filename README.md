# Sudoku
Sudoku megoldási segédlet.
Nem oldja meg magától a feladványt, de segít meglátni dolgokat.
##### Fogalmak, szóhasználatok:
Cella,  
sor, oszlop, blokk; együttesen ház (9-es egység),  
rálát egyik cella a másikra = egy házban van vele.  
Lásd még: http://www.math.u-szeged.hu/Sudoku/sudoku.pdf  
Kitöltött = megfejtett cella: egy nagy számjegy látható benne. A nem kitöltött cellában 1..9 db apró számjegy van: ezek a:  
lehetőségek, vagy még lehetséges számok.
##### Kezelőszervek:
- Aktuális szám(ok) kijelző doboza.
- Számkijelölő gombok.
  Alapesetben egy kijelölt szám van: az, amit itt megkattintanak.
  "Többes kijelölés" módban a gomb ki-bekapcsolja a szám kijelölését.
- Rádiógombok: mi történjen egy cella megkattintásakor.
  - Be: Az aktuális kijelölt számmal kitölti a megkattintott cellát. A "Többes kijelölés" módot kikapcsolja.
  - Ki: A megkattintott cellában kitörli a lehetőségek közül a kijelölt számo(ka)t.
  - Reset: a cellát kitöltetlenné teszi és mind a kilenc szám lehetőségként belekerül.
  - Ki a többi: egy kitöltött cellára rákattintva az összes olyan cellából, amire ez a cella "rálát" (egy sorban, oszlopban, vagy blokkban ("egy házban") van vele), kitörli a lehetőségek közül a cellában levő számot. "Aut. ki a többi" módban ez a funkció automatikus.
  - Sor/Oszlop/Blokk kijelöl: Csak "Többes kijelölés" módban működnek. A megkattintott sorban/oszlopban/blokkban található még lehetséges számokat kijelöli.
- Módok:
  - Aut. ki a többi: Egy cella kitöltésekor a "Ki a többi" funkció automatikus.
  - Színezés, ahol a szám még lehetséges: Színezi azokat a cellákat, ahol a kijelölt szám(ok) lehetőségként megvan(nak).  
  Zöld: ha csak az(ok) lehetséges(ek) a cellában. (Leginkább többes kijelölésnél.)  
  Sárga: egyébként.
  - Többes kijelölés: több szám lehet egyszerre kijelölve.
- Állapotkijelző doboz. Kijelzi:
  - hogy melyik számból hány van megfejtve (kitöltve),
  - hányadik lépésnél tartunk,
  - hány visszacsinált, újracsinálható lépés van.
- Import-export mező és import gomb.
  Be lehet másolni 81 karaktert, ami lehet egy számjegy 1-től 9-ig, vagy bármi más. Amelyik cellára számjegy jut, azt kitölti az Import funkció.  
  Minden lépés után kijelződik az aktuális állapot (81 számjegy, a nem kitöltött 0), amit lehet máshová másolni (export).
- Visszacsináló (<) és újracsináló (>) gombok.
