---
description: Configurar eventos del menú
---

# Eventos

Puedes hacer que el menú ejecute acciones cuando se ejecuta un evento por parte de TrMenu

**Formas de escribirlo**

* **Normal:** Events
* **RegEx:** event\(s\)?

```yaml
Events:
  Open:
    - 'SOUND: BLOCK_CHEST_OPEN-1-0'
  Close:
    - 'SOUND: BLOCK_CHEST_CLOSE-1-0'
  Click:
    - 'SOUND: ENTITY_ITEM_BREAK-1-0'
```

* Puedes configurar que se ejecuten ciertas acciones al abrir, cerrar o darle click al menú, además verificar que se cumplan condiciones como razones al abrir o cerrar.
* Para más información sobre condiciones puedes ir a:

{% page-ref page="../../funciones/condiciones.md" %}

* Para más información sobre las acciones puedes ver sus tipos en:

{% page-ref page="../../acciones/tipos/" %}

* Para ver diferentes razones y resultados al abrir o cerrar el menú puedes ir a:

{% page-ref page="../../api/eventos/menuopenevent.md" %}

{% page-ref page="../../api/eventos/menucloseevent.md" %}

{% page-ref page="../../api/eventos/menuclickevent.md" %}

## I. Al abrir el menú

**Formas de escribirlo**

* **Normal:** Open
* **RegEx:** open\(s\)?

{% tabs %}
{% tab title="EJEMPLO 1" %}
```yaml
# Este ejemplo simple solo hace que el menú reproduzca un
# sonido al abrir el menú
Events:
  Open:
    - 'SOUND: BLOCK_CHEST_OPEN-1-0'
```
{% endtab %}

{% tab title="EJEMPLO 2" %}
```yaml
# Este ejemplo verifica alguna de estas cosas:
# 1- Que el jugador tenga el permiso menu.abrir
# 2- Que la consola le haya abierto el menú al jugador
# Si se cumple alguna de estas cosas el menú abrirá
# correctamente y reproducirá un sonido.
#
# Si ninguna de estas cosas se cumple entonces el jugador
# no podrá abrir el menú.
Events:
 # Evento al abrir
  Open:
    # Condición
    - condition: 'hasPerm.menu.abrir or is.{reason}.CONSOLE'
      # Acciones al cumplir la condición
      actions:
        - 'SOUND: BLOCK_CHEST_OPEN-1-0'
      # Acciones si no se cumple la condición
      deny:
        - 'SOUND: ENTITY_ITEM_BREAK-1-0'
        - 'TELL: &cNo tienes permiso para abrir este menú!'
        # La acción RETURN es necesaria para evitar que
        # se abra el menú
        - 'RETURN'
```
{% endtab %}
{% endtabs %}

## II. Al cerrar el menú

**Formas de escribirlo**

* **Normal:** Close
* **RegEx:** close\(s\)?

```yaml
# Este ejemplo simple solo hace que el menú reproduzca un
# sonido al cerrar el menú
Events:
  Close:
    - 'SOUND: BLOCK_CHEST_CLOSE-1-0'
```

## III. Al darle click al menú

**Formas de escribirlo**

* **Normal:** Click
* **RegEx:** click\(s\)?

```yaml
# Este ejemplo simple solo hace que el menú reproduzca un
# sonido al darle click a un botón
Events:
  Click:
    - 'SOUND: ENTITY_ITEM_BREAK-1-0'
```

