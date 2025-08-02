# API C EncounterJournal.GetSectionIconFlags

**Contributor:** Artur91425

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_EncounterJournal|system=EncounterJournal}}
Returns the icon flags for a section, such as Magic Effect and Heroic Difficulty
 iconFlags = C_EncounterJournal.GetSectionIconFlags(sectionID)

==Arguments==
:;sectionID:{{apitype|number}} : {{dbc|journalencountersection|JournalEncounterSection.ID}}

==Returns==
:;iconFlags:{{apitype|number[]?}} - Flag IDs to display for this section.
:: Refer to the {{dbc|globalstrings#search=ENCOUNTER_JOURNAL_SECTION_FLAG|ENCOUNTER_JOURNAL_SECTION_FLAG}} globals for the flag titles.
:: For convenience there is [https://www.townlong-yak.com/framexml/go/EncounterJournal_SetFlagIcon EncounterJournal_SetFlagIcon()] which sets the texture coords for [https://wow.tools/files/#search=UI-EJ-Icons interface/encounterjournal/ui-ej-icons.blp]

{|class="darktable zebra" style="margin-left: 1.75em"
! ID !! Flag !! ID !! Flag 
|-
| align="center" | 0 || style="min-width: 12em" | [[Image:Tank_icon.png]] Tank Alert
| align="center" | 7 || [[Image:Magic_icon.png]] Magic Effect
|-
| align="center" | 1 || style="min-width: 12em" | [[Image:Dps_icon.png]] Damage Dealer Alert
| align="center" | 8 || [[Image:Curse_icon.png]] Curse Effect
|-
| align="center" | 2 || [[Image:Healer_icon.png]] Healer Alert
| align="center" | 9 || [[Image:Poison_icon.png]] Poison Effect
|-
| align="center" | 3 || [[Image:Heroic_icon.png]] Heroic Difficulty
| align="center" | 10 || [[Image:Disease_icon.png]] Disease Effect
|-
| align="center" | 4 || [[Image:Deadly_icon.png]] Deadly
| align="center" | 11 || [[Image:Enrage_icon.png]] Enrage
|-
| align="center" | 5 || [[Image:Important_icon.png]] Important
| align="center" | 12 || [[Image:Mythic_icon.png]] Mythic Difficulty
|-
| align="center" | 6 || [[Image:Interruptable_icon.png]] Interruptible
| align="center" | 13 || [[Image:Bleed_icon.png]] Bleed
| colspan="2" |
|}

==Example==
<syntaxhighlight lang="lua">
-- local copy since Blizzard_EncounterJournal is LoadOnDemand
local function EncounterJournal_SetFlagIcon(texture, index)
	local iconSize = 32
	local columns = 256/iconSize
	local rows = 64/iconSize
	local l = mod(index, columns) / columns
	local r = l + (1/columns)
	local t = floor(index/columns) / rows
	local b = t + (1/rows)
	texture:SetTexCoord(l, r, t, b)
end

local f = CreateFrame("Frame", nil, UIParent)
f:SetPoint("CENTER")
f:SetSize(32, 32)

local tex = f:CreateTexture()
tex:SetAllPoints(f)
tex:SetTexture("Interface/EncounterJournal/UI-EJ-Icons")

local function SetEncounterJournalIcon(sectionID)
	local iconFlags = C_EncounterJournal.GetSectionIconFlags(sectionID)
	if iconFlags then
		for _, flag in pairs(iconFlags) do
			print(flag, _G["ENCOUNTER_JOURNAL_SECTION_FLAG"..flag])
			EncounterJournal_SetFlagIcon(tex, flag)
		end
	end
end

-- Vanessa VanCleef: sectionID 2065 [Powder Explosion]
SetEncounterJournalIcon(2065)
</syntaxhighlight>
 > 4, "Deadly"

[[File:API_C_EncounterJournal.GetSectionIconFlags.png|thumb|none]]

==Patch changes==
* {{Patch 7.3.5|note=Added, this functionality was separated from {{api|C_EncounterJournal.GetSectionInfo}}.}}
```