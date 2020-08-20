---
description: Aprende a convertir menús de plugins viejos a menús de TrMenu
---

# Convertidor/Migración

### Plugins Compatibles

| Plugin | Compatibilidad |
| :--- | :--- |
| TrMenu v1 | √ |
| DeluxeMenus | Próximamente |
| BossShopPro | × |
| ChestCommands | × |

### ¿Cómo convertir menús?

* Con TrMenu puedes convertir menús mediante archivos separados o convertir una carpeta llena de menús viejos
* Si quieres convertir menús de TrMenu v1 debes escribir "legacy" en lugar del nombre del plugin.
* Los menús viejos con renombrados con .MIGRATED al final, se sugiere eliminarlos después de eso

### Archivos separados

* Para convertir archivos por separado debes poner el archivo en la carpeta de TrMenu y luego usar el comando: `/trmenu migrate <plugin> <archivo>`
* Ejemplos:
  * `/trmenu migrate legacy kits.yml`
  * `/trmenu migrate DeluxeMenus menusViejos/menu.yml`

### Carpeta con menús

* Para convertir una carpeta con menús debes ponerla dentro de la carpeta de TrMenu y luego usar el comando: `/trmenu migrate <plugin> <carpeta>`
* Ejemplos:
  * `/trmenu migrate legacy menusViejos`
  * `/trmenu migrate DeluxeMenus gui_menus`

Si todo sale bien encontrarás los menús convertidos en la ubicación`/plugins/TrMenu/migrated/`

Luego si quieres que el menú migrado funcione muévelo a la ubicación`/plugins/TrMenu/menus/` y usa el comando `/trmenu reload`

