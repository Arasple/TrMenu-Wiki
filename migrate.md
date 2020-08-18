---
description: >-
  Convertir des fichiers de configuration de menus d'autres plugins dans le
  format de TrMenu
---

# Conversion

## Supported Plugins

| Plugins | Supported? |
| :--- | :--- |
| TrMenu v1 | √ |
| DeluxeMenus | Bientôt |
| BossShopPro | × |
| ChestCommands | × |

## Comment convertir des menus?

### Fichiers Séparés

* Pour convertir des fichiers séparément, mettez le fichier dans votre dossier TrMenu et exécutez cette commande depuis la console: `trmenu migrate <plugin> <fichier>` 
* Exemples:
  * `trmenu migrate TrMenuV1 kits.yml`
  * `trmenu migrate TrMenuV1 anciensMenus/menu.yml`

### Dossier Complet

* Pour convertir un dossier complet de menus, mettez le dossier dans votre dossier TrMenu et exécutez cette commande depuis la conse: `trmenu migrate <plugin> <chemin du dossier>`
* Exemple:
  * `trmenu migrate TrMenuV1 anciensMenus`

Si tout se passe bien, vous trouverez vos menus convertis dans dans le dossier `/TrMenu/migrated/`

Pour charger les menus convertis, copiez les juste dans votre dossier `/TrMenu/menus/` et exécutez`/trmenu reload`

