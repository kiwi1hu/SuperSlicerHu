# extruder\_temperature\_offset

* Technológia : FDM
* Csoport : [Réglages de l'Imprimante](../printer_settings/printer_settings.md)
* Alcsoport : [Extrudeuse](../printer_settings/printer_settings.md#extrudeuse) - Décalages \(pour les imprimantes multi-extrudeuse\)
* Mód : Szakértő

## Décalage de la température de l'extrudeuse

### Leírás

Ce décalage sera ajouté à toutes les températures d'extrusion définies par le réglage filament.

Notez que vous devez définir 'M104 S{first\_layer\_temperature\[initial\_extruder\]+ extruder\_temperature\_offset\[initial\_extruder\]}' au lieu de 'M104 S\[ [first\_layer\_temperature](first_layer_temperature.md) \]' dans le [start\_gcode](start_gcode.md).

[Vissza a változók listájához](variable_list.md)

