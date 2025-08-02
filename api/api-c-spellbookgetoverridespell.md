# API C SpellBook.GetOverrideSpell

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_SpellBook|system=SpellBook}}
Needs summary.
 overrideSpellID = C_SpellBook.GetOverrideSpell(spellID [, spec, onlyKnown, ignoreOverrideSpellID])

==Arguments==
:;spellID:{{apitype|number}}
:;spec:{{apitype|number?|default=0}}
:;onlyKnown:{{apitype|boolean?|default=true}}
:;ignoreOverrideSpellID:{{apitype|number?|default=0}}

==Returns==
:;overrideSpellID:{{apitype|number}} - Returns the spellID passed in if there is no override
```