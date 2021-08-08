# perimeter\_bonding

* Technológia : FDM
* Csoport : [Réglages de l'Impression](../print_settings/print_settings.md)
* Alcsoport : [Périmètre et enveloppe](../print_settings/print_settings.md#périmètre-et-enveloppe) - Périmètre extérieur en premier
* Mód : Szakértő

## Une meilleur liaison

### Leírás

Ce réglage peut dégrader un peu la qualité de votre périmètre externe, en échange d'une meilleure liaison entre les périmètres. Utilisez-le si vous avez de grandes difficultés avec le collage des périmètres, par exemple avec des filaments à haute température. Ce pourcentage est le % de chevauchement entre les périmètres, un peu comme [perimeter\_overlap](perimeter_overlap.md) et [external\_perimeter\_overlap](external_perimeter_overlap.md), mais en sens inverse. Vous devez définir [perimeter\_overlap](perimeter_overlap.md) et [external\_perimeter\_overlap](external_perimeter_overlap.md) à 100 %, sinon ce paramètre n'a aucun effet.

> 0 : aucun effet, 50% : la moitié de la buse sera au-dessus d'un périmètre déjà extrudé pendant l'extrusion d'un nouveau périmètre, sauf s'il s'agit d'un périmètre externe.

Ce paramètre est très expérimental, veuillez faire un rapport sur l'utilité. Il peut être supprimé s'il n'y a pas d'utilité pour ça.

[Vissza a változók listájához](variable_list.md)

