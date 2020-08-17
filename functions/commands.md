---
description: All TrMenu's commands explained and detailed!
---

# Commands

## /trmenu action &lt;player&gt; &lt;action&gt;

Execute a TrMenu action for the specified player.

## /trmenu debug

Enable/Disable the Debug mode to get more information in the console about everything related to TrMenu

## /trmenu item &lt;toJson/fromJson&gt;

### /trmenu item toJson

Allows you to get the JSON format of the item you are currently holding

### /trmenu item fromJson

-

## /trmenu itemRepo &lt;add/give/remove&gt; &lt;identifier&gt;

### /trmenu itemRepo add &lt;identifier&gt;

Adds the item you are currently holding to the the item repository with the specified identifier  
You can then give yourself the item with the next command, or display it in menus by setting the material to `<repo:<identifier>>`

### /trmenu ItemRepo give &lt;identifier&gt;

Gives the specified item from the repository to the player

### /trmenu itemRepo remove &lt;identifier&gt;

Removes the specified item from the repository

## /trmenu list \[filter\]

Lists all loaded menus  
You can set a filter to only get the menus with the specified characters

## /trmenu migrate &lt;plugin&gt; &lt;file/folder&gt;

Migrates menu files from another plugin into TrMenu's format  
More info:

{% page-ref page="../migrate.md" %}

## /trmenu open &lt;menu&gt;:\[shape\] \[player\] \[args....\]

Opens a menu to a player \(if specified, else, the user executing the command\) with arguments \(if specified\)

## /trmenu reload

Reloads TrMenu's configuration files

## /trmenu sounds \[filter\]

-

## /trmenu template \[size\]

Allows you to quickly generate a menu where you can dispose your items, and then get a link to a Hastebin paste containing the menu configuration when closing the template menu.

