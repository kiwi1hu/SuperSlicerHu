# feature\_gcode

* Technológia : FDM
* Csoport : [Réglages de l'Imprimante](../printer_settings/printer_settings.md)
* Alcsoport : [G-Code personnalisé](../printer_settings/printer_settings.md#g-code-personnalisé)
* Mód : Szakértő

## G-Code après changement de couche

### Leírás

Ce code personnalisé est inséré à chaque changement de type d'extrusion. Notez que vous pouvez utiliser des variables de substitution pour tous les paramètres SuperSlicer, ainsi que pour [layer\_num](layer_num.md), [layer\_z](layer_z.md) et [extrusion\_role](extrusion_role.md) pouvant prendre ces valeurs de chaîne:

* Perimeter
* ExternalPerimeter
* OverhangPerimeter
* InternalInfill
* SolidInfill
* TopSolidInfill
* BridgeInfill
* GapFill
* Skirt
* SupportMaterial
* SupportMaterialInterface
* WipeTower
* Mixed

Mixed n'est utilisé que lorsque le rôle de l'extrusion n'est pas unique, pas uniquement dans une catégorie ou n'est pas connu.

[Vissza a változók listájához](variable_list.md)

