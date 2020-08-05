---
description: 让玩家以 OP 身份执行命令
---

# 执行命令 \(OP\)

## 节点

```text
op(erator)?(s)?
```

## 示例

```yaml
- 'op: kick ${input}'
```

```yaml
- 'op: kick ${input} ; broadcast I just kicked ${input}'
```

## 注意

{% hint style="danger" %}
当前情况下，Bukkit 所能实现此效果的方法只能是 **授予 OP，执行操作，撤销 OP**

在可以用 **CONSOLE** 控制台执行命令实现需求的情况下，**不推荐**使用此动作
{% endhint %}

