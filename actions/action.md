---
description: >-
  Actions can be used in the actions section of the buttons, in menu events,
  tasks, input catchers, etc...
---

# Action

## Normal Example

```yaml
actions:
 - 'tell: Hello, %player_name%'
```

## Conditionnal Example

```yaml
actions:
  condition: 'hasMoney.100'
  actions:
  - 'tell: You have enough money.'
  deny-actions:
  - 'tell: You don''t have enough money.'
```

## Multi-Conditions Example

```yaml
    actions:
      all:
        - condition: 'utils.chance(0.1)'
          priority: 3
          actions:
            - 'tell: Prize 1'
            - 'return'
        - condition: 'utils.chance(0.5)'
          priority: 2
          actions:
            - 'tell: Prize 2'
            - 'return'
        - condition: 'true'
          priority: 1
          actions:
            - 'tell: Prize 3'
```

## Note

* When using multiples groups of conditions, you can set priorities to define the order to check the conditions 
* If a break/return/cancel action is executed, the entire group will stop
* There are many aliases for nodes names such as:

```yaml
requirement: 'hasPoints.100'
execute: 'tell: You have 100 points'
deny: 'tell: You dont have 100 points'
```

