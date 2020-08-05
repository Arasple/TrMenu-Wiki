---
description: 物品的描述
---

# Lore

## 节点

```text
(display)?(-)?lore(s)?
```

## 示例

```yaml
# 嵌套 List，多组动态 Lore
lore:
  - - '&7Thanks &f:> &7for using!'
  - - '&7Thanks &f:) &7for using!'

# 静态 Lore 描述
lore:
  - 'Hello There'
  - 'Hello TrMenu!'
```

## 条件

{% hint style="info" %}
此功能将在每次更新 Lore 时进行计算条件，可能影响插件性能表现
{% endhint %}

```yaml
lore:
  - 'Line 1'
  - 'Line 2'
  # 当玩家有 vip.user 权限时显示此行
  - 'You are VIP User<condition: hasPerm.vip.user>'
  - 'Line 3'
```

## 小技巧

* Lore 中支持使用 \n 换行，也支持变量中的换行符号
* 可以在配置文件中配置默认 Lore 行的颜色



