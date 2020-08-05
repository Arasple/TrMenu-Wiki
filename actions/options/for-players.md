# 遍历执行

## 节点

```text
<((p|(for|all)?(-)?players))[:=]?(.+)?>
```

## 示例

```yaml
- 'tell: broadcast message<Players>'
- 'tell: broadcast message for VIP<Players:hasPerm.vip.user>'
```

