# API C SpellBook.GetSpellBookItemInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_SpellBook|system=SpellBook}}
Returns info for a [[spellbook]] item.
 spellBookItemInfo = C_SpellBook.GetSpellBookItemInfo(spellBookItemSlotIndex, spellBookItemSpellBank)

==Arguments==
:;spellBookItemSlotIndex:{{apitype|number}} - Spellbook slot index, ranging from 1 through the total number of spells across all tabs and pages
:;spellBookItemSpellBank:{{apitype|Enum.SpellBookSpellBank}}
{{:Enum.SpellBookSpellBank|nocaption=1}}

==Returns==
:;spellBookItemInfo:{{apitype|SpellBookItemInfo?}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| {{apiname|actionID}} || {{apitype|number}} || Represents a base spellID for spells, flyoutID for flyouts, or petActionID for pet actions || 
|-
| {{apiname|spellID}} || {{apitype|number?}} || May be nil if item is not a spell; Will be the overriding spellID if spell is overriden, otherwise will match <code>actionID</code> || 
|-
| {{apiname|itemType}} || {{apitype|Enum.SpellBookItemType}} || 
|-
| {{apiname|name}} || {{apitype|string}} || The localized name of the spell
|-
| {{apiname|subName}} || {{apitype|string}} || May be empty if flyout, or if spell's data isn't loaded yet; Listen for {{api|t=e|SPELL_TEXT_UPDATE}} event, or use [[SpellMixin]] to load asynchronously
|-
| {{apiname|iconID}} || {{apitype|fileID}} || The spell icon texture
|-
| {{apiname|isPassive}} || {{apitype|boolean}} || True if the item is a passive spell; Will always be false if it is not a spell
|-
| {{apiname|isOffSpec}} || {{apitype|boolean}} || True if the item belongs to a non-active specialization
|-
| {{apiname|skillLineIndex}} || {{apitype|number?}} || Index of the SkillLine this SpellBookItem is part of; nil if this SpellBookItem isn't part of a SkillLine
|}

{{:Enum.SpellBookItemType}}

==Example==
Prints all spells in the spellbook for the player, except the profession tab ones.
<syntaxhighlight lang="lua">
for i = 1, C_SpellBook.GetNumSpellBookSkillLines() do
	local skillLineInfo = C_SpellBook.GetSpellBookSkillLineInfo(i)
	local offset, numSlots = skillLineInfo.itemIndexOffset, skillLineInfo.numSpellBookItems
	for j = offset+1, offset+numSlots do
		local spellBookItemInfo = C_SpellBook.GetSpellBookItemInfo(j, Enum.SpellBookSpellBank.Player)
		local spellType, id = spellBookItemInfo.itemType, spellBookItemInfo.actionID
		local spellName
		if spellType == Enum.SpellBookItemType.Spell then
			spellName = C_Spell.GetSpellName(id)
			spellType = "Spell"
		elseif spellType == Enum.SpellBookItemType.FutureSpell then
			spellName = C_Spell.GetSpellName(id)
			spellType = "Future Spell"
		elseif spellType == Enum.SpellBookItemType.Flyout then
			spellName = GetFlyoutInfo(id)
			spellType = "Flyout"
		end
		print(i, j, spellType, id, spellName)
	end
end
</syntaxhighlight>
[[File:API_GetSpellBookItemInfo_01.png]]

Prints all pet spells.
<syntaxhighlight lang="lua">
for i = 1, C_SpellBook.HasPetSpells() do
	local spellBookItemInfo = C_SpellBook.GetSpellBookItemInfo(i, Enum.SpellBookSpellBank.Pet)
	local id = spellBookItemInfo.actionID
	local spellID = bit.band(0xFFFFFF, id)
	-- not sure what the non-spell IDs are
	local spellName = spellID > 100 and C_Spell.GetSpellName(spellID) or C_SpellBook.GetSpellBookItemName(i, Enum.SpellBookSpellBank.Pet)
	local hasActionButton = C_ActionBar.HasPetActionButtons(id)
	print(i, "Pet", id, spellID, spellName, hasActionButton)
end
</syntaxhighlight>
[[File:API_GetSpellBookItemInfo_02.png]]

==Patch changes==
* {{Patch 11.0.0|note=Added, replacement for {{api|GetSpellBookItemInfo}}.}}
```