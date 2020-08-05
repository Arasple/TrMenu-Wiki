---
description: 初次安装本插件后，会在插件目录下产生一些文件
---

# 配置

## 文件

{% tabs %}
{% tab title="lang/zh\_CN.yml" %}
TLocale 语言文件, 你可以编辑大多数插件的消息
{% endtab %}

{% tab title="menus" %}
默认的菜单加载目录
{% endtab %}

{% tab title="items.yml" %}
物品仓库存储功能
{% endtab %}

{% tab title="settings.yml" %}
插件的设置文件
{% endtab %}
{% endtabs %}

## 设置

* 使用文本编辑器打开 settings.yml，你可以在此编辑插件的相关设置
* 插件将自动监听保存改动，重新载入

{% code title="settings.yml" %}
```yaml
#
# 插件的相关选项
#
Options:
  # 是否启用调试模式 (将打印更多信息到控制台)
  Debug: false
  # 使用的语言文件
  # 可用： zh_CN, zh_TW, en_US
  Locale: zh_CN
  # 是否隐藏插件启动时的 Logo
  Hide-Logo: false
  # 联网加载头颅材质是否使用 Mojang API
  # 不启用则默认使用 https://api.minetools.eu/
  Skull-Mojang-API: false

#
# 自定义加载菜单的文件或目录
# 支持多级子目录itemRepo
#
Load-Menu-Files:
  - 'plugins/CustomMenusFolder'

#
# 动作相关设置
#
Actions:
  # 指定取消捕获器的内容, 支持正则
  Catcher-Cancel-Words:
    - '(?i)cancel|quit|exit|end|stop'
    - '取消|退出'

#
# 菜单物品相关
#
Item:
  # 默认物品名称的颜色
  Default-Color-Name: '&7'
  # 默认物品描述的颜色
  Default-Color-Lore: '&7'

#
# 快捷操作执行动作
#
Shortcuts:
  Offhand: []
  Sneaking-Offhand:
    - condition: 'hasPerm.trmenu.shortcut'
      execute: 'open: Example'
  Right-Click-Player: []
  Sneaking-Right-Click-Player: []
  PlayerInventory-Border-Left: []
  PlayerInventory-Border-Right: []

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

#
# 控制一些插件监听的 Bukkit 事件，是否忽略已被取消的事件
# 如果遇到一些兼容性问题可以尝试调整
#
Events-Ignore-Cancelled:
  # 监听菜单打开命令
  PlayerCommandPreprocessEvent: true

```
{% endcode %}

