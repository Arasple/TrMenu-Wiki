---
description: 对菜单的一些事件执行条件动作反应
---

# Events

## 示例

```yaml
#
# 菜单的事件处理
#
Events:
  # 开启菜单事件
  Open:
    - requirement: 'hasPerm.trmenu.use or is.{reason}.RELOAD or is.{reason}.CONSOLE'
      actions:
        - 'sound: BLOCK_CHEST_OPEN-1-0'
      deny-actions:
        - 'sound: ENTITY_ITEM_BREAK-1-0'
        - 'title: <title=&c&l权限不足><subtitle=&7&l本菜单需要权限 &6&ltrmenu.use &7&l方能浏览>'
        - 'return'
  # 关闭菜单事件
  Close:
    - 'sound: BLOCK_CHEST_CLOSE-1-0'
```

## 注意

* 事件中的反应写法后面会详解
* 在开启菜单事件中，{reason} 变量将返回

  ```text
  me.arasple.mc.trmenu.api.events.MenuOpenEvent.Reason
  ```

* 若执行 return 动作，事件将被取消

