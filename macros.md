# Makrók

A SuperSlicer kétféle makró létrehozását teszi lehetővé az egyéni G-kód szakaszokban:  

**Feltételes értékelés :**

```text
{if <condition_1>}<GCode_condition_1>[][{else}<GCode_else>]{endif}
```

**A kifejezés kiértékelése :**

```text
{<expression>}
```

Mindkét konstrukcióban a SuperSlicer konfigurációs változói névvel \(pl. `layer_z`\), a tömbváltozók elemei pedig szögletes zárójelek segítségével érhetők el \(pl. `temperature[0]` az első extruder hőmérsékletére utal\).

A többdimenziós tömbök jelenleg csak egyszerű tömbváltozóként érhetőek el, ami egy string értéket eredményez \(pl. ha az `extruder_offset` változó 0x0,nx0 értéket tartalmaz, akkor csak `extruder_variable[1]`-ként érhető el, ami egy string értéket \[n, 0\] eredményez - megjeleníthető a G-kódban, de nem használható aritmetikai műveletekben\).

Les chaînes sont identifiées par des guillemets `"chaîne"` et les expressions régulières par des barres obliques `/` . Les chaînes ne sont pas analysées récursivement, c'est-à-dire que les crochets et les crochets à l'intérieur des chaînes apparaîtront dans la sortie. Cela permet des constructions telles que `{"[texte entre crochets]"}`

## Opérateurs

Les opérateurs suivants sont autorisés :

1. Comparaison

   ```text
    <,>, ==,! =, <>, <=,> =
   ```

   1. Exemple :

      `{if layer_height == 0.2}; Faire quelque chose {endif}`

2. Logique booléenne ou les équivalents,

   ```text
    &&, ||,!
   ```

   1. Exemple :

      `{if layer_height> 0.1 and first_layer_temperature [0]> 220}; Faire quelque chose {endif}`

3. Arithmétique

   ```text
    +, -, 
   ```

   1. Exemple :

      `M104 S {first_layer_temperature[0]2/3}`

      \(Notez que first\_layer\_temperature est un tableau\)

4. Opérateur [ternaire](https://fr.wikipedia.org/wiki/Op%C3%A9ration_ternaire#:~:text=En%20informatique%2C%20un%20op%C3%A9rateur%20ternaire,qui%20d%C3%A9finit%20une%20expression%20conditionnelle.) `?`

   ```text
    <condition> ? <cond_true>:<cond_false>
   ```

   1. Exemple :

      `M104 S {(first_layer_temperature [0]> 220? 230 : 200)}`

      Cela semble devoir être placé entre parenthèses pour fonctionner. . Cette expression règle la température de l'extrudeur à 230 ou 200 selon que la première couche doit être supérieure à 220°.

5. Correspondance d'expressions régulières

   ```text
    = ~ (correspondant), ! ~ (ne correspondant pas)
   ```

6. Les expressions régulières sont placées entre des barres obliques /. 1. Exemple :

   ```text
        {if printer_notes=~/./};Printer is Prusa{endif}
   ```

## Fonctions

```text
Minimum min(a,b)

Maximum max(a,b)
```

## Variables scalaires

Ces valeurs sont scalaires et peuvent être directement référencées.

* printer\_notes \(chaîne\)
* layer\_z \(uniquement disponible dans le G-Code de changement de couche\)
* layer\_num \(uniquement disponible dans le G-Code de changement de couche\)

## Variables sous forme de tableau

Ces variables sont des tableaux et doivent être accédées en indiquant l'indice du tableau.

* temperature
* first\_layer\_temperature
* bed\_temperature \(notez qu'il s'agit d'un tableau, même si une seule valeur a du sens : bed\_temperature\[0\]\)
* first\_layer\_bed\_temperature \(voir remarque ci-dessus \)

## Tableaux multidimensionnels

Ces variables ne sont accessibles que sous forme de tableaux simples et ne peuvent pas être utilisées dans les expressions arithmétiques.

* extruder\_offset
* bed\_shape

## Exemples

### Tour de température

Vous pouvez utiliser le G-code personnalisé "Avant changement de couche" pour diminuer lentement la température de la hotend. Tout d'abord, on peut utiliser l'expression if/elseif/else :

```text
{if layer_z < 10}M104 S265

{elsif layer_z <17}M104 S260

{elsif layer_z < 24}M104 S255

{elsif layer_z < 31}M104 S250

{elsif layer_z < 38}M104 S245

{elsif layer_z < 45}M104 S240

{endif}
```

Le même résultat peut être obtenu par une expression if/else/endif plus courte avec une interpolation linéaire :

```text
M104 S{if layer_z < 10}265{elsif layer_z > 45}240{else}265+(240-265)
```

Ou on peut utiliser l'opérateur ternaire :

```text
M104 S{(layer_z < 10) ? 265 : (layer_z > 45) ? 240 : 265+(240-265)(layer_z-10.0)/(45-10)}
```

A kód eredménye a G-kód testreszabási ablakban a réteg módosítása előtt

