# API EJ GetEncounterInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns encounter info from the journal.
 name, description, journalEncounterID, rootSectionID, link, journalInstanceID, dungeonEncounterID, instanceID
    = EJ_GetEncounterInfo(journalEncounterID)
    = EJ_GetEncounterInfoByIndex(index [, journalInstanceID])

==Arguments==
===<font color="#4ec9b0">EJ_GetEncounterInfo</font>===
:;journalEncounterID:{{apitype|number}} : [[JournalEncounterID]]
===<font color="#4ec9b0">EJ_GetEncounterInfoByIndex</font>===
:;index:{{apitype|number}} 
:;journalInstanceID:{{apitype|number?}} : {{dbc|JournalInstance|JournalInstance.ID}} - If omitted, defaults to the currently selected instance from {{api|EJ_SelectInstance}}()
:::<font color="#dda0dd">''quirk''</font>: Requires <code>EJ_SelectInstance</code> to be called at least once during this session when passing a <code>journalInstanceID</code>.

==Returns==
:;name:{{apitype|string}}
:;description:{{apitype|string}}
:;journalEncounterID:{{apitype|number}} : [[JournalEncounterID]] - IDs for the Encounter Journal
:;rootSectionID:{{apitype|number}} : {{dbc|journalencountersection|JournalEncounterSection.ID}} - The first section article that describes the boss abilities
:;link:{{apitype|string}} : [[Hyperlinks#journal|journalLink]]
:;journalInstanceID:{{apitype|number}} : {{dbc|journalinstance|JournalInstance.ID}} - The dungeon instance as used by the Encounter Journal
:;dungeonEncounterID:{{apitype|number}} : [[DungeonEncounterID]] - IDs from [[ENCOUNTER_START]]
:;instanceID:{{apitype|number}} : [[InstanceID]] - The map instance

==Example==
 /dump EJ_GetEncounterInfo(95)
<syntaxhighlight lang="lua">
[1] = "Vanessa VanCleef", -- name
[2] = "As a young girl, Vanessa witnessed the gruesome death of her father and former Defias Brotherhood leader, Edwin VanCleef. She has since taken up his mantle of leadership, plotting to exact vengeance on Stormwind from the dark corridors of the Defias's stronghold in the Deadmines.", -- description
[3] = 95,    -- journalEncounterID
[4] = 2060,  -- rootSectionID
[5] = "|cff66bbff|Hjournal:1:95:0|h[Vanessa VanCleef]|h|r", -- link 
[6] = 63,    -- journalInstanceID
[7] = 1081,  -- dungeonEncounterID
[8] = 36     -- instanceID
</syntaxhighlight>
Illustrates the quirk when passing a <code>journalInstanceID</code> without calling <code>EJ_SelectInstance</code>.
<syntaxhighlight lang="lua">
local name1 = EJ_GetEncounterInfoByIndex(1, 1208)
print(name1) -- nil

EJ_SelectInstance(1195) -- this can be an arbitrary journalInstanceID

local name2 = EJ_GetEncounterInfoByIndex(1, 1208)
print(name2) -- Kazzara, the Hellforged
</syntaxhighlight>

==Patch changes==
* {{Patch 8.2.0|note=Added <code>dungeonEncounterID, instanceID</code> returns.<sup>[https://www.townlong-yak.com/framexml/8.2.0/Blizzard_EncounterJournal/Blizzard_EncounterJournal.lua/diff#3270]</sup>}}
* {{Patch 8.0.1|note=Added <code>journalInstanceID</code> return.<sup>[https://www.townlong-yak.com/framexml/8.0.1/Blizzard_SharedMapDataProviders/EncounterJournalDataProvider.lua#53]</sup>}}
* {{Patch 4.2.0|note=Added.}}

<!-- luals
---@param journalEncounterID number
---@return string name
---@return string description
---@return number journalEncounterID
---@return number rootSectionID
---@return string link
---@return number journalInstanceID
---@return number dungeonEncounterID
---@return number instanceID
function EJ_GetEncounterInfo(journalEncounterID) end

---[Documentation](https://warcraft.wiki.gg/wiki/API_EJ_GetEncounterInfoByIndex)
---@param index number
---@param journalInstanceID? number
---@return string name
---@return string description
---@return number journalEncounterID
---@return number rootSectionID
---@return string link
---@return number journalInstanceID
---@return number dungeonEncounterID
---@return number instanceID
function EJ_GetEncounterInfoByIndex(index, journalInstanceID) end
-->
```