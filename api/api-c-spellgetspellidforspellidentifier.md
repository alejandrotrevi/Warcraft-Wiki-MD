# API C Spell.GetSpellIDForSpellIdentifier

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Spell|system=Spell}}
Returns the spell ID for a given SpellIdentifier.
 spellID = C_Spell.GetSpellIDForSpellIdentifier(spellIdentifier)

==Arguments==
:;spellIdentifier:{{apitype|SpellIdentifier}} - Using name will always check for an override on that spell; If passed a spell ID, will return same id as was passed

==Returns==
:;spellID:{{apitype|number}}

==Details==
* Meant primarily for getting a spell id from a spell name or link; Returns nothing if spell does not exist.
```