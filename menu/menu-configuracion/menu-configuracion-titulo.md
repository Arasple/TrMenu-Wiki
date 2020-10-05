---
description: Configurar título del menú
---

# Título

**Formas de escribirlo**

* **Normal:** Title
* **RegEx:** title\(s\)?

## I. Título normal

* Un solo título que se mostrará arriba del menú
* Se pueden usar códigos de color &

```yaml
Title: '&4Esto es un título'
```

## II. Título dinámico

* Varios títulos que cambiarán constantemente
* Esta opción va acompañada con el actualizador de título

{% tabs %}
{% tab title="FORMA 1" %}
```yaml
Title:
  - '&1Esto'
  - '&2es'
  - '&3un'
  - '&4título'
  - '&5animado'

#Cada cuantos ticks quieres que se actualice el título del menú
# 20 ticks = 1 segundo
Title-Update: 20
```
{% endtab %}

{% tab title="FORMA 2" %}
```yaml
Title: ['&1Esto','&2es','&3un','&4título','&5animado']

#Cada cuantos ticks quieres que se actualice el título del menú
# 20 ticks = 1 segundo
Title-Update: 20
```
{% endtab %}
{% endtabs %}

**Formas de escribir el actualizador de título**

* **Normal:** Title-Update
* **RegEx:** title\(s\)?\(-\)?update\(s\)?

