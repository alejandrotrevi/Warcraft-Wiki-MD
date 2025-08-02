# API CastSpell

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{restrictedapi|protected|note=Use the "spell" action type of [[SecureActionButtonTemplate]] or the [[MACRO cast|/cast]] slash command.}}
Casts a spell from the spellbook.
 CastSpell(spellIndex, spellbookType)

==Arguments==
:;spellIndex:{{apitype|number}} - index of the spell to cast.
:;spellbookType:{{apitype|string}} - spellbook to cast the spell from; one of 
:* BOOKTYPE_SPELL ("spell") for player spells
:* BOOKTYPE_PET ("pet") for pet abilities

==Details==
* This function cannot be used from insecure execution paths except to "cast" trade skills (e.g. Cooking, Alchemy).

==Patch changes==
* {{Patch 2.0.1|note=Protected.}}

==See also==
* {{api|CastSpellByName}}
```