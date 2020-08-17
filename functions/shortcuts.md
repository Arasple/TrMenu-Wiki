---
description: Simple shortcuts to execute actions
---

# Shortcuts

Configuration

{% code title="settings.yml" %}
```yaml
#
# Actions Shortcuts Configuration
#
Shortcuts:
  Offhand: 'open: Example'
  Sneaking-Offhand:
    - condition: 'hasPerm.trmenu.shortcut'
      execute: 'open: Example'
  Right-Click-Player: []
  Sneaking-Right-Click-Player: []
  PlayerInventory-Border-Left: []
  PlayerInventory-Border-Right: []
  PlayerInventory-Border-Middle: []
```
{% endcode %}

## Note

* After the event is triggered, the actions will be executed and the event is cancelled
* If a shortcut isn't used, you can set it to `[]`to disable it

{% page-ref page="../actions/action.md" %}



