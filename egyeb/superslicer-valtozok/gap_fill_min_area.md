# gap\_fill\_min\_area

* Technológia : FDM
* Csoport : [Nyomtatási beállítások](../../konfig/print_settings.md)
* Alcsoport : [Kerület és héj](../../beallitasok/print_settings.md#périmètre-et-enveloppe)- [Haladó](gap_fill_min_area.md)
* Mód : Szakértő
* Minimális érték :  0

## Minimális hézagkitöltő felület

### Leírás

Ez a paraméter a falak közötti hézagkitöltő extrudálás létrehozásához szükséges minimális mm²-t jelenti.

> Lehet a \(kerület szélességének\)² %-a.

Az alábbi példában látható, hogy a 0,4285 szélességű [külső kerület](external_perimeter_extrusion_spacing.md) esetén a szűrési érték a csúcsokon

Példa = külső méretei: 1,35 x 20 mm \(1,35-2x 0,4285\) x \(20-2x04285\) = 9,43 mm² -&gt; szűrés _\*10 mm²-en_

A paraméter akkor érhető el, ha a [falak közötti lyukak kitöltése](gap_fill.mp) opció aktív.

[Vissza a változók listájához](/)

