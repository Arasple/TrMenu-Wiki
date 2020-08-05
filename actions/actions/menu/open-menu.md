# 打开菜单

## 节点

```text
open(s)?|(open)?(-)?gui|(tr)?menu
```

## 示例

```yaml
- 'open: Example'
```

```yaml
# 打开菜单 Shop-Handler,
# 指定参数为 [APPLE, 10, 1]

- 'open: Shop-Handler APPLE 10 1'
```

```yaml
# 打开菜单 Test 的页码 3,
# 指定参数为 [Hello Arasple, Arg2]

- 'open: Test:2 `Hello Arasple` Arg2'
```

