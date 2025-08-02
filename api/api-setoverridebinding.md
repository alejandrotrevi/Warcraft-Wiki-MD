# API SetOverrideBinding

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{restrictedapi|nocombat|note=Restricted since patch 2.0}}
Sets an override key binding.
 SetOverrideBinding(owner, isPriority, key, command)

==Arguments==
:;owner:{{apitype|Frame}} - The frame this binding "belongs" to; this can later be used to clear all override bindings belonging to a particular frame.
:;isPriority:{{apitype|boolean}} - true if this is a priority binding, false otherwise. Both types of override bindings take precedence over normal bindings.
:;key:{{apitype|string}} - Binding to bind the command to. For example, "Q", "ALT-Q", "ALT-CTRL-SHIFT-Q", "BUTTON5"
:;command:{{apitype|string}} - Any name attribute value of a Bindings.xml-defined binding, or an action command string; nil to remove an override binding. For example:
::* "SITORSTAND" : a Bindings.xml-defined binding to toggle between sitting and standing
::* "CLICK PlayerFrame:LeftButton" : Fire a left-click on the PlayerFrame.
::* "SPELL Bloodrage" :  Cast Bloodrage.
::* "ITEM Hearthstone" : Use {{item|Hearthstone}}
::* "MACRO Foo" : Run a macro called "Foo"
::* "MACRO 1" : Run a macro with index 1.

==Details==
* Override bindings take precedence over the normal {{api|SetBinding}} bindings. Priority override bindings take precedence over non-priority override bindings.
* Override bindings are never saved, and will be wiped by an interface reload.

==See also==
* {{api|SetOverrideBindingSpell}}
* {{api|SetOverrideBindingItem}}
* {{api|SetOverrideBindingMacro}}
* {{api|SetOverrideBindingClick}}
* {{api|ClearOverrideBindings}}
```