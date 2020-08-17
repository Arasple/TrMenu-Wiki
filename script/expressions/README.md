---
description: Easy to understand expression returning a boolean
---

# Expressions

TrMenu v2 provides a new writing method for expressions more user-friendly  
It doens't support custom expression at the moment  
Parameters are most of the time seperated by a `.`

## Example

```yaml
# Check if the player has both the permission test and 10 levels
hasPerm.test and hasLevel.10
```

## Meaning

* and = &&
  * The expression returns `true` only when both parts of the condition are met 
* or = \|\|
  * The expression returns `true` when at least one of both parts of the conditions are met

