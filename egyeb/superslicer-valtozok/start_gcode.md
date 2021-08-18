# start\_gcode

* Technológia : FDM & SLA
* Csoport : [Nyomtató beállítások](../../beallitasok/printer_settings.md)
* Alcsoport : [Egyedi G-kód](../../beallitasok/printer_settings.md#g-code-personnalisé)
* Mód : Szakértő

## G-Code de début

### Leírás

Cette procédure de démarrage est insérée au début, après que le plateau ait atteint la température cible et que l'extrudeuse vient de commencer à chauffer, et avant que l'extrudeuse n'ait fini de chauffer. Si Slic3r détecte M104 ou M190 dans vos codes personnalisés, ces commandes ne seront pas ajoutées automatiquement, vous êtes donc libre de personnaliser l'ordre des commandes de chauffage et des autres actions personnalisées. Notez que vous pouvez utiliser des variables de remplacement pour tous les paramètres Slic3r, vous pouvez donc mettre un \"M109 S[first\_layer\_temperature](first_layer_temperature.md)\" commande où vous voulez. Autres variables disponiblent : [initial\_extruder](initial_extruder.md), [total\_layer\_count](total_layer_count.md), [has\_wipe\_tower](has_wipe_tower.md), [has\_single\_extruder\_multi\_material\_priming](has_single_extruder_multi_material_priming.md), [total\_toolchanges](total_toolchanges.md), bounding\_box\[minx,miny,maxx,maxy\]"

[Vissza a változók listájához](/)

