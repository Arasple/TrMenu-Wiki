---
description: Configurar tipo de inventario del menú
---

# Tipo de Inventario

**Formas de escribirlo**

* **Normal:** Type
* **RegEx:** \(inv\(entory\)?\)?\(-\)?type\(s\)?

### Tipo de inventario

* El tipo de inventario es la forma como quieres que se vea el menú, ya sea como un cofre o un dispensador.. etc.
* Algunos tipos de inventarios no son compatibles con el diseño del menú, así que en caso de usarlos deberás omitir la configuración del diseño del menú y tendrás que añadirle a cada botón por separado el slot o posición donde se mostrarán en el menú.

```yaml
Type: CHEST
```

**Tipos de inventarios disponibles:**

<table>
  <thead>
    <tr>
      <th style="text-align:left">Tipo</th>
      <th style="text-align:left">Traducci&#xF3;n (No usar)</th>
      <th style="text-align:left">
        <p>Compatible con</p>
        <p>el Dise&#xF1;o</p>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">CHEST</td>
      <td style="text-align:left">Cofre</td>
      <td style="text-align:left">SI</td>
    </tr>
    <tr>
      <td style="text-align:left">DROPPER</td>
      <td style="text-align:left">Soltador</td>
      <td style="text-align:left">SI</td>
    </tr>
    <tr>
      <td style="text-align:left">DISPENSER</td>
      <td style="text-align:left">Dispensador</td>
      <td style="text-align:left">SI</td>
    </tr>
    <tr>
      <td style="text-align:left">ANVIL</td>
      <td style="text-align:left">Yunque</td>
      <td style="text-align:left">NO</td>
    </tr>
    <tr>
      <td style="text-align:left">BEACON</td>
      <td style="text-align:left">Faro</td>
      <td style="text-align:left">NO</td>
    </tr>
    <tr>
      <td style="text-align:left">BREWING</td>
      <td style="text-align:left">Destiler&#xED;a de pociones</td>
      <td style="text-align:left">NO</td>
    </tr>
    <tr>
      <td style="text-align:left">CRAFTING</td>
      <td style="text-align:left">Crafteo r&#xE1;pido (2x2)</td>
      <td style="text-align:left">NO</td>
    </tr>
    <tr>
      <td style="text-align:left">CREATIVE</td>
      <td style="text-align:left">Accesos r&#xE1;pidos</td>
      <td style="text-align:left">NO</td>
    </tr>
    <tr>
      <td style="text-align:left">ENCHANTING</td>
      <td style="text-align:left">Mesa de encantar</td>
      <td style="text-align:left">NO</td>
    </tr>
    <tr>
      <td style="text-align:left">ENDER_CHEST</td>
      <td style="text-align:left">Cofre ender</td>
      <td style="text-align:left">NO</td>
    </tr>
    <tr>
      <td style="text-align:left">FURNACE</td>
      <td style="text-align:left">Horno</td>
      <td style="text-align:left">NO</td>
    </tr>
    <tr>
      <td style="text-align:left">HOPPER</td>
      <td style="text-align:left">Tolva</td>
      <td style="text-align:left">NO</td>
    </tr>
    <tr>
      <td style="text-align:left">MERCHANT</td>
      <td style="text-align:left">Men&#xFA; de aldeano</td>
      <td style="text-align:left">NO</td>
    </tr>
    <tr>
      <td style="text-align:left">PLAYER</td>
      <td style="text-align:left">Selector de armadura</td>
      <td style="text-align:left">NO</td>
    </tr>
    <tr>
      <td style="text-align:left">SHULKER_BOX</td>
      <td style="text-align:left">Caja Shulker</td>
      <td style="text-align:left">NO</td>
    </tr>
    <tr>
      <td style="text-align:left">WORKBENCH</td>
      <td style="text-align:left">Mesa de crafteo</td>
      <td style="text-align:left">NO</td>
    </tr>
  </tbody>
</table>

