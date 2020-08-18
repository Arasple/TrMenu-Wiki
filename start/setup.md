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
# Charger des menus depuis un chemin menant à un dossier ou difrectement un fichier
# Supporte des fichiers de repo d'items pour avoir des items custom dans vos menus 
#
Load-Menu-Files:
  - 'plugins/CustomMenusFolder'

#
# Configuration d'Actions
#
Actions:
  # Customise les mots d'annulation des Input Catchers, supporte RegEx
  Catcher-Cancel-Words:
    - '(?i)cancel|quit|exit|end|stop'
    - '(?i)annul(e|er|é)?'

#
# Configuration d'Items de Menus
#
Item:
  # Couleur par défaut des noms d'items 
  Default-Color-Name: '&7'
  # Couleur par défaut des lores d'items
  Default-Color-Lore: '&7'

#
# Configuration des Raccourcis d'Actions
#
Shortcuts:
  # Seconde Main
  Offhand: 'open: Example'
  # Accroupi + Seconde Main
  Sneaking-Offhand:
    - condition: 'hasPerm.trmenu.shortcut'
      execute: 'open: Example'
  # Clic-Droit sur Joueur
  Right-Click-Player: []
  # Accroupi + Clic-Droit sur Joueur
  Sneaking-Right-Click-Player: []
  # Clic sur Bordure Gauche de l'inventaire
  PlayerInventory-Border-Left: []
  # Clic sur Bordure Droite de l'inventaire
  PlayerInventory-Border-Right: []
  # Clic au Milieu de l'inventaire
  PlayerInventory-Border-Middle: []

#
# Enregistrer des commandes avec des actions et arguments
# Supporte l'auto-complétion!
# (ATTENTION: Un redémmarage du serveur est requis pour ajouter, modifier ou supprimer des commandes)
#
RegisterCommands:
  # Nom de la Commande
  openMenus:
    # Aliases de la Commande
    aliases: []
    # Permission Requise
    permission: null
    # Actions exécutées sans aucun arguments
    execute:
      - 'tell: &7Argument `example` Required!'
    # Arguments avec leurs actions
    arguments:
      example: 'open: example'

#
# Quand activé,TrMenu ignorera les évènements annulés utilisés pas certains plugins
# Si vous rencontrer des problèmes de compatibilitées, essayez de modifier les options.
#
Events-Ignore-Cancelled:
  PlayerCommandPreprocessEvent: true
  InventoryOpenEvent: true
  InventoryClickEvent: true
```
{% endcode %}

