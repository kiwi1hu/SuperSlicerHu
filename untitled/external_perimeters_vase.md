# external\_perimeters\_vase

* Technológia : FDM
* Csoport : [Réglages de l'Impression](../print_settings/print_settings.md)
* Alcsoport : [Périmètre et enveloppe](../print_settings/print_settings.md#périmètre-et-enveloppe) - Périmètre extérieur en premier
* Mód : Szakértő

## En Mód vase

### Leírás

Imprimez les périmètres de contour en deux cercles de manière continue, un peu comme pour le Mód vase. Il faut que le paramètre [external\_perimeters\_first](external_perimeters_first.md) soit actif. Ne fonctionne pas pour la première couche, car cela pourrait endommager le plateau. Remarquez qu'il utilisera [min\_layer\_height](min_layer_height.md) de votre configuration matérielle comme hauteur de base \(elle ne commence pas à 0\). Veillez donc à indiquer la valeur la plus basse possible que votre imprimante puisse gérer. Si sa hauteur n'est pas inférieure à deux fois la hauteur actuelle de la couche, l'algorithme normal est utilisé, car il n'y a pas assez de place pour effectuer deux boucles. Par exemple, pour que cet algorithme ai un vrai impact, il faut que la hauteur minimale soit au moins à 0.05 pour une hauteur de couche de 0.2.

[Vissza a változók listájához](variable_list.md)

