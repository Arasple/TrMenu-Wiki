# Tipos

## Introduction

* TrMenu provides a lot of action types improving the efficiency of the menu and reducing the use of commands = less plugins for commands needed
* Whether you want to display a Title, an Actionbar or a JSON message all supporting a huge amount of placeholders, you can easily achive this
* With all of this, you can also add per actions options:
  * Delay
  * Conditions
  * Probability
  * All Players

## Placeholders

* Every single action supports PlaceholderAPI placeholders and color codes
* They also support TrMenu's own placeholders such as Arguments, Metas/Datas, Scripts...

## All in One line

* You can bind together multiple actions on one single line
* Use `&&&` or `_||_` to do so

```yaml
- 'rem-meta: angryBee &&& refresh &&& sound: ENTITY_SPIDER_STEP-1-2<delay:80>'

# Equivalent to:
- 'rem-meta: angryBee<delay:80>'
- 'refresh<delay:80>'
- 'sound: ENTITY_SPIDER_STEP-1-2<delay:80>'
```

