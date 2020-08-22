---
description: Execute actions for all online players
---

# All Players

## Usage

```text
<((p|(for|all)?(-)?players))[:=]?(.+)?>
```

## Example

```yaml
- 'tell: broadcast message<Players>'
- 'tell: broadcast message for VIP<Players:hasPerm.group.vip>'
```

