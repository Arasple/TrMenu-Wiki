---
description: Open the specified menu
---

# Open

## Usage

```text
open(s)?|(open)?(-)?gui|(tr)?menu
```

## Examples

```yaml
- 'open: Example'
```

```yaml
# Opens the menu Shop-Handler,
# with the arguments [APPLE, 10, 1]

- 'open: Shop-Handler APPLE 10 1'
```

```yaml
# Opens the menu Test at the third layout,
# and the arguments [Hello Arasple, Arg2]

- 'open: Test:2 `Hello Arasple` Arg2'
```

