# API C EncounterJournal.GetSectionInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_EncounterJournal|system=EncounterJournal}}
Returns information about an entry in the Abilities section of the Encounter Journal.
 info = C_EncounterJournal.GetSectionInfo(sectionID)

==Arguments==
:;sectionID:{{apitype|number}} : {{dbc|journalencountersection|JournalEncounterSection.ID}}

==Returns==
:;info:{{apitype|EncounterJournalSectionInfo}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| spellID || {{apitype|number}} || 
|-
| title || {{apitype|string}} || Section title, e.g. "Stage One: The Final Assault", "Mutated Corruption", "Impale"
|-
| description || {{apitype|string?}} || Description text, e.g. "A Mutated Corruption appears shortly after assaulting a platform"
|-
| headerType || {{apitype|number}} || Section depth, i.e. the number of ancestors it has before reaching a sibling of the root section for the encounter (0 for the root section and its siblings, 1 for their children, 2 for their children's children...).
|-
| abilityIcon || {{apitype|number}} || Path to a texture to display as an icon next to the section title, or "" if no static icon should be shown.
|-
| creatureDisplayID || {{apitype|number}} || [[DisplayID]] as the icon next to the section title, or 0 if no model-based icon should be shown.
|-
| uiModelSceneID || {{apitype|number}} || [[ModelSceneID]]
|-
| siblingSectionID || {{apitype|number?}} || Section ID of the next section on the same depth as this one, nil if none.
|-
| firstChildSectionID || {{apitype|number?}} || Section ID of the first child section of this section, nil if none.
|-
| filteredByDifficulty || {{apitype|boolean}} || True if this section should be hidden because it does not apply to the current [[DifficultyID]]}, false otherwise.
|-
| link || {{apitype|string}} || [[Hyperlinks#journal|journalLink]] to this section, e.g. " |cff66bbff|Hjournal:2:4102:4|h[Cataclysm]|h|r".
|-
| startsOpen || {{apitype|boolean}} || True if the section should be expanded by default, false if it should be collapsed by default.
|}

==Details==
* {{api|EJ_GetEncounterInfo}}() returns the <code>rootSectionID</code> for a given encounter: the ''first'' Ability section to display. Subsequent sections can be navigated through the <code>siblingSectionID</code> and <code>firstChildSectionID</code> return values of this function.
*  The returned <code>link</code> is affected by the current {{api|EJ_SetDifficulty|difficulty}}; this function can return invalid difficulty/section combinations. If you attempt to send one of those links in a chat message, it will be filtered by the server.

==Example==
The following snippet prints links to all sections of a given encounter in the Encounter Journal.
<syntaxhighlight lang="lua">
function PrintAllEncounterSections(encounterID, difficultyID)
	EJ_SetDifficulty(difficultyID)
	local stack, encounter, _, _, curSectionID = {}, EJ_GetEncounterInfo(encounterID)
	print(encounter.." abilities:")
	
	repeat
		local info = C_EncounterJournal.GetSectionInfo(curSectionID)
		if not info.filteredByDifficulty then
			print(("  "):rep(info.headerType)..info.link.. ": "..info.description)
		end
		table.insert(stack, info.siblingSectionID)
		if not info.filteredByDifficulty then
			table.insert(stack, info.firstChildSectionID)
		end
		curSectionID = table.remove(stack)
	until not curSectionID
end

-- Print everything in 25-man Normal Madness of Deathwing:
PrintAllEncounterSections(333, 4)
</syntaxhighlight>

==Patch changes==
* {{Patch 8.0.1|note=Added <code>spellID</code> field.}}
* {{Patch 7.3.5|note=Moved to <code>C_EncounterJournal.GetSectionInfo()</code><sup>[https://www.townlong-yak.com/framexml/7.3.5/Blizzard_Deprecated/Deprecated_7_3_5.lua#31]</sup>}}
* {{Patch 4.2.0|note=Added as <code>EJ_GetSectionInfo()</code>}}

==See also==
* {{api|C_EncounterJournal.GetSectionIconFlags}}()
```