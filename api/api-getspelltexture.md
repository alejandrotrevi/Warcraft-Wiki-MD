# API GetSpellTexture

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{deprecatedapi|patch=11.0.0|removed=11.0.2}}
Returns the icon texture of a spell.
 icon = GetSpellTexture(spell)
      = GetSpellTexture(index, bookType)

==Arguments==
{{:SpellArg}}

==Returns==
:;icon:{{apitype|number}} ([[fileID]]) - icon texture used by the spell.

==See also==
* {{api|GetSpellBookItemTexture}}
```