# extrusion\_width

* Technológia : FDM
* Csoport : [Réglages de l'Impression](../print_settings/print_settings.md)
* Alcsoport : [Largeur et Débit](../print_settings/print_settings.md#largeur-et-débit) - Largeur d'extrusion
* Mód : Haladó

## Largeur d'extrusion

### Leírás

Définissez ce paramètre à une valeur non nulle pour définir une largeur d'extrusion manuellement. S'il est laissé à zéro, SuperSlicer dérive les largeurs d'extrusion à partir du [diamètre de la buse](nozzle_diameter.md) \(voir les info bulles pour la largeur d'[extrusion du périmètre](perimeter_extrusion_width.md), la [largeur d'extrusion du remplissage](infill_extrusion_width.md), etc\).

Si elle est exprimée en pourcentage \(par exemple : 105%\), elle sera calculée sur le [diamètre de la buse](nozzle_diameter.md).

Vous pouvez définir soit [_**Espacement**_](extrusion_spacing.md), soit [_**Largeur**_](extrusion_width.md) ; l'autre sera calculée en utilisant les pourcentages de [Chevauchement du périmètre](perimeter_overlap.md) et la [hauteur de couche](layer_height.md) par défaut.

[Vissza a változók listájához](variable_list.md)
