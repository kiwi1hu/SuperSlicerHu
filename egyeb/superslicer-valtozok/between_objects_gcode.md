# between\_objects\_gcode

* Technológia : FDM
* Csoport : [Nyomtató beállítások](../../konfig/printer_settings.md)
* Alcsoport : [Egyedi G-kód](../../konfig/printer_settings.md#egyedig-kód)
* Mód : Szakértő

## Objektumok közötti G-kód \( Szekvenciális nyomtatáshoz\)

### Leírás

Ez a kód a szekvenciális nyomtatás használatakor az objektumok közé kerül. Alapértelmezés szerint az extruder és az ágy hőmérséklete visszaáll, és a várakozás nélküli parancsot használja; azonban ha az M104, M109, M140 vagy M190 parancsokat észleli ebben az egyéni kódban, a SuperSlicer nem ad hozzá hőmérséklet-parancsokat. Ne feledje, hogy az általános változókat minden SuperSlicer beállításhoz használhatja, így bárhová beírhat egy "M109S\[[first\_layer\_temperature](../first_layer_temperature)\]" parancsot.

[Vissza a változók listájához](/)

