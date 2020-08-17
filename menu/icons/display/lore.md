---
description: Lore of the item
---

# Lore

## Usage

```text
(display)?(-)?lore(s)?
```

## Examples

```yaml
# Multiples groups of lore lines -> Dynamic effect
lore:
  - - ' '
    - '&7Thanks &f:> &7for using!'
  - - ' '
    - '&7Thanks &f:) &7for using!'

# Simple static lore lines
lore:
  - 'Hello There'
  - 'Hello TrMenu!'
```

## Conditions

{% hint style="info" %}
Conditions are checked each time the lore is updated, which may impact performances
{% endhint %}

```yaml
lore:
  - 'Line 1'
  - 'Line 2'
  # Displays the line if the player has the permission `vip.user`
  - 'You are a VIP User<condition: hasPerm.vip.user>'
  - 'Line 3'
```

## Tips

* The lore supports `\n` for line breaks \(works with placeholders too\)
* The default color of lore lines can be configured in the `setting.yml` file



