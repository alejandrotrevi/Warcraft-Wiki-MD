# API GetSpellAutocast

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns true if a (pet) spell is autocastable.
 autocastable, autostate = GetSpellAutocast("spellName" or spellId, bookType)

==Arguments==
:;spellName:{{apitype|string}} - the name of the spell.
:;spellId:{{apitype|number}} - the offset (position) of spell in spellbook. SpellId can change when you learn new spells.
:;bookType:{{apitype|string}} - Either BOOKTYPE_SPELL ("spell") or BOOKTYPE_PET ("pet").

==Returns==
:;autocastable:{{apitype|number}} - whether a spell is autocastable.
::Returns 1 if the spell is autocastable, nil otherwise.
:;autostate:{{apitype|number}} - whether a spell is currently set to autocast.
::Returns 1 if the spell is currently set for autocast, nil otherwise.

==Details==
*As of patch 3.0.3, the only auto-castable spells exist in the pet spellbook (BOOKTYPE_PET).
*Both return values will be nil in the following conditions:
**The spell is not autocastable
**The spell does not exist (or you don't know it)
```