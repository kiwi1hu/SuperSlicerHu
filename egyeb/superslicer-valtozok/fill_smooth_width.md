# fill\_smooth\_width

* Technológia : FDM
* Csoport : [Nyomtatási beállítások](../../konfig/print_settings.md)
* Alcsoport : [Kitöltés](../../beallitasok/print_settings.md#remplissage) - [Speciális kitöltési lehetőségek](fill_smooth_width.md)
* Mód : Szakértő
* Mértékegység : mm/%
* Minimális érték :  0
* Alapértelmezett érték : 50 %

## A vasalási vonalak közötti távolság

### Leírás

Ez a vasalási menet szélessége, a felső töltelék extrudálás szélességének %-ában, nem lehet több mint 50% \(kétszer több vonal, 50%-os átfedés\). Nem szükséges 25% alá menni \(négyszer több vonal, 75%-os átfedés\). Ha problémái vannak a vasalással, ne felejtse el megnézni a áramlás -&gt;híd feletti áramlást, mivel ezt a beállítást minimum 110%-ra kell állítani, hogy elegendő műanyag legyen a felső rétegben. A túl alacsony értéktől az extruder megeszi a filamentet.

Az opció akkor aktív, ha a töltési minták közül legalább az egyik [Tömör kitöltési minta](solid_fill_pattern.md) , [Felső kitöltési minta](top_fill_pattern.md) vagy [Alsó kitöltési minta](bottom_fill_pattern.md) vasalásra van állítva.

[Vissza a változók listájához](/)

