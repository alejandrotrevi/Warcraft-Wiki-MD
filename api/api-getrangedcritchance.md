# API GetRangedCritChance

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=PlayerScript}}
Returns the ranged critical hit chance.
 rangedCrit = GetRangedCritChance()

==Returns==
:;rangedCrit:{{apitype|number}} - The player's ranged critical hit chance, as a percentage; e.g. 5.3783211 corresponding to a ~5.38% crit chance.

==Details==
If you are displaying this figure in a UI element and want it to update, hook to the UNIT_INVENTORY_CHANGED and SPELLS_CHANGED events as well as any other that effect equipment and buffs.
```