---
description: Bind the menu to commands and/or items
---

# Bindings

## Example

```yaml
#Ways to open the menu. 
Bindings:
  # Defines the commands used to open this menu.
  Commands:
    - '(?i)example(-)?(gui)?(s)?'
   #Defines the items which will open this menu when clicked.
  Items:
    #Any compass
    - 'material:compass'
    #Clocks with the lore `OPEN_MENU` 
    - 'material:clock,lore:OPEN_MENU'
    #Player Heads with the specified texture
    - 'texture:eyJ0ZXh0dXJlcyI6eyJTS0lOIjp7InVybCI6Imh0dHA6Ly90ZXh0dXJlcy5taW5lY3JhZnQubmV0L3RleHR1cmUvNDRmNDUyZDk5OGVhYmFjNDY0MmM2YjBmZTVhOGY0ZTJlNjczZWRjYWUyYTZkZmQ5ZTZhMmU4NmU3ODZlZGFjMCJ9fX0='

```

## Note

* Commands suppoprt RegEx ! For example, with `(?i)example(-)?(gui)?(s)?`:
  * `(?i)` will make the command ignore the case: `/example` and `/eXamPle` would work.
  * `(gui)?` and `(s)?` make `gui` and `s` optionnal in the command: `/example` , `/examplegui`and `/exampleguis` would work.
* Binded commands support spaces and arguments, the plugin will automatically match and read the real arguments without 
* To understand the syntax of binded items, please see the following wiki page:

  {% page-ref page="../../functions/item-identifiers.md" %}



