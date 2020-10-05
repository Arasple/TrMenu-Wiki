---
description: Configurar opciones del menú
---

# Opciones

Las opciones del menú son cosas varias para el menú, algunas son importantes para la creación de menús complejos.

**Formas de escribirlo**

* **Normal:** Options
* **RegEx:** \(option\|setting\)\(s\)?

```yaml
Options:
  Arguments: true
  Default-Arguments:
    - 'asd'
    - '123'
  Default-Layout:
    - '+++++++C+'
    - '+1+3+4A++'
    - '+     +++'
  Hide-Player-Inventory: true
  Min-Click-Delay: 200
  Depend-Expansions:
    - 'Math'
    - 'Player'
    - 'Server'
```

## I. Activar detección de argumentos

* Con esta opción el menú detecta los argumentos que hay después del comando para abrir el menú, por ejemplo `/comando argumento1 argumento2`
* Para más información sobre los argumentos puedes ir a:

{% page-ref page="../../funciones/argumentos.md" %}

**Formas de escribirlo**

* **Normal:** Arguments
* **RegEx:** \(transfer\)?\(-\)?arg\(ument\)?\(s\)?

```yaml
Options:
  Arguments: true
```

## II. Argumentos por defecto

* En caso de que tu menú requiera argumentos para funcionar y que alguien use el comando sin ningún argumento entonces puedes definir argumentos por defecto.

**Formas de escribirlo**

* **Normal:** Default-Arguments
* **RegEx:** def\(ault\)?\(-\)?arg\(ument\)?\(s\)?

```yaml
Options:
  Default-Arguments:
    - 'manzana'
    - 'naraja123'

# También lo puedes escribir de la manera:
Options:
  Default-Arguments: ['manzana','naraja123']
```

## III. Diseño por defecto

* En caso de no haber definido el diseño de tu menú entonces puedes hacerlo aquí.

**Formas de escribirlo**

* **Normal:** Default-Layout
* **RegEx:** def\(ault\)?\(-\)?lay\(out\)?\(s\)?

```yaml
Options:
  Default-Layout:
    - '+++++++C+'
    - '+1+3+4A++'
    - '+     +++'
```

## IV. Ocultar items del jugador

* Con esta opción puedes ocultar los items del jugador cuando abras el menú.
* Esto es bastante útil en caso de usar el diseño del inventario de jugador.
* Por defecto viene desactivado.

**Formas de escribirlo**

* **Normal:** Hide-Player-Inventory
* **RegEx:** hide\(-\)?player\(-\)?inv\(entory\)?\(s\)?

```yaml
Options:
  Hide-Player-Inventory: true
```

## V. Retraso requerido entre los clicks

* Con esta opción puedes evitar los típicos hacks que sacan items del menú spameando clicks.
* El retraso o delay requerido se escribe en milisegundos.

**Formas de escribirlo**

* **Normal:** Min-Click-Delay
* **RegEx:** min\(-\)?click\(-\)?delay

```yaml
Options:
  # Si quieres evitar hacks que sacan items del menú lo ideal
  # es dejar esta opción en 200
  Min-Click-Delay: 200
```

## VI. Expansiones requeridas

* Con esta opción defines las expansiones de PlaceholderAPI requeridas para usar el menú.
* En caso de que el servidor no tenga alguna de estas expansiones descargadas entonces TrMenu se encargará de descargarla e instalarla.

**Formas de escribirlo**

* **Normal:** Depend-Expansions
* **RegEx:** depend\(-\)?expansion\(s\)?

```yaml
Options:
  Depend-Expansions:
    - 'Math'
    - 'Player'
    - 'Server'

# También lo puedes escribir de la manera:
Options:
  Depend-Expansions: ['Math','Player','Server']
```

