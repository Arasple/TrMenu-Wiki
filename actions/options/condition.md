---
description: Execute actions if the conditioons are met
---

# Condition

## Usage

```text
<(r|require(ment)?|condition)[:=]( )?(.+>)
```

## Example

```yaml
- 'tell: VIP Message<Condition=hasPerm.group.vip>'
```

{% page-ref page="../../script/expressions/" %}

