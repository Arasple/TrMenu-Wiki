---
description: 提供一些简单的快捷动作，用于执行动作
---

# Shortcuts

## 配置

{% code title="settings.yml" %}
```yaml
#
# 快捷操作执行动作
#
Shortcuts:
  Offhand: 'open: Example'
  Sneaking-Offhand:
    - condition: 'hasPerm.trmenu.shortcut'
      execute: 'open: Example'
  Right-Click-Player: []
  Sneaking-Right-Click-Player: []
  PlayerInventory-Border-Left: []
  PlayerInventory-Border-Right: []
  PlayerInventory-Border-Middle: []
```
{% endcode %}

## 注意

* 触发动作后均执行 **反应**，且将取消事件
* 若不需要该项快捷动作，直接删除节点或者设置为空

{% page-ref page="../actions/action.md" %}



