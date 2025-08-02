# API CanInspect

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns true if the player can inspect the unit.
 canInspect = CanInspect(unit [, showError])

==Arguments==
:;unit:{{apitype|string}} : [[UnitId]]
:;showError:{{apitype|boolean?}} - If true, the function will display an error message ("You can't inspect that unit") if you cannot inspect the specified unit.

==Returns==
:;canInspect:{{apitype|boolean}} - True if you can inspect the specified unit

==Details==
* You cannot inspect NPCs, nor PvP-enabled hostile players in PvP-enabled locations.

==See also==
* {{api|NotifyInspect}}
```