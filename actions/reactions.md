---
description: 可以在图标的动作部分、菜单事件、周期任务等地方使用
---

# 反应

## 常规写法

```yaml
actions:
 - 'tell: Hello, %player_name%'
```

## 三元写法

```yaml
actions:
  condition: 'hasMoney.100'
  actions:
  - 'tell: You have enough money.'
  deny-actions:
  - 'tell: You don''t have enough money.'
```

## 多组三元写法

```yaml
    actions:
      all:
        - condition: 'utils.chance(0.1)'
          priority: 3
          actions:
            - 'tell: Prize 1'
            - 'return'
        - condition: 'utils.chance(0.5)'
          priority: 2
          actions:
            - 'tell: Prize 2'
            - 'return'
        - condition: 'true'
          priority: 1
          actions:
            - 'tell: Prize 3'
```

## 注意

* 使用多个反应组时，可以设置优先级，按降序执行
* 若执行到任意**中断动作**，整个动作组将停止
* 节点别称有许多，例如

```yaml
requirement: 'hasPoints.100'
execute: 'tell: You have 100 points'
deny: 'tell: You dont have 100 points'
```

