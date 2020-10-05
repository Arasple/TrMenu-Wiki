---
description: 同内置脚本类似的用法，随处可用
---

# Script Placeholder

## 格式

```yaml
${js: <function>}
```

## 示例

```yaml
# Lore 中
- '&8| &7ONLINE: &e%server_online% &6${js: utils.getOnlinePlayers().size() > 1 ? "Players" : "Player"}'
```

