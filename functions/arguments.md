# Arguments

## Enable

* The Option to transfer arguments is enabled by default, you can disable it by adding the option and setting it to false

{% page-ref page="../menu/structure/options.md" %}

## Usage

If a binded command is specified and the argument option is enabled, the player will be able to specify arguments by executing the command followed by some text, example: `/example arg0 arg1 arg2 ...`

You can also specify arguments in the `/trmenu open <menu> <player> arg0 arg1 ....`command, in the `open: <menu> arg0 arg1 ...`action and even change them through the menu with the `set-args: arg0 arg1 ...`action.

{% page-ref page="../actions/types/menu/open-menu.md" %}

{% page-ref page="arguments.md" %}

You can specify arguments with multiple words by surrounding them with \`\`, example:

```text
/example `arg 0` `arg 1`
```

## Application

You can call the arguments with a variable inside the menu:

* Use `{0}` for the first argument, `{1}`for the second, `{2}, {3}...`
* You can also call arguments through a PlaceholderAPI placeholder: `%trmenu_args_#%` where \# is the number of the argument

{% page-ref page="../plugins-compatibles/placeholderapi.md" %}

