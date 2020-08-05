---
description: 以玩家身份执行命令
---

# 执行命令

## 节点

```text
command|cmd|player|execute
```

## 示例

```yaml
- 'command: spawn'
```

```yaml
# 以 ; 分隔，可以执行多个命令
# 下方动作等同于
# - 'command: spawn'
# - 'command: say I am Back'

- 'command: spawn ; say I am Back'
```

