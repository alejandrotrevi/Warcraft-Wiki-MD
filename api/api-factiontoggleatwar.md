# API FactionToggleAtWar

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Toggles the [[At War]] status for a faction.
 FactionToggleAtWar(rowIndex)

==Arguments==
:;rowIndex:{{apitype|number}} - The row index of the faction to toggle the At War status for. The row must have a true canToggleAtWar value (From [[API GetFactionInfo|GetFactionInfo]])

==Details==
The UPDATE_FACTION event will be fired after the change.
```