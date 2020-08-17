---
description: Menu options
---

# Options

## Example

```yaml
#Menu Options (All are optional)

Options:
  #Use the arguments of an open command as variables (Example: {0} for the first argument, {1} for the second etc...)
  Arguments: false
  #Default arguments when you open the menu without any (Example: [hello,all,1,5] )
  Default-Arguments: []
  #Default shape used when you open the menu.
  Default-Layout: 0
  #Hide the inventory of the player when he opens the menu (the player still has his items, TrMenu will just make the client think he doesn't until he closes the menu).
  Hide-Player-Inv: false
  #Delay between each click on a button
  Min-Click-Delay: 200
  #Automatically download PlaceholderAPI's expansions
  Depend-Expansions:
    - 'server'
    - 'player'
    - 'progress'
    - 'math'
```

## Notes

* If the default arguments option is set, the arguments not provided by the player will be taken from the default arguments. Example:
  * `Default-Arguments: ["TrMenu", "Arasple"]`
  * If the player provides only the argument `TrMenu`, then the second argument will be automatically defined as `Arasple`
* The `default-Layout: #` option will show the first layout if the specified one doesn't exist. You can also set the layout if you open the menu with the command \`/trmenu open &lt;menu&gt;:&lt;layout&gt;
  * Example: `/trmenu open ShopGUI+:2 Tanguygab`

