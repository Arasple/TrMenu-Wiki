---
description: Migrate configuration files from other menus into TrMenu's format
---

# Migrate

## Supported Plugins

| Plugins | Supported? |
| :--- | :--- |
| TrMenu v1 | √ |
| DeluxeMenus | × |
| BossShopPro | × |
| ChestCommands | × |

## How to migrate menus?

### Seperated Files

* To migrate files speerately, put the file in your TrMenu folder and execute this command from the console: 
* Examples:
  * `trmenu migrate TrMenuV1 kits.yml`
  * `trmenu migrate TrMenuV1 oldMenus/menu.yml`

### Whole Folder

* To migrate a whole folder of menus at once, put the file in your TrMenu folder and execute this command from the console: `trmenu migrate <plugin> <path to file>`
* Example:
  * `trmenu migrate TrMenuV1 oldMenus`

If everything goes well, you can find all your migrated menus in `/TrMenu/migrated/`

To load the migrated menus, just copying them into the `/TrMenu/menus/` and execute `/trmenu reload`

