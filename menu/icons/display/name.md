---
description: Display name of the item
---

# Name

Usage

```text
(display)?(-)?name(s)?
```

## Examples

```yaml
  'Next':
    display:
      material: 'Cyan Stained Glass Pane'
      name: '&bN&3ext Page'
```

```yaml
  'Close':
    update: [25, 5, -1, -1]
    display:
      materials:
      - 'Red Stained Glass Pane'
      - 'Orange Stained Glass Pane'
      # Dynamic name with an update interval of 5 ticks
      name: ['&cC&7lose', '&cCl&7ose', '&cClo&7se', '&cClos&7e', '&cClose']
```



