# first\_layer\_size\_compensation

* Technológia : FDM & SLA
* Csoport : [Nyomtatási beállítások](../../konfig/print_settings.md)
* Alcsoport : [Szeletelés](../../beallitasok/print_settings.md#couche) - [Rétegmódosítások](first_layer_size_compensation.md)
* Mód : Haladó
* Mértékegység : mm
* Alapértelmezett érték : 0

## XY Első réteg kompenzáció

### Leírás

Ez a beállítás csak a kezdeti réteget terjeszti ki, amely a nyomtatóágyon van.Az [xy méretkompenzáció](xy_size_compensation.md) vagy [xy belső méretkompenzáció](xy_inner_size_compensation.md) értékekhez hasonlóan a pozitív érték növeli a kezdeti réteget, míg a negatív érték csökkenti azt.

A kezdeti réteget gyakran fűtött ágyra nyomtatják, amely kissé folyékony állapotban tartja, hogy javítsa az ágyhoz való tapadást. A kezdeti réteg általában sokkal vastagabb, mint a többi réteg. Ez elegendő időt és anyagot biztosít ahhoz, hogy a réteg oldalirányban megereszkedjen, ami az úgynevezett **elefántláb** jelenséget hozza létre, amikor a lenyomat alján egy kissé szélesebb perem keletkezik. Ez a beállítás kompenzálhatja az elefántlábat azáltal, hogy a kezdeti réteget vékonyabbá teszi. Adjon ennek a beállításnak egy kis negatív értéket, hogy kompenzálja az elefántlábat.

[Vissza a változók listájához](/)

