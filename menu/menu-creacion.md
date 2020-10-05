---
description: Cómo hacer un menú con TrMenu
---

# Creación

Existen diversas maneras de crear menús, van desde métodos simples a métodos complejos.

## Método I. Crear un menú en la carpeta de menús

* Ve a la ubicación `plugins/TrMenu/menus`, y crea un archivo .yml
* El nombre del archivo será el identificador del menú

Por ejemplo, al crear un archivo llamado `MenuNormal.yml` el menú se llamará "MenuNormal" dentro del plugin.

{% hint style="info" %}
Puedes crear carpetas dentro de la la ubicación **plugins/TrMenu/menus** para guardar tus menús de manera más organizada
{% endhint %}

## Método II. Crear una ubicación externa

* En la configuración del plugin existe la opción de "Load-Menu-Files" donde puedes añadir ubicaciones externas al plugin para cargar los menús.
* Puedes añadir ubicaciones de carpetas o archivos específicos.

{% tabs %}
{% tab title="EJEMPLO" %}
```yaml
# Con esta configuración cargará carpetas en diferentes lugares
Load-Menu-Files:
  - 'plugins/ASD/Carpeta'
  - 'world/playerdata/Carpeta'
  # También puede cargar archivos en específico
  - 'plugins/menus/MenuNormal.yml'
```
{% endtab %}
{% endtabs %}

