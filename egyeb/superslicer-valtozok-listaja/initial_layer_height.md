# initial\_layer\_height

* Technológia : FDM & SLA
* Csoport : [Nyomtatási beállítások](../../../konfig/print_settings)
* Alcsoport : [Szeletelés](../../../konfig/print_settings#szeletelés) - [Rétegmagasság](../../../konfig/print_settings#rétegmagasság)
* Mód: Haladó
* Mértékegység : mm
* Minimális érték: 0
* Alapértelmezett érték: 0,2

## Az első réteg magassága

### Leírás

Ez a beállítás határozza meg a nyomtatás első rétegének vastagságát. A kezdőréteget általában vastagabban nyomtatják, mint a többit, hogy erősebb kötést hozzanak létre az ágyon. Ezzel a beállítással a kezdeti réteg vastagsága növelhető anélkül, hogy a nyomtatás többi részének felbontása csökkenne.

A kezdeti réteg vastagságának növelésével a fúvóka ugyanarra a távolságra több anyagot présel ki. Ez extra erőt igényel, mivel az anyag szétterül az oldalakon, hogy kitöltse a vonal teljes szélességét. Ez a plusz erő jobban rátapasztja az anyagot az ágyra. Ezenkívül a vastagabb réteg segít kompenzálni a felület egyenetlenségeit. Ha az ágy kissé el van csavarodva, a változékonyságot az első réteg vastagsága elnyeli, míg ellenkező esetben a fúvóka a második rétegbe kaparhatja.

Ha az első réteg túl vastag, az első réteg jobban megereszkedik, ami elefántlábat eredményez. Az [Első réteg XY kompenzáció](first_layer_size_compensation.md) paraméter ezt megakadályozhatja, ha kis negatív értéket ad meg.

[Vissza a változók listájához](../../variable_list)

