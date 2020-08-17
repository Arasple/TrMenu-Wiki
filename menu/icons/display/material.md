---
description: Material of the displayed item
---

# Material

## Property

```text
(mat(erial)?|texture)(s)?
```

## Example

```yaml
  '*':
    update: [-1, 5, 20, -1]
    display:
      material: '<skull:9842dc3b917b1a796c303e15105474a8e315de7982b6ca54feafb5a4d13d4e95>'
```

```yaml
  'Close':
    update: [25, 5, -1, -1]
    display:
      # Dynamic material effect
      materials:
      - 'Red Stained Glass Pane'
      - 'Orange Stained Glass Pane'
      name: ['&cC&7lose', '&cCl&7ose', '&cClo&7se', '&cClos&7e', '&cClose']
```

## Basic Items 

```yaml
# Standart material name
material: 'CYAN_STAINED_GLASS_PANE'

# Ignore the case
material: 'Cyan Stained Glass Pane'

# (1.8-1.12) ID in numbers
material: 160

# (1.8-1.12) ID in numbers + Data value
material: '3:2'
```

## Data value

```yaml
# Same as stated above: '3:2'
# or also:
material: '3<data:2>'
```

## CustomModelData value

```yaml
# (1.14+) Write the specific model tag after the material 
material: 'coal<model-data:1>'
```

## Player Heads

```yaml
# You can use player names...
material: '<head:BlackSKY>'

# ...or also placeholders
material: '<head:%player_name%>'
```

* TrMenu uses NMS to get the head of all online players + an asynchronous network to get those from other players
* Does not impact the TPS

## Skull from Texture

```yaml
# Type Ⅰ
material: '<skull:eyJ0ZXh0dXJlcyI6eyJTS0lOIjp7InVybCI6Imh0dHA6Ly90ZXh0dXJlcy5taW5lY3JhZnQubmV0L3RleHR1cmUvNDRmNDUyZDk5OGVhYmFjNDY0MmM2YjBmZTVhOGY0ZTJlNjczZWRjYWUyYTZkZmQ5ZTZhMmU4NmU3ODZlZGFjMCJ9fX0=>'

# Type Ⅱ
material: '<skull:44f452d998eabac4642c6b0fe5a8f4e2e673edcae2a6dfd9e6a2e86e786edac0>'
```

{% embed url="https://minecraft-heads.com/custom-heads" %}

## Leather Armor with RGB colors

```yaml
# Add the rgb next to the armor material 
material: 'leather chestplate<dye:255,255,0>'
```

## Custom Banners Patterns

```yaml
material: 'white banner<banner:RED MOJANG,WHITE>'
```

{% embed url="https://hub.spigotmc.org/javadocs/bukkit/org/bukkit/block/banner/PatternType.html" %}

## JSON Items

```yaml
material: '{"type":"DIAMOND_SWORD","data":0,"amount":1,"meta":{"Damage":{"type":"INT","data":0}}}'
```

* Use the `/trmenu item toJson` command to get the JSON format of the item you are holding
* Supports all materials

## Item Repository

```yaml
material: '<repo:My_Custom_Item>'
```

* Use the `/trmenu itemRepo` command to manage your Item Repository

## HeadDatabase heads

```yaml
# Head ID
material: '<head-database:100>'

# Random head
material: '<head-database:random>'
```

## SkinsRestorer heads

```yaml
material: '<skins-restorer:JYBH>'
```

* For cracked servers with the SkinRestorer plugin installed, you can use this material type to get the head of your players through SR
* Supports placeholders

## Oraxen items

```yaml
material: '<oraxen:Id>'
```

