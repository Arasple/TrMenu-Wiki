---
description: Perfom (conditional) actions when opening/closing the menu
---

# Events

## Example

```yaml
Events:
 #Open events
  Open:
    #Condition which requires the player to have the permission trmenu.use to open it
    #OR if he reopened the menu because of the auto-reload
    #OR if the console opened the menu for the player. 
    - condition: 'hasPerm.trmenu.use or is.{reason}.RELOAD or is.{reason}.CONSOLE'
      #Actions executed if the player has the permission trmenu.use.
      actions:
        - 'sound: BLOCK_CHEST_OPEN-1-0'
      #Actions executed if the player doesn't have the permission trmenu.use.
      deny:
        - 'sound: ENTITY_ITEM_BREAK-1-0'
        - 'title: <title=&c&lPermission Required><subtitle=&7&lYou need permission &6&ltrmenu.use &7&lto open this menu>'
        #The return action won't let the menu open.
        - 'return'
  #Close events
  Close:
    #A simple sound action
    - 'sound: BLOCK_CHEST_CLOSE-1-0'
```

## Note

* The conditions will be explained in details later
* In the open menu event, the {reason} variable will return

  ```text
  me.arasple.mc.trmenu.api.events.MenuOpenEvent.Reason
  ```

  You can see how it is used in the example above, we check if the menu has been opened for the player by the console or if it was reopen for the player because of a reload.

* If the `return` action is executed,  the event will be canceled. You can see that we use this in the open event of the example in the deny commands of the condition. This way, if the player doesn't met the condition, it won't open the menu.
* Check this section of the wiki to get all Menu Events \(and their reasons for the Open and Close events\).

{% page-ref page="../../api/events/" %}



