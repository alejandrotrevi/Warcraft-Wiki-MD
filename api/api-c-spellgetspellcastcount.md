# API C Spell.GetSpellCastCount

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Spell|system=Spell}}
Returns number of times a spell can be cast, typically based on availability of things like required reagent items; Returns 0 if spell is not found
 castCount = C_Spell.GetSpellCastCount(spellIdentifier)

==Arguments==
:;spellIdentifier:{{apitype|SpellIdentifier}}

==Returns==
:;castCount:{{apitype|number}}
```