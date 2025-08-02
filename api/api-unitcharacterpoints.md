# API UnitCharacterPoints

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the number of unspent talent points of the player.
 talentPoints = UnitCharacterPoints(unit)

==Arguments==
:;unit:{{apitype|string}} : [[UnitId]] - Only works on the player unit.

==Returns==
:;talentPoints:{{apitype|number}} - The quantity of unspent talent points the unit has available.

==Patch changes==
* {{Patch 4.0.1|note=Removed. The <code>emptyProfessions</code> return was replaced by {{api|GetProfessions}}()}}
```