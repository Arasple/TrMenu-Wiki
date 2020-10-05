---
description: Configuración básica de TrMenu
---

# Configuración

## Archivos y Carpetas

Después de instalar TrMenu aparecerán varios archivos y carpetas en la ubicación /plugins

{% tabs %}
{% tab title="/settings.yml" %}
Archivo de configuración principal del plugin
{% endtab %}

{% tab title="/menus/" %}
Carpeta donde estarán ubicados los menús
{% endtab %}

{% tab title="/lang/es\_MX.yml" %}
Archivo de los mensajes del plugin en español
{% endtab %}

{% tab title="/items.yml" %}
Archivo donde se guardan los items del comando `/trmenu itemRepo`
{% endtab %}
{% endtabs %}

## Configuración del plugin

* Aquí verás el archivo `settings.yml` traducido al español con sus respectivas explicaciones.
* Conforme vayas revisando esta wiki entenderás para que sirve cada cosa de la configuración.
* Si editas este archivo el plugin aplicará los cambios al instante.

{% code title="settings.yml" %}
```yaml
#
# Configuración
#
Options:
  # Activar o desactivar el modo debug (se enviará más información sobre el plugin en la consola)
  Debug: false
  # Lenguaje del plugin
  # Disponibles： zh_CN, zh_TW, en_US, fr_FR, th_TH, es_MX
  Locale: es_MX
  # Activar o desactivar el logo del plugin en la consola al iniciar el servidor
  Hide-Logo: false
  # Cuando está activo se obtendrá la textura de las cabezas desde el API de Mojang
  # [RECOMENDADO] Si está desactivado, se obtendrá la textura desde https://api.minetools.eu/
  Skull-Mojang-API: false

#
# Opción para obtener menús desde una carpeta en específico
# Soporta archivos ItemRepo para obtener archivos pre-hechos de tus menús
#
Load-Menu-Files:
  - 'plugins/CustomMenusFolder'

#
# Configuración de los items de menú
#
Item:
  # Color por defecto del nombre de los items
  Default-Color-Name: '&7'
  # Color por defecto del lore de los items
  Default-Color-Lore: '&7'

#
# Atajos de la configuración de acciones
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
# Registrar comandos con acciones y argumentos
# Soporta tab-completition !
# (AVISO: Si cambias o mueves comandos debes reiniciar el servidor)
#
RegisterCommands:
  # Nombre del comando
  openMenus:
    # Alias del comandos
    aliases: []
    # Permiso requerido
    permission: null
    # Acciones que se ejecutarán sin argumentos
    execute:
      - 'tell: &7Argument `example` Required!'
    # Argumentos con sus respectivas acciones
    arguments:
      example: 'open: example'

#
# Cuando algo está activado, TrMenu ignorará los eventos monitoreados de otros plugins
# Si tienes incompatibilidades, trata desactivando la opción.
#
Events-Ignore-Cancelled:
  PlayerCommandPreprocessEvent: true
  InventoryOpenEvent: true
  InventoryClickEvent: true
```
{% endcode %}

