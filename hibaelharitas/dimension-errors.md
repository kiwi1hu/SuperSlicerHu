# Dimenzió hibák

Ha nem elégedett a nyomatok méretpontosságával, először győződjön meg arról, hogy a **firmware** helyesen van-e konfigurálva: az **X, Y és Z** tengelyek **lépés/mm** értékeit a szíjak, csigák és csavarok alapján kell kiszámítani. Ne próbálkozzon a kalibrálással próbálgatással: ezeknek az értékeknek pontosnak kell lenniük. Használja Josef Prusa eszközét: [Kalkulátor](http://calculator.josefprusa.cz).

## Függőleges méretek

Ha a függőleges méretek nem megfelelőek \(azaz **a Z tengely mentén**\) - és a tárgy általában rövidebb a vártnál - az azt jelenti, hogy a fúvóka **túl alacsonyan** van, és ezért az első réteg túlságosan rá van nyomva a nyomtatóágyra. A probléma megoldásához növelheti a Z-stopot vagy a _Z eltolás_ opciót a SuperSlicerben.

## Vízszintes méretek

A szokásos probléma a túl kicsi lyukakkal kapcsolatos. Ez általában csak a vízszintes síkban \(XY\) lévő lyukakat érinti. Ennek több oka is lehet. Lássuk őket egyenként:

### A műanyag zsugorodása

A műanyag **hűtés hatására zsugorodik**. A különböző műanyagtípusok különböző zsugorodást mutatnak, ami a hőmérséklettől is függhet. E zsugorodás miatt az extruder által névleges átmérővel készített kör \(vagy sokszögletű\) lyukak a lehűlés után kisebbek lesznek.

### Több anyag rakódik le belül

Ha egy görbe mentén extrudál, akkor egységnyi távolságra több anyag rakódik le a homorú részen. Ez a felesleges anyag kisebbé teszi a belső sugarat. Adrian Bowyer javasolt egy \[kompenzációs algoritmust\] \([http://reprap.org/wiki/ArcCompensation](http://reprap.org/wiki/ArcCompensation)\), amelyet a SuperSlicerben megvalósítottak egy ideje, de sok felhasználó panaszkodott, hogy a lyukak túl nagyok - ezt később eltávolították, mivel a kis lyukak előnyösebbek a nagyoknál, mivel azokat meg lehet fúrni.

### A görbéket sokszögek alkotják

Az STL-fájlok csak sík háromszögekből álló hálót tartalmaznak, így a síkbeli metszeteik csak sokszög alakzatokat tartalmazhatnak. Például egy kör alakú lyukat egy sokszöggel közelíthetünk meg:

![](../.gitbook/assets/dimension-errors_001.png)

Ha az STL fájl exportálása előtt megnöveli a **szegmensek számát** a CAD-ben, az segít csökkenteni a hibát. Az OpenSCAD felhasználók használhatják a [nophead](http://hydraraptor.blogspot.it/2011/02/polyholes.html) által kifejlesztett `polyhole()` függvényt, amely kiszámítja a szegmensek optimális számát.

### A szál hajlamos lekerekíteni a sarkokat

Mivel a görbéket sokszögek alkotják, csúcsaik hegyesek. A **műanyag azonban hajlamos lekerekített sarkokat kialakítani**, ami tovább csökkenti a lyuk belső felületét.

### Z billegés

Még ha egy réteg méretpontossága helyes is, több egymásra helyezett réteg kisebbé teheti a lyukat, ha nem pontosan igazodnak egymáshoz. A mechanikai problémák okozta Z ingadozás csökkenti a lyuk méretét az egymásra helyezett rétegek belső héján.

![](../.gitbook/assets/dimension-errors_002.png)

### Szálkeresztmetszet

A gyenge és közepes minőségű szálak átmérője nem túl szabályos. Ha megmérjük az átmérőjüket egyetlen méter hosszan, gyakran sok különböző értéket találunk \(és sok gyenge minőségű szál még a keresztmetszetük sem tökéletesen kerek\). Ez a folyamatos **átmérő-változás** **szabálytalan áramlást** eredményez, és az így keletkező lyuk még mindig az összes réteg belső burkát fogja alkotni.

![](../.gitbook/assets/dimension-errors_003.png)

### Visszahatás

A holtjáték egy vagy több tengely mechanikai hibája, amely lényegében csökkenti a tényleges mozgás mértékét, amikor a motor megfordítja a forgásirányt. Ezt általában a meglazult szíjak okozzák. A mozgó ágyazású nyomtatóknál a tengely \(általában az Y-tengely\) a tehetetlenség miatt hajlamosabb a holtjátékra. Tehát **ha az X és Y méretekben eltérő hibákat kap, az a holtjáték miatt van**. Meg kell húznia a szíjat. Egyetlen szoftver sem képes ésszerűen kompenzálni egy rosszul összeszerelt nyomtatót.

### Áramlási számítások

Egyetértek, a fenti okok nem mindegyike függ a SuperSlicer-től, és ahol lehetséges, ezeket ki kell javítani **a szoftveres megoldás megkísérlése előtt**.

Ennek ellenére a SuperSlicer-ben használt áramlási matematika fontos szerepet játszik a helyes méretek meghatározásában, mivel megpróbálja megtippelni az extrudált anyag alakját és az extrudálás vastagságát a vízszintes síkban egy adott anyagmennyiség esetén. Mivel ez egy közelítés, hibával jár. Az ilyen problémák kezelésének szokásos módja az _Extrudálás szorzó_ paraméter beállítása a műanyag mennyiségének növelésére/csökkentésére, így az extrudálás vastagabbá vagy vékonyabbá válik. Ez azonban a szilárd felületeket is érinti, így nem ideális megoldás.

A pontosabb méretekhez ellenőrizze a **Először a külső kerületeket** opciót. Ha először a külső kerületeket nyomtatja ki, elkerülheti az átfedő extrudátumok okozta eltolódást. Másrészt, ha először a belső peremeket nyomtatja ki, jobban elrejti a varratokat, így ez csak Önön múlik.

Új opcióként bevezetésre került a **XY méretkompenzáció** is. Lehetővé teszi a tárgy alakjának felnagyítását/ kicsinyítését a mért hiba kompenzálása érdekében. Tegyük fel, hogy a lyukak 0,1 mm-rel kisebbek, akkor a -0,05 értéket beírhatja ebbe az opcióba, és a lyukak kompenzálásra kerülnek \(a negatív előjel a befelé zsugorodást jelenti\).

