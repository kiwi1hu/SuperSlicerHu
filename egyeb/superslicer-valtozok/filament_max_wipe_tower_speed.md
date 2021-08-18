# filament\_max\_wipe\_tower\_speed

* Technológia : FDM
* Csoport : [Szál beállítások](../filament_settings/filament_settings.md)
* Alcsoport : [Többanyagú](../filament_settings/filament_settings.md#multimatériaux) - [Tisztítótorony paraméterei](filament_max_wipe_tower_speed.md)
* Mód : Szakértő
* Mértékegység : %
* Minimális érték :  0
* Maximális érték :  200
* Alapértelmezett érték : 0

## Maximális sebesség a tisztítótornyon

### Leírás

Ez a paraméter a maximális sebesség beállítására szolgál, amikor a tisztítótoronyban extrudál \(használja az M220-at\). A %-ban állítsa 0-ra a letiltáshoz, és használja helyette a szál típusát.

Ha deaktiválják őket, az ilyen típusú szálak alapértelmezett értékűek lesznek:

* PVA    : 60% és 80% között
* SCAFF  : 35%
* FLEX   : 35%
* EGYÉB  : 100%

  Vegye figyelembe, hogy a tisztítótorony minden esetben 100%-ra állítja vissza a sebességet a kihúzáshoz.

> Ha Marlin-t használ, az M220 B/R a isztítótorony nyomtatása előtti sebességmentésre szolgál.

[Vissza a változók listájához](/)

