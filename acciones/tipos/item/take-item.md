---
description: Take items from the player's inventory
---

# Take-Items

## Usage

```text
(take|remove)(-)?item(s)?
```

## Example

```yaml
# Take a specified amount of items
- 'take-item: material:DIAMOND,amount:64'
```

```yaml
# Take a stack of iron ingots and half a stack of gold ingots
- 'take-item: material:IRON_INGOT,amount:64;material:GOLD_INGOT,amount:32'
```

## Note

* This action **does not check** whether the player has the required items or not
* The item material must be unified with each parts seperated by a `_`

{% page-ref page="../../../funciones/identificador-item.md" %}

{% page-ref page="../../../scripts/expresiones/hasitem.md" %}

