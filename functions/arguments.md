# Arguments

## 启用

* 菜单传参默认是开启的，你也可以在菜单配置的选项中关闭

{% page-ref page="../menu/structure/options.md" %}

## 传递

* 若菜单设置开启命令为 Example, 且开启参数功能
* 当玩家输入 /Example Agument1 Argument2 时，其菜单参数将设置为
  * \[Argument1, Argument2\] 2个
* 你也可以在开启命令、打开菜单动作中传递参数，或是通过设置参数动作二次更改参数
* 对于含有空格的参数，使用 \` \` 框起来

## 应用

* 菜单的参数可以当作 **变量** 来使用,
* {0} 对应第一个参数，{1} 对应第二个参数, 依此类推
* 对于 10个 以上的参数或是在部分特殊情况下，你也可以通过 PlaceholderAPI 变量来使用参数

{% page-ref page="../hook/placeholderapi.md" %}

