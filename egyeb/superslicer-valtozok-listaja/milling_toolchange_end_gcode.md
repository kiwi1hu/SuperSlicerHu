# milling\_toolchange\_end\_gcode

* Technológia : FDM
* Csoport : [Nyomtató beállítások](../../beallitasok/printer_settings.md)
* Alcsoport : [Milling](../../beallitasok/printer_settings.md#milling) - Comportement
* Mód : Haladó

## G-Code pour arrêter cette tête de fraisage

### Leírás

Mettez ici le G-Code pour terminer l'action de la tête d'outil, comme l'arrêt de la broche. Vous avez accès à [next\_extruder](next_extruder.md) et [previous\_extruder](previous_extruder.md). previous\_extruder est le 'numéro d'extrudeuse' de l'outil de fraisage actuel, est égal à l'index \(commençant à 0\) de l'outil de fraisage plus le nombre d'extrudeuses. [Next\_extruder](next_extruder.md) est le 'numéro d'extrudeuse' de l'outil suivant, il peut être un extrudeuse normal, s'il est inférieur au nombre d'extrudeuses. Le nombre d' extrudeuses est disponible dans la variable [extruder](extruder.md) et le nombre d'outils de fraisage dans [milling\_cutter](milling_cutter.md).

La valeur de [milling\_count](milling_count.md) doit être &gt; 0 pour que le paramètre soit accessible.

[Vissza a változók listájához](../../variable_list)

