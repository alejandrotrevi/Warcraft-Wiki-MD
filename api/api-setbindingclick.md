# API SetBindingClick

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{restrictedapi|nocombat|note=Restricted since patch 2.0; Snippets executed by [[SecureHandlers]] may alter [override] bindings while in combat.}}
Sets a binding to click the specified Button widget.
 ok = SetBindingClick(key, buttonName[, button])

==Arguments==
:;key:{{apitype|string}} - Any binding string accepted by World of Warcraft. For example: "ALT-CTRL-F", "SHIFT-T", "W", "BUTTON4".
:;buttonName:{{apitype|string}} - Name of the button you wish to click.
:;button:{{apitype|string}} - Value of the button argument you wish to pass to the OnClick handler with the click; "LeftButton" by default.

==Returns==
:;ok:{{apitype|boolean}} - 1 if the binding has been changed successfully, nil otherwise.

==Details==
* This function is functionally equivalent to the following statement.
 ok = {{api|SetBinding}}("key", "CLICK " .. buttonName .. (button and (":" .. button) or ""));
* A single binding can only be bound to a single command at a time, although multiple bindings may be bound to the same command. The Key Bindings UI will only show the first two bindings, but there is no limit to the number of keys that can be used for the same command.
* You must use {{api|SetBinding}} to unbind a key.

==See Also==
* {{api|SetBinding}}
```