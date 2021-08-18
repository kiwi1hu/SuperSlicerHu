# milling\_diameter

* Technológia : FDM
* Csoport : [Nyomtató beállítások](../../beallitasok/printer_settings.md)
* Alcsoport : [Milling](../../beallitasok/printer_settings.md#milling) - Taille
* Mód : Haladó

## Diamètre de fraisage

### Leírás

Diamètre de l'outil de fraisage. Le paramètre est disponible sous le forme de tableau.

Exemple d'appel du diamètre de fraisage `M6 T {current_extruder} D{milling_diameter[next_extruder]}`

La valeur de [milling\_count](milling_count.md) doit être &gt; 0 pour que le paramètre soit accessible.

[Vissza a változók listájához](../../variable_list)

