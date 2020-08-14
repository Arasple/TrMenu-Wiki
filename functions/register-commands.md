---
description: Create your own commands with tab-completition!
---

# Register Commands

## Configuration

{% code title="settings.yml" %}
```yaml
#
# Register commands with actions and arguments
# Supports tab-completition!
# (WARNING: A server restart is required to add, change or remove commands)
#
RegisterCommands:
  # Command name
  openMenus:
    # Command Aliases
    # Required permission
    permission: null
    aliases: []
    # Actions executed without any arguments
    execute:
      - 'tell: &7Argument `example` Required!'
    # Arguments with their actions
    arguments:
      example: 'open: example'

```
{% endcode %}

* If a new command is added, you must restart the server, but you can edit the options here and they will update instantly

