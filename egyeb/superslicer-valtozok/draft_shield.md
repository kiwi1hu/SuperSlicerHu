# draft\_shield

* Technológia : FDM
* Csoport : [Nyomtatási beállítások](../../konfig/print_settings.md)
* Alcsoport : [Szoknya és perem](../../konfig/print_settings.md#szoknya-es-perem) - [Szoknya](../../konfig/print_settings.md#szoknya)
* Mód : Haladó 

## Légáramlási pajzs

### Leírás

Ha aktiválva van, a szoknya olyan magas lesz, mint a legmagasabb nyomtatott tárgy. Ez az ABS vagy ASA nyomatok védelmét szolgálja a deformálódástól vagy a nyomtatólemez leválásától a légáramlás miatt.

A pajzsnak több jelentős hatása van a nyomatra:

* Ez állandóbbá teszi a nyomtatás hőmérsékletét. Ez a pajzs kívánt hatása. Ezért csökkenteni kell a helyiség hőmérséklet-változásaiból eredő hibákat.
* Általában a pajzs belsejében magasabb a hőmérséklet. Ennek oka, hogy a hő nehezebben tud távozni, és nem alakulhatnak ki konvekciós áramlatok, amelyek a nyomtatásból származó forró levegővel együtt emelkednek fel. Ez a nyomtatás minden aspektusára hatással van. Különösen több lesz a zsinórosodás és a megereszkedés.
* A nyomtatófej ventilátorai kevésbé hatékonyak lesznek. A pajzs ezen a ponton is akadályozza a légáramlást. A nyomtatófejen lévő ventilátorok hatékonyságának növelése érdekében a pajzs távolsága \([skirt\_distance](skirt_distance.md)\) növelhető.
* A pajzs kerületének számát a szoknyához hasonlóan a hurkok száma \([skirts](skirts.md)\) határozza meg.
* A pajzs tisztítótoronyként használható. Mivel a pajzsot a tárgy előtt nyomtatják ki, a pajzs nyomtatása az anyag megtisztításának egy módja, mielőtt elkezdené az új réteg nyomtatását. Meg kell jegyezni, hogy annyi peremre van szükség, ahány extruder fut, hogy minden extruder tisztítható legyen a pajzson. Ebben az esetben a pajzsot nem nyomtatják ki teljesen az alkatrész előtt, hanem minden kerületet kinyomtatnak, amikor egy új extruder kiürül.

[Vissza a változók listájához](./)

