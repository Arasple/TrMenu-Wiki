---
description: 为图标设置点击后的动作交互
---

# Actions

## 示例

```yaml
'Close':
  update: [-1, 5, -1, -1]
  display:
    material: Red Stained Glass Pane
    name: ['&cC&7lose', '&cCl&7ose', '&cClo&7se', '&cClos&7e', '&cClose']
  # 动作部分
  actions:
    # 点击类型 - 反应
    all: close
```

```yaml
  '*':
    update: [-1, 5, 20, -1]
    display: # ...
    # 动作部分
    actions:
      # 点击类型（左键）
      left:
        - 'set-meta: icon_server_hide true'
        - 'sound: BLOCK_NOTE_BLOCK_BIT-1-0'
        - 'refresh'
```

## 点击类型

```kotlin
package me.arasple.mc.trmenu.api.inventory

/**
 * @author Arasple
 * @date 2020/3/22 10:23
 */
enum class InvClickType {

    /**
     * 左键点击
     */
    LEFT,

    /**
     * 按住 Shift 并左键点击
     */
    SHIFT_LEFT,

    /**
     * 右键点击
     */
    RIGHT,

    /**
     * 按住 Shift 并右键点击
     */
    SHIFT_RIGHT,

    /**
     * 中键点击 (摁住鼠标滚轮)
     */
    MIDDLE,

    /**
     * 按住 Shift 并中键点击
     */
    DOUBLE_CLICK,

    /**
     * 丢弃键 (默认为 Q)
     */
    DROP,

    /**
     * 切换副手 (默认为 F) (1.16+)
     */
    OFFHAND,

    /**
     * Ctrl + 丢弃键
     */
    CONTROL_DROP,

    /**
     * 创造模式 + 中键
     */
    CREATIVE,

    /**
     * 数字键 1 - 9
     */
    NUMBER_KEY,

    /**
     * 数字键 1
     */
    NUMBER_KEY_1,

    /**
     * 数字键 2
     */
    NUMBER_KEY_2,

    /**
     * 数字键 3
     */
    NUMBER_KEY_3,

    /**
     * 数字键 4
     */
    NUMBER_KEY_4,

    /**
     * 数字键 5
     */
    NUMBER_KEY_5,

    /**
     * 数字键 6
     */
    NUMBER_KEY_6,

    /**
     * 数字键 7
     */
    NUMBER_KEY_7,

    /**
     * 数字键 8
     */
    NUMBER_KEY_8,

    /**
     * 数字键 9
     */
    NUMBER_KEY_9,

    /**
     * 点击容器左侧区域
     */
    WINDOW_BORDER_LEFT,

    /**
     * 点击容器右侧区域
     */
    WINDOW_BORDER_RIGHT,

    /**
     * 所有触发方式
     */
    ALL;

}
```

## 小技巧

* 你可以为同一个反应快速添加多种触发的点击方式，用逗号分隔开，例如

```csharp
actions:
  # 左键、中键 或按 数字键 8
  left,middle,number_key_8:
   - 'tell: Hello'
```

## 注意

* **反应** 支持多种写法，与 周期任务、菜单事件 中的相同，后面会详解
* 动作部分节点与显示部分节点同级
* 默认图标和子图标都可以有独立的动作交互部分

