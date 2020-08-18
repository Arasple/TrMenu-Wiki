---
description: >-
  près avoir installé TrMenu,  des fichiers seront générés dans le dossier
  plugins
---

# Setup

## Files/Folders

{% tabs %}
{% tab title="/settings.yml" %}
Configuration principale du plugin.
{% endtab %}

{% tab title="/menus/" %}
Dossier par défaut de chargement des menus
{% endtab %}

{% tab title="/lang/fr\_FR.yml" %}
Vous pouvez modifier la majorité des messages du plugin dans le fichier langage
{% endtab %}

{% tab title="/items.yml" %}
Stockage pour items créés avec la commande `/trmenu itemRepo`
{% endtab %}
{% endtabs %}

## Setup

* Le fichier `settings.yml` est la configuration principale de TrMenu.
* Le plugin détectera tout changements automatiquement et rechargera le fichier.

{% code title="settings.yml" %}
```yaml
#
# Configuration
#
Options:
  # Activer ou désactiver le mode debug (plus d'information sera envoyé dans la console)
  Debug: false
  # Langage du plugin
  # Disponible: zh_CN, zh_TW, en_US, fr_FR, th_TH, es_MX
  Locale: en_US #Vous pouvez le modifier en fr_FR pour mettre le plugin en français
  # Cacher le Logo du plugin dans la console au démmarage
  Hide-Logo: false
  # Quand activé, TrMenu récupèrera les données des têtes des joueurs depuis l'API de Mojang
  # [RECOMMENDED] Si désactivé, il les récupèrera avec https://github.com/Electroid/mojang-api
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

