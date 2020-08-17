---
description: SImilar as the Built-In Script
---

# Script Placeholder

## Usage

```yaml
${js: <function>}
```

## Example

```yaml
# Usage in Lore
- '&8| &7ONLINE: &e%server_online% &6${js: utils.getOnlinePlayers().size() > 1 ? "Players" : "Player"}'
```

