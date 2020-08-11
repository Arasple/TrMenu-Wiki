---
description: 给予玩家 JSON 格式物品或构建简单物品
---

# 给予物品

## 节点

```text
(give|add)(-)?item(s)?
```

## 示例

```yaml
# 给予半组显示名称为 "&bCustom Diamond" 的钻石
- 'give-item: material:DIAMOND,amount:32,name:&bCustom Diamond'
```

## 注意

* 支持给予通过命令转换的 JSON 格式物品

