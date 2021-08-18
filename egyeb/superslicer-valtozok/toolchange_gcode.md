# toolchange\_gcode

* Technológia : FDM
* Csoport : [Nyomtató beállítások](../../beallitasok/printer_settings.md)
* Alcsoport : [Egyedi G-kód](../../beallitasok/printer_settings.md#g-code-personnalisé)
* Mód : Szakértő

## G-Code de changement d'extrudeuse

### Leírás

Ce code personnalisé est inséré à chaque changement d'extrudeuse. Si vous ne laissez pas ce champ vide, vous devrez vous occuper du code de changement de la buse vous-même. SuperSlicer ne fournira aucun autre code G pour changer le filament. Vous pouvez utiliser des variables de substitution pour tous les paramètres SuperSlicer, ainsi que pour \[previous\_extruder\] et \[next\_extruder\], par exemple. La commande standard toolchange peut être écrite sous la forme T \[[next\_extruder](next_extruder.md)\].

**!! Attention !! Si un quelconque caractère est écrit ici, Slic3r n'écrira aucun G-code de changement de buse par lui-même.**

[Vissza a változók listájához](/)

