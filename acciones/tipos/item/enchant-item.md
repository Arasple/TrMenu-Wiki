---
description: Enchant the specified items in the player's inventory
---

# Enchant-Item

## Usage

```text
enchant(-)?item(s)?
```

## Examples

```yaml
# Will enchant the item in the player's main hand with Unbreaking 4
- 'enchant-item: hand,DURABILITY,4'
# Will enchant the item in 20th slot of the player's inventory with Fire Aspect 2
- 'enchant-item: 20,FIRE_ASPECT,2'
```

## Note

* You can use `hand,offhand,helmet,chestplate,leggings and boots` or a number to enchant a specific slot of the player's inventory
* You can also use ranges of numbers `'enchant-item: 20,FIRE_ASPECT,0-2'`for example which will enchant the item with a level of Fire Aspect between 0 and 2 \(included\), so either 0, 1 or 2

