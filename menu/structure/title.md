---
description: 标题即容器显示的标题，以及多个标题之间切换的周期
---

# Title

## 示例

```yaml
#
# 菜单的标题, 支持动态标题周期切换
#
Title:
  - 'Hello, TrMenu!'
  - 'Support Animated Titles'

#
# 若有多个标题, 切换的周期 (ticks)
#
Title-Update: 40
```

## 注意

* **标题更新周期** 只有当存在多个标题时有效
* 若使用非动态标题，可以使用 **设置标题** 等动作对标题二次修改

