---
description: 从玩家背包中扣除指定的物品
---

# 扣除物品

## 节点

```text
(take|remove)(-)?item(s)?
```

## 示例

```yaml
# 扣除一组钻石
- 'take-item: material:DIAMOND,amount:64'
```

```yaml
# 扣除一组铁锭和半组金锭
- 'take-item: material:IRON_INGOT,amount:64;material:GOLD_INGOT,amount:32'
```

## 注意

* 扣除物品的动作并**不会主动检测**玩家背包是否包含该物品，实现商店需要配合条件表达式
* 物品特征写法和其它部分完全统一

{% page-ref page="../../../functions/item-identifiers.md" %}

{% page-ref page="../../../script/expressions/hasitem.md" %}

