# Fordítás létrehozása és frissítése

Ne feledje, hogy a Slic3r csak a balról jobbra haladó nyelveket támogatja \(ha ezt meg akarja változtatni, szívesen látjuk, ha hozzájárul\).

A nyelvednek [kóddal](https://www.loc.gov/standards/iso639-2/php/code_list.php) kell rendelkeznie \(használja az ISO 639-1 második oszlopát\). Egy könyvtár létrehozása és egy .mo fájl elhelyezése benne automatikusan hozzáadja a fordítást a Slic3r-ben.

Egy '.po' szövegfájlt kell kitölteni egy szövegszerkesztővel vagy egy speciális ide-vel, mint a poedit. Amikor a fordítási munka befejeződött, egy '.mo' fájlba kell fordítania, ez nem olvasható szövegszerkesztővel, de a szoftver által olvasható.

Ha a nyelv már itt van, akkor az összes jelenlegi fájlt eltávolíthatja, hogy a nulláról kezdhesse, vagy átnevezheti őket, hogy kiindulópontként használhasd őket.

Ha furcsa fordítást találtál, és meg akarod változtatni, menjen a B\) részhez.

## A\) Készítsen saját fordítást

Hasznos eszközök:

* windows:
  * [python](https://www.python.org/)
  * [gettext](http://gnuwin32.sourceforge.net/downlinks/gettext.php)
* linux:
  * python: győződjön meg róla, hogy tudja futtatni a python3-at, telepítse, ha nincs itt.
  * gettext: ha nem tudja futtatni az msgfmt-t, telepítse a 'gettext' csomagot.
* macos: talán mint a linux?

### 1\) Inicializálás

nyissa meg a settings.ini fájlt minden olyan fájlhoz, amely hasznos fordítást tartalmazhat, hozzon létre/szerkesszen létre egy "data" sort, amely az említett fájlra mutat. Az 'input' tulajdonságnak a Slic3r.pot elérési útvonalának kell lennie. A 'output' tulajdonságnak a Slic3r.po fájlnak kell lennie. A 'todo' a befejezendő po fájl elérési útját tartalmazza.

vegye figyelembe, hogy az első adatsor elsőbbséget élvez a többivel szemben \(az első fordítást használják\).

Ebben a példában a magyar fordítást fogjuk frissíteni. A régi és a jelenlegi SuperSlicer fordítási fájlt fogjuk használni. A SuperSlicer .mo fájljának dekompilálásához használja a következő parancsot`msgunfmt SuperSlicer.mo -o SuperSlicer.po`. Tehát a **settings.ini** ezeket a sorokat tartalmazza:

```text
data = hu/Slic3r.po
data = MyKnowledgeBase.po
data = hu/SuperSlicer_hu.po

database_out = MyKnowledgeBase.po

ui_dir = ../ui_layout
allow_msgctxt = false
ignore_case = false
remove_comment = true
percent_error_similar = 0.4
max_similar = 3
language = magyar
language_code = hu

input = Slic3r.pot
todo = hu/todo.po
output = hu/Slic3r.po
```

**Megjegyzések:**

* a 'todo' és 'output' fájlok törlődnek, ezért győződjön meg róla, hogy semmi fontosnak nincs ilyen neve \(vagy írjon másik nevet\).
* az 'database\_out' fájlba kerül az adatfájlokból létrehozott összes adatbázis. Így megtartja az új és a régi, nem használt fordításokat arra az esetre, ha a szövegezés visszatérne, vagy hogy referenciaként használják a segédprogram számára.
* `ui_dir` a `slic3r/resources/ui_layout könyvtár` elérési útvonalának kell lennie. Ha a `slic3r/resources/localization` könyvtárban van, akkor ez az érték jó.
* allow\_msgctxt egy bool, amely engedélyezi a msgctxt címkék megtartását. Ehhez a gettext egy újabb verziójára van szüksége.
* ignore\_case egy bool, amely lehetővé teszi az eszköz számára, hogy figyelmen kívül hagyja az esetet a msgid összehasonlításakor, ha nem talál fordítást.
* remove\_comment egy bool, amely eltávolítja az összes megjegyzést a kimeneti fájlban. Ezzel elkerülhetőek a felesleges változtatások a git commitban.
* percent\_error\_similar egy 0 és 1 közötti szám. Ez aktiválja a segédprogramot, amely segítő megjegyzést ír a TODO fájlba. Ezek hasonló, már lefordított karakterláncokat fognak bemutatni, hogy a már lefordított részeket kiválaszthassa, hogy elkerülje az összes munka újbóli elvégzését. Ez a megengedett eltérés százalékos aránya \(0 = azonos, 1 = minden, 0,5 = a karakterlánc legfeljebb fele eltérő\), a \(levenshtein távolság / msgid hossza\) segítségével.
* max\_similar: a segédfordítások maximális száma elemenként
* language és language\_code: a fejlécben feltüntetendő szöveg.

### 2\) Indítsa el a segédprogramot

* Szüksége van pythonra \(v3\). Ha nincs, letöltheti.
* Nyisson meg egy konzolt
* cd a honosítási könyvtárba,
* futtassa a `python pom_merger.py` parancsot
  * python3 használata, ha a python a python v2 exe
  * használhatja a python.exe teljes elérési útját, ha most telepítette, és nincs az elérési útvonalában. Windowson alapértelmezés szerint az appdata-ba van telepítve.

    Megmondja, ha hibát követett el az útvonalakkal, az újra felhasznált fordítások számával és az elvégzendő fordítások számával kapcsolatban.

### 3\) A fordítási fájl elkészítése

Ezután meg kell nyitnia az es/todo.po fájlt, és ki kell töltenie az összes fordítást.

* msgid sorok az angol szövegek
* msgstr a lefordított, üres karakterláncnak \(""\) kell lennie.

Fontos:

* egy sorba kell írnia, használja a \n-t a sorváltás beviteléhez. 
* a %1, %2, ... szintén be kell tenni a fordításba, mivel ez egy helyőrző a bemeneti számok számára, ha az egyik kimarad, a szoftver összeomlik, ezért legyünk óvatosak. A '%%' a '%' írásának módja anélkül, hogy a program összeomlana. A segédprogramnak figyelmeztetnie kell minden olyan fordításnál, ahol a '%' különböző számmal szerepel.

### 4\) A segédprogram újraindítása

A todo.po-t másolhatja/mentheti egy másik fájlba, ha. A todo fájl kitöltése után módosítsa a settings.ini fájlt:

```text
data = hu/todo.po
data = MyKnowledgeBase.po

database_out = MyKnowledgeBase.po

ui_dir = ../ui_layout
allow_msgctxt = false
ignore_case = false
remove_comment = true
percent_error_similar = 0.4
max_similar = 3
language = magyar
language_code = hu

input = Slic3r.pot
todo = hu/todo.po
output = hu/Slic3r.po
```

Ez azt fogja mondani, hogy használja a todo-t és az újonnan létrehozott/szerkesztett Slic3r.po-t, mielőtt a másik régebbi fájlt használná a meg nem talált karakterláncok befejezéséhez. A harmadik fájlból származó fordítás nem törli a másodikból származó fordítást, kivéve, ha az üres \(kevesebb, mint 3 karakter\), az új pedig nem az. Ha egy fordítás kicserélődik, az eszköz tájékoztatni fogja Önt.

És újraindítja a segédprogramot.

Ismételje meg \(ha szükséges\), amíg szinte semmi nem marad a todo.po fájlban \(az egybetűs fordításokat, mint a ".", a segédprogram nem másolja át\).

Ha kész , fordítsa le a .po fájlt a következő paranccsal `msgfmt Slic3r.po -o Slic3r.mo`. Ezután elindíthatja a Slic3r-t a teszteléshez. Vegye figyelembe, hogy át kell neveznie SuperSlicer.mo-ra, ha Superslicert használ, és ugyanezt a PrusaSlicer esetében is.

## B\) Meglévő .po fájl frissítése

* Nyissa meg a problémás .po nyelvi fájlt egy szövegszerkesztővel.
* Keresse meg a hibás mondatot.
* Módosítsa a lefordított mondatot \(a 'msgstr' jobb oldalán\).
  * Ne feledje, hogy minden sor mindkét oldalán meg kell hagynia egy-egy '"'' betűt, de ha szeretné, a több sort egybe is fűzheti.
  * A '\n' billentyűvel egy 'új sor'-t is beilleszthet a mondatba.
* Ha kész, fordítsa le a .po-t .mo-vá, és cserélje le a jelenlegi .mo-t.
* Nyissa meg a Slic3r-t, és ellenőrizze, hogy a mondat működik-e. Ha a Slic3r összeomlik, akkor valószínűleg rosszul működik.
* Küldje be a változtatást egy issue megnyitásával \(keressen rá az "is:issue translation" kifejezésre a issue keresősávban, hogy egy már létezőt is átvegyen, ha van ilyen\).

