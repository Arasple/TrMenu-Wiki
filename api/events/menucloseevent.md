# MenuCloseEvent

```kotlin
package me.arasple.mc.trmenu.api.events

import io.izzel.taboolib.module.event.EventCancellable
import me.arasple.mc.trmenu.display.Menu
import org.bukkit.entity.Player

/**
 * @author Arasple
 * @date 2020/7/7 9:31
 */
class MenuCloseEvent(val player: Player, val menu: Menu, val page: Int, val reason: Reason, val silent: Boolean) : EventCancellable<MenuCloseEvent>() {

    enum class Reason {

        CONSOLE,

        OP,

        PLAYER,

        MENU_RELOAD,

        SWITCH_MENU,

        SWITCH_BUKKIT_INVENTORY,

        SWITCH_PAGE,

        ERROR;

        fun isSwitch() = this == SWITCH_MENU || this == SWITCH_PAGE || this == MENU_RELOAD

    }

}
```

