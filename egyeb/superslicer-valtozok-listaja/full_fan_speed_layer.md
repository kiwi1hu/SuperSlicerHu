# full\_fan\_speed\_layer

* Technológia : FDM
* Csoport : [Szál beállítások](../filament_settings/filament_settings.md)
* Alcsoport : [Hűtés](../filament_settings/filament_settings.md#refroidissement) - [Ventilátor sebessége](full_fan_speed_layer.md)
* Mód : Szakértő
* Minimális érték :  0
* Maximális érték :  1000
* Alapértelmezett érték :  0

## Teljes ventilátor fordulatszám a rétegben

### Leírás

A ventilátor sebessége [a ventilátor kikapcsolása az első rétegeknél](disable_fan_first_layers.md) réteg esetében a nullától a [teljes ventilátor fordulatszám a rétegben](full_fan_speed_layer.md) esetében a maximumig lineárisan növekszik. A [teljes ventilátor fordulatszám a rétegben](full_fan_speed_layer.md) értéket figyelmen kívül hagyja, ha kisebb, mint [a ventilátor kikapcsolása az első rétegeknél](disable_fan_first_layers.md), amely esetben a ventilátor [a ventilátor kikapcsolása az első rétegeknél](disable_fan_fan_first_layers.md) +1 réteghez megengedett maximális sebességgel fog működni.

[Vissza a változók listájához](../../variable_list)

