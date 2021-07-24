# Makrók

A SuperSlicer kétféle makró létrehozását teszi lehetővé az egyéni G-kód szakaszokban:

**Feltételes kiértékelés :**

```text
{if <condition_1>}<GCode_condition_1>[][{else}<GCode_else>]{endif}
```

**Kifejezés kiértékelése :**

```text
{<expression>}
```

Mindkét konstrukcióban a SuperSlicer konfigurációs változói névvel \(pl. `layer_z`\), a tömbváltozók elemei pedig szögletes zárójelek segítségével érhetők el \(pl. a `temperature[0]` az első extruder hőmérsékletére utal\).

A többdimenziós tömbök jelenleg csak egyszerű tömbváltozóként érhetőek el, ami egy string értéket eredményez \(pl. ha az `extruder_offset` változó 0x0,nx0 értéket tartalmaz, akkor csak \`extruder\_variable\[1\]-ként érhető el, ami egy \[n, 0\] string értéket eredményez - G-kódban megjeleníthető, de nem használható aritmetikai műveletekben\).

A karakterláncokat fordított vesszőkkel `"string"`, a reguláris kifejezéseket pedig perjelekkel `/` azonosítjuk. A karakterláncokat nem elemzi rekurzívan, azaz a szögletes zárójelek és a karakterláncokon belüli zárójelek megjelennek a kimeneten. Ez lehetővé teszi az olyan konstrukciókat, mint a \`{"\[zárójeles szöveg\]"}".

## Operátorok

A következő operátorok engedélyezettek :

1. Összehasonlítás

   ```text
    <,>, ==,! =, <>, <=,> =
   ```

   1. Példa :

      `{if layer_height == 0.2}; Csináljon valamit {endif}`

2. Boole-logika vagy annak megfelelői,

   ```text
    &&, ||,!
   ```

   1. Példa :

      `{if layer_height> 0.1 and first_layer_temperature [0]> 220}; Csináljon valamit {endif}`

3. Aritmetikai

   ```text
    +, -, 
   ```

   1. Példa :

      `M104 S {first_layer_temperature[0]2/3}`

      \(Megjegyezzük, hogy a first\_layer\_temperature egy tömb\)

4. Operátor [terner](https://hu.abcdef.wiki/wiki/Ternary_operation) `?`

   ```text
    <condition> ? <cond_true>:<cond_false>
   ```

   1. Példa :

      `M104 S {(first_layer_temperature [0]> 220? 230 : 200)}`

      Úgy tűnik, hogy ezt zárójelben kell elhelyezni, hogy működjön. Ez a kifejezés az extruder hőmérsékletét 230-ra vagy 200-ra állítja be, attól függően, hogy az első rétegnek 220° fölött kell-e lennie.

5. Szabályos kifejezések illesztése

   ```text
    = ~ (megfelel), ! ~ (nem felel meg)
   ```

6. A reguláris kifejezéseket perjelek \(/\) fogják körül. 1. Példa :

   ```text
        {if printer_notes=~/./};Printer is Prusa{endif}
   ```

## Funkciók

```text
Minimum min(a,b)

Maximum max(a,b)
```

## Skaláris változók

Ezek az értékek skalárisak és közvetlenül hivatkozhatók.

* printer\_notes \(string\)
* layer\_z \(csak a rétegváltás G-kódjában érhető el\)
* layer\_num \(csak a rétegváltás G-kódjában érhető el\)

## Változók tömb alakban

Ezek a változók tömbök, és a tömbindex megadásával kell őket elérni.

* temperature
* first\_layer\_temperature
* bed\_temperature \(jegyezzük meg, hogy ez egy táblázat, még akkor is, ha csak egy értéknek van értelme. : bed\_temperature\[0\]\)
* first\_layer\_bed\_temperature \(lásd a fenti megjegyzést \)

## Többdimenziós tömbök

Ezek a változók csak egyszerű tömbökként érhetők el, és nem használhatók aritmetikai kifejezésekben.

* extruder\_offset
* bed\_shape

## Példák

### Hőmérséklet fordulat

A "Rétegváltás előtt" egyéni G-kóddal lassan csökkentheti a hotend hőmérsékletét. Először is, használhatja az if/elseif/else kifejezést:

```text
{if layer_z < 10}M104 S265

{elsif layer_z <17}M104 S260

{elsif layer_z < 24}M104 S255

{elsif layer_z < 31}M104 S250

{elsif layer_z < 38}M104 S245

{elsif layer_z < 45}M104 S240

{endif}
```

Ugyanezt az eredményt egy rövidebb if/else/endif kifejezéssel is el lehet érni lineáris interpolációval:

```text
M104 S{if layer_z < 10}265{elsif layer_z > 45}240{else}265+(240-265)
```

Vagy használhatja a terner operátort :

```text
M104 S{(layer_z < 10) ? 265 : (layer_z > 45) ? 240 : 265+(240-265)(layer_z-10.0)/(45-10)}
```

A kód eredménye a G-kód testreszabási ablakban a réteg módosítása előtt

