---
description: 'Stops the execution of all following actions, menu events or input catchers'
---

# Break

## Usage

```text
return|break|cancel
```

## Examples

```yaml
actions:
  all:
    condition: 'hasMoney.100'
    actions:
      - 'tell: You have enough money!'
    deny:
      - 'tell: You don''t have enough money!'
      - 'break'

Events:
  Open:
    - condition: 'hasPerm.trmenu.use'
      actions:
      deny:
        - 'tell: You don''t have the permission!'
        - 'return'
```

