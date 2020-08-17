---
description: Enchantment effect
---

# Glow

## Usage

```text
(shiny|glow)(s)?
```

## Example

```yaml
# Set a boolean (true/false) directly to set it on/off
shiny: true

# Dynamic effect (conditions)
shiny: 'hasPerm.vip.user and hasMoney.1000'
```

## Unnecessary usages

{% tabs %}
{% tab title="Longer way" %}
```yaml
  A:
    refresh: 20
    update: 20
    display: # ...
    actions: # ...
    icons:
    - condition: 'hasPerm.vip.user'
      display:
        glow: true
```
{% endtab %}

{% tab title="Shorter way" %}
```yaml
  A:
    update: 20
    display:
      # ...
      shiny: 'hasPerm.vip.user'
    actions: # ...
```
{% endtab %}
{% endtabs %}

## Note

* Dynamic sjiny effects will be updated alongside the material update interval

