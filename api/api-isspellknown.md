# API IsSpellKnown

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{deprecatedapi|future=1|patch=11.2.0|link=https://github.com/Gethe/wow-ui-source/blob/11.2.0/Interface/AddOns/Blizzard_DeprecatedSpellBook/Deprecated_SpellBook.lua#L16-L20}}
Returns whether the player (or pet) knows the given spell.
 isKnown = IsSpellKnown(spellID [, isPetSpell])

==Arguments==
:;spellID:{{apitype|number}} - the spell ID number
:;isPetSpell:{{apitype|boolean?}} - if true, will check if the currently active pet knows the spell; if false or omitted, will check if the player knows the spell

==Returns==
:;isKnown:{{apitype|boolean}} - whether the player (or pet) knows the given spell

==Details==
* This function may return false when querying learned spells that are passive effects. Consider using {{api|IsPlayerSpell}} for these.
* Returns false if querying a spell that has "replaced" a known spell, which returns true whether or not it's replaced (i.e. Retribution's Templar's Verdict (85256) will always be true and Final Verdict (336872) will be false whether or not you have the related legendary equipped). In these cases, use IsSpellKnownOrOverridesKnown(spellID) to check for spells like Final Verdict.
* May return false even if the spell is known if invoked too quickly after learning the spell.

==See also==
* {{api|IsPlayerSpell}}
* {{api|IsSpellKnownOrOverridesKnown}}
```