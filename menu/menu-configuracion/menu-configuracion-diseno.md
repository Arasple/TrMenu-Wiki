---
description: Configurar diseño del menú
---

# Diseño

### I. Diseño del menú

* Cada símbolo o letra representa un botón del menú
* Si un botón tiene 2 letras o más en su identificador entonces debes escribirlo como \`ID\`, por ejemplo ```boton1```
* Al repetir símbolos hace que el botón se vea en varios espacios al mismo tiempo
* Cada línea define el tamaño del menú \(suponiendo que el tipo de inventario sea **CHEST**\)

**Formas de escribirlo**

* **Normal:** Layout
* **RegEx:** \(layout\|shape\)\(s\)?

{% tabs %}
{% tab title="CHEST 1" %}
```yaml
#Acomodar los items en un menú normal de 5 líneas
Layout:
  - '########C'
  - ' QTRMENU '
  - '   SAP   '
  - '         '
  - '#########'
```
{% endtab %}

{% tab title="CHEST 2" %}
```yaml
#Acomodar los items en un menú normal de 5 líneas
Layout: ['########C',' QTRMENU ','   SAP   ','         ','#########']
```
{% endtab %}

{% tab title="OTROS 1" %}
```yaml
#Acomodar los items para un menú tipo DISPENSER o DROPPER
Shape:
  - '###'
  - 'ABC'
  - '##X'
```
{% endtab %}

{% tab title="OTROS 2" %}
```yaml
#Acomodar los items para un menú tipo DISPENSER o DROPPER
Shape: ['###','ABC','##X']
```
{% endtab %}
{% endtabs %}

**Múltiples páginas**

* TrMenu tiene la opción de hacer varios diseños diferentes para que el menú tenga varias páginas.
* La primer página se define como la página 0
* Si quieres obtener la página actual del menú puedes escribir `{shape}` en el título del menú o en cualquier otro texto del menú.
* Si quieres obtener el número de página +1, osea que la página 0 será la 1, la página 1 será la 2.. etc. Puedes escribir `{page}`.

{% tabs %}
{% tab title="FORMA 1" %}
```yaml
Layout: 
  # {shape} = 0 | {page} = 1
  - - '+++++++++'
    - '+ABCDEFG+'
    - '+++++++++'
  # {shape} = 1 | {page} = 2
  - - '+++++++++'
    - '+HIJKLMN+'
    - '+++++++++'
```
{% endtab %}

{% tab title="FORMA 2" %}
```yaml
Layout: 
  # {shape} = 0 | {page} = 1
  - ['+++++++++','+ABCDEFG+','+++++++++']
  # {shape} = 1 | {page} = 2
  - ['+++++++++','+HIJKLMN+','+++++++++']

# También se puede acomodar de esta forma:
Layout: 
  - ['+++++++++',
     '+ABCDEFG+',
     '+++++++++']
  - ['+++++++++',
     '+HIJKLMN+',
     '+++++++++']
```
{% endtab %}

{% tab title="FORMA 3" %}
```yaml
Layout: [
['+++++++++','+ABCDEFG+','+++++++++'],
['+++++++++','+HIJKLMN+','+++++++++']]

# También se puede acomodar de esta forma:
Layout: [
['+++++++++',
 '+ABCDEFG+',
 '+++++++++'],
['+++++++++',
 '+HIJKLMN+',
 '+++++++++']]
```
{% endtab %}
{% endtabs %}

### II. Diseño del inventario del jugador \(Opcional\)

* Además de editar el menú que abres, también puedes convertir el inventario del jugador como parte del menú mientras tengas el menú abierto.
* Para acomodar los botones se siguen las mismas reglas del diseño del menú, excepto el tamaño ya que el inventario del jugador solo tiene 4 líneas.
* Para evitar que se muestren los ítems del jugador dentro del menú puedes añadir la opción `Hide-Player-Inv` en el apartado de opciones del menú.
* También se pueden hacer múltiples páginas en el diseño del inventario del jugador usando el mismo concepto del diseño del menú.

**Formas de escribirlo**

* **Normal:** PlayerInventory
* **RegEx:** \(layout\|shape\)\(-\)?player\(-\)?inv\(entory\)?\(s\)?

{% tabs %}
{% tab title="FORMA 1" %}
```yaml
PlayerInventory:
  - '         '
  - ' A B C D '
  - '      2  '
  - '  1      '
```
{% endtab %}

{% tab title="FORMA 2" %}
```yaml
PlayerInventory: ['         ',' A B C D ','      2  ','  1      ']

# También se puede acomodar de esta forma:
PlayerInventory: [
 '         ',
 ' A B C D ',
 '      2  ',
 '  1      ']
```
{% endtab %}
{% endtabs %}

