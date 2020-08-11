---
description: 为玩家创建输入捕获器，并根据输值做出反应
---

# 输入捕获

## 节点

```text
(input)?(-)?catcher(s)?
```

## 旧版写法示例

```yaml
- |-
  Catcher:
   <Type=CHAT>
   <Before=tell:请输入一个值>
   <Valid=tell: 你成功输入了一个数值 ${input}>
   <Invalid=tell: 你输入的不是一个数值>
   <Require=isNumber.${input}>
   <Cancel=tell: 已取消捕获器>
```

{% tabs %}
{% tab title="Type" %}
捕获器的类型
{% endtab %}

{% tab title="Before" %}
玩家输入内容之前，执行的动作
{% endtab %}

{% tab title="Valid" %}
玩家输入值，并且满足 Require 条件时执行的动作
{% endtab %}

{% tab title="Invalid" %}
玩家输入值，并且不满足 Require 条件时执行的动作
{% endtab %}

{% tab title="Require" %}
玩家输值后，满足此条件则执行 Valid 动作，否则执行 Invalid 中动作
{% endtab %}
{% endtabs %}

## 高级写法示例

```yaml
- catcher:

    target:
      type: CHAT
      before: 'tell: 请输入一名玩家的名称'
      cancel: 'tell: 已取消捕获器'
      reactions:
        - condition: 'isOnline.${input_target}'
          execute: 'tell: 名称确认. ${input_target}'
          deny:
            - 'tell: 抱歉, 但玩家 ${input_target} 不在线'
            - 'return'

    amount:
      type: CHAT
      before: 'tell: 请提供支付数额'
      cancel: 'tell: 已取消捕获器'
      reactions:
        - condition: 'isNumber.${input_amount}'
          execute:
            - 'tell: 数额确认. ${input_amount}'
            - 'command: pay ${input_target} ${input_amount}'
          deny:
          - 'tell: 请提供有效数字'
          - 'retype'
```

* 执行到中断动作 **Return** 将会中断该输入捕获器
* 执行到重新输入动作 **Retype** 将重新执行当前的子捕获器

{% page-ref page="reinput.md" %}

## 类型

* CHAT
  * 捕获玩家发送到聊天框的内容
* SIGN
  * 向玩家发送一个虚拟木牌，捕获输入的内容
* ANVIL
  * 向玩家发送一个虚拟铁砧，捕获命名的内容

