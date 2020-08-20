---
description: Repair the specified items in the player's inventory
---

# Repair-Item

## Usage

```text
repair(-)?item(s)?
```

## Examples

```yaml
# Will repair all items in the player's inventory
- 'repair-item: all'
# You can repair multiple items by seperating them with ;
# Will repair the items in hand, in the slot 20 and the offhand of the player's inventory
- 'repair-item: hand;20;offhand'
```

## Note

* You can use `hand,offhand,helmet,chestplate,leggings,boots and all` or a number to enchant a specific slot of the player's inventory

