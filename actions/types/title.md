---
description: Display a title (and a subtitle) to the player
---

# Title/SubTitle

## Usage

```text
(send)?(-)?(sub)?title(s)?
```

## Examples

```yaml
# OLD FORMAT: You need to specify the every property in the <Key=Value> format
- 'title: <TITLE=WELCOME><SUBTITLE=%player_name%~><FADEIN=20><STAY=20><FADEOUT=10>'
```

```yaml
# NEW FORMAT: Use \s instead instead of spaces in the title
- 'title: Hello\sand\sWELCOME %player_name%~ 20 20 10'
```

