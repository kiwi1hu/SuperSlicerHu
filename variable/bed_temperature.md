# bed_temperature

* Technológia : FDM
* Csoport: Szál beállítások
* Alcsoport : Hőmérséklet

## Ágy hőmérséklet (Egyéb rétegek)

### Leírás

Egyes nyomtatók fűtött nyomtatóággyal rendelkeznek. Ez a beállítás határozza meg az ágy hőmérsékletét.

Az ágy melegítésekor az anyag kissé folyékony és ragadós marad. Egyes anyagok hűtéskor kikristályosodnak, aminek következtében az anyag hűtéskor jelentősen zsugorodik. A fűtött ágy az anyagot éppen a kikeményedési hőmérséklet felett tartja, hogy megakadályozza ezt a zsugorodást. Ennek célja, hogy javítsa a nyomat tapadását a nyomólemezhez. Az [első réteg nyomtatása](first_layer_temperature.md) során más fűtési hőmérséklet értéket is be lehet állítani.

Ha azonban az ágyat túl forrón tartják, a nyomtatás nagyon folyós lesz az ágy érintkezési felületén. Az anyag ekkor egy kicsit megereszkedik, így a lenyomat alsó oldala úgy néz ki, mint egy elefántláb. Ez kompenzálható az [XY kompenzáció első réteg](first_layer_size_compensation.md) paraméterrel, de ez befolyásolja a méretpontosságot. Az ágy  felmelegedése hőmérséklet-különbséget hoz létre az ágyon fekvő és a modellben feljebb lévő anyag között, ami a magasabb anyag zsugorodásával megvetemedést okoz.

* Mértékegység : °C
* Minimális érték : 0
* Maximális érték : 300
* Alapértelmezett érték : 0
