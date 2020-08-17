---
description: >-
  The menu layout is a major feature of TrMenu which allows you to quicly design
  menus easily (it looks better with items with a single character).
---

# Layout

## Example

```yaml
Layout:
  - '########`Close`'
  - '         '
  - '         '
  - '         '
  - '########`Next`'

PlayerInventory:
  - '         '
  - '         '
  - '         '
  - '         '
```

* The characters represent the buttons' identifiers. 
* You can also use buttons with multiple characters if you surround them by ````````
* This defines the size of the menu at the same time
* The PlayerInventory feature, allows you to have 4 rows more in your menu by using the player's inventory!

## Multiples pages

```yaml
Layout:
  - - '########`Close`'
    - '         '
    - '         '
    - '         '
    - '########`Next`'
    
  - - '########`Close`'
    - '         '
    - ' *       '
    - '         '
    - '`Pre`########'

PlayerInventory:
  - - '         '
    - '  | `Close` `Next`  '
    - '         '
    - '         '
    
  - - '         '
    - '  `Pre` `Close` |  '
    - '         '
    - '         '

```

* You can also have multiples Shapes \(multiples pages\) which you can then change with the `set-shape` action
* And the PlayerInventory works alongside multiples shapes too!

## Note

* If a Layout doesn't have a corresponding PlayerInventory layout, then the player's inventory won't be used on this page
* The player's items will still be shown and hidden if there's a button in the same slot. 
  * You can also use this feature with the `Hide-Player-Inv` option \(see in on the Options wiki page\).

