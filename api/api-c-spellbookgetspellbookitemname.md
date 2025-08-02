# API C SpellBook.GetSpellBookItemName

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_SpellBook|system=SpellBook}}
Returns the name of a [[spellbook]] item.
 name, subName = C_SpellBook.GetSpellBookItemName(spellBookItemSlotIndex, spellBookItemSpellBank)

==Arguments==
:;spellBookItemSlotIndex:{{apitype|number}} - Spellbook slot index, ranging from 1 through the total number of spells across all tabs and pages
:;spellBookItemSpellBank:{{apitype|Enum.SpellBookSpellBank}}
{{:Enum.SpellBookSpellBank|nocaption=1}}

==Returns==
:;name:{{apitype|string}} - Name of the spell as it appears in the spell book, e.g. ''"Lesser Heal"''
:;subName:{{apitype|string}} - May be empty if spell's data isn't loaded yet; Listen for {{api|t=e|SPELL_TEXT_UPDATE}} event, or use [[SpellMixin]] to load asynchronously

==Details==
* This function will return nested flyout spells, but the names returned may not be functional (a hunter will see "Call <petname>" instead of "Call Pet 1" but "/cast Call <petname>" will not function in a macro or from the command line). Use care with the results returned.
* Spell book information is first available after the {{api|t=e|SPELLS_CHANGED}} event fires.

==Example==
<onlyinclude>Prints all spells in the spellbook for the player, except the profession tab ones.
<syntaxhighlight lang="lua">
for i = 1, C_SpellBook.GetNumSpellBookSkillLines() do
	local skillLineInfo = C_SpellBook.GetSpellBookSkillLineInfo(i)
	local offset, numSlots = skillLineInfo.itemIndexOffset, skillLineInfo.numSpellBookItems
	for j = offset+1, offset+numSlots do
		local name, subName = C_SpellBook.GetSpellBookItemName(j, Enum.SpellBookSpellBank.Player)
		local spellID = select(2,C_SpellBook.GetSpellBookItemType(j, Enum.SpellBookSpellBank.Player))
		print(i, j, name, subName, spellID)
	end
end
</syntaxhighlight>
[[File:API_GetSpellBookItemName_01.png]]

Prints the spells shown in the profession tab.
<syntaxhighlight lang="lua">
for _, i in pairs{GetProfessions()} do
	local skillLineInfo = C_SpellBook.GetSpellBookSkillLineInfo(i)
	local offset, numSlots = skillLineInfo.itemIndexOffset, skillLineInfo.numSpellBookItems
	for j = offset+1, offset+numSlots do
		local name, subName = C_SpellBook.GetSpellBookItemName(j, Enum.SpellBookSpellBank.Player)
		local spellID = select(2,C_SpellBook.GetSpellBookItemType(j, Enum.SpellBookSpellBank.Player))
		print(i, j, name, subName, spellID)
	end
end

> 7, 126, "Tailoring", "", 3908
> 8, 128, "Engineering", "", 4036
> 6, 122, "Cooking", "", 2550
> 6, 123, "Cooking Fire", "", 81
</syntaxhighlight>

Prints the spells shown in the pet tab.
<syntaxhighlight lang="lua">
local numSpells, petToken = C_SpellBook.HasPetSpells()  -- nil if pet does not have spellbook, 'petToken' will usually be "PET"
for i=1, numSpells do
    local petSpellName, petSubType = C_SpellBook.GetSpellBookItemName(i, Enum.SpellBookSpellBank.Pet)
	local spellID = select(2,C_SpellBook.GetSpellBookItemType(i, Enum.SpellBookSpellBank.Pet))
    print("petSpellName", petSpellName)  --like "Dash"
    print("petSubType", petSubType) -- like "Basic Ability" or "Pet Stance"
    print("spellID", spellId)
end

</syntaxhighlight>

Note that not all spells available from the API are shown in the spellbook.
<syntaxhighlight lang="lua">
local i = 1
while C_SpellBook.GetSpellBookItemName(i, Enum.SpellBookSpellBank.Player) do
	print(i, C_SpellBook.GetSpellBookItemName(i, Enum.SpellBookSpellBank.Player))
	i = i + 1
end
</syntaxhighlight></onlyinclude>

==Patch changes==
* {{Patch 11.0.0|note=Added, replacement for {{api|GetSpellBookItemName}}.}}
```