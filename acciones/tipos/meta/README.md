# Datas

## Introduction

* TrMenu provides two data types: Meta and Data
  * The Meta is stored in the plugin's memory and will be reset on reload
  * The Data is stored in a SQLite database and will be kept until erased \(check the `/plugins/TabooLib/playerdata/`folder\)

## Usage

After you defined the Meta/Data, you can call them with the following placeholders:

```text
{meta:<KeyName>}
```

```text
{data:<KeyName>}
```

## Example

```yaml
Bee:
  update: [-1, -1, -1, 20]
  display:
    material: '<skull:b727d0ab03f5cd022f8705d3f7f133ca4920eae8e1e47b5074433a137e691e4e>'
    name: '&eBee ~'
    slots:
      - [9]
      - [18]
      - [28]
      - [29]
      - [30]
      - [31]
      - [32]
      - [33]
      - [34]
      - [35]
      - [26]
      - [16]
      - [15]
      - [14]
      - [13]
      - [12]
      - [11]
      - [10]
  actions:
    all:
     # Here, we set the meta angryBee to true
      - 'set-meta: angryBee true'
      - 'sound: ENTITY_ENDERMAN_HURT-1-2'
      # Then we refresh and remove it at the same time to make the icon change a bit random
      - 'rem-meta: angryBee &&& refresh &&& sound: ENTITY_SPIDER_STEP-1-2<Delay=80>'
      - 'refresh'
  icons:
    # We then check for the angreeBee meta, if it equals true, it will display this icon
    - condition: 'equals.{meta:angryBee}.true'
      inherit: true
      display:
        name: '&cBee &4~'
        material: '<skull:e6b74e052b74288799ba6d9f35c5d0221cf8b04331547ec2f68d73597ae2c9b>'
      actions:
        all: 'sound: ENTITY_ENDERMAN_HURT-1-2'
```

