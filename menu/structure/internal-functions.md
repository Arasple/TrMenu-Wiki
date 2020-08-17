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

* Each script must have a unique identifier
* You can use `${SCRIPT_IDENTIFIER}` to get the value returned by a script
* You can use arguments with \`${IDENTIFIER\_ARG1\_ARG2} and then get the value in the script with {0}, {1}...
* Since you have to use {0} for \*scripts\*' arguments, you have to use PlaceholderAPI placeholders to get the menu's arguments: `%trmenu_args_0%,%trmenu_args_1%, %trmenu_args_2%...`

```yaml
'Health':
  update: 20
  display:
    material: RED_STAINED_GLASS_PANE
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

