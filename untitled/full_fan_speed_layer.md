# full\_fan\_speed\_layer

* Technológia : FDM
* Csoport : [Réglages du Filament](../filament_settings/filament_settings.md)
* Alcsoport : [Refroidissement](../filament_settings/filament_settings.md#refroidissement) - Vitesse du ventilateur par défaut
* Mód : Szakértő

## Ventilateur à pleine vitesse pour la couche

### Leírás

La vitesse du ventilateur va augmenter de façon linéaire en partant de zéro pour la couche [disable\_fan\_first\_layers](disable_fan_first_layers.md) jusqu'au maximum pour la couche [full\_fan\_speed\_layer](full_fan_speed_layer.md). [full\_fan\_speed\_layer](full_fan_speed_layer.md) sera ignorée si inférieure à [disable\_fan\_first\_layers](disable_fan_first_layers.md), auquel cas le ventilateur fonctionnera à la vitesse maximum autorisée pour la couche [disable\_fan\_first\_layers](disable_fan_first_layers.md) +1.

[Vissza a változók listájához](variable_list.md)

