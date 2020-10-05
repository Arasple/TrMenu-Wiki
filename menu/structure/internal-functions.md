---
description: 可在菜单内快速调用的内置脚本
---

# Built-in Scripts

## 示例

{% code title="无参数脚本" %}
```yaml
#
# 菜单内置的自定义脚本变量
# 通过 ${ID_参数_参数} 的方式可以调用
#

Functions:
  health: |-
    function math(){
      return player.getHealth()
    }
    math()
```
{% endcode %}

{% code title="带参数脚本" %}
```yaml
Functions:
  flash: |-
    function flash() {
      var parsed = "%animations_<flash>{0}</flash>%"
      return parsed.isEmpty() ? utils.emptyString("{0}".length()) : parsed
    }
    flash()
```
{% endcode %}

## 调用

* 每个内置脚本都有独一无二的 Id 标识
* 在菜单内容中，你可以使用 **${Id}** 的形式调用
* 若需提供参数，则按照 **${Id\_参数1\_参数2}** 的格式调用
* 参数在脚本中以 {0}, {1} ... 的形式使用，若需要菜单传参，则使用 PlaceholderAPI 变量

```yaml
'Health':
  update: 20
  display:
    material: 'Red Stained Glass Pane'
    name: 'Health'
    lore:
    - ''
    - '&cHealth: ${health}'
    - ''
  actions:
    all: 'close'
```

```yaml
# ...
lore:
 - '&b${flash_➥} &3Left-Click &7to display more info.'
```

