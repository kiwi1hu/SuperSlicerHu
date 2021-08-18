# perimeter\_bonding

* Technológia : FDM
* Csoport : [Nyomtatási beállítások](../../../konfig/print_settings)
* Alcsoport : [Kerület és héj](../../beallitasok/print_settings.md#périmètre-et-enveloppe) - [Először a külső kerületet](perimeter_bonding.md)
* Mód : Szakértő
* Mértékegység : %
* Minimális érték :  0
* Maximális érték :  50
* Alapértelmezett érték : 0

## Jobb kötés

### Leírás

Ez a beállítás egy kicsit ronthatja a külső keretek minőségét, cserébe a keretek közötti jobb kötésért. Akkor használja, ha nagy nehézségei vannak a kerületi tapadással, például magas hőmérsékletű szálakkal. Ez a százalék a kerület átfedés %-ában, kicsit olyan, mint a [kerületi átfedés](perimeter_overlap.md) és a [külső kerületi átfedés](external_perimeter_overlap.md), de fordítva. A [kerületi átfedés](perimeter_overlap.md) és a [külső kerületi átfedés](external_perimeter_overlap.md) értékeket 100%-ra kell állítani, különben ennek a beállításnak nincs hatása.

> 0: nincs hatása, 50%: a fúvóka fele egy már extrudált kerület felett lesz egy új kerület extrudálása során, kivéve, ha az egy külső kerület.

Ez a beállítás nagyon kísérleti jellegű, kérjük, számoljon be a hasznosságáról. Eltávolítható, ha nincs rá szükség.

[Vissza a változók listájához](../../variable_list)

