---
description: การกระทำที่จะเกิดขึ้นเมื่อคุณกดปุ่ม
---

# Actions

## ตัวอย่าง

```yaml
'Close':
  update: [-1, 5, -1, -1]
  display:
    material: Red Stained Glass Pane
    name: ['&cC&7lose', '&cCl&7ose', '&cClo&7se', '&cClos&7e', '&cClose']
  # actions section
  actions:
    # Click type (all of the supported ones)
    all: close
```

```yaml
  '*':
    update: [-1, 5, 20, -1]
    display: # ...
    # Actions section
    actions:
      # Click type (left click)
      left:
        - 'set-meta: icon_server_hide true'
        - 'sound: BLOCK_NOTE_BLOCK_BIT-1-0'
        - 'refresh'
```

## ประเภทการกด

```kotlin
package me.arasple.mc.trmenu.api.inventory

/**
 * @author Arasple
 * @date 2020/3/22 10:23
 */
enum class InvClickType {

    /**
     * Left CLick
     */
    LEFT,

    /**
     * Shift + Left Click
     */
    SHIFT_LEFT,

    /**
     * Right CLick
     */
    RIGHT,

    /**
     * Shift + Right Click
     */
    SHIFT_RIGHT,

    /**
     * Middle Click (mouse wheel)
     */
    MIDDLE,

    /**
     * Shift + Middle Click
     */
    DOUBLE_CLICK,

    /**
     * Drop key (Q by default)
     */
    DROP,

    /**
     * Switch Item in Offhand (F by default) (1.16+)
     */
    OFFHAND,

    /**
     * Ctrl + Drop key
     */
    CONTROL_DROP,

    /**
     * Creative mode + Middle Click
     */
    CREATIVE,

    /**
     * Number Keys from 1 to 9
     */
    NUMBER_KEY,

    /**
     * Number Key 1
     */
    NUMBER_KEY_1,

    /**
     * NumberKey 2
     */
    NUMBER_KEY_2,

    /**
     * Number Key 3
     */
    NUMBER_KEY_3,

    /**
     * Number Key 4
     */
    NUMBER_KEY_4,

    /**
     * Number Key 5
     */
    NUMBER_KEY_5,

    /**
     * Number Key 6
     */
    NUMBER_KEY_6,

    /**
     * Number Key 7
     */
    NUMBER_KEY_7,

    /**
     * Number Key 8
     */
    NUMBER_KEY_8,

    /**
     * Number Key 9
     */
    NUMBER_KEY_9,

    /**
     * Left Border of the Inventory
     */
    WINDOW_BORDER_LEFT,

    /**
     * Right Border of the Inventory
     */
    WINDOW_BORDER_RIGHT,

    /**
     * All above supported types
     */
    ALL;

}
```

## Tips

* You can easily combine multiple click types to execute the same actions

```csharp
actions:
  # The action will be executed if you left clicked the button,
  # middle clicked it, or pressed the 8 key button.
  left,middle,number_key_8:
    - 'tell: Hello'
```

## หมายเหตุ

* Actions support multiple action types, the same as those in the Periodic Tasks and in the Menu Events. They will be listed and detailed later.
* The `actions` section must be at the same level as the `display`section
* Both default button icons and conditionnal icons can have seperated actions.

