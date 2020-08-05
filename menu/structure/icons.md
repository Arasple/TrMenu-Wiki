---
description: 图标将显示物品，且可交互执行一定反应
---

# Icons

## 示例

```yaml
#
# 菜单的图标
#
Icons:
  # 图标的唯一 ID, 可配合布局使用
  '#':
    # 显示图标的动态更新周期, 若设置多个则依次对应为 Material, Name, Lore, Slots
    # 设置一个即为所有项相同更新周期
    update: [-1, 10, 15, -1]
    # 菜单的显示部分
    display:
      material: 'Gray Stained Glass Pane'
      name: ['&fTr&7Menu', '&7Tr&8Menu', '&8Tr&0Menu','&7Tr&8Menu']
      lore:
        - - '&7Thanks &f:> &7for using!'
        - - '&7Thanks &f:) &7for using!'
    # 点击菜单后执行的动作
    actions:
      all: 'sound: BLOCK_NOTE_BLOCK_PLING-1-2'
```

```yaml
#
# 优先级图标示例
#
Icons:
  '#':
    update: 20
    display:
      material: 'Gray Stained Glass Pane'
      name: '&7Normal'
    actions:
      all: 'sound: BLOCK_NOTE_BLOCK_PLING-1-2'
    icons:
      # 条件，拥有 mvp.user
      - condition: 'hasPerm.mvp.user'
        prioriry: 2
        # 深度继承默认图标
        inherit: true
        display:
          name: '&bMVP'
        actions:
          all: 'tell: Hello, MVP User!'
      # 条件，拥有 vip.user
      - condition: 'hasPerm.vip.user'
        priority: 1
        display:
          name: '&aVIP'
        actions:
          all: 'tell: Hello, VIP User!'
```

## 结构

* 更新周期
  * 材质
  * 名称
  * Lore
  * 槽位
* 刷新周期（重新计算优先级）
* 显示部分
* 动作部分
* 子图标
  * 条件
  * 优先级
  * 是否继承
  * 显示部分
  * 动作部分

## 注意

* 所有图标均配置在 **Icons** 节点下
* 更新周期支持多个属性（材质，名称，Lore，槽位）的独立周期，若只配置一个则默认全部（如 v1）
* 子图标优先级按降序，选取第一个符合条件的子图标
* 默认情况下，子图标仅继承默认图标的位置、材质，若开启继承且未设置名称，Lore，则将继承
* 材质、名称、Lore、槽位等均支持动态效果

{% page-ref page="../icons/display/" %}

