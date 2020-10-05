---
description: 执行 JavaScript 脚本
---

# 执行脚本

## 节点

```text
(java)?(-)?script(s)?|js
```

## 示例

```yaml
- 'js: player.setNoDamageTicks(600)'
- 'js: player.setVelocity(player.getVelocity().setY(25))'
- 'js: bukkitServer.broadcastMessage("A Broadcast Message")'
```

## 了解更多

{% page-ref page="../../script/scripts.md" %}

