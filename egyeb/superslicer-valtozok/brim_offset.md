# brim\_offset

* Technológia : FDM
* Csoport : [Nyomtatási beállítások](../../konfig/print_settings.md)
* Alcsoport : [Szoknya és perem](../../konfig/print_settings.md#szoknyaésperem) - [Perem](../../konfig/print_settings.md#perem)
* Mód : Szakértő
* Mértékegység : mm
* Minimális érték :  0
* Alapértelmezett érték : 0

## Eltolt perem

### Leírás

A perem és az alkatrész közötti távolság. Normális esetben az értéket 0-nál kell tartani, hacsak nem okoz nagy nehézséget a perem és a modell szétválasztása.

A távolságot kivonjuk a [Peremszélesség](../brim_width) és a [Belső peremszélesség](../brim_width_interior) értékekből, tehát kisebbnek kell lennie ezeknél.

Ennek a távolságnak az a célja, hogy megkönnyítse a modell peremének eltávolítását. Ha a peremeket kissé távolabb helyezzük a tényleges modelltől \(fél vonalnyi távolságra\), a perem és a modell közötti kapcsolat gyengébb lesz, mint egy réteg, így az peremek könnyebben eltávolíthatók. Ez csökkenti a hegesedést vagy az "elefántlábat" is, amelyet az eltávolítás után a perem hagyott maga után. Ez a módszer különösen akkor hatékony, ha a [kezdeti rétegmagasság](../initial_layer_height) nagyobb, mivel a vastag peremet általában nehezebb eltávolítani. Másrészt csökkenti a perem hatékonyságát a modellnek az ágyhoz való tapadásában.

[Vissza a változók listájához](/)

