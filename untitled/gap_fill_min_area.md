# gap\_fill\_min\_area

* Technológia : FDM
* Csoport : [Réglages de l'Impression](../print_settings/print_settings.md)
* Alcsoport : [Périmètre et enveloppe](../print_settings/print_settings.md#périmètre-et-enveloppe)
* Mód : Szakértő

## _Remplir les trous entre les parois_ Surface minimum

### Leírás

Ce paramètre représente le minimum de mm² pour la création d’une extrusion de remplissage d’espace entre les parois.

> Peut être un % de \(largeur du périmètre\)²

Sur l'exemple ci dessous on peut voir que pour une largeur de [périmètre extérieure](external_perimeter_extrusion_spacing.md) de 0.4285 la valeur de filtration sur les bossages sera respectivement de 5,10,15 et 20 mm².

Exemple = bossage dimensions extérieures : 1.35 x 20 mm \(1.35-2x 0.4285\) x \(20-2x04285\) = 9.43 mm² -&gt; filtrage à _\*10 mm²_

Le paramètre est accessible si l'option \(Remplir les trous entre les parois\) [gap\_fill](gap_fill.mp) est active.

[Vissza a változók listájához](variable_list.md)

