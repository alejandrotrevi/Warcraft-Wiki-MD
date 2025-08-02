# API UnitDamage

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Unit}}
Returns the damage stats for the unit.
 minDamage, maxDamage, offhandMinDamage, offhandMaxDamage, posBuff, negBuff, percent = UnitDamage(unit)
 
==Arguments==
:;unit:{{apitype|UnitToken}} - Likely only works for <code>"player"</code> and <code>"pet"</code>. Possibly for [[Beast Lore]] <code>"target"</code>.

==Returns==
:;minDamage:{{apitype|number}} - The unit's minimum melee damage.
:;maxDamage:{{apitype|number}} - The unit's maximum melee damage.
:;offhandMinDamage:{{apitype|number}} - The unit's minimum offhand melee damage.
:;offhandMaxDamage:{{apitype|number}} - The unit's maximum offhand melee damage. (same as above)
:;posBuff:{{apitype|number}} - positive physical Bonus (should be >= 0)
:;negBuff:{{apitype|number}} - negative physical Bonus (should be <= 0)
:;percent:{{apitype|number}} - percentage modifier (usually 1; 0.9 for warriors in defensive stance)

==Details==
* Doesn't seem to return usable values for mobs, NPCs. The method returns 7 values, only some of which appear to be useful.
```