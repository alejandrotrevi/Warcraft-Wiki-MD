# API PickupMacro

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{restrictedapi|nocombat|note=Restricted since patch 2.2}}
Places a macro onto the cursor.
 PickupMacro(name)

==Arguments==
:;name:{{apitype|number,string}} - The position or name (case insensitive) of the macro in the macro window, from left to right and top to bottom. Slots 1-120 are used for general macros, and 121-138 for character-specific macros.

==Example==
* Picks up the first character macro.
 PickupMacro(121)
* The macro named "Reload" is placed on the cursor. If there is no such named macro then nothing happens.
 PickupMacro("Reload")
```