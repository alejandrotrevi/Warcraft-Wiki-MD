# API GetManaRegen

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=PlayerScript}}
Returns the mana regeneration per second.
 baseManaRegen, castingManaRegen = GetManaRegen()

==Returns==
:;baseManaRegen:{{apitype|number}} - Mana regeneration per second when not casting spells.
:;castingManaRegen:{{apitype|number}} - Mana regeneration per second while casting spells.

==Details==
* To get the same values as displayed in the PaperDoll, multiply the values by 5.
```