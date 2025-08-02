# API UnitStat

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Unit}}
Returns the basic attributes for a unit (strength, agility, stamina, intellect).
 currentStat, effectiveStat, statPositiveBuff, statNegativeBuff = UnitStat(unit, statID)

==Arguments==
:;unit:{{apitype|UnitToken}} - Only works for <code>"player"</code> and <code>"pet"</code>. Will work on <code>"target"</code> as long as it is equal to <code>"player"</code>)
:;statID:{{apitype|number}} - An internal id corresponding to one of the stats.
<onlyinclude>:::* <code>1: LE_UNIT_STAT_STRENGTH</code>
:::* <code>2: LE_UNIT_STAT_AGILITY</code>
:::* <code>3: LE_UNIT_STAT_STAMINA</code>
:::* <code>4: LE_UNIT_STAT_INTELLECT</code>
:::* <code>5: LE_UNIT_STAT_SPIRIT</code> (not anymore available in 9.0.5)</onlyinclude>

==Return==
:;currentStat:{{apitype|number}} - The unit's stat. Seems to always return the same as effectiveStat, regardless of values of pos/negBuff.
:;effectiveStat:{{apitype|number}} - The unit's current stat, as displayed in the [[paper doll|paper doll frame]].
:;statPositiveBuff:{{apitype|number}} - Any positive buffs applied to the stat. Including gear.
:;statNegativeBuff:{{apitype|number}} - Any negative buffs applied to the stat.

==Example==
Shows your current strength.
 local stat, effectiveStat, posBuff, negBuff = UnitStat("player", 1);
 DEFAULT_CHAT_FRAME:AddMessage("Your current Strength is ".. stat);
```