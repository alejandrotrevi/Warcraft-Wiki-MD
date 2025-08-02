# API SetOverrideBindingClick

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{restrictedapi|nocombat|note=Restricted since patch 2.0}}
Sets an override binding that performs a button click.
 SetOverrideBindingClick(owner, isPriority, key, buttonName [, mouseClick])

==Arguments==
:;owner:{{apitype|Frame}} - The frame this binding "belongs" to; this can later be used to clear all override bindings belonging to a particular frame.
:;isPriority:{{apitype|boolean}} - true if this is a priority binding, false otherwise. Both types of override bindings take precedence over normal bindings.
:;key:{{apitype|string}} - Binding to bind the command to. For example, "Q", "ALT-Q", "ALT-CTRL-SHIFT-Q", "BUTTON5"
:;buttonName:{{apitype|string}} - Name of the button widget this binding should fire a click event for.
:;mouseClick:{{apitype|string?}} - Mouse button name argument passed to the OnClick handlers.

==Details==
* Override bindings take precedence over the normal {{api|SetBinding}} bindings. Priority override bindings take precedence over non-priority override bindings.
* Override bindings are never saved, and will be wiped by an interface reload.
* You cannot use this function to clear an override binding; use {{api|SetOverrideBinding}} instead.

==See also==
* {{api|SetOverrideBinding}}
* {{api|SetOverrideBindingSpell}}
* {{api|SetOverrideBindingItem}}
* {{api|SetOverrideBindingMacro}}
* {{api|ClearOverrideBindings}}
```