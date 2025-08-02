# API GetSpellBonusDamage

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=PlayerScript}}
Returns the raw spell damage bonus for the specified spell tree.
 bonusDamage = GetSpellBonusDamage(school)

==Arguments==
:;school:{{apitype|number}} - the spell tree:
:::* 1: Physical
:::* 2: Holy
:::* 3: Fire
:::* 4: Nature
:::* 5: Frost
:::* 6: Shadow
:::* 7: Arcane

==Returns==
:;bonusDamage:{{apitype|number}} - The raw spell damage bonus of the player for that spell tree
```