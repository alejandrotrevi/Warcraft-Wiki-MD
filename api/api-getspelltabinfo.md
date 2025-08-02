# API GetSpellTabInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{deprecatedapi|patch=11.0.0|removed=11.0.2}}
Returns info for the specified spellbook tab.
 name, texture, offset, numSlots, isGuild, offspecID = GetSpellTabInfo(tabIndex)

==Arguments==
:;tabIndex:{{apitype|number}} - The index of the tab, ascending from 1.

==Returns==
:;name:{{apitype|string}} - The name of the spell line (General, Shadow, Fury, etc.)
:;texture:{{apitype|string}} - The texture path for the spell line's icon
:;offset:{{apitype|number}} - Number of spell book entries before this tab (one less than index of the first spell book item in this tab)
:;numSlots:{{apitype|number}} - The number of spell entries in this tab.
:;isGuild:{{apitype|boolean}} - true for Guild Perks, false otherwise
:;offspecID:{{apitype|number}} - 0 if the tab contains spells you can cast (general/specialization/trade skill/etc); or specialization ID of the specialization this tab is showing the spells of.

==Details==
* {{api|GetNumSpellTabs}} returns the number of class-skill tabs available to your character.
* Due to flyouts, more spellbook item indices may be used by a tab than suggested by the offset/numEntries values.
* Professions are tabs, too: {{api|GetProfessions}} returns tab indices that contain profession spells, beyond the range specified by {{api|GetNumSpellTabs}}.

==Example==
{{:API_GetSpellBookItemName}}

==Patch changes==
* {{Patch 11.0.0|note=Removed, replaced by {{api|C_SpellBook.GetSpellBookSkillLineInfo}}.}}
* {{Patch 5.0.4|note=Added <code>offspecID</code> return value.}}
```