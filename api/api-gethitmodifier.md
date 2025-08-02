# API GetHitModifier

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=PlayerScript}}
Returns the amount of Melee Hit %, not from Melee Hit Rating, that your character has.
 hitMod = GetHitModifier()

==Returns==
:;hitMod:{{apitype|number}} - hit modifier (e.g. 16 for 16%)

==Example==
Returns the Melee Hit Chance displayed in the paper doll.
 /dump GetCombatRatingBonus(CR_HIT_MELEE) + GetHitModifier()

==See also==
* [[API GetSpellHitModifier]]
```