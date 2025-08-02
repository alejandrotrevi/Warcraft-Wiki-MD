# API GetProfessionInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Gets details on a profession from its index including name, icon, and skill level.
 name, icon, skillLevel, maxSkillLevel, numAbilities, spelloffset, skillLine, skillModifier, specializationIndex, specializationOffset = GetProfessionInfo(index)

==Arguments==
:;index:{{apitype|number}} - The spell tab index from {{api|GetProfessions}}

==Returns==
:name, icon, skillLevel, maxSkillLevel, numAbilities, spelloffset, skillLine, skillModifier
:;name:{{apitype|string}} - The localized skill name
:;icon:{{apitype|string}} - the location of the icon image
:;skillLevel:{{apitype|number}} - the current skill level
:;maxSkillLevel:{{apitype|number}} - the current skill cap (75 for apprentice, 150 for journeyman etc.)
:;numAbilities:{{apitype|number}} - The number of abilities/icons listed. These are the icons you put on your action bars.
:;spelloffset:{{apitype|number}} - The offset id of the first Spell of this profession. (you can CastSpell(spelloffset + 1, "Spell") to use the first spell of this profession)
:;[[TradeSkillLineID|skillLine]]:{{apitype|number}} - Reference to the profession.
:;skillModifier:{{apitype|number}} - Additional modifiers to your profession levels. IE: Lures for Fishing.
:;specializationIndex:{{apitype|number}} - A value indicating which specialization is known (ie. Transmute specialist for Alchemist)
:;specializationOffset:{{apitype|number}} - Haven't figured this one out yet

==Details==
This also seems to return some kind of data on the talent trees and guild perks.

==Patch changes==
* {{Patch 4.0.1|note=Added.}}
```