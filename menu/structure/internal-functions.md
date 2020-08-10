---
description: Built-in scripts which can be called quickly and easily in the menu.
---

# Built-in Scripts

## Examples

{% code title="Script without arguments" %}
```yaml
#
# A simple custom script
# The returned value can be obtained with ${ID_OF_THE_SCRIPT}
#

Functions:
  health: |-
    function health(){
      return player.getHealth()
    }
    health()
```
{% endcode %}

{% code title="Script with arguments" %}
```yaml
#
# You can create a script wich requires arguments 
# You can specify them with ${ID_arg1_arg2_...} 
# and use them in the script with {0}, {1}, ....
#

Functions:
  flash: |-
    function flash() {
      var parsed = "%animations_<flash>{0}</flash>%"
      return parsed.isEmpty() ? utils.emptyString("{0}".length()) : parsed
    }
    flash()
```
{% endcode %}

## Usage

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

