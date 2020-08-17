---
description: 'หลังจากติดตั้งปลั๊กอินแล้ว, ไฟล์จะถูกสร้างภายในโฟลเดอร์ plugins'
---

# ตั้งค่าปลั๊กอิน

## ไฟล์/โฟลเดอร์

{% tabs %}
{% tab title="/settings.yml" %}
ไฟล์ตั้งค่าหลักของปลั๊กอิน
{% endtab %}

{% tab title="/menus/" %}
โฟลเดอร์สำหรับเก็บเมนูของปลั๊กอิน
{% endtab %}

{% tab title="/lang/en\_US.yml" %}
คุณสามารถแก้ไขข้อความทั้งหมดของปลั๊กอินได้ในไฟล์นี้
{% endtab %}

{% tab title="/items.yml" %}
ที่เก็บข้อมูลไอเท็มที่สร้างด้วยคำสั่ง `/trmenu itemRepo`
{% endtab %}
{% endtabs %}

## การตั้งค่า

* ไฟล์`settings.yml` คือไฟล์ตั้งค่าหลักของปลั๊กอินนี้
* ปลั๊กอินจะทำการ reload โดยอัตโนมัติ เมื่อมีการแก้ไขไฟล์ตั้งค่า

{% code title="settings.yml" %}
```yaml
#
# Configuration
#
Options:
  # Whether the debug mode should be enabled or not (more information will be sent to the console)
  Debug: false
  # Language of the plugin
  # Available： zh_CN, zh_TW, en_US, fr_FR, th_TH, es_MX
  Locale: en_US
  # Whether to hide the Logo of the plugin in the console on startup
  Hide-Logo: false
  # When enabled TrMenu will get the player heads datas from Mojang's API
  # [RECOMMENDED] If disabled, it will get them with https://github.com/Electroid/mojang-api
  Skull-Mojang-API: false

#
# Get menus from a path leading to a folder or directly a menu
# Supports ItemRepo files to get pre-made items for your menus
#
Load-Menu-Files:
  - 'plugins/CustomMenusFolder'

#
# Actions Configuration
#
Actions:
  # Customize the words used to cancel an input catcher, supports regex
  Catcher-Cancel-Words:
    - '(?i)cancel|quit|exit|end|stop'

#
# Menu Items Configuration
#
Item:
  # Default color for items' names
  Default-Color-Name: '&7'
  # Default color for items' lores
  Default-Color-Lore: '&7'

#
# Actions Shortcuts Configuration
#
Shortcuts:
  Offhand: 'open: Example'
  Sneaking-Offhand:
    - condition: 'hasPerm.trmenu.shortcut'
      execute: 'open: Example'
  Right-Click-Player: []
  Sneaking-Right-Click-Player: []
  PlayerInventory-Border-Left: []
  PlayerInventory-Border-Right: []
  PlayerInventory-Border-Middle: []

#
# Register commands with actions and arguments
# Supports tab-completition !
# (WARNING: A server restart is required to add, change or remove commands)
#
RegisterCommands:
  # Command name
  openMenus:
    # Command Aliases
    aliases: []
    # Required permission
    permission: null
    # Actions executed without any arguments
    execute:
      - 'tell: &7Argument `example` Required!'
    # Arguments with their actions
    arguments:
      example: 'open: example'

#
# When enabled, TrMenu will ignore cancelled events monitored by some plugins
# If you encouter compatibilities issues, try to toggle the option.
#
Events-Ignore-Cancelled:
  PlayerCommandPreprocessEvent: true
  InventoryOpenEvent: true
  InventoryClickEvent: true
```
{% endcode %}

