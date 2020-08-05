---
description: 通常为一行的脚本表达式，返回布尔值
---

# Expressions

* TrMenu v2 提供全新的表达式写法，简单易懂
* 暂时不支持自定义添加
* 参数通常由 . 分开

## 示例

```yaml
# 同时拥有权限 test 和 等级 >= 10
hasPerm.test and hasLevel.10
```

## 连词

* and = &&
  * "与"，需要相连的两部分均返回 true 时，表达式才返回 true
* or = \|\|
  * "或者"，需相连两部分任意一部分返回 true 时，表达式即返回 true

