---
description: Ask the player to provide an input and get its value
---

# Input Catcher

## Usage

```text
(input)?(-)?catcher(s)?
```

## Example of the Old version

```yaml
- |-
  Catcher:
   <Type=CHAT>
   <Before=tell:请输入一个值>
   <Valid=tell: 你成功输入了一个数值 ${input}>
   <Invalid=tell: 你输入的不是一个数值>
   <Require=isNumber.${input}>
   <Cancel=tell: 已取消捕获器>
```

{% tabs %}
{% tab title="Type" %}
Type of the catcher \(see below\)
{% endtab %}

{% tab title="Before" %}
Actions executed before that the player inputs a message
{% endtab %}

{% tab title="Valid" %}
Actions executed when the input is given and when the requirements are met \(if defined\)
{% endtab %}

{% tab title="Invalid" %}
Actions executed when the requirements are not met
{% endtab %}

{% tab title="Require" %}
Once the player inputs a message, if the conditions are met, the Valid actions will be executed, else, the Invalid ones will
{% endtab %}
{% endtabs %}

## Example of the New Advanced version

```yaml
- catcher:

    target:
      type: CHAT
      before: 'tell: Enter a player name'
      cancel: 'tell: Cancelled...'
      reactions:
        - condition: 'bukkitServer.getOfflinePlayer("${input_target}").hasPlayedBefore() || isOnline.${input_target}'
          execute: 'tell: Player selected. ${input_target}'
          deny:
            - 'tell: ${input_target} has never played on this server before!'
            - 'return'

    amount:
      type: CHAT
      before: 'tell: Provide an amount to pay'
      cancel: 'tell: Cancelled'
      reactions:
        - condition: 'isNumber.${input_amount}'
          execute:
            - 'tell: Amount selected. $${input_amount}'
            - 'command: pay ${input_target} ${input_amount}'
          deny:
          - 'tell: You didn''t provide a valid number!'
          - 'retype'
```

* The `return`action will stop the following input catchers and actions
* The `retype`action will re-execute the input catcher

{% page-ref page="reinput.md" %}

## Types of Input Catcher

* CHAT
  * Gets the input of the player from the chat
* SIGN
  * Makes a sign pop-up and gets the input of the player
* ANVIL
  * Makes an anvil pop-up and gets the input of the player

