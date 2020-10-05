---
description: 显示的物品材质
---

# 材质

## 节点

```text
(mat(erial)?|texture)(s)?
```

## 示例

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
      # 动态材质，更新周期 25 ticks
      materials:
      - 'Red Stained Glass Pane'
      - 'Orange Stained Glass Pane'
      name: ['&cC&7lose', '&cCl&7ose', '&cClo&7se', '&cClos&7e', '&cClose']
```

## 原版物品

```yaml
# 直接书写标准材质名称
material: 'CYAN_STAINED_GLASS_PANE'

# 忽略大小写
material: 'Cyan Stained Glass Pane'

# (1.8-1.12) 数字 Id
material: 160

# (1.8-1.12) 数字 Id + 子 Id
material: '3:2'
```

## Data 值

```yaml
# 同上 '3:2'
material: '3<data:2>'
```

## CustomModelData 值

```yaml
# (1.14+) <ModelData> 标签前写具体的物品材质
material: 'coal<model-data:1>'
```

## 玩家头颅

```yaml
# 直接点名
material: '<head:BlackSKY>'

# 通过变量获取
material: '<head:%player_name%>'
```

* TrMenu 采用本地 NMS 读取在线玩家 + 异步联网读取离线玩家 皮肤材质
* 不会卡顿服务器，放心使用

## 纹理头颅

```yaml
# 类型 Ⅰ
material: '<skull:eyJ0ZXh0dXJlcyI6eyJTS0lOIjp7InVybCI6Imh0dHA6Ly90ZXh0dXJlcy5taW5lY3JhZnQubmV0L3RleHR1cmUvNDRmNDUyZDk5OGVhYmFjNDY0MmM2YjBmZTVhOGY0ZTJlNjczZWRjYWUyYTZkZmQ5ZTZhMmU4NmU3ODZlZGFjMCJ9fX0=>'

# 类型 Ⅱ
material: '<skull:44f452d998eabac4642c6b0fe5a8f4e2e673edcae2a6dfd9e6a2e86e786edac0>'
```

{% embed url="https://minecraft-heads.com/custom-heads" caption="" %}

## 染色皮革

```yaml
# <Dye> 标签前面写皮革物品对应的原版材质名
material: 'leather chestplate<dye:255,255,0>'
```

## 自定义旗帜

```yaml
material: 'white banner<banner:RED MOJANG,WHITE>'
```

{% embed url="https://hub.spigotmc.org/javadocs/bukkit/org/bukkit/block/banner/PatternType.html" caption="" %}

## JSON 物品

```yaml
material: '{"type":"DIAMOND_SWORD","data":0,"amount":1,"meta":{"Damage":{"type":"INT","data":0}}}'
```

* 通过 Item 子命令将物品转为 JSON 文本格式, 直接粘贴使用
* 支持一切物品材质

## 物品仓库

```yaml
material: '<repo:My_Custom_Item>'
```

## HeadDatabase 物品

```yaml
# 头颅 Id
material: '<head-database:100>'

# 随机头颅
material: '<head-database:random>'
```

## SkinsRestorer 头颅

```yaml
material: '<skins-restorer:JYBH>'
```

* 对于安装了 SkinsRestorer 皮肤插件的离线服务器，可以使用此类型来取得玩家头颅
* 同理支持使用变量

## Oraxen 物品

```yaml
material: '<oraxen:Id>'
```

