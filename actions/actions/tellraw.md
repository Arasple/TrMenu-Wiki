---
description: 向玩家发送一条原版 Json 消息，或利用 TrMenu 轻松构建一条
---

# 发送 Tellraw

## 节点

```text
tellraw|json
```

## 示例

{% tabs %}
{% tab title="原版 JSON" %}
```yaml
- 'json: {"text":"Hello World!"}'
```
{% endtab %}

{% tab title="构建消息 1" %}
```
- 'json: Hello World! <ClickMe?command=spawn&hover=to spawn> <--- Click That'
```
{% endtab %}

{% tab title="构建消息 2" %}
```
- 'json: &3Hello, &b{player_name}&3, Buy Ranks on our <&2&nstore?url=https://store.example.net> &3site.'
```
{% endtab %}
{% endtabs %}



