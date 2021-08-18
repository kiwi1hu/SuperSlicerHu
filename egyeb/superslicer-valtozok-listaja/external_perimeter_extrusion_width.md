# external\_perimeter\_extrusion\_width

* Technológia : FDM
* Csoport : [Nyomtatási beállítások](../../../konfig/print_settings)
* Alcsoport : [Szélesség és áramlás](../../beallitasok/print_settings.md#largeur-et-débit) - [Extrudálás szélessége](external_perimeter_extrusion_width.md)
* Mód : Haladó
* Mértékegység : mm vagy %
* Minimális érték :  0
* Maximális érték :  1000
* Alapértelmezett érték : 0

## Külső kerület szélessége

### Leírás

Állítsa ezt a paramétert nem nulla értékre, ha a külső peremek extrudálási szélességét kézzel kívánja meghatározni. Ha nulla marad, akkor az alapértelmezett [extrudálás szélessége](extrusion_width.md) lesz használva, ha be van állítva, különben a [fúvóka átmérő](nozzle_diameter.md) 1,05-szeresét fogja használni.

Ha százalékban van kifejezve \(pl. 112,5%\), akkor a [fúvóka átmérője](nozzle_diameter.md) alapján kerül kiszámításra.

Beállíthatja a [Távolság](external_perimeter_extrusion_spacing.md), vagy [Szélesség](external_perimeter_extrusion_width.md) ; a másik az alapértelmezett [kerületi átfedés](perimeter_overlap.md) és [rétegmagasság](layer_height.md) százalékos értékek felhasználásával kerül kiszámításra.

[Vissza a változók listájához](../../variable_list)

