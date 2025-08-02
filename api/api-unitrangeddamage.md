# API UnitRangedDamage

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Unit}}
Returns the ranged attack speed and damage of the unit.
 speed, minDamage, maxDamage, posBuff, negBuff, percent = UnitRangedDamage(unit)

==Arguments==
:;unit:{{apitype|UnitToken}} - The unit to get information from. (Likely only works for <code>"player"</code> and <code>"pet"</code> -- unconfirmed)

==Returns==
:;speed:{{apitype|number}} - The unit's ranged weapon speed (0 if no ranged weapon equipped).
:;minDamage:{{apitype|number}} - The unit's minimum ranged damage.
:;maxDamage:{{apitype|number}} - The unit's maximum ranged damage.
:;posBuff:{{apitype|number}} - The unit's positive Bonus on ranged attacks (includes Spelldamage increases)
:;negBuff:{{apitype|number}} - The unit's negative Bonus on ranged attacks
:;percent:{{apitype|number}} - percentage modifier (usually 1)

==Example==
Calculates your average damage per second.
 local speed, lowDmg, hiDmg = UnitRangedDamage("player");
 local avgDmg = (lowDmg + hiDmg) / 2;
 local avgDps = avgDmg / speed;
```