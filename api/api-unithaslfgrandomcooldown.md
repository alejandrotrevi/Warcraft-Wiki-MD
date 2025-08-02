# API UnitHasLFGRandomCooldown

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns whether the unit is currently under the effects of the random dungeon cooldown.
 hasRandomCooldown = UnitHasLFGRandomCooldown(unit)

==Arguments==
:;unit:{{apitype|string}} : [[UnitId]] - the unit that would assist (e.g., "player" or "target")

==Returns==
:;hasRandomCooldown:{{apitype|boolean}} - true if the unit is currently unable to queue for random dungeons due to the random cooldown, false otherwise.

==Details==
* Players may also be prevented from using the dungeon finder entirely, as part of the dungeon finder deserter effect. Use {{api|UnitHasLFGDeserter}}("unit") to query that.

==History==
* Added in [[Patch 3.3.3]]
```