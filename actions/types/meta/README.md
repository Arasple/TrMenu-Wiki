# 数据

## 介绍

* TrMenu 目前提供 Meta / Data 两种变量数据变量
* 前者（Meta）存储在内存中，将在插件重载后失效
* 后者（Data）玩家独立存储在本地 SQLite 中，不会失效

## 应用

* 设置 Meta 或 Data 后，你都可以以变量的形式调用它们

```text
{meta:<KeyName>}
```

```text
{data:<KeyName>}
```

## 示例

```yaml
Bee:
  update: [-1, -1, -1, 20]
  display:
    material: '<skull:b727d0ab03f5cd022f8705d3f7f133ca4920eae8e1e47b5074433a137e691e4e>'
    name: '&eBee ~'
    slots:
      - [9]
      - [18]
      - [28]
      - [29]
      - [30]
      - [31]
      - [32]
      - [33]
      - [34]
      - [35]
      - [26]
      - [16]
      - [15]
      - [14]
      - [13]
      - [12]
      - [11]
      - [10]
  actions:
    all:
      - 'set-meta: angryBee true'
      - 'sound: ENTITY_ENDERMAN_HURT-1-2'
      - 'rem-meta: angryBee &&& refresh &&& sound: ENTITY_SPIDER_STEP-1-2<Delay=80>'
      - 'refresh'
  icons:
    - condition: 'equals.{meta:angryBee}.true'
      inherit: true
      display:
        name: '&cBee &4~'
        material: '<skull:e6b74e052b74288799ba6d9f35c5d0221cf8b04331547ec2f68d73597ae2c9b>'
      actions:
        all: 'sound: ENTITY_ENDERMAN_HURT-1-2'
```

