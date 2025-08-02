# API UnitHasLFGDeserter

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns whether the unit is currently unable to use the dungeon finder due to leaving a group prematurely.
 isDeserter = UnitHasLFGDeserter(unit)

==Arguments==
:;unit:{{apitype|string}} : [[UnitId]] - the unit that would assist (e.g., "player" or "target")

==Returns==
:;isDeserter:{{apitype|boolean}} - true if the unit is currently an LFG deserter (and hence unable to use the dungeon finder), false otherwise.

==History==
* Added in [[Patch 3.3.3]].
```