# API FindSpellOverrideByID

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the ID for the override spell.
 overrideSpellID = FindSpellOverrideByID(spellID)

==Arguments==
:;spellID:{{apitype|number}} - The base spell ID

==Returns==
:;overrideSpellID:{{apitype|number}}

==Details==
* Override spells replace a base spell; they are usually gained via talents.
** For example, [[Gloomblade]] overrides (replaces) [[Backstab]] if you have selected the talent for it.
* If querying with a spell that does not have an override in effect then its own spellID will be returned.

==Patch changes==
* {{Patch 8.0.1|note=Added.}}

==See also==
* {{api|FindBaseSpellByID}}
```