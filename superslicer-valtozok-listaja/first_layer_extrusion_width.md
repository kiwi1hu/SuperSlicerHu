# first\_layer\_extrusion\_width

* Technológia : FDM
* Csoport : [Réglages de l'Impression](../print_settings/print_settings.md)
* Alcsoport : [Largeur et Débit](../print_settings/print_settings.md#largeur-et-débit) - Largeur d'extrusion
* Mód : Haladó

## _Première couche_ Largeur

### Leírás

Définissez ce paramètre à une valeur non nulle pour définir une largeur d'extrusion manuelle pour la première couche. Vous pouvez l'utiliser pour forcer des cordons plus gros pour une meilleure adhérence.

Si elle est exprimée en pourcentage \(par exemple 140%\), elle sera calculée sur le [diamètre de la buse](nozzle_diameter.md) utilisée pour le type d'extrusion.

> Si elle est définie à zéro, il utilisera la largeur d'extrusion par défaut.

Vous pouvez définir soit [_**Espacement**_](first_layer_extrusion_spacing.md), soit [_**Largeur**_](first_layer_extrusion_width.md) ; l'autre sera calculée en utilisant les pourcentages de [Chevauchement du périmètre](perimeter_overlap.md) et la [hauteur de couche](layer_height.md) par défaut.

* Valeur par défaut : 140 %

[Vissza a változók listájához](variable_list.md)

