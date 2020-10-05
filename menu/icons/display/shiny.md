---
description: 附魔发光效果
---

# Glow

## 节点

```text
(shiny|glow)(s)?
```

## 示例

```yaml
# 直接设置布尔值，开启或关闭
shiny: true

# 动态效果（条件表达式）
shiny: 'hasPerm.vip.user and hasMoney.1000'
```

## 误用示范

{% tabs %}
{% tab title="繁琐的条件图标" %}
```yaml
  A:
    refresh: 20
    update: 20
    display: # ...
    actions: # ...
    icons:
    - condition: 'hasPerm.vip.user'
      display:
        glow: true
```
{% endtab %}

{% tab title="简洁一步到位" %}
```yaml
  A:
    update: 20
    display:
      # ...
      shiny: 'hasPerm.vip.user'
    actions: # ...
```
{% endtab %}
{% endtabs %}

## 注意

* 物品的发光效果不提供独立的更新周期设置，将随着每次物品刷新更新

