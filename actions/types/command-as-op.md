---
description: Execute commands as an operator
---

# Command \(as OP\)

## Usage

```text
op(erator)?(s)?
```

## Examples

```yaml
- 'op: kick ${input}'
```

```yaml
- 'op: kick ${input} ; broadcast I just kicked ${input}'
```

## Note

{% hint style="danger" %}
As of now, the only way Bukkit can make this action work is by granting the player OP, executing the command and then removing the OP.  
This process can lead to serious problems with hackers trying to execute operator commands when they click on the button while the server is lagging \(= slower process\).

**It is recommended to use the `console` action type instead when possible, or else, give the player the correct permission before and removing it after the command.**
{% endhint %}

