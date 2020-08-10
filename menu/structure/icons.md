---
description: Buttons format
---

# Buttons

## Example

```yaml
#
# Menu Button
#
Buttons:
  # The identifier of the icon which can be used in the layout.
  '|':
    #The dynamic update interval of the button's properties.
    #If multiples intervals are set, they will correspond in that 
    #order to the Material, the Name, the Lore and the Slots.
    #If you set only one number like that `update: #` it will apply for all 
    update: [-1, 10, 15, -1]
    #The display section of the item
    display:
      material: 'Gray Stained Glass Pane'
      name: ['&fTr&7Menu', '&7Tr&8Menu', '&8Tr&0Menu','&7Tr&8Menu']
      lore:
        - - '&7Thanks &f:> &7for using!'
        - - '&7Thanks &f:) &7for using!'
    # 
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

## Structure

* Update cycle
  * Material
  * Name
  * Lore
  * Slot
* Refresh cycle \(recalculates icons priorities\)
* Display section
* Actions section
* Conditionnal icons
  * Condition
  * Priority
  * Inherit
  * Display section
  * Actions section

## Note

* All conditionnal icons are configured under the Icons section
* You can set a different update cycle for each properties. If only is set, all will be affected.
* For icons, the higher the number is, the higher the priority is.
* By default, all conditionnal icons inherit the materials and slots. If \`inherit: true\` is defined, it will also inherit the name, lore and amount \(except if they are specified\).
* The material, the name, lore, slots, etc... all support dynamic effects.

{% page-ref page="../icons/display/" %}

