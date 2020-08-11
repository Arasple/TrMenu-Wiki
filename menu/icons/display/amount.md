---
description: Amount of items displayed
---

# Amount

## Usage

```text
(amt|amount)(s)?
```

## Example

```yaml
# Static amount
amount: 10

# Dynamic quantity (the placeholder must return a number)
amount: '%server_time_s%'
```

## Note

* Dynamic amounts will be updated alongside the material update interval
* If the value given is 65 or above, the amount will stay at 64.
* If the value is 0, the item won't be displayed.

