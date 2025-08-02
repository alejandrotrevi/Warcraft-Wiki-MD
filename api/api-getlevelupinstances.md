# API GetLevelUpInstances

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns a list of dungeon/raid IDs that are advertised as available at a given level.
 id1, id2, ... = GetLevelUpInstances(level, isRaid)

==Arguments==
:;level:{{apitype|number}} - level at which to list newly-available instances.
:;isRaid:{{apitype|boolean}} - true to list raid instances, false to list dungeons.

==Returns==
:;id1, id2, ...:{{apitype|number}} - LFG Dungeon IDs of dungeons/raids that are advertised to a character reaching a given level.

==Details==
* This function does not return ''all'' available dungeon IDs -- rather, it appears to return some selection that might be immediately approachable by a player reaching that level. For instance, for level 60, the only raid instance returned is [[Molten Core]].
* You can retrieve information about the offered dungeons using {{api|GetLFGDungeonInfo}}.

==Patch changes==
* {{Patch 11.2.0|note=Readded.}}
* {{Patch 9.1.0|note=Removed.}}
* {{Patch 5.0.4|note=Added.}}
```