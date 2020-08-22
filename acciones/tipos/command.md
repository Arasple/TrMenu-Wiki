---
description: Execute commands as the player
---

# Command \(as Player\)

## Usage

```text
command|cmd|player|execute
```

## Examples

```yaml
- 'command: spawn'
```

```yaml
# Seperate multiple commands with ;
# The action at the bottom is the equivalent of those:
# - 'command: spawn'
# - 'command: say I am Back'

- 'command: spawn ; say I am Back'
```

