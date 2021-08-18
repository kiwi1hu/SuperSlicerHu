# layer\_height

* Technológia : FDM & SLA
* Csoport : [Nyomtatási beállítások](../../../konfig/print_settings)
* Alcsoport : [Szeletelés](../../../konfig/print_settings#szeletelés) - [Rétegmagasság](../../../konfig/print_settings#rétegmagasság)
* Mód: Haladó
* Mértékegység : mm
* Minimális érték: 0
* Alapértelmezett érték: 0,2

## Rétegmagasság

### Leírás

A 3D nyomtató a műanyagot rétegenként rakja le. A rétegmagasság a rétegek vastagsága milliméterben. Ez a legfontosabb tényező mind a végső nyomat vizuális minősége, mind a nyomtatási idő szempontjából.

A réteg magassága a legfontosabb paraméter, amely befolyásolja az általános minőséget, és fordítva, a nyomtatási időt:

* A vékonyabb rétegek növelik a nyomtatás vizuális minőségét. Mivel a rétegek vékonyabbak, a lépcsőzetes hatás csökken. Ezenkívül a rétegek közelebb lesznek egymáshoz, és a rétegek közötti rések kisebbek lesznek, ami összességében simább felületet eredményez.
* A vékonyabb rétegek lehetővé teszik, hogy a nyomtató több részletet tudjon előállítani a nyomat tetején és alján.
* A vastagabb rétegek általában erősebbé teszik a nyomatot, egy bizonyos pontig. A vastagabb rétegek kevésbé könnyen nyíródnak.
* A vastagabb rétegek csökkentik a nyomtatási időt.

### Hauteur des couches par rapport aux profils

De nombreux paramètres dépendent de la hauteur de la couche. Comme la hauteur de la couche affecte considérablement le débit du matériau à travers la buse, de nombreux paramètres du processus d'impression vont changer. Ceci est très complexe. Par exemple, lorsque vous augmentez la hauteur de la couche, vous devez probablement augmenter légèrement la température d'impression pour compenser le taux supplémentaire de perte de chaleur. La température affecte alors la fluidité du matériau, ce qui aura une incidence sur la netteté de vos coins et sur le refroidissement nécessaire, etc.

### További megjegyzések

Nagyon alacsony rétegmagasságok esetén elérheti a Z-tengely felbontási határát. Ellenőrizze a nyomtató Z-tengelyének osztásméretét, és győződjön meg arról, hogy a rétegmagasság ennek többszöröse. Ha nem egyeznek, egyes rétegek vastagabbak lesznek a többinél, ami csíkok formájában vizuális hibákat eredményez a nyomatokon.

_Megjegyezzük, hogy az alap rétegmagasság beállítása nem vonatkozik a kezdeti nyomtatási rétegre, amelynek saját beállítása van a rétegek magasságának külön-külön történő beállítására._

[Vissza a változók listájához](../../variable_list)

