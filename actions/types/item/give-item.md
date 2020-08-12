---
description: Give items to the player
---

# Give-Item

## Usage

```text
(give|add)(-)?item(s)?
```

## Example

```yaml
# Give half a stack of diamonds with the name `&bCustom Diamond`
- 'give-item: material:DIAMOND,amount:32,name:&bCustom Diamond'
```

## Note

* Supports items in JSON format converted via the `/trmenu item toJson` command

