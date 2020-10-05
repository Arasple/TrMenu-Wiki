# 动作

## 介绍

* TrMenu 提供大量完善的 **动作** ，皆在提高菜单制作效率 & 减少繁琐命令
* 无论是显示 Title、Actionbar，还是构建一条支持变量的 Json 消息，你都可以轻松实现
* 除此之外，每条动作都支持多个独立的动作 **选项** ，包括延时、条件、概率和遍历等

## 变量

* 动作的所有内容均支持使用 **PlaceholderAPI 变量，颜色代码**
* 也支持使用 TrMenu 的 菜单参数, Meta 元素，内置函数 等

## 捆绑

* 将多个动作绑定到一行内容，动作选项共享
* 使用 **&&&** 或 **\_**_\*\*\|\|\_ **连接** ，\*\*例如\_

```yaml
- 'rem-meta: angryBee &&& refresh &&& sound: ENTITY_SPIDER_STEP-1-2<delay:80>'

# 实质上等同于
- 'rem-meta: angryBee<delay:80>'
- 'refresh<delay:80>'
- 'sound: ENTITY_SPIDER_STEP-1-2<delay:80>'
```

