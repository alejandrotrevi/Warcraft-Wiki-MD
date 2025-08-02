# API GetSpellCount

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{deprecatedapi|patch=11.0.0|removed=11.0.2}}
Returns the number of times a spell can be cast. Generally used for spells limited by the number of available item reagents.
 numCasts = GetSpellCount(spell)
          = GetSpellCount(index, bookType)

==Arguments==
{{:SpellArg}}

==Returns==
:;numCasts:{{apitype|number}}
```