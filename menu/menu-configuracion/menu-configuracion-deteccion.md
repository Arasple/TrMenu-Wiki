---
description: Configurar detección de eventos del menú
---

# Detección de eventos

Puedes abrir menús mediante comandos u otros eventos como interactuar con items.

**Formas de escribirlo**

* **Normal:** Bindings
* **RegEx:** \(bind\(ing\)?\|bound\)\(s\)?

```yaml
Bindings:
  Commands:
    - 'abrirmenu'
    - '(?i)ejemplo'
    - '(?i)abrir(-)?(menu)?(s)?'
  Items:
    - 'material:compass'
    - 'material:clock,lore:OPEN_MENU'
```

### I. Comandos

* Puedes definir con cuales comandos se abrirá el menú.
* Se pueden usar textos en RegEx
* Se sugiere añadir \(?i\) al principio para que el comando funcione sin importar las mayúsculas o minúsculas.

**Formas de escribirlo**

* **Normal:** Commands
* **RegEx:** command\(s\)?

```yaml
Bindings:
  Commands:
    - 'abrirmenu'
    - '(?i)ejemplo'
    - '(?i)abrir(-)?(menu)?(s)?'
```

### II. Items

* Puedes abrir el menú al interactuar con ítems.
* Aquí defines con cuales ítems se podrá abrir.

**Formas de escribirlo**

* **Normal:** Items
* **RegEx:** item\(s\)?

```yaml
Bindings:
  Items:
    # Una brújula
    - 'material:compass'
    # Un reloj que tenga en el lore el texto "ABRIR_MENU"
    - 'material:clock,lore:ABRIR_MENU'
```

Para más información sobre la detección de items puedes ir a:

{% page-ref page="../../funciones/identificador-item.md" %}

