# feature\_gcode

* Technológia : FDM
* Csoport : [Nyomtató beállítások](../../beallitasok/printer_settings.md)
* Alcsoport : [Egyedi G-kód](../../beallitasok/printer_settings.md#g-code-personnalisé)
* Mód : Szakértő

## Extrudálás típus változás G-kód

### Leírás

Ez az egyéni kód minden egyes alkalommal beillesztésre kerül, amikor az extrudálás típusa megváltozik. Vegye figyelembe, hogy a helyettesítő változókat használhatja az összes SuperSlicer paraméterhez, valamint a [rétegszám](), [réteg Z magassága](layer_z.md) et [extrudálás típusa](extrusion_role.md) amelyek felvehetik ezeket a karakterlánc-értékeket:

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

A vegyes csak akkor használatos, ha az extrudálás szerepe nem egyedi, nem csak egy kategóriába tartozik vagy nem ismert.

[Vissza a változók listájához](../../variable_list)

