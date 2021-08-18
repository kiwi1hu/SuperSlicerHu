# extrusion\_width

* Technológia : FDM
* Csoport : [Nyomtatási beállítások](../../konfig/print_settings.md)
* Alcsoport : [Szélesség és áramlás](../../beallitasok/print_settings.md#largeur-et-débit) - [Extrudálás szélessége](extrusion_width.md)
* Mód : Haladó
* Mértékegység : mm vagy %
* Minimális érték :  0
* Maximális érték :  1000
* Alapértelmezett érték : 0

## Extrudálás szélessége

### Leírás

Az extrudálás szélességének kézi meghatározásához állítsa ezt a paramétert nem nulla értékre. Ha nullán hagyja, a SuperSlicer az extrudálás szélességét a [fúvóka átmérőjéből](nozzle_diameter.md) származtatja \(lásd a [kerület extrudálás szélessége](perimeter_extrusion_width.md), [kitöltési extrudálás szélessége](infill_extrusion_width.md) stb. eszköztippeket\).

Ha százalékban van megadva \(pl. 105%\), akkor a [fúvókaátmérő](nozzle_diameter.md) alapján kerül kiszámításra.

Beállíthatja az [extrudálás távolsága](extrusion_spacing.md) vagy az [extrudálás szélessége](extrusion_width.md) értéket; a másik értéket a [kerületi átfedés](perimeter_overlap.md) és az alapértelmezett [rétegmagasság](layer_height.md) érték százalékos értékei alapján számítja ki a rendszer.

[Vissza a változók listájához](/)

