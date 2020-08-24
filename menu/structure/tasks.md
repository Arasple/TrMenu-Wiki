---
description: Custom tasks executed at the set interval for the time whenthe menu is opened
---

# Tasks

## Example

```yaml
#
# Custom menu periodic tasks
#

Tasks:
  # Task identifier
  tikTok:
    # Execution interval (In Ticks)
    period: 20
    # Actions executed
    task:
      - requirement: 'isOperator.'
        actions:
          - 'sound: BLOCK_NOTE_BLOCK_BIT-1-2'
```

## Note

* Each task is made of 3 parts: the identifier, the interval, and the actions.
* After opening the menu, all tasks will start and then stop when the menu is closed.

{% page-ref page="../../actions/action.md" %}

