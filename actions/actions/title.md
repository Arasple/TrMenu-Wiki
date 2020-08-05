---
description: 向玩家显示 TITLE & SUBTITLE
---

# 发送 Title & SubTitle

## 节点

```text
(send)?(-)?(sub)?title(s)?
```

## 示例

```yaml
# 旧版写法，需要以 <Key=Value> 的格式指定各属性
- 'title: <TITLE=WELCOME><SUBTITLE=%player_name%~><FADEIN=20><STAY=20><FADEOUT=10>'
```

```yaml
# 新版简写方法
# 用 \s 代替标题中需要使用的空格
- 'title: WELCOME %player_name%~ 20 20 10'
```

