# API SetOverrideBindingSpell

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{restrictedapi|nocombat|note=Restricted since patch 2.0}}
Creates an override binding that casts a spell
 SetOverrideBindingSpell(owner, isPriority, key, spell)

==Arguments==
:;owner:{{apitype|Frame}} - The frame this binding "belongs" to; this can later be used to clear all override bindings belonging to a particular frame.
:;isPriority:{{apitype|boolean}} - true if this is a priority binding, false otherwise. Both types of override bindings take precedence over normal bindings.
:;key:{{apitype|string}} - Binding to bind the command to. For example, "Q", "ALT-Q", "ALT-CTRL-SHIFT-Q", "BUTTON5"
:;spell:{{apitype|string}} - Name of the spell you want to cast when this binding is triggered.

==Details==
* Override bindings take precedence over the normal {{api|SetBinding}} bindings. Priority override bindings take precedence over non-priority override bindings.
* Override bindings are never saved, and will be wiped by an interface reload.
* You cannot use this function to clear an override binding; use {{api|SetOverrideBinding}} instead.

==See also==
* {{api|SetOverrideBinding}}
* {{api|SetOverrideBindingClick}}
* {{api|SetOverrideBindingItem}}
* {{api|SetOverrideBindingMacro}}
* {{api|ClearOverrideBindings}}
```