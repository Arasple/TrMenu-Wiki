---
description: Configurar scripts del menú
---

# Scripts

Los scripts son bloques de código Javascript que se pueden usar dentro del menú.

**Formas de escribirlo**

* **Normal:** Functions
* **RegEx:** \(fun\(ction\)?\|script\)\(s\)?

```kotlin
Icons:
  'A':
    update: 20
    display:
      material: 'STONE'
      name: '&c&lBotón A'
      lore:
        - '&7Texto que desaparece'
        - '&7cada segundo:&f ${flash_Texto}'

Functions:
  flash: |-
    function flash() {
      var display = new Date().getSeconds() % 2 == 0
      return display ? "{0}" : "  "
    }
    flash()
```

Para más información sobre como hacer Scripts puedes ir a:

{% page-ref page="../../scripts/bloques-de-codigo.md" %}

