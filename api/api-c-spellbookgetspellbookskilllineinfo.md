# API C SpellBook.GetSpellBookSkillLineInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_SpellBook|system=SpellBook}}
Returns info for the specified spellbook skill line.
 skillLineInfo = C_SpellBook.GetSpellBookSkillLineInfo(skillLineIndex)

==Arguments==
:;skillLineIndex:{{apitype|number}} - The index of the skill line, ascending from 1.

==Returns==
:;skillLineInfo:{{apitype|SpellBookSkillLineInfo?}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| {{apiname|name}} || {{apitype|string}} || The name of the spell line (General, Shadow, Fury, etc)
|-
| {{apiname|iconID}} || {{apitype|fileID}} || The spell icon texture
|-
| {{apiname|itemIndexOffset}} || {{apitype|number}} || This value + 1 is the first Spell Book Item slotIndex within this skill line
|-
| {{apiname|numSpellBookItems}} || {{apitype|number}} || The number of spell entries in this skill line
|-
| {{apiname|isGuild}} || {{apitype|boolean}} || True for [[Guild Perks]], false otherwise
|-
| {{apiname|shouldHide}} || {{apitype|boolean}} || 
|-
| {{apiname|specID}} || {{apitype|number?}} || Will be nil if this skill line is not associated with a specialization
|-
| {{apiname|offSpecID}} || {{apitype|number?}} || Will be nil if this skill line is not associated with a non-active specialization
|}

==Details==
* {{api|C_SpellBook.GetNumSpellBookSkillLines}} returns the number of class-skill tabs available to your character.
* Due to flyouts, more spellbook item indices may be used by a tab than suggested by the offset/numEntries values.
* Professions are tabs, too: {{api|GetProfessions}} returns tab indices that contain profession spells, beyond the range specified by {{api|C_SpellBook.GetNumSpellBookSkillLines}}.

==Example==
{{:API_C_SpellBook.GetSpellBookItemName}}

==Patch changes==
* {{Patch 11.0.0|note=Added, replacement for {{api|GetSpellTabInfo}}.}}
```