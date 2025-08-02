# API GetRangedHaste

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=PlayerScript}}
Returns the player's ranged haste amount granted through buffs.
 rangedHaste = GetRangedHaste()

==Returns==
:;rangedHaste:{{apitype|number}} - The player's ranged haste amount granted through buffs, as a percentage; e.g. 36.36363 corresponding to a ~36.36% increased attack speed.

==Details==
* Reports only the ranged haste granted from buffs, such as [[Rapid Fire]] and Quick Shots (from [[Improved Aspect of the Hawk]]) but excluding a hunter's quiver.
{| {{apitable}}
{{apirow | Related API | {{api|GetCombatRating}}(CR_HASTE_RANGED)<br>{{api|GetCombatRatingBonus}}(CR_HASTE_RANGED) }}
|}
```