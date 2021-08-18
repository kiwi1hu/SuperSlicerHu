# start\_filament\_gcode

* Technológia : FDM
* Csoport : [Szál beállítások](../filament_settings/filament_settings.md)
* Alcsoport : [Egyedi G-kód](../../beallitasok/printer_settings.md#g-code-personnalisé)
* Mód : Szakértő

## G-Code de début

### Leírás

Cette procédure de démarrage est insérée au début, après un gcode de démarrage de l'imprimante \(et après tout changement de filaments vers ce filament, si vous utilisez l'option multi-matériaux\).

Elle est utilisée pour remplacer les réglages pour un filament spécifique.

Si SuperSlicer détecte des commandes M104, M109, M140 ou M190 dans vos codes personnalisés ces commandes ne seront pas ajoutées automatiquement, de cette manière vous pouvez personnaliser la procédure de chauffe et autres actions.

Notez que vous pouvez utiliser des variables Általánoss pour tous les réglages de SuperSlicer, donc vous pouvez saisir une commande "M109 S\[[first\_layer\_temperature](first_layer_temperature.md)\] " où vous voulez.

Si vous avez plusieurs extrudeuses, le G-Code sera exécuté dans l'ordre des extrudeuses.

[Vissza a változók listájához](/)

