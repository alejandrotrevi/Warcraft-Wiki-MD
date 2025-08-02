# API GetNumSpellTabs

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{deprecatedapi|patch=11.0.0|removed=11.0.2}}
Returns the number of tabs in the spellbook.
 numTabs = GetNumSpellTabs()

==Returns==
:;numTabs:{{apitype|number}} - number of ability tabs in the player's spellbook (e.g. 4 -- "General", "Arcane", "Fire", "Frost")

==Details==
* Each of the player's professions also gets a spellbook tab, but these tabs are not included in the count returned by this function.

==Patch changes==
* {{Patch 11.0.0|note=Removed, replaced by {{api|C_SpellBook.GetNumSpellBookSkillLines}}.}}
```