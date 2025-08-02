# API GetSpellBookItemInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns info for a [[spellbook]] item.
 spellType, id = GetSpellBookItemInfo(spellName)
               = GetSpellBookItemInfo(index, bookType)

==Arguments==
{{:SpellArg|onlyname=1}}

==Returns==
:;spellType:{{apitype|string}} - The type of the spell: <code>["SPELL", "FUTURESPELL", "PETACTION", "FLYOUT"]</code>
:;id:{{apitype|number}}
::* For SPELL and FUTURESPELL, the SpellID used in {{api|GetSpellInfo}}()
::* For PETACTION, the ActionID used in {{api|C_ActionBar.HasPetActionButtons}}(); furthermore, the ''SpellID'' can be obtained by applying the bitmask 0xFFFFFF.
::* For FLYOUT, the FlyoutID used in {{api|GetFlyoutInfo}}()

==Example==
Prints all spells in the spellbook for the player, except the profession tab ones.
<syntaxhighlight lang="lua">
local spellFunc = {
	SPELL = GetSpellInfo,
	FUTURESPELL = GetSpellInfo,
	FLYOUT = GetFlyoutInfo,
}

for i = 1, GetNumSpellTabs() do
	local _, _, offset, numSlots = GetSpellTabInfo(i)
	for j = offset+1, offset+numSlots do
		local spellType, id = GetSpellBookItemInfo(j, BOOKTYPE_SPELL)
		local spellName = spellFunc[spellType](id)
		print(i, j, spellType, id, spellName)
	end
end
</syntaxhighlight>
[[File:API_GetSpellBookItemInfo_01.png]]

Prints all pet spells.
<syntaxhighlight lang="lua">
for i = 1, HasPetSpells() do
	local spellType, id = GetSpellBookItemInfo(i, BOOKTYPE_PET)
	local spellID = bit.band(0xFFFFFF, id)
	-- not sure what the non-spell IDs are
	local spellName = spellID > 100 and GetSpellInfo(spellID) or GetSpellBookItemName(i, BOOKTYPE_PET)
	local hasActionButton = C_ActionBar.HasPetActionButtons(id)
	print(i, spellType, id, spellID, spellName, hasActionButton)
end
</syntaxhighlight>
[[File:API_GetSpellBookItemInfo_02.png]]

==Patch changes==
* {{Patch 11.0.0|note=Removed, replaced by {{api|C_SpellBook.GetSpellBookItemInfo}}.}}
```