# A SuperSlicer célja

\# A SuperSlicer célja

## Az oldal tartalma

* A SuperSlicer célja
  * [Melyek a SuperSlicer fő jellemzői? Mik a fő különbségek?]() 
  * [Melyek a SuperSlicer / PrusaSlicer / Slic3r fő jellemzői?]() 
  * [Egyéb főbb jellemzők]()
  * [Fejlesztés]()
  * [Licencelés és tulajdonjog]()
* [Vissza a főoldalra](../superslicer.md)

**SuperSlicer** a PrusaSlicer \(amely a slic3r egy változata\) \(korábban Slic3r++\) egy változata.

A Windows, Linux és macOS előre lefordított 64 bites változatai a [git kiadások oldal](https://github.com/supermerill/SuperSlicer/releases) oldalon érhetőek el. A Linux és macOS verziók nem teszteltek, csak lefordítottak, ezért kérjük, jelezzétek az esetlegesen a használat során felmerülő hibákat. Az éjszakai buildek elérhetőek a [git műveletek oldal](https://github.com/supermerill/SuperSlicer/actions) oldalon. Kattints a platformodnak megfelelő verzióra, majd a jobb felső sarokban a 'Artifacts \(1\)' gombra.

A SuperSlicer 3D modelleket \(STL, OBJ, AMF\) fogad el, és G-kód utasításokká alakítja át FFF nyomtatókhoz vagy PNG rétegekké SLA 3D nyomtatókhoz. Kompatibilis az összes modern RepRap alapú nyomtatóval, amelyek Marlin, Prusa, Klipper stb. alapú firmware-t használnak.

A SuperSlicer a Prusa Research által készített [PrusaSlicer](https://github.com/prusa3d/PrusaSlicer/issues/2729) alapján készült. A PrusaSlicer az Alessandro Ranellucci és a RepRap közösség által készített \[Slic3r\]-en \([https://github.com/Slic3r/Slic3r](https://github.com/Slic3r/Slic3r)\) alapul.

A fordítási információkért lásd a [wiki](https://github.com/supermerill/SuperSlicer/wiki) és a [dokumentációs könyvtár](https://github.com/supermerill/SuperSlicer/tree/master/doc).

## Melyek a SuperSlicer fő jellemzői? Mik a fő különbségek?

* Egyedi generált kalibrációs tesztek.
* _**A felső felület simítása**_ és számos új paraméter a felső felület minőségének finomítására, mint például az "egy kerület a tetején".
* Egy "sűrűbb kitöltés" lehetőség a felső \(tömör\) rétegek alátámasztására.
* Jobb vékony falak \(a nyomtatás belsejében rögzítve, nincs több véletlenszerű darab a végeken, integrálva a kerületi hurkokba\).
* Lehetőségek a lyukak méreteinek és/vagy geometriájának módosítására a megfelelő méretű nyomtatáshoz.
* Jobb túlfolyások \(ha szükséges, adjunk hozzá kerületeket, vágjuk őket az ellenkező 

  irányban ellentétes irányban minden réteghez\).

* Szélek retusálása: sokkal több lehetőség \(csak belül, csak kívül, “sarkok”,

   objektumonként\).

* Néhány új varrási lehetőség, hogy segítsen elrejteni őket.
* Integrált kalibrációs nyomtatások 
* Integrált objektum generáló szkript \(FreeCad\)
* Az elmozdulások elkerülése érdekében a kerületeket egy nagyméretűvé egyesítheti.
* Sok más apró lehetőség és korrekció \(mint például a kitöltött koncentrikus minta\).
* A PrusaSlicer összes jelenlegi funkciójával rendelkezik.

**A változások teljes listája** [**itt**](https://github.com/supermerill/SuperSlicer/wiki) .További információk a szoftverről a [wiki](https://github.com/supermerill/SuperSlicer/wiki) oldalon találhatók.

## Melyek a SuperSlicer / PrusaSlicer / Slic3r fő jellemzői?

A főbb jellemzők a következők:

* _**Multiplatform**_ \(Linux/Mac/Win\) és önálló, függőségek nélküli alkalmazásként kerül terjesztésre.
* **Teljes parancssori felület** a GUI nélküli használathoz
* Több anyagból készült tárgyak nyomtatása \(**több extruder**\)
* Többféle G-kód támogatása \(RepRap, Makerbot, Mach3, Machinekit, stb.\)
* Több objektum nyomtatásának lehetősége _**különböző nyomtatási beállításokkal**_.
* Többszálú feldolgozás
* Automatikus STL javítás \(tolerancia az érvénytelen modellekre\)
* Kiterjesztett automatizált egységtesztelés

  **Egyéb főbb jellemzők**

* Kitöltő rétegek kombinációja minden “n” kerületenként és változó sűrűséggel a nyomtatás felgyorsítása érdekében.
* _**3D előnézet**_ \(beleértve a több anyagot tartalmazó fájlokat is\).
* _**Többféle rétegmagasság**_ egy nyomtatásban.
* Spirálváza mód a domborzat nélküli vázákhoz.
* A sebesség, a gyorsulás és az extrudálás szélességének finom beállítása.
* Számos kitöltési minta, köztük méhsejtek, spirálok, Hilbert-görbék és gyroidok állnak rendelkezésre.
* A támasz, a tutaj, a perem és a szoknya geometriája.
* **Készenléti hőmérséklet** és automatikus törlés több extruderrel történő nyomtatáshoz
* **Testreszabható G-kód makrók** és kimeneti fájlnév változó helyőrző karakterekkel.
* **Utófeldolgozó szkriptek** támogatása
* A ventilátor sebességét és a dinamikus nyomtatási sebességet vezérlő hűtési logika

  **Fejlesztés**

  **Milyen nyelven van megírva?**

  Szinte minden C++ nyelven készült.

A szeletelőmotor magja a libslic3r könyvtár, amely önállóan is fejleszthető és használható. A parancssori interfész a libslic3r csomagolása. Letölthet egy előre lefordított csomagot a kiadási oldalról - ez függőségek nélkül is működni fog.

### Segíthetek valamiben?

Hát persze! A következő módon találhatja meg azokat a dolgokat, amelyekben segítségünkre lehet:

* Adjon hozzá egy problémát a [GitHub nyomkövetőhöz](https://github.com/supermerill/SuperSlicer/issues) **ha még nincs ilyen**.

A javítások és kérelmek elküldése előtt lépjen kapcsolatba velünk \(lehetőleg a GitHubon egy probléma megnyitásával vagy egy meglévő, kapcsolódó probléma kommentálásával\), hogy megbeszéljük a javasolt változtatásokat. Így biztosíthatjuk, hogy senki sem vesztegeti az idejét, és nem merülnek fel konfliktusok a fejlesztés során.

## Licencelés és tulajdonjog

A SuperSlicer a GNU Affero General Public License, 3. verziója alatt áll. A SuperSlicer a PrusaResearch PrusaSliceren alapul.

A SuperSlicer a GNU Affero General Public License, 3. verziója alatt áll. A SuperSlicer a PrusaResearch PrusaSliceren alapul.

A PrusaSlicer a GNU Affero General Public License, 3. verziója alatt áll. A PrusaSlicer a Prusa Research tulajdonában van. A PrusaSlicer eredetileg az Alessandro Ranellucci által készített Slic3r-en alapul.

A Slic3r a GNU Affero General Public License, 3. verziója alatt áll. A Slic3r-t Alessandro Ranellucci hozta létre sok más közreműködő segítségével.

A GNU Affero General Public License 3. verziója garantálja, hogy ha a szoftver bármely részét bármilyen módon használja \(még egy webszerver mögött is\), akkor a szoftverét ugyanezen licenc alatt kell kiadni.

[Következő szakasz: Támogatás igénybevétele](../getting-support.md)

[Vissza a főoldalra](../superslicer.md)

