# API GetSpellBookItemName

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{deprecatedapi|patch=11.0.0|removed=11.0.2}}
Returns the name of a [[spellbook]] item.
 spellName, spellSubName, spellID = GetSpellBookItemName(spellName)
                                  = GetSpellBookItemName(index, bookType)

==Arguments==
{{:SpellArg|onlyname=1}}

==Returns==
:;spellName:{{apitype|string}} - Name of the spell as it appears in the spell book, e.g. ''"Lesser Heal"''
:;spellSubName:{{apitype|string}} - The spell rank or sub type, e.g. ''"Grand Master"'', ''"Racial Passive"''. This can be an empty string. '''Note:''' for the ''Enchanting'' trade skill at rank ''Apprentice'', the returned string contains a trailing space, i.e. ''"Apprentice "''. This might be the case for other trade skills and ranks also. Not readily available on function call, see [[SpellMixin#ContinueOnSpellLoad|SpellMixin:ContinueOnSpellLoad]]()
:;spellID:{{apitype|number}}

==Details==
* This function will return nested flyout spells, but the names returned may not be functional (a hunter will see "Call <petname>" instead of "Call Pet 1" but "/cast Call <petname>" will not function in a macro or from the command line). Use care with the results returned.
* Spell book information is first available after the {{api|t=e|SPELLS_CHANGED}} event fires.

==Example==
<onlyinclude>Prints all spells in the spellbook for the player, except the profession tab ones.
<syntaxhighlight lang="lua">
for i = 1, GetNumSpellTabs() do
	local offset, numSlots = select(3, GetSpellTabInfo(i))
	for j = offset+1, offset+numSlots do
		print(i, j, GetSpellBookItemName(j, BOOKTYPE_SPELL))
	end
end
</syntaxhighlight>
[[File:API_GetSpellBookItemName_01.png]]

Prints the spells shown in the profession tab.
<syntaxhighlight lang="lua">
for _, i in pairs{GetProfessions()} do
	local offset, numSlots = select(3, GetSpellTabInfo(i))
	for j = offset+1, offset+numSlots do
		print(i, j, GetSpellBookItemName(j, BOOKTYPE_SPELL))
	end
end

> 7, 126, "Tailoring", "", 3908
> 8, 128, "Engineering", "", 4036
> 6, 122, "Cooking", "", 2550
> 6, 123, "Cooking Fire", "", 81
</syntaxhighlight>

Prints the spells shown in the pet tab.
<syntaxhighlight lang="lua">
local numSpells, petToken = HasPetSpells()  -- nil if pet does not have spellbook, 'petToken' will usually be 'PET'
for i=1, numSpells do
    local petSpellName, petSubType, unmaskedSpellId = GetSpellBookItemName(i,"pet")
    print("petSpellName", petSpellName)  --like "Dash"
    print("petSubType", petSubType) -- like "Basic Ability" or "Pet Stance"
    print("unmaskedId", unmaskedSpellId) -- don't have to appy the 0xFFFFFF mask like you do for GetSpellBookItemInfo
end

</syntaxhighlight>

Note that not all spells available from the API are shown in the spellbook.
<syntaxhighlight lang="lua">
local i = 1
while GetSpellBookItemName(i, BOOKTYPE_SPELL) do
	print(i, GetSpellBookItemName(i, BOOKTYPE_SPELL))
	i = i + 1
end
</syntaxhighlight></onlyinclude>

==Patch changes==
* {{Patch 11.0.0|note=Removed, replaced by {{api|C_SpellBook.GetSpellBookItemName}}.}}
* {{Patch 4.0.1|note=Added. Replaces {{api|GetSpellName}}.}}
```