# API GetAchievementCriteriaInfo

**Contributor:** Numynum

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns info for the specified achievement criteria.
 criteriaString, criteriaType, completed, quantity, reqQuantity, charName, flags, assetID, quantityString, criteriaID, eligible, duration, elapsed
    = GetAchievementCriteriaInfo(achievementID, criteriaIndex [, countHidden])
    = GetAchievementCriteriaInfoByID(achievementID, criteriaID)

==Arguments==
===<font color="#4ec9b0">GetAchievementCriteriaInfo</font>===
:;achievementID:{{apitype|number}} - Achievement ID the queried criteria belongs to.
:;criteriaIndex:{{apitype|number}} - Index of the criteria to query, ascending from 1 up to [[API_GetAchievementNumCriteria|GetAchievementNumCriteria]](achievementID).
:;countHidden:{{apitype|boolean}}

===<font color="#4ec9b0">GetAchievementCriteriaInfoByID</font>===
:;achievementID:{{apitype|number}}
:;criteriaID:{{apitype|number}} - Unique ID of the criteria to query.

==Returns==
:;1. criteriaString:{{apitype|string}} - The name of the criteria.
:;2. criteriaType:{{apitype|number}} - Criteria type; specifies the meaning of the assetID.
:;3. completed:{{apitype|boolean}} - True if you've completed this criteria; false otherwise.
:;4. quantity:{{apitype|number}} - Quantity requirement imposed by some <code>criteriaType</code>.
:;5. reqQuantity:{{apitype|number}} - The required quantity for the criteria. Used mostly in achievements with progress bars. Usually 0.
:;6. charName:{{apitype|string}} - The name of the character that completed this achievement.
:;7. flags:{{apitype|number}} - Some flags. Currently unknown purpose.
:;8. assetID:{{apitype|number}} - Criteria data whose meaning depends on the type.
:;9. quantityString:{{apitype|string}} - The string used to display the current quantity. Usually the string form of the quantity return.
:;10. criteriaID:{{apitype|number}} - Unique criteria ID.
:;11. eligible:{{apitype|boolean}} - True if the criteria is eligible to be completed; false otherwise. Used to determine whether to show the criteria line in the objectives tracker in red or not.
:;12. duration:{{apitype|number}}
:;13. elapsed:{{apitype|number}}

==Values==
See {{dbc|Criteria}}
{| class="sortable darktable zebra col1-center"
|+ Achievement Criteria Info
|-
! Value !! Description !! Corresponding AssetID
|-
| 0 || Monster kill || Monster ID
|-
| 1 || Winning PvP objectives in a thorough manner (holding all bases, controlling all flags) || 
|-
| 5 || Reaching a player level || Player level
|-
| 7 || Weapon skill || probably a skill ID of some sort{{fact}}
|-
| 8 || Another achievement || Achievement ID
|-
| 9 || Completing quests globally || 
|-
| 10 || Completing a daily quest every day || 
|-
| 11 || Completing quests in specific areas || 
|-
| 12 || Collecting currency || Currency ID
|-
| 14 || Completing daily quests || 
|-
| 16 || Dying in specific locations || Location
|-
| 20 || Defeating a boss encounter || NPC ID
|-
| 27 || Completing a quest || Quest ID
|-
| 28 || Getting a spell cast on you || Spell ID
|-
| 29 || Casting a spell (often crafting) || Spell ID
|-
| 30 || PvP objectives (flags, assaulting, defending) || 
|-
| 31 || PvP kills in battleground PvP locations || 
|-
| 32 || Winning ranked arena matches in specific locations || (probably a location ID){{fact}}
|-
| 34 || Squashling (owning a specific pet?){{fact}} || Spell ID
|-
| 35 || PvP kills while under the influence of something || 
|-
| 36 || Acquiring items (soulbound) || Item ID
|-
| 37 || Winning arenas || 
|-
| 38 || Highest-reached arena team rating || Team size
|-
| 39 || Achieving arena team rating || Team size
|-
| 41 || Eating or drinking a specific item || Item ID
|-
| 42 || Fishing things up || Item ID
|-
| 43 || Exploration || (location ID?){{Fact}}
|-
| 44 || Reaching a PvP rank (old PvP system) || Rank
|-
| 45 || Purchasing 7 bank slots || 
|-
| 46 || Exalted rep || Faction ID
|-
| 47 || 5 reputations to exalted || 
|-
| 49 || Equipping items || Slot ID (quality is presumably encoded into flags)
|-
| 52 || Killing specific classes of player || 
|-
| 53 || Kill-a-given-race || (Race ID?){{fact}}
|-
| 54 || Using emotes on targets || (likely the emote ID){{fact}}
|-
| 55 || Healing || 
|-
| 56 || Being a wrecking ball in Alterac Valley || 
|-
| 57 || Having items (tabards and legendaries) || Item ID
|-
| 59 || Getting gold from vendors || 
|-
| 62 || Getting gold from quest rewards || 
|-
| 67 || Looting gold || 
|-
| 68 || Reading books || Object ID
|-
| 70 || Killing players in world PvP locations || 
|-
| 72 || Fishing things from schools or wreckage || Object ID
|-
| 73 || Killing Mal'Ganis on Heroic. Why? Who can say. || 
|-
| 74 || Earning a title (for guild achievements) || 
|-
| 75 || Obtaining mounts || 
|-
| 96 ||  Obtaining battle pets || NPC ID of the pet
|-
| 109 || Fishing, either in general or in specific locations || 
|-
| 110 || Casting spells on specific target || Spell ID
|-
| 112 || Learning cooking recipes || 
|-
| 113 || Honorable kills || 
|-
| 124 || Spending guild gold on repairs || 
|-
| 125 || Reaching a guild level || 
|-
| 126 || Crafting items as a guild || 
|-
| 127 || Fishing as a guild || 
|-
| 128 || Purchasing guild bank tabs || 
|-
| 129 || Guild achievement points || 
|-
| 130 || Winning rated battlegrounds || 
|-
| 132 || Reaching rated battleground rating || 
|-
| 133 || Purchasing a guild crest || 
|}

==Patch changes==
* {{Patch 5.0.4|note=Added <code>GetAchievementCriteriaInfoByID()</code>}}
* {{Patch 3.0.2|note=Added <code>GetAchievementCriteriaInfo()</code>}}

<!-- luals
---@param achievementID number
---@param criteriaIndex number
---@param countHidden? boolean
---@return string criteriaString
---@return number criteriaType
---@return boolean completed
---@return number quantity
---@return number reqQuantity
---@return string charName
---@return number flags
---@return number assetID
---@return string quantityString
---@return number criteriaID
---@return boolean eligible
---@return number duration
---@return number elapsed
function GetAchievementCriteriaInfo(achievementID, criteriaIndex, countHidden) end

---[Documentation](https://warcraft.wiki.gg/wiki/API_GetAchievementCriteriaInfoByID)
---@param achievementID number
---@param criteriaID number
---@return string criteriaString
---@return number criteriaType
---@return boolean completed
---@return number quantity
---@return number reqQuantity
---@return string charName
---@return number flags
---@return number assetID
---@return string quantityString
---@return number criteriaID
---@return boolean eligible
---@return number duration
---@return number elapsed
function GetAchievementCriteriaInfoByID(achievementID, criteriaID) end
-->
```