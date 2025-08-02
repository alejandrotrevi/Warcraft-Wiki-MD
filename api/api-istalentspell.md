# API IsTalentSpell

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns true if the specified spell is learned from a talent.
 isTalentSpell = IsTalentSpell( spellName or slotIndex, bookType )

==Arguments==
:;spellName:{{apitype|string}} - Name of a spell currently in the player's spellbook

or

:;slotIndex:{{apitype|number}} - spell book item index. Valid values are 1 through total number of spells in the spell book on all pages and all tabs, ignoring empty slots.
:;bookType:{{apitype|string}} - one of BOOKTYPE_SPELL ("spell") or BOOKTYPE_PET ("pet").

==Returns==
:;isTalentSpell:{{apitype|boolean}} - true if the spell is learned from a talent, false otherwise.

==Details==
* The default UI uses this function to determine whether to show the word "Talent" underneath the spell name in the spell book.
```