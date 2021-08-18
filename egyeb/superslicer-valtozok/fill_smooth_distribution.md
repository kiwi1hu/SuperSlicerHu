# fill\_smooth\_distribution

* Technológia : FDM
* Csoport : [Nyomtatási beállítások](../../konfig/print_settings.md)
* Alcsoport : [Kitöltés](../../beallitasok/print_settings.md#remplissage) - [Speciális kitöltési lehetőségek](fill_smooth_distribution.md)
* Mód : Szakértő
* Mértékegység : %
* Alapértelmezett érték : 10

## Vasalási áramlás

### Leírás

Ez az áramlás százalékos aránya, amelyet a második vasalási menethez használnak fel. Tipikusan 10-20%. Nem lehet nagyobb, mint 20%, kivéve, ha a felső extrudálás szélessége jóval nagyobb, mint a fúvóka szélessége. Egy túl alacsony érték és az extruder megeszi a szálakat. Túl magas érték esetén az első menet nem fog jól nyomtatni.

Az opció akkor aktív, ha a töltési minták közül legalább az egyik [Tömör kitöltési minta](solid_fill_pattern.md) , [Felső kitöltési minta](top_fill_pattern.md) vagy [Alsó kitöltési minta](bottom_fill_pattern.md) vasalásra van állítva.

[Vissza a változók listájához](/)

