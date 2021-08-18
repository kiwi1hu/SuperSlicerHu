# extruder\_temperature\_offset

* Technológia : FDM
* Csoport : [Nyomtató beállítások](../../beallitasok/printer_settings.md)
* Alcsoport : [Extruder](../../beallitasok/printer_settings.md#extrudeuse) - [Eltolás \(több extruderrel működő nyomtatók esetében\)](extruder_temperature_offset.md)
* Mód : Szakértő
* Mértékegység : °C
* Alapértelmezett érték : 0

## Extruder hőmérséklet eltolás

### Leírás

Ez az eltolás hozzáadódik a szálbeállításokban beállított összes extruder-hőmérséklethez. Megjegyezzük, hogy a start\_gkódban az 'M104 S{first\_layer\_temperature\[initial\_extruder\] + extruder\_temperature\_offset\[initial\_extruder\]}' helyett az 'M104 S\[first\_layer\_temperature\]'-t kell beállítani.

[Vissza a változók listájához](../../variable_list)

