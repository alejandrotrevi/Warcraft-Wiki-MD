# API UnitDistanceSquared

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{restrictedapi|noinstance}}
Returns the squared distance to a unit in your group.
 distanceSquared, checkedDistance = UnitDistanceSquared(unit)

==Arguments==
:;unit:{{apitype|string}} : [[UnitId]] - The unit id of a player in your group.

==Returns==
:;distanceSquared:{{apitype|number}} - the squared distance to that unit
:;checkedDistance:{{apitype|boolean}} - true if the distance result is valid, false otherwise (eg. unit not found or not in your group)

==Patch changes==
* {{Patch 7.1.0|note=Returns nil while inside a restricted area (instance/battleground/arena).}}
```