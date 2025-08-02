# API GetMacroIndexByName

**Contributor:** Numynum

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the index for a macro by name.
 macroSlot = GetMacroIndexByName(name)

==Arguments==
:;name:{{apitype|string}} - Macro name to query.

==Returns==
:;macroSlot:{{apitype|number}} - Macro slot index containing a macro with the queried name, or 0 if no such slot exists.

==Details==
* Slots 1-120 are used for general macros, and 121-150 for character-specific macros.
* Seems to return the first matching index, if there are duplicates

==See also==
* {{api|GetMacroInfo}}
```