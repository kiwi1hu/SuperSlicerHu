# between\_objects\_gcode

* Technológia : FDM
* Csoport : [Réglages de l'Imprimante](../printer_settings/printer_settings.md)
* Alcsoport : [G-Code personnalisé](../printer_settings/printer_settings.md#g-code-personnalisé)
* Mód : Szakértő

## Entre le G-Code des objets \( Pour une impression séquentielle\)

### Leírás

Ce code est inséré entre des objets lorsque vous utilisez l'impression séquentielle. Par défaut la température de l'extrudeuse et du plateau est réinitialisée et utilise la commande sans-attente; toutefois si des commandes M104, M109, M140 ou M190 sont détectées dans ce code personnalisé, SuperSlicer n'ajoutera pas de commandes de température. Notez que vous pouvez utiliser des variables Általánoss pour tous les réglages de SuperSlicer, donc vous pouvez entrer une commande "M109S\[ [first\_layer\_temperature](first_layer_temperature.md) \]" où vous le souhaitez.

[Vissza a változók listájához](variable_list.md)

