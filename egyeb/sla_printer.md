# SLA szeletelés

## Geometriai pontosságú objektumok előállítása

A mechanikus alkatrészeket, az egymáshoz illeszkedő tárgyakat precízen kell nyomtatni. Míg az SLA 3D nyomtatók leginkább organikus formák vagy figurák nyomtatására alkalmasak, geometriai formák és összeszerelhető alkatrészek is nyomtathatók. A kulcs itt az, hogy **a támasztékokat stratégiailag a tárgy szélei mentén helyezzük el**.

Az ok egyszerű: folyékony gyantával történő nyomtatás esetén a kikeményített anyag a bevilágítás után még viszonylag puha, ami azt jelenti, hogy **a tárgy a platform mozgása során nagyon enyhén** elfordulhat. **A legtöbb gyanta hajlamos egy kicsit zsugorodni** az UV-fény által történő kikeményítés után, ami a nyomtatott tárgyon enyhén torzított éleket eredményezhet. A nyomtatott geometria fenntartásához ezért elengedhetetlen a megfelelő mennyiségű alátámasztás.

![A t&#xE1;maszt&#xE9;k meghat&#xE1;roz&#xE1;sa SLA &#xFC;zemm&#xF3;dban](../.gitbook/assets/sla_printer_001.jpg)

 _Nem organikus formák nyomtatásakor használja a kézi támaszték elhelyező eszközt, hogy vastagabb támasztékot helyezzen el a tárgy szélei mentén_.

Ne feledje azt sem, hogy amikor közvetlenül a platformra nyomtat tárgyakat, az első néhány réteg általában kialakul az úgynevezett **elefántláb** - ahogy az első néhány réteg megszilárdul, az anyag egy kicsit kitágul, és egyenetlen felületet hoz létre. Ezért **ajánlott a bázis használata**.

Mint már említettük, a nyomtatás mindig ugyanannyi időt vesz igénybe, függetlenül a nyomtatási platformon lévő objektumok számától. A teljes időt a megszilárduló rétegek száma határozza meg. Használja ezt ki: ha egy bonyolult, kényes tájolású objektummal rendelkezik, helyezzen több példányt a nyomtatási platformra, és forgassa el mindegyik objektumot más-más irányba. Ez segít időt megtakarítani.

![ A nyomtatand&#xF3; objektumok elhelyez&#xE9;se SLA nyomtat&#xE1;shoz \(Prusa k&#xE9;p\)](../.gitbook/assets/sla_printerl_002.jpg)

 _Nyomtassa ki a tárgyat egyszerre több elforgatással, hogy gyorsan megtalálja az optimális tájolást - a nyomtatási idő nem változik._

## Fa támaszok

Az FDM támaszokkal ellentétben, amelyek jellemzően rács- vagy rácsszerűek, az SLA támaszok **három alakú, nagyon vékony végű állványzatra** hasonlítanak. Könnyen eltávolíthatók, és eltávolításuk után alig vagy egyáltalán nem hagynak nyomot a nyomtatott tárgy felületén. Ez azt is jelenti, hogy a túl kevés rögzítés nemkívánatos hatásokkal járhat - például a nehéz tárgyak leválhatnak nyomtatás közben. A támaszték kéz a kézben jár az objektum orientációjával - az objektum optimális pozícióba történő elforgatásával minimalizálhatja a támaszték szükségességét.

![Fa t&#xED;pus&#xFA; t&#xE1;maszt&#xE9;k](../.gitbook/assets/sla_printerl_003.jpg)

Sok támasztól megszabadulhat, ha az objektumot optimális pozícióba forgatja.

Ne feledje azt sem, hogy a támaszok eltávolítása apró nyomokat hagyhat a felületen, ezért ha a tárgyának vannak olyan területei, amelyeknek tökéletesen rendben kell lenniük \(egy ékszer dísze, egy figura arca\), próbálja meg távol tartani tőlük a támaszokat.

A SuperSlicer 2.3 teljes mértékben fel van szerelve automatikus fa típusú támaszok generálására:

1. Válassza ki a támogatást igénylő objektumot
2. Kattintson az SLA támogatási pontok ikonra
3. Válassza ki a támogatási pontok sűrűséget és a minimális ponttávolságot \(az alapértelmezett értékek a legtöbb objektum esetében jól működnek\).
4. Kattintson az pontok automatikusan generálása gombra, és várja meg a folyamat végét.
5. Az előnézeti módban ellenőrizheti, hogy minden "sziget" támogatott-e - ha nem, akkor manuálisan beállíthatja a támogatásokat.

![SLA t&#xE1;mogat&#xE1;si men&#xFC; a SuperSlicerben](../.gitbook/assets/sla_printerl_004.jpg)

Egy másik dolog, amit érdemes megfontolni, az a bázis. A **bázis** \(alapértelmezés szerint engedélyezve\) egy nagyméretű szerkezet a nyomtatás alján, amely a hordozó alapjául szolgál. Bár a támaszték közvetlenül az alumínium nyomtatási platformra is nyomtatható, az alap sokkal jobb stabilitást biztosít.

![Az SLA nyomtat&#xF3; t&#xE1;maszt&#xE9;k hozz&#xE1;ad&#xE1;sa](../.gitbook/assets/sla_printerl_005.jpg)

Lehetőség van a szoftver jobb oldali részében meghatározni a **Bázis** definícióját, amely lehet :

* Tárgy alatt 
* Tárgy körül
* vagy letilthatja \(Nincs\)

![B&#xE1;zis a t&#xE1;rgy alatt](../.gitbook/assets/sla_printerl_006.jpg)

![B&#xE1;zis a t&#xE1;rgy k&#xF6;r&#xFC;l](../.gitbook/assets/sla_printerl_007.jpg)

  A fenti képek a különbséget mutatják a **tárgy alatt** és a **tárgy körül** lévő bázis között.

### A támaszték kézi szerkesztése

Néhány esetben az automatikus támaszték generálás nem ad 100%-ban tökéletes eredményt - ez normális, mivel az importált objektumok végtelenül összetettek lehetnek. Folyamatosan fejlesztjük a támaszték generálás rutinjainkat, hogy megelőzzük az ilyen helyzetek kialakulását. Vannak azonban olyan esetek, amikor a támasztékot manuálisan kell hozzáadni - ez akkor is megtehető, ha már vannak automatikusan generált támasztékok.

![Az automatikusan gener&#xE1;lt &#xE9;s a k&#xE9;zzel szerkesztett t&#xE1;maszt&#xE9;k &#xF6;sszehasonl&#xED;t&#xE1;sa \(Prusa k&#xE9;p\)](../.gitbook/assets/sla_printerl_008.jpg)

Kattintson a **Kézzel történő szerkesztés** gombra. A korábban generált támaszok ideiglenesen eltűnnek, hogy jobban láthassa a modellt. Az **bal egérgombbal** **új támaszpontok hozzáadásához**. A támaszték vastagságát a kézi szerkesztési módban a **Fejátmérő** csúszkával módosíthatja, vagy a **Nyomtatási beállítások - Támaszték** menüpontban módosíthatja a következő beállításokat a támaszték vastagságának növelése érdekében:

* A tartófej elülső átmérője: 0,6 mm
* A tartófej behatolása: 0,6 mm
* Tartóoszlop átmérő: 1,3 mm

**Hasznos rövidítések**

**CTRL** + bal egérkattintás **Egyetlen támaszpont hozzáadása a kijelöléshez** **ALT** + bal egérkattintás

**ALT** + Bal egérkattintás **Egyetlen támaszpont törlése a kijelölésből** **ALT** + Húzás bal egérkattintással

**ALT** + Bal egérgombos húzás **Másik pont törlése a kijelölésből** **CTRL** + **Egyetlen támpont hozzáadása a kijelöléshez** \*\*CTRL

**CTRL** + **A** **Minden pont kiválasztása** **CTRL** + Kerék

**CTRL** + egérkerék **Vágási sík mozgatása** **CTRL** + egérkerék **Vágási sík mozgatása**

## Egy objektum tájolása

Az objektumorientáltság kulcsfontosságú a **SLA** nyomtatásnál. Ez nagyban befolyásolja a nyomtatás minőségét, és az SL1 esetében, amely a teljes réteget egyszerre keményíti, közvetlenül szabályozza a nyomtatási időt.

Talán már észrevette, hogy a **SLA** nyomatokat gyakran **45 fokos szögben** helyezik el. Ennek több oka is van:

* A nagy, sík, vízszintes felületek nagy erőt igényelnek ahhoz, hogy a bevonat megszilárdulásakor elváljanak a tartály aljától \(több támasztékra lenne szükségük\).
* A megdöntött tárgyak nagyobb területet fednek le, így az alattuk lévő támaszok egyenletesebben oszlanak el.
* Jobb élsimítás-csökkentés

A tárgyak fokozatos, ferde szögben történő növesztése általában a legbiztosabb módja a jó lenyomatok készítésének. Ennek ellenére **néhány tárgyat közvetlenül a nyomtatási platformra** is elhelyezhet a legjobb eredmény érdekében.

A legtöbb esetben az objektumnak egynél több jó orientációja van. Ez általában ékszerekkel vagy különböző szobrokkal történik. Az általános szabály itt az, hogy a tárgyat úgy próbáljuk meg elforgatni, hogy a lehető legkevesebb olyan pont legyen, ahol a tárgy a levegőben indul. Ezeket a pontokat szigetnek nevezzük. Ezeket a területeket nem lehet alátámasztás nélkül kinyomtatni - és mivel általában a legjobb, ha nem használunk alátámasztást, mindig meg kell próbálnunk jobb tájolást találni.

Az objektumok tájolásának megváltoztatására 3 eszköz áll rendelkezésre:

* Forgatás eszköz \(**R**\)
* Helyezze egy síkra eszköz \(**F**\)
* Tájolás optimalizálása eszköz \(jobb egérgombbal kattintva a szövegkörnyezeti menüben\)

![A Forgat&#xE1;s eszk&#xF6;z \(balra\), az Helyezze egy s&#xED;kra eszk&#xF6;z \(k&#xF6;z&#xE9;pen\) &#xE9;s az T&#xE1;jol&#xE1;s optimaliz&#xE1;l&#xE1;sa eszk&#xF6;z \(jobbra\).](../.gitbook/assets/sla_printerl_009.jpg)

### Tájolás optimalizálása

Ha **jobb egérgombbal** kattint egy sablonra, a felugró menüből kiválaszthatja a **Tájolás optimalizálása** lehetőséget. A SuperSlicer megpróbálja megtalálni az optimális nyomtatási tájolást. Vegye figyelembe, hogy ez a művelet sok poligonból álló, összetett modellek esetén némi időt vehet igénybe.

Az algoritmus **nem meghatározható**, ami azt jelenti, hogy az optimalizálás megismétlése ugyanarra a modellre mindig **minden alkalommal más orientációt eredményez**. Végül, ez az eszköz nem veszi figyelembe a maximális nyomtatási mennyiséget. Ha az új tájolás miatt a modell egy része a nyomtatási területen kívülre kerül, csökkentse a modellt, vagy állítsa be a tájolást.

### Nyomtatási idő

Az SL1 nyomtatási idejét egyszerű szorzással határozzuk meg: _rétegek száma × \(expozíciós idő + billentési idő\)_. Függetlenül a nyomtatási platformon lévő objektumok számától \(és összetettségétől\), az expozíciós idők a nyomtatási folyamat során végig állandóak - kivéve az első tíz réteget, amelyek elkészülte kissé hosszabb időt vesz igénybe.

Más szóval, egy magas tárgy nyomtatása kevesebb időt vesz igénybe, ha laposan fekteti a nyomtatási platformra. **Az idő szempontjából nem számít, hogy egy tárgyat helyezel el a platformon - vagy egy tucatot**. A nyomtatási idő mindig a rétegek számának és az egy réteg expozíciós idejének szorzata.

## Üreges

Az SLA nyomtatókhoz szeletelt összes objektum alapértelmezés szerint **teljesen tömör**. **Nincs kitöltési minta**, mint az FDM 3D nyomtatásnál. A folyékony gyantából nyomtatott tömör tárgyak nehezek és robusztusak lehetnek, de a gyantafogyasztás magas az üreges tárgyakhoz képest, különösen nagyméretű modellek nyomtatásakor.

A 3D modell kivájása nagyszerű módja annak, hogy :

* Jelentős mennyiségű **anyag** megtakarítása \(csökkenti a nyomtatási árat\)
* Csökkentse az egyes rétegek **felületét** - ez csökkenti a nyomtatásnak a kijelzőről való leválasztásához szükséges erőt a következő rétegre való áttéréskor. 
* Csökkenti a **szükséges támasztékok számát** \(a nyomtatott modell súlyának csökkentése\).

Javasoljuk, hogy legalább két **lefolyónyílást** helyezzen el. Ezek nélkül a kikeményítetlen gyanta a kész nyomatban reked.

### Az üreges szerszám használata

A süllyesztés minden modellhez külön-külön konfigurálható a **bal oldali eszköztáron** található Süllyesztés eszközzel. Alternatívaként az összes modell számára egyszerre is beállíthatja a mélyedést a **Nyomtatási beállítások - Süllyesztés** menüpontban.

A süllyesztés és a leeresztőnyílás munkafolyamata **nem roncsoló**. A süllyesztés bármikor visszavonható, és a lefolyónyílások bármikor áthelyezhetők vagy törölhetők.

A modellmélyedés a következő paraméterekkel van konfigurálva:

<table>
  <thead>
    <tr>
      <th style="text-align:left">
        <p>A keletkez&#x151; h&#xE9;j vastags&#xE1;ga.</p>
        <p>A minim&#xE1;lis &#xE9;rt&#xE9;k 1 mm.</p>
        <p></p>
        <p>A pontoss&#xE1;g &#xE9;s a teljes&#xED;tm&#xE9;ny k&#xF6;z&#xF6;tti kompromisszum.
          Ha alacsony bem&#xE9;lyed&#xE9;si pontoss&#xE1;got &#xE1;ll&#xED;t be,
          a kapott modell falvastags&#xE1;ga egyenetlen lehet. Ez&#xE9;rt kis m&#xE9;lyed&#xE9;svastags&#xE1;g
          eset&#xE9;n (v&#xE9;kony h&#xE9;jak eset&#xE9;n) nagyobb m&#xE9;lyed&#xE9;si
          pontoss&#xE1;g aj&#xE1;nlott a minim&#xE1;lis falvastags&#xE1;g biztos&#xED;t&#xE1;sa
          &#xE9;rdek&#xE9;ben.</p>
        <p></p>
        <p>A m&#xE9;lyed&#xE9;s elt&#xE1;vol&#xED;tja a z&#xE1;r&#xE1;si t&#xE1;vols&#xE1;g
          k&#xFC;sz&#xF6;b&#xE9;rt&#xE9;k&#xE9;n&#xE9;l keskenyebb &#xFC;regeket,
          &#xE9;s kit&#xF6;lti a bels&#x151; fal &#xE9;les homor&#xFA; sarkait is,
          amelyekb&#x151;l egy&#xE9;bk&#xE9;nt neh&#xE9;z lenne elt&#xE1;vol&#xED;tani
          az er&#x151;sen viszk&#xF3;zus, nem kikem&#xE9;nyedett gyant&#xE1;t.</p>
      </th>
      <th style="text-align:left">
        <p></p>
        <p>
          <img src="../.gitbook/assets/sla_printerl_010.png" alt="Image : R&#xE9;glage &#xC9;paisseur d&apos;&#xE9;videment"
          />
        </p>
      </th>
    </tr>
  </thead>
  <tbody></tbody>
</table>

### Leeresztő lyukak hozzáadása

A leeresztőnyílások hozzáadásához **bal egérgombbal** kattintás az objektumra, amikor az SLA üreges manipulátor aktív.

A lyukak később áthelyezhetők a hálóra húzva.

Minden lyuk mindig merőleges a felületre, és **átmérője** és **mélysége** konfigurálható - az újonnan elhelyezett lyukaknál az aktuális beállítások lesznek használva.

A lyukak törlésére az egyikre **jobb gombbal kattintva** van lehetőség.

**A lyukakat még a süllyesztéssel letiltott modellekhez is hozzáadhatja**. Ez olyan modellek esetében hasznos, amelyeket egy külső programban üregesített.

Felhívjuk a figyelmét, hogy ha a bemeneti háló sérült, a lyukfúró algoritmus megtagadhatja a folytatást, hogy elkerülje a program összeomlását vagy a hibás eredményeket.

### Az üreges háló megerősítése és előnézetének megtekintése

Az üregesítés és a furatfúrás az Előzetes üregesítés és fúrás modell gomb megnyomása után történik. Vegye figyelembe, hogy mind az üregesítés, mind a furatfúrás számításigényes feladat, és némi időt vesz igénybe, különösen összetett modellek esetén. Ha a felhasználó nem maga nyomja meg a gombot, az üregesítés és a fúrás a szeletelési folyamat során történik.

A vágási sík eszközzel az objektum belsejébe lehet belelátni \(ugyanez az eszköz megtalálható az SLA támpontok szerkesztő manipulátorba is\). A csúszkát balról jobbra mozgatva mozgathatja a vágási síkot. Átnézheti az üregesített geometriát, és megfelelően elhelyezheti a leeresztő lyukakat.

![V&#xE1;g&#xE1;si s&#xED;k be&#xE1;ll&#xED;t&#xE1;sa](../.gitbook/assets/sla_printerl_011.jpg)

Az Irány **visszaállítása gomb** a vágási sík eszközt az aktuális kameranézettel párhuzamosan igazítja. Ha például azt szeretné, hogy a vágási sík fel-le mozogjon, nézze a modellt felülről \( **Felső nézet**\), és nyomja meg a Visszaállítás iránya gombot.

![Ir&#xE1;ny vissza&#xE1;ll&#xED;t&#xE1;sa](../.gitbook/assets/sla_printerl_012.jpg)

Az Irány visszaállítása gomb csak akkor látható, ha a Vágási sík eszközt nem nulla értékre mozgatja.

![Metszeti n&#xE9;zet](../.gitbook/assets/sla_printerl_013.jpg)

Az üreges és fúrt modellt a **Fájl - Exportálás - Lemez exportálása STL-be**  menüpont kiválasztásával exportálhatja.

Bármely paraméter megváltoztatása a háló érvénytelenítését kényszeríti ki \(például egy lyuk áthelyezése, az objektum méretezése stb.\). A modell nézete visszaáll az eredeti objektumra a fúrt lyukak és az alkalmazott mélyedés nélkül.

Példa a tömör vs. üreges modellre

Tömör modell: 237 ml, gyanta ára $13.75

Üreges modell: 81 ml, gyanta ára $4.70

![P&#xE9;lda: Hellboy mellszobor bara t&#xF6;m&#xF6;r jobbra &#xFC;reges](../.gitbook/assets/sla_printerl_014.jpg)

Az üregesítés és a lyukfúrás funkciói az [OpenVDB](https://www.openvdb.org/) és a [CGAL](https://www.cgal.org/) könyvtárakon alapulnak. Köszönet mindkét könyvtár szerzőinek.

