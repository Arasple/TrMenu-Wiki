---
description: 在 settings.yml 配置该功能，你可以创建支持 TAB 补全的自定义命令
---

# RegisterCommands

## 配置

{% code title="settings.yml" %}
```yaml
#
# 注册命令执行动作
# (增改命令需要重启服务器, TAB补全才能生效)
#
RegisterCommands:
  # 主命令
  openMenus:
    # 别称
    aliases: []
    # 权限
    permission: null
    # 无参数执行时
    execute:
      - 'tell: &7Argument Required!'
    # 参数及对应的反应
    arguments:
      example: 'open: example'

```
{% endcode %}

* 任何修改保存配置文件后都将自动生效
* 若新增命令，TAB 补全功能必须重启服务器才会有效

