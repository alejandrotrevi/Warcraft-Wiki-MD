# API SetMacroSpell

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Changes the spell used for dynamic feedback for a macro. 
 SetMacroSpell(name, spell [, target])

==Arguments==
:;name:{{apitype|number,string}} - Index of the macro, using the values 1-36 for the first page and 37-54 for the second; or the name of the macro.
:;spell:{{apitype|string}} - Localized name of a spell to assign.
:;target:{{apitype|UnitToken}} - The unit to assign (for range indication).

==Details==
* When assigned to an action button, macros can provide dynamic feedback such as range indication, cooldown, and charges/quantity remaining.
* Normally, this dynamic feedback corresponds the action that the macro will take; however, this function directs the macro to provide feedback based on a particular spell instead.
* This only changes the visual cues appearing on the action buttons, but not the actual logic.  Clicking an action button executes the macro as written.

==See also==
* {{api|SetMacroItem}}
```