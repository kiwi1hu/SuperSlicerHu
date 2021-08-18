# external\_perimeters\_vase

* Technológia : FDM
* Csoport : [Nyomtatási beállítások](../../../konfig/print_settings)
* Alcsoport : [Kerület és héj](../../beallitasok/print_settings.md#périmètre-et-enveloppe) - [Először a külső kerületet](external_perimeters_vase.md)
* Mód : Szakértő

## Váza mód

### Leírás

Nyomtasson kontúrkörvonalakat két körben, folyamatos módon, mint a spirál vázánál. A működéshez szüksége van a [először a külső kerületeket](external_perimeters_first.md) paraméterre. Nem működik az első rétegnél, mivel az ágyat túlságosan megrongálhatja. Ne feledje, hogy a hardver beállításokba megadott [min rétegmagasság](min_layer_height.md) értéket fogja használni alapmagasságként \(nem 0-ról indul\). Ezért mindenképpen adja meg a lehető legalacsonyabb értéket, amelyet a nyomtatója kezelni tud. Ha a magassága nem kisebb, mint az aktuális réteg magasságának kétszerese, akkor a normál algoritmus kerül alkalmazásra, mivel nincs elég hely két ciklus végrehajtásához. Például ahhoz, hogy ez az algoritmus valódi hatást gyakoroljon, a minimális magasságnak legalább 0,05-nek kell lennie 0,2 rétegmagasság esetén.

[Vissza a változók listájához](../../variable_list)

