# API GetAttackPowerForStat

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=PlayerScript}}
Returns the amount of attack power contributed by a specific amount of a stat.
 attackPower = GetAttackPowerForStat(stat, value)

==Arguments==
:;stat:{{apitype|number}} - Index of the stat (Strength, Agility, ...) to check the bonus AP of.
{{:API_UnitStat}}
:;value:{{apitype|number}} - Amount of the stat to check the AP value of.

==Returns==
:;attackPower:{{apitype|number}} - Amount of attack power granted by the specified amount of the specified stat.
```