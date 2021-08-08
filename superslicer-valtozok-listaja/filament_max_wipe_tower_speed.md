# filament\_max\_wipe\_tower\_speed

* Technológia : FDM
* Csoport : [Réglages du Filament](../filament_settings/filament_settings.md)
* Alcsoport : [Multimatériaux](../filament_settings/filament_settings.md#multimatériaux) - Paramètres de la tour de purge
* Mód : Szakértő

## Vitesse maximum de la tour de purge

### Leírás

Ce paramètre est utilisé pour définir la vitesse maximale lors de l'extrusion à l'intérieur de la tour de purge \(utilisez M220\). En %, mettez 0 pour désactiver et utiliser le type de filament à la place.

S'ils sont désactivés, ces types de filaments auront une valeur par défaut de:

* PVA    : 80% à 60%
* SCAFF  : 35%
* FLEX   : 35%
* AUTRES : 100%

  Notez que la tour de purge réinitialise la vitesse à 100% pour le débrayage dans tous les cas.

> Si vous utilisez Marlin, M220 B/R est utilisé pour sauvegarder la vitesse avant l'impression de la tour de purge.

[Vissza a változók listájához](variable_list.md)

