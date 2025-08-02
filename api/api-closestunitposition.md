# API ClosestUnitPosition

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Unit}}
Returns the unit position of the closest creature by ID. Only works for mobs in the starting zones.
 xPos, yPos, distance = ClosestUnitPosition(creatureID)

==Arguments==
:;creatureID:{{apitype|number}} - NPC ID of a [[GUID]] of a creature.

==Returns==
:;xPos:{{apitype|number}}
:;yPos:{{apitype|number}}
:;distance:{{apitype|number}} - Relative distance in yards.

==Patch changes==
* {{Patch 8.0.1|note=Added.}}
```