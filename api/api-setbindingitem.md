# API SetBindingItem

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{restrictedapi|nocombat|note=Restricted since patch 2.0; Snippets executed by [[SecureHandlers]] may alter [override] bindings in-combat.}}
Sets a binding to use a specified item.
 ok = SetBindingItem(key, item)

==Arguments==
:;key:{{apitype|string}} - Any binding string accepted by World of Warcraft. For example: "ALT-CTRL-F", "SHIFT-T", "W", "BUTTON4".
:;item:{{apitype|string}} - Item name (or item string) you want the binding to use. For example: "Hearthstone", "item:6948"

==Returns==
:;ok:{{apitype|boolean}} - 1 if the binding has been changed successfully, nil otherwise.

==Details==
* This function is functionally equivalent to the following statement.
 ok = {{api|SetBinding}}("key", "ITEM " .. item);
* A single binding can only be bound to a single command at a time, although multiple bindings may be bound to the same command. The Key Bindings UI will only show the first two bindings, but there is no limit to the number of keys that can be used for the same command.
* You must use {{api|SetBinding}} to unbind a key.

==See Also==
* {{api|SetBinding}}
```