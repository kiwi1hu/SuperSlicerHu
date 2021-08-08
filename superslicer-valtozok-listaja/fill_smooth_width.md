# fill\_smooth\_width

* Technológia : FDM
* Csoport : [Réglages de l'Impression](../print_settings/print_settings.md)
* Alcsoport : [Remplissage](../print_settings/print_settings.md#remplissage) - Options Haladós de remplissage
* Mód : Szakértő

## Espacement des lignes de lissage

### Leírás

Il s'agit de la largeur de la passe de lissage, en % de la largeur de l'extrusion du remplissage du dessus, ne doit pas être supérieure à 50% \(deux fois plus de lignes, 50% de chevauchement\). Il n'est pas nécessaire de descendre en dessous de 25% \(quatre fois plus de lignes, 75% de chevauchement\). Si vous avez des problèmes avec votre processus de lissage, n'oubliez pas de regarder le débit -&gt; débit au-dessus du pont, car ce paramètre doit être réglé à min 110% pour s'assurer d'avoir assez de plastique dans la couche du dessus. Une valeur trop basse fera que votre extrudeuse rognera le filament.

Option active si au moins un des motifs de remplissage [solid\_fill\_pattern](solid_fill_pattern.md) , [top\_fill\_pattern](top_fill_pattern.md) ou [bottom\_fill\_pattern](bottom_fill_pattern.md) est réglé sur lissage.

* Valeur par défaut : 50 %

[Vissza a változók listájához](variable_list.md)

