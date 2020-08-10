---
description: Update the button's placeholdefrs and/dynamic effects
---

# Update

## Usage

* The update interval for the material, the name, lore and slots of the button
* You can set them independently as an array to define different intervals for each property

## Example

```yaml
# Same interval for all four properties
update: 20
```

```yaml
# Incomplete setting
# Here, only the material, name and lore are set to: 20, -1, 15
# The slot update interval will be set to the highest of the defined values, in this case: 20
update: [20, -1, 15]
```

```yaml
# Complete setting, the numbers will match in the same order the: Material, Name, Lore and Slot
update: [-1, 5, 25, 30]
```

## Note

* If the update interval is not set, the button won't update at all.
* Conditionnal icons do not support custom update interval and will just use the one from the default button icon.

