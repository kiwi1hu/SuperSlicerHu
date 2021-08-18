# milling\_toolchange\_start\_gcode

* Technológia : FDM
* Csoport : [Nyomtató beállítások](../../beallitasok/printer_settings.md)
* Alcsoport : [Milling](../../beallitasok/printer_settings.md#milling) - Comportement
* Mód : Haladó

## G-Code pour passer à cette tête de fraisage

### Leírás

Mettez ici le G-Code pour changer la tête d'outil \(appelé après le g-code T \[ [next\_extruder](next_extruder.md) \] \). Vous avez accès à [next\_extruder](next_extruder.md) et [previous\_extruder](previous_extruder.md). [Next\_extruder](next_extruder.md) est le 'numéro d'extrudeuse' du nouveau outil de fraisage, il est égal à l'index \(commençant à 0\) de l'outil de fraisage plus le nombre d'extrudeuses. previous\_extruder est le 'numéro d'extrudeuse' de l'outil précédent, il peut s'agir d'une extrudeuse normale, s'il est inférieur au nombre d'extrudeuses. Le numéro d'extrudeuse est disponible à [extruder](extruder.md) et le numéro de la fraise est disponible à [milling\_cutter](milling_cutter.md).

La valeur de [milling\_count](milling_count.md) doit être &gt; 0 pour que le paramètre soit accessible.

Exemple de code :

`M6 T {current_extruder} D{milling_diameter[next_extruder]}`

[Vissza a változók listájához](../../variable_list)

